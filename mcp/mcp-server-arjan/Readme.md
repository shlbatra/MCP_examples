-- Configure claude cli to use MCP server below -
claude mcp add -s user youtube_videos -- uv --directory /Users/shlba/Desktop/Docs/Study/code/MCP_examples/mcp/mcp-server-arjan run mcp_videos.py
claude mcp add -s user youtube_videos_api -- uv --directory /Users/shlba/Desktop/Docs/Study/code/MCP_examples/mcp/mcp-server-arjan run mcp_videos_api.py

-- Sample curl request to test API
curl -X GET "http://localhost:8000/videos?search=python%20design%20patterns&max_results=3" -H "accept: application/json"