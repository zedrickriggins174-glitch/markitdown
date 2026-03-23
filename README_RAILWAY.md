# Railway Deployment

This fork includes a FastAPI entrypoint in `app.py` so the repository can run as a web service on Railway.

## What this service does
- `GET /health` returns a health status payload
- `POST /convert` accepts a file upload and returns Markdown text converted by MarkItDown

## Railway setup
1. Create a new Railway project.
2. Deploy from the GitHub repo `zedrickriggins174-glitch/markitdown`.
3. Use the start command below:

```bash
uvicorn app:app --host 0.0.0.0 --port $PORT
```

## Test after deploy
- Health check: `/health`
- Conversion endpoint: `/convert`

## Notes
- `requirements.txt` lists the packages Railway needs to install.
- `railway.json` tells Railway how to start the service.
