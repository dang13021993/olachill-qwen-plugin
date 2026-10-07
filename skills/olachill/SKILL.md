---
name: olachill
description: Use when the user wants to find, compare, price or check availability of travel services in Japan - tours and day trips, activities and cultural experiences, attraction or transport tickets, ryokan stays, private airport transfers, cars with driver, charter buses or coaches, helicopter flights, golf or a Japan eSIM - or asks about an existing OlaChill booking. Uses the OlaChill MCP tools.
license: MIT
---

# OlaChill - Japan travel services

OlaChill (MIA Co., Ltd., Osaka) offers bookable and request-based travel services in Japan. The tools come from the `olachill` MCP server.

## Pick the most specific tool

| The user wants | Tool |
|---|---|
| Suggestions or a shortlist from preferences (area, interests, budget) | `recommend_japan_travel_options` |
| A named place, product or type of tour, activity, ticket or ryokan | `search_travel_products`, then `check_product_availability` for dates |
| Helicopter sightseeing, charter or transfer | `search_helicopter_experiences` |
| Private car to or from an airport for 1-6 people | `search_private_transfers` |
| Bus, coach, minibus or van with driver for a group | `search_charter_vehicles`, then `get_charter_quote` for a specific itinerary |
| Golf rounds or golf trips | `search_golf_packages` |
| Car with driver by the day or hour (Alphard, Lexus...) | `search_chauffeur_services` |
| Japan eSIM data plans | `search_esim_plans` |
| An existing booking or request | `get_booking_status` |
| Any other OlaChill service | `list_olachill_services` |

## Rules

- Search before quoting. Every tool is read-only except `request_charter_quote`.
- `request_charter_quote` sends a real quotation request to OlaChill. Call it only after `get_charter_quote`, after showing the user the trip details, and only when the user explicitly says to send it and has given their name and email. Set `user_confirmed: true` only in that case. Never call it on your own initiative or to test it.
- Prices are "from" prices, dated reference prices or estimates. Say so. Do not invent prices, availability, booking references or services that the tools did not return.
- Give the user the product link the tool returns so they can book on olachill.com.
- Contact for questions: booking@olachill.com (tours, tickets, activities) or partners@olachill.com (vehicles and charter buses).
