# OlaChill for Qwen Code

Find and compare travel services in Japan from Qwen Code: tours and day trips, activities, attraction and transport tickets, ryokan on request, private airport transfers, cars with driver, charter buses, helicopter flights, golf and travel eSIM.

This is an [Agent Plugins v1](https://agent-plugins.org/) package. It contains configuration only: it connects Qwen Code to OlaChill's public MCP server at `https://olachill.com/mcp` (Streamable HTTP) and adds one skill that tells the assistant which tool to use. No code runs on your machine, and no sign-in or API key is needed.

## Install

```bash
qwen extensions install <path-or-git-url-of-this-package>
qwen extensions list
qwen mcp list
```

## Tools (13)

| Tool | What it does |
|---|---|
| `recommend_japan_travel_options` | Shortlist of tours, activities, tickets or ryokan from preferences |
| `search_travel_products` | Search tours, activities, tickets and ryokan |
| `check_product_availability` | Dates for a product found by search |
| `search_helicopter_experiences` | Helicopter sightseeing, charter and transfers |
| `search_private_transfers` | Private airport transfers for 1-6 people |
| `search_charter_vehicles` | Buses, coaches, minibuses and vans with driver |
| `get_charter_quote` | Estimated price for a charter itinerary |
| `request_charter_quote` | Sends a quotation request to OlaChill - only after the user explicitly confirms |
| `search_chauffeur_services` | Car with driver by the day or hour |
| `search_golf_packages` | Golf rounds and golf trips |
| `search_esim_plans` | Japan eSIM data plans |
| `get_booking_status` | Status of an existing booking or request |
| `list_olachill_services` | Other OlaChill services |

All tools are read-only except `request_charter_quote`, which requires `user_confirmed: true` and the traveller's contact details.

Prices are "from" prices or estimates; final prices are confirmed on olachill.com or by email.

## Example prompts

- "Find a ryokan in Hakone for two people in March."
- "Private car from Haneda to Shibuya for 2 people - how much?"
- "We are 40 people going from Tokyo to Hakone on 2027-03-20. Which bus and what price?"
- "Japan eSIM for 7 days."

## Contact

- Website: https://olachill.com
- Tours, tickets, activities: booking@olachill.com
- Vehicles, charter buses, partnerships: partners@olachill.com

Operated by MIA Co., Ltd. (Osaka, Japan). License: MIT.
