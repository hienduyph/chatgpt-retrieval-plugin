# How to use

Tutorials https://betterprogramming.pub/enhancing-chatgpt-with-infinite-external-memory-using-vector-database-and-chatgpt-retrieval-plugin-b6f4ea16ab8

```bash
# random generate token stuff
export BEARER_TOKEN=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJoZWxsbyI6IndvcmxkIiwiaWF0IjoxNjg0MDcwMzMwfQ.m-wncgcc7ODklU1W6Dmk_bC0IMYg27MS51dwEEZZsxw
export OPENAI_API_KEY='<>' # insert your key here

export DATASTORE=qdrant
export QDRANT_URL=http://127.0.0.1
export QDRANT_PORT=6333
export QDRANT_GRPC_PORT=6334
export QDRANT_COLLECTION=chatgpt_plugins

# start qdrant
docker-compose -f ./docker-compose.yaml up -d

# index the data
python ./database_util.py

# try some chat stuf
python ./chat.py

# Q: "Who are some major characters in the world of Auroria and list their stories"
```
