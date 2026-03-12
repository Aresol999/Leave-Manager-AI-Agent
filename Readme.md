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

# Project Structure


leave-manager-mcp/
│
├── server.py # MCP server implementation
├── README.md # Project documentation


---

# Installation

## 1. Clone the repository

```bash
git clone https://github.com/yourusername/leave-manager-mcp.git
cd leave-manager-mcp
2. Install dependencies
pip install mcp
Running the MCP Server

Start the server using:

python server.py

This launches the LeaveManager MCP server, which exposes the defined tools and resources to MCP-compatible clients.

Available MCP Tools
1. Get Leave Balance

Returns the remaining leave days for an employee.

Function
get_leave_balance(employee_id: str)
Example

Input

employee_id = "E001"

Output

E001 has 18 leave days remaining.
2. Apply Leave

Allows an employee to request leave for specific dates.

Function
apply_leave(employee_id: str, leave_dates: List[str])
Example

Input

employee_id = "E001"
leave_dates = ["2025-04-17", "2025-04-18"]

Output

Leave applied for 2 day(s). Remaining balance: 16.
3. Get Leave History

Returns all leave dates previously taken by the employee.

Function
get_leave_history(employee_id: str)
Example Output
Leave history for E001: 2024-12-25, 2025-01-01
MCP Resource
Greeting Resource

Provides a personalized greeting message.

Resource URI
greeting://{name}
Example
greeting://John
Response
Hello, John! How can I assist you with leave management today?
Example Employee Data

The system uses an in-memory datastore:

employee_leaves = {
    "E001": {"balance": 18, "history": ["2024-12-25", "2025-01-01"]},
    "E002": {"balance": 20, "history": []}
}

In production, this would typically be replaced with:

PostgreSQL

MySQL

MongoDB

HR management APIs

Example Use Case

An LLM connected through MCP can perform tasks like:

“How many leave days does employee E001 have?”

“Apply leave for E002 on April 17 and April 18.”

“Show leave history for E001.”

The MCP server executes the corresponding tool and returns structured responses.
