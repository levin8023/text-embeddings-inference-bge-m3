# text-embeddings-inference-bge-m3

startup with docker: 

```
docker run -p 8080:80 levin8023/text-embeddings-inference-bge-m3
```

docs: ```localhost:8080/docs```


orgin Dockerfile:

```
FROM ghcr.io/huggingface/text-embeddings-inference:cpu-1.5

COPY BAAI/bge-m3 /data/BAAI/bge-m3/

EXPOSE 80

ENTRYPOINT ["text-embeddings-router"]

CMD ["--model-id", "/data/BAAI/bge-m3"]

```
