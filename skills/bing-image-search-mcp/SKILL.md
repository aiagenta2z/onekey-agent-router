---
name: bing-image-search-mcp
description: Auto-generated skill for bing-image-search-mcp tools via OneKey Agent Router.
---

### OneKey Agent Router
Use One Access Key to connect to various commercial APIs. Please visit the [OneKey Router Keys](https://www.deepnlp.org/workspace/keys) and read the docs [OneKey MCP Router Doc](https://www.deepnlp.org/doc/onekey_mcp_router) and [OneKey Agent Router Doc](https://deepnlp.org/doc/onekey_agent_router).


# bing-image-search-mcp Skill
Use the OneKey Agent Router to access tools for this server via a unified access key.
## Quick Start
Set your OneKey access key:
```bash
export DEEPNLP_ONEKEY_ROUTER_ACCESS=YOUR_API_KEY
```
If no key is provided, the scripts fall back to the demo key `BETA_TEST_KEY_MARCH_2026`.
Common settings:
- `unique_id`: `bing-image-search-mcp/bing-image-search-mcp`
- `api_id`: one of the tools listed below
## Tools
### `search_images`
Get Public Available Stock Symbols from Global Marketplace

        Args:
            query: str, query used in Bing search engine
            limit: int, number of images information returned
  
        Return: 
            str: json str with below values samples

            [{'title': 'Italy Travel Guide: The Ultimate 2-week Road Trip · Salt in our Hair',
               'thumbnail_url': 'http://ts2.mm.bing.net/th?id=OIP.TEuPMUk1s2A3OBkq3LrTnwHaFc&pid=15.1',
               'url': 'http://ts2.mm.bing.net/th?id=OIP.TEuPMUk1s2A3OBkq3LrTnwHaFc&pid=15.1'},
              {'title': '25 Best Places to Visit in Italy (+ Map to Find Them!) - Our Escape Clause',
               'thumbnail_url': 'http://ts2.mm.bing.net/th?id=OIP.kle1eO_p_4crE4lRtWK8AgHaE8&pid=15.1',
               'url': 'http://ts2.mm.bing.net/th?id=OIP.kle1eO_p_4crE4lRtWK8AgHaE8&pid=15.1'}
               ]

Parameters:
- `query` (string, optional):
- `limit` (integer, optional):
### `search_images_batch`
Batch Method of Search Images From Bing Web Search

        Args:
            query_list: List[str], List of query used in Bing Image search engine
            limit: int, number of images information returned
  
        Return: 
            Dict: json Dict with below values samples

            [{'title': 'Italy Travel Guide: The Ultimate 2-week Road Trip · Salt in our Hair',
               'thumbnail_url': 'http://ts2.mm.bing.net/th?id=OIP.TEuPMUk1s2A3OBkq3LrTnwHaFc&pid=15.1',
               'url': 'http://ts2.mm.bing.net/th?id=OIP.TEuPMUk1s2A3OBkq3LrTnwHaFc&pid=15.1'},
              {'title': '25 Best Places to Visit in Italy (+ Map to Find Them!) - Our Escape Clause',
               'thumbnail_url': 'http://ts2.mm.bing.net/th?id=OIP.kle1eO_p_4crE4lRtWK8AgHaE8&pid=15.1',
               'url': 'http://ts2.mm.bing.net/th?id=OIP.kle1eO_p_4crE4lRtWK8AgHaE8&pid=15.1'}
               ]

Parameters:
- `query_list` (array of string, required):
- `limit` (integer, optional):
## Scripts
Each tool has a dedicated script in this folder:
- `skills/bing-image-search-mcp/scripts/search_images.py`
- `skills/bing-image-search-mcp/scripts/search_images_batch.py`
### Example
```bash
python3 scripts/<tool_name>.py --data '{"key": "value"}'
```

### Related DeepNLP OneKey Router Documents
[AI Agent Marketplace](https://www.deepnlp.org/store/ai-agent)    
[Skills Marketplace](https://www.deepnlp.org/store/skills)
[AI Agent A2Z Deployment](https://www.deepnlp.org/workspace/deploy)    
[PH AI Agent Router](https://www.producthunt.com/products/deepnlp-ai-agent-marketplace-router)    
[PH AI Agent A2Z Infra](https://www.producthunt.com/products/ai-agent-a2z-infra-deployment-platform)    
[GitHub AI Agent Marketplace](https://github.com/aiagenta2z/ai-agent-marketplace)
