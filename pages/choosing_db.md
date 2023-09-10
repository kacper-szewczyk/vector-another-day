
# Wybór bazy danych

## Baza relacyjna:

<div v-click>
- dodawanie działa szybko - O(1)
</div>

<div v-click="2">
- aktualizacja działa ok - O(log(N)) 
</div>

<div v-click="3">
- usuwanie działa ok -O(log(N))
</div>

<div v-click="4">
- wyszukiwanie działa wolno -O(N)
</div>

<div v-click="5">

### Bo nie dodaliśmy indexów

</div>

---

# Wynik

<img src="fight.gif" style="width: 100%" v-click>

<div v-click="2">
- wyszukiwanie działa szybciej - O(log(N))
</div>

<div v-click="3">
- ale dodawanie działa wolniej - O(N)
</div>

<div v-click="4">

### Ok... a co z wyszukiwaniem `like`?

</div>

---

# Sukces?

<img src="fight.gif" style="width: 100%" v-click>

---

<img src="einstein.jpeg" style="width: 100%" v-click>

---

<img src="vaas.webp" style="width: 75%; margin: auto">

---

# Szaleństwem jest robić wciąż to samo i oczekiwać różnych rezultatów ~ Albert Einstein

---

# Coś innego?

<img src="elastic.svg" style="width: 50%; margin: auto" v-click>

---

# Wybór bazy danych

## Baza NoSQL (MongoDB):

<div v-click>
- dodawanie działa szybko - O(1)
</div>

<div v-click="2">
- aktualizacja działa ok - O(log(n))
</div>

<div v-click="3">
- usuwanie działa ok - O(log(n))
</div>

<div v-click="4">
- wyszukiwanie działa wolno - O(log(n))
</div>
