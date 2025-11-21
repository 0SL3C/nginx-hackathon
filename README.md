# NGINX Log Explorer & Anomaly Dashboard
A Dashboard app that parses NGINX access logs in the browser, visualizes traffic and status trends, highlights anomalies, and optionally enriches IPs with geolocation and AI analysis.

# Features
### Dashboard
- Requests over time, status code distribution, unique visitors, total data served, top endpoints.
### Logs parsing
- Filterable, sortable table of parsed NGINX entries (method, path, status, size, user agent, time).
### Anomalies analysis
- Heuristics: excessive 5xx, high-frequency requests, sequential crawling, excessive 404s, sensitive resource scans, suspicious user agents.
- Drawer view with AI summary (optional, requires VITE_OPENAI_API_KEY).

# Tech stack
- Built with React, Vite, TypeScript, Tailwind CSS, Radix UI, TanStack Table, and Recharts.
- No backend required; all processing happens client-side using a bundled sample log.
- Optional integrations:
Geoapify for IP geolocation dots map.
OpenAI for concise anomaly analysis.
# Environmental Variables
##### ```VITE_GEOAPI_KEY```
Key needed for fetching geolocation data from [Geoapify](https://www.geoapify.com/). You can get a free API key by signing up on their website.
##### `VITE_OPENAI_API_KEY`
Key needed for OpenAI API for anomaly analysis.