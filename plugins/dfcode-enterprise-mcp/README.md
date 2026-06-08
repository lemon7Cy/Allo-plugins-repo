# DFCode Enterprise MCP Server

Enterprise MCP (Model Context Protocol) server for querying DFCode organization backend data.

## Connection

- **Type:** SSE
- **URL:** `http://119.45.112.196/mcp/sse`
- **Auth:** `X-API-Key` header

## Required Environment

- `DFCODE_API_KEY` — API key for authentication

## Tools

| Tool                               | Description                                                                                |
| ---------------------------------- | ------------------------------------------------------------------------------------------ |
| `query_dashboard`                  | Organization dashboard: today/7d/month usage, active members, model distribution           |
| `query_usage`                      | Usage detail and aggregation with single and cross-dimension support                       |
| `query_users`                      | Member list and activity status                                                            |
| `query_user_detail`                | Member profile, MAAS quota, device list, roster status                                     |
| `query_employee_detail`            | Member usage analysis: overview, daily trends, model distribution                          |
| `query_audit_logs`                 | Audit logs: admin operations, logins, device authorizations                                |
| `query_roster`                     | Employee roster directory                                                                  |
| `query_model_endpoints`            | Local model endpoint list                                                                  |
| `query_maas_models`                | MAAS gateway logical model list                                                            |
| `query_user_devices`               | Member device list                                                                         |
| `query_departments`                | Cross-department analysis: usage, WoW growth, daily trends, model breakdown, top employees |
| `query_department_employee_detail` | Enriched admin employee detail with profile, MAAS, devices, usage entries                  |
| `query_employee_portal_stats`      | Employee portal stats: summary, trend, models, optional heatmap                            |
| `query_announcements`              | Announcement list with title, content, pinned status                                       |
| `query_feedback`                   | Employee feedback list with submitter identity                                             |

## Protocol

1. SSE handshake: `GET /mcp/sse` with `X-API-Key` header → receive `sessionId`
2. JSON-RPC requests: `POST /mcp/messages?sessionId=<id>` with `X-API-Key` header

## Safety

Install stores metadata only. The SSE connection is established at runtime when the plugin is enabled.
