FROM python:3.14-slim
WORKDIR /app
COPY searxng_mcp.py .
RUN python -m pip install --no-cache-dir "mcp[cli]" httpx
EXPOSE 8081
CMD ["python", "searxng_mcp.py"]
