# Test Repo

## What is an MCP Server?

An **MCP (Model Context Protocol) Server** is a program that exposes tools, resources, and data to AI models in a standardized way. It acts as the **provider** side of the MCP protocol — offering capabilities that AI clients can discover and use.

### Key responsibilities of an MCP Server:
- **Expose tools** – Functions the AI can call (e.g., search the web, query a database, send an email).
- **Provide resources** – Structured data or files the AI can read (e.g., documents, API responses).
- **Handle requests** – Listen for incoming requests from MCP clients and respond with results.
- **Maintain context** – Optionally manage session state across multiple interactions.

Examples of MCP Servers include integrations for Google Drive, GitHub, Slack, Asana, and more.

---

## What is an MCP Client?

An **MCP (Model Context Protocol) Client** is a program or interface that connects to one or more MCP servers on behalf of an AI model. It acts as the **consumer** side of the MCP protocol — discovering available tools and invoking them as needed.

### Key responsibilities of an MCP Client:
- **Connect to servers** – Establish connections to one or more MCP servers.
- **Discover capabilities** – Query servers to find out which tools and resources are available.
- **Invoke tools** – Call server-side tools and pass the results back to the AI model.
- **Relay responses** – Return tool outputs to the AI so it can continue reasoning and responding.

AI assistants like Claude act as MCP clients when they connect to external services to retrieve information or perform actions.

---

## How They Work Together

```
┌─────────────────┐        MCP Protocol        ┌─────────────────┐
│   MCP Client    │ ◄─────────────────────────► │   MCP Server    │
│  (e.g., Claude) │   requests / responses      │ (e.g., GitHub,  │
│                 │                             │  Google Drive)  │
└─────────────────┘                             └─────────────────┘
```

1. The **client** sends a request describing what it needs (e.g., "list my GitHub issues").
2. The **server** processes the request, interacts with the underlying service, and returns a structured response.
3. The **client** passes the response back to the AI model to use in its answer.

This architecture allows AI models to be extended with real-world capabilities in a modular, secure, and standardized way.
