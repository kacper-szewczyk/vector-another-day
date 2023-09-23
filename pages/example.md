
# Use Case from my project
Details of the project

1. Map aplication
2. Search made by third party provider using API as a proxy
3. Filtering done on API side
4. Filtering returnes list of object with POI (points of interests) near by

---

# Use Case from my project
Initial setup:

1. Data about POI is scrapped to DB (Postgres) from third party provider
2. Data is stored in DB as a point (lat, lng), type of POI and name of the POI
3. Results from third party are filtered one by one if there are near by POI in DB

---

# UseCase from my project
Problems that we have:

1. Data from third party provider is not paginated at all - the limitation is only in radius of search - so it could return up to 20k results (response time from third party ~10s)
2. In DB we have 1M POI
3. Filtering is done one by one - so it is slow


---

# UseCase from my project
Solution using vector database:

1. Use vector database or pgvector to improve searching for the nearest POI
2. High number of similarity search threshold, based on coordinates will be more effective. 
