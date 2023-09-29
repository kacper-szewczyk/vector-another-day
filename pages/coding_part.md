
# Connection to vector database
Inserting elements

```ts {all|1-2|4-5|7-16|all}
import { Vector } from "@pinecone-database/pinecone";
import { Pipeline } from "@xenova/transformers";
...
const { pipeline } = await import("@xenova/transformers");
this.pipe = await pipeline("embeddings", "Xenova/all-MiniLM-L6-v2");
...
async embed(text: string): Promise<Vector> {
    const result = this.pipe && (await this.pipe(text));
    return {
        id: uuidv4(),
        metadata: {
            text,
        },
        values: Array.from(result.data),
    };
}

```


---


# Connection to vector database

Inserting elements

```ts {all|1-10|1,11-13|14-20|all}
import { PineconeClient, utils } from "@pinecone-database/pinecone";
...
const pineconeClient = new PineconeClient();

await pineconeClient.init({
    apiKey: getEnv("PINECONE_API_KEY"),
    environment: getEnv("PINECONE_ENVIRONMENT"),
});

const index = pineconeClient.Index(indexName);
...
const { chunkedUpsert } = utils;
...
const embeddings = await embed(text);
await chunkedUpsert(index, embeddings, "default");

```

---

# Connection to vector database

Searching

```ts {all|1|3-11|all}
const queryEmbedding = await embed(query)

const results = await index.query({
  queryRequest: {
    vector: queryEmbedding.values,
    topK,
    includeMetadata: true,
    includeValues: false,
    namespace: 'default'
  }
})
```


---


<img src="/batman-question.png" style="width:100%; padding: 32px; marging-top: 32px;">