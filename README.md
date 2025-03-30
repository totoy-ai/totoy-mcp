# @totoy/totoy-mcp

## MCP client config

Add the following to `~/Library/Application\ Support/Claude/claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "totoy-mcp": {
      "command": "npx",
      "args": ["-y", "@totoy/totoy-mcp"],
      "env": {
        "API_KEY": "..."
      }
    }
  }
}
```

## Customizing the base URL

Set the environment variable `OPEN_MCP_BASE_URL` to override each tool's base URL. This is useful if your OpenAPI spec defines a relative server URL.

## Other environment variables

- `API_KEY`

## Tools

### createexplanation

### createknowledgebase

### listknowledgebases

### getknowledgebase

### modifyknowledgebase

### deleteknowledgebase

### chatwithknowledgebase

### addknowledgebasesources

### listknowledgebasesources

### getknowledgebasesource

### deleteknowledgebasesource

### createtextsource

### createdocumentsource

### listsources

### getsource

### modifysource

### deletesource

### getsourcecontent

### createproject

### listprojects

### getproject

### modifyproject

### deleteproject

### getorganization

## Inspector

Needs access to port 3000 for running a proxy server, will fail if http://localhost:3000 is already busy.

```bash
npx -y @modelcontextprotocol/inspector npx -y @totoy/totoy-mcp
```

- Open http://localhost:5173
- Transport type: `STDIO`
- Command: `npx`
- Arguments: `-y @totoy/totoy-mcp`
- Click `Environment Variables` to add
- Click `Connect`

It should say _MCP Server running on stdio_ in red.

- Click `List Tools`
