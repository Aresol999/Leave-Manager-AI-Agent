# LeaveManager MCP Server

A lightweight **Leave Management System** built using the **Model Context Protocol (MCP)** and **Python**.  
This server exposes leave management functionality as **LLM-accessible tools**, enabling natural language interaction for HR-related operations such as checking leave balance, applying for leave, and retrieving leave history.

The project demonstrates how MCP servers can act as **agentic backends** that expose structured operations to large language models.

---

# Features

- Check employee leave balance
- Apply leave for specific dates
- Retrieve employee leave history
- Provide dynamic greeting resources
- Expose operations as MCP tools for LLM agents
- Simple in-memory datastore for demonstration

---

# Tech Stack

- **Python**
- **Model Context Protocol (MCP)**
- **FastMCP Server**
- **Python typing module**


---

# Installation

## 1. Clone the repository


git clone https://github.com/yourusername/leave-manager-mcp.git
cd leave-manager-mcp

## 2. Install dependencies
pip install mcp
Running the MCP Server

## Start the server using:

python server.py

This launches the LeaveManager MCP server, which exposes the defined tools and resources to MCP-compatible clients.

## 3. Prompt Claude Desktop about leave for employees
