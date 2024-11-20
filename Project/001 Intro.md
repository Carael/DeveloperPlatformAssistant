# Developer Platform Assistant
Tool that helps developers in common work + take common tasks of the Platform Team shoulders. 

## How does it work
DPA is a Coopilot chat that support can understand natural language and will assist the user. If the scenario is not known, based on the request the bot will determine responsible team and create a ticket. 

## Which scenarios would we like to support
1. Knowledge database search
It's often that the user would just like to search our knowledge database. Coommon questions are:
- how do I use elastic in dotnet application?
- how to send sms with notification system?
- how to access swiss life github?
- how to make contribution to swiss life open source repository?
- how to start working with ui monorepository?

The bot should scan our sourcecode and wiki from sample azure dev ops instance and provide valid answer. The bot should only use external data source feedback (the thing called 'internet') if nothing is found in internal will and explicitly inform the user that the knowledge is from external data source.

Things needed:
- https://copilotstudio.microsoft.com/
- https://dev.azure.com/hack-cologne/TeamsRequestManager/

2. Repository creation automation
User ask to create a repository with all required permissions. The bot ask for the name and then check if such repository already exists. If yes then just add the user the permissions. If repository doesn't exist creates new and apply branch policies and creates and adds user to the repository contributors. Owner i always a group (name tbd). 

Before adding the permissions a approval flow should be started.

5. Create fallback flow - if the user request cannot be handled start fallback flow.

The fallback flow should create a ticket in Azure Dev Ops. The user which is creating the request should be set as creator, the content should be in ticket description. Copilot with the help of data verse should determine the ticket priority (low/high/prio) and responsible team (security/cloud/general)