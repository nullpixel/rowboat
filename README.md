# Rowboat

[![](https://discordapp.com/api/guilds/290923757399310337/embed.png?style=banner2)](https://discord.gg/rowboat)

Rowboat is a private Discord bot focused on being a highly powerful and configurable moderation and utilitarian bot for Discord. Rowboat is built to feel and behave similarly to [AutoModerator](https://github.com/Deimos/AutoModerator) for reddit.

## Should I Run Rowboat Locally?

Probablly not. Rowboat has enough moving pieces that running a local version is complicated. The main purpose of having the source released is to allow others to understand and audit the functionality. The code is by no means meant to be easy to setup or bootstrap, and I don't plan on supporting folks trying to run locally. That said, feel free to run a local version of Rowboat for your server (but not a public version please).

### Notes to run locally:
Rowboat depends on a lot of third party tools. The example configuration file outlines all things you will need, but these.

* Install redis, and start it on the default port
* Install postgresql, and make two databases, `rowboat`, and `rowboat_stats`. Give the user `rowboat` access to these.

To grant yourself admin, you need to update the column in the `rowboat` database, then run `redis-cli`, `SELECT 11`, and then `sadd global_admins <your id>`. 

These steps are only here to help you get it running locally for if you want to contribute. 

## Development

Rowboat development is focused on the requirements of servers looking to move onto Rowboat as their core moderation bot. Generally a good overview of the planned or in-development tasks is the [Trello Board](https://trello.com/b/wiCACp0k/rowboat), although its by no means a purely-true source.

## Can You Add Rowboat To My Server?

Maybe. If you are interested in having Rowboat on your server, please join ([discord.gg/rowboat](https://discord.gg/rowboat)) the server and provide an invite and some general information. Rowboat is only added to larger (1-2k+ average CCU) servers that have more complex moderation requirements.

## Can I Contribute?

Maybe. Feel free to submit PRs, but unless they are explicitly bug fixes that have good documentation and clean code, I likely won't merge. Features will not be accepted through PR unless stated elsewhere. Do not submit feedback on this repository, the server is the right place for that. PRs focused around the frontend and web panel are more likely to be accepted.

