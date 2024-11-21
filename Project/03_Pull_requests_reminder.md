## Pull requests reminder (optional - probably an power automate flow)

Some developers are waiting long time for thier Pull Requests beeing checked. This automation would daily check if there are any pull requests not checked. If not checked PR is found then:
- the bot should try to determine users that need to check the pr
- if not user is determined then team should be determined (creator team)
- the bot should send direct messages and message on team channel with summary or all team non checked pr's (the oldest on top, newest on bottom)