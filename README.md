# Agent Router Python SDK

AI Agent choose the most appropriate tools 

[PyPI](https://www.pypi.org/project/onekey_agent_router)|[Document](http://www.deepnlp.org/doc/mcp_marketplace)|[MCP Marketplace](http://www.deepnlp.org/store/ai-agent/mcp-server)|[AI Agent Search](http://www.deepnlp.org/search/agent)|[MCP Router Ranking List](https://www.deepnlp.org/agent/rankings)




**Notice** Use Cautiously

```
pip install onekey_agent_router

```


### Usage 

```
import onekey_agent_router as router


query = "Help me find last month stock price of Tesla and output to excel"

### RAG of available registered agents
agents = router.router_agent(query)

results = []
for agent in agents:
	tool_input = agent.function_call(query)
	results = agents.tool_call(tool_input)

```


### Features

0. A Lightweight Agent Router to help your LLM choose appropriate tools from the index and registry
1. Search API of AI AGENT Tools: Users can search MCP Servers Meta Info and tools fit for mcp.json by query, such as "map", "payment", "browser use"

### Related
- [MCP Marketplace DeepNLP](http://deepnlp.org/store/ai-agent/mcp-server)
- [MCP Marketplace PulseMCP](https://www.pulsemcp.com/)
- [Pypi](https://pypi.org/project/mcp-marketplace)
- [Github](https://github.com/aiagenta2z/mcp-marketplace)
- [AI Agent Marketplace](http://www.deepnlp.org/store/ai-agent)

