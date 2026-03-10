# Agent Router Python

OneKey AI Agent Router Connec to Skills Agent and Commercial APIs
[PyPI](https://www.pypi.org/project/onekey_agent_router)|[Document](http://www.deepnlp.org/doc/mcp_marketplace)|[MCP Marketplace](http://www.deepnlp.org/store/ai-agent/mcp-server)|[AI Agent Search](http://www.deepnlp.org/search/agent)|[MCP Router Ranking List](https://www.deepnlp.org/agent/rankings)


### Features

0. A Lightweight Agent Router to help your LLM choose appropriate tools from the index and registry
1. Search API of AI AGENT Tools: Users can search MCP Servers Meta Info and tools fit for mcp.json by query, such as "map", "payment", "browser use"
2. Skills Support, One Access Key to use commercial APIs


### QuickStart

```shell
pip install ai-agent-marketplace
```
### Python API Usages

Using Agent Router API from Python Code and related Skills. Generate the [OneKey Router Keys](https://www.deepnlp.org/workspace/keys) here.

```shell
export DEEPNLP_ONEKEY_ROUTER_ACCESS=BETA_TEST_KEY_MARCH_2026
```

```python
    import os
    from ai_agent_marketplace import OneKeyAgentRouter
    onekey = os.getenv("KEY_DEEPNLP_ONEKEY_ROUTER_ACCESS", "BETA_TEST_KEY_MARCH_2026")
    agent_router = OneKeyAgentRouter(onekey=onekey)
    print (f"DEBUG: Connectin to agent_router google-maps")
    result = agent_router.invoke(
        unique_id = "google-maps/google-maps",
        api_id = "maps_directions",
        data = {
            "origin": "Boston", "destination": "New York", "mode": "driving"
        }
    )
    print("Google Map Result:", result)
```



### Skills

Skills are organized under `./skills`. Each skill provides a `SKILL.md` with its tool list and usage details. Use the table below for a quick index of skill names, their `SKILL.md` shortcuts, and the tools exposed by each skill.

| Skill | SKILL.md | Tools |
| --- | --- | --- |
| amap-maps-streamableHTTP | [skills/amap-maps-streamableHTTP/SKILL.md](skills/amap-maps-streamableHTTP/SKILL.md) | `maps_direction_bicycling`, `maps_direction_driving`, `maps_direction_transit_integrated`, `maps_direction_walking`, `maps_distance`, `maps_geo`, `maps_regeocode`, `maps_ip_location`, `maps_schema_personal_map`, `maps_around_search`, `maps_search_detail`, `maps_text_search`, `maps_schema_navi`, `maps_schema_take_taxi`, `maps_weather` |
| baidu-maps-sse | [skills/baidu-maps-sse/SKILL.md](skills/baidu-maps-sse/SKILL.md) | `maps_geocode`, `maps_reverse_geocode`, `maps_search_places`, `maps_place_details`, `maps_distance_matrix`, `maps_elevation`, `maps_directions` |
| bing-image-search-mcp | [skills/bing-image-search-mcp/SKILL.md](skills/bing-image-search-mcp/SKILL.md) | `search_images`, `search_images_batch` |
| brave-search | [skills/brave-search/SKILL.md](skills/brave-search/SKILL.md) | `brave_web_search`, `brave_local_search` |
| craftsman-agent-build-plans | [skills/craftsman-agent-skills/SKILL.md](skills/craftsman-agent-skills/SKILL.md) | `generate_lego_build_plan`, `generate_minecraft_build_plan` |
| firecrawl-mcp | [skills/firecrawl-mcp/SKILL.md](skills/firecrawl-mcp/SKILL.md) | `firecrawl_scrape`, `firecrawl_map`, `firecrawl_search`, `firecrawl_crawl`, `firecrawl_check_crawl_status`, `firecrawl_extract`, `firecrawl_agent`, `firecrawl_agent_status`, `firecrawl_browser_create`, `firecrawl_browser_execute`, `firecrawl_browser_delete`, `firecrawl_browser_list` |
| gemini-nano-banana | [skills/gemini-nano-banana/SKILL.md](skills/gemini-nano-banana/SKILL.md) | `generate_image_gemini`, `generate_image_nano_banana` |
| github | [skills/github/SKILL.md](skills/github/SKILL.md) | `add_comment_to_pending_review`, `add_issue_comment`, `create_branch`, `create_or_update_file`, `create_pull_request`, `create_repository`, `delete_file`, `fork_repository`, `get_commit`, `get_file_contents`, `get_label`, `get_latest_release`, `get_me`, `get_release_by_tag`, `get_tag`, `get_team_members`, `get_teams`, `issue_read`, `issue_write`, `list_branches`, `list_commits`, `list_issue_types`, `list_issues`, `list_pull_requests`, `list_releases`, `list_tags`, `merge_pull_request`, `pull_request_read`, `pull_request_review_write`, `push_files`, `request_copilot_review`, `search_code`, `search_issues`, `search_pull_requests`, `search_repositories`, `search_users`, `sub_issue_write`, `update_pull_request`, `update_pull_request_branch` |
| google-maps | [skills/google-maps/SKILL.md](skills/google-maps/SKILL.md) | `maps_geocode`, `maps_reverse_geocode`, `maps_search_places`, `maps_place_details`, `maps_distance_matrix`, `maps_elevation`, `maps_directions` |
| google-search | [skills/google-search/SKILL.md](skills/google-search/SKILL.md) | `google_search` |
| mcp-server-chart | [skills/mcp-server-chart/SKILL.md](skills/mcp-server-chart/SKILL.md) | `generate_area_chart`, `generate_bar_chart`, `generate_boxplot_chart`, `generate_column_chart`, `generate_district_map`, `generate_dual_axes_chart`, `generate_fishbone_diagram`, `generate_flow_diagram`, `generate_funnel_chart`, `generate_histogram_chart`, `generate_line_chart`, `generate_liquid_chart`, `generate_mind_map`, `generate_network_graph`, `generate_organization_chart`, `generate_path_map`, `generate_pie_chart`, `generate_pin_map`, `generate_radar_chart`, `generate_sankey_chart`, `generate_scatter_chart`, `generate_treemap_chart`, `generate_venn_chart`, `generate_violin_chart`, `generate_waterfall_chart`, `generate_word_cloud_chart`, `generate_spreadsheet` |
| perplexity | [skills/perplexity/SKILL.md](skills/perplexity/SKILL.md) | `perplexity_ask`, `perplexity_research`, `perplexity_reason`, `perplexity_search` |
| tavily-remote-mcp | [skills/tavily-remote-mcp/SKILL.md](skills/tavily-remote-mcp/SKILL.md) | `tavily_search`, `tavily_extract`, `tavily_crawl`, `tavily_map`, `tavily_research` |


### Related
- [MCP Marketplace DeepNLP](http://deepnlp.org/store/ai-agent/mcp-server)
- [MCP Marketplace PulseMCP](https://www.pulsemcp.com/)
- [Pypi](https://pypi.org/project/mcp-marketplace)
- [Github](https://github.com/aiagenta2z/mcp-marketplace)
- [AI Agent Marketplace](http://www.deepnlp.org/store/ai-agent)
