# SearXNG MCP
Application called docker needed, MCP connect via cline / roo code (vscode plugin)

Docker Compose setup for running a local SearXNG instance and exposing it to Continue through the `searxng-mcp` Python library.

## Start
RIGHT CLICK MCPSERVER FILE, OPEN VIA CMD
```powershell
docker compose up -d --build
```

## Stop

```powershell
docker compose down
```

## Restart

```powershell
docker compose restart
```

## View Logs

```powershell
docker compose logs -f
```

To view only the MCP server logs:

```powershell
docker compose logs -f searxng-mcp
```

## Continue Config

Use the SSE endpoint, including `/sse`:

```yaml
mcpServers:
  - name: SearXNG Search
    transport: sse
    url: http://localhost:8081/sse
```

SearXNG is available at `http://localhost:8080`.
The MCP server is available at `http://localhost:8081/sse`.
