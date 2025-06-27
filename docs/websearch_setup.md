# 🔍 Web Search MCP Setup Guide

## Prerequisites

1. **Brave Search API Account**: Free tier available
2. **API Key**: Generate from Brave Search dashboard

## Getting a Brave Search API Key

1. Visit https://brave.com/search/api/
2. Click "Get Started" or "Sign Up"
3. Create a free account (includes 2,000 queries/month)
4. Navigate to API Keys section
5. Generate a new API key
6. Copy the key for configuration

## Installation

```bash
npm install -g @modelcontextprotocol/server-brave-search
```

## Configuration

### Windows
```cmd
set BRAVE_SEARCH_API_KEY=your_api_key_here
```

### macOS/Linux  
```bash
export BRAVE_SEARCH_API_KEY=your_api_key_here
```

### Or add to your shell profile:
```bash
echo 'export BRAVE_SEARCH_API_KEY=your_api_key_here' >> ~/.bashrc
```

## Verify Installation

1. Restart Cursor IDE
2. Check MCP is loaded: Look for search operations in available tools
3. Test with: `!ws CursorRIPER framework` (web search)

## Available Operations

- **Web Search**: General web queries, news, articles
- **Local Search**: Business listings, places, services
- **URL Fetch**: Retrieve and parse web content
- **Cache Management**: Store and retrieve search results

## Mode Restrictions

- **RESEARCH (Ω₁)**: Full search access
- **INNOVATE (Ω₂)**: Full search access
- **PLAN (Ω₃)**: Search + cache management
- **EXECUTE (Ω₄)**: ⛔ NO SEARCH (maintain focus!)
- **REVIEW (Ω₅)**: Verification searches only

## Search Quotas

- Free tier: 2,000 queries/month
- Basic tier: 10,000 queries/month ($5)
- Professional: 100,000 queries/month ($50)
- Rate limit: 10 searches per minute

## Best Practices

1. **Cache Results**: Use cache in PLAN mode to avoid redundant searches
2. **Specific Queries**: More specific = better results
3. **Local Search**: Use for business/location queries
4. **EXECUTE Mode**: Remember - no searching allowed!

## Troubleshooting

1. **API Key not found**: Ensure BRAVE_SEARCH_API_KEY is set
2. **Quota exceeded**: Check your usage on Brave dashboard
3. **No results**: Try broader search terms
4. **Rate limited**: Wait 1 minute between batches
