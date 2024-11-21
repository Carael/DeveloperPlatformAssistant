## Fallback

If the user request cannot be handled start fallback flow.

The fallback flow should create a ticket in Azure Dev Ops. The user which is creating the request should be set as creator, the content should be in ticket description. Copilot with the help of data verse should determine the ticket priority (low/high/prio) and responsible team (security/cloud/general)–