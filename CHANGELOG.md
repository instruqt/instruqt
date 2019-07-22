# Changelog

All notable changes to the Instruqt platform will be documented in this file.
If you have any feature requests or bugs to report you can do so [here](https://github.com/instruqt/instruqt/issues).

If you have any questions regarding this changelog, feel free to reach out to us on [Slack](https://join.slack.com/t/instruqt/shared_invite/enQtMzcwNTY1OTQ5NzE2LTQ5YTgxODgzNTk4NzY0OWU0OTczZjlhNThlMGJjYmFlNTNiNTMxZTVhNjE4MTczYzkxNDNkNTc1NzYwN2RlY2M) or through [our website](https://instruqt.com).

## Unreleased
NEW FEATURES:
- Embedded Instruqt

## July
NEW FEATURES:
- Add option to override ENTRYPOINT/CMD of a container

IMPROVEMENTS:
- Inject container/vm env vars into setup, check and cleanup scripts

DEPRECATIONS:
- Removed vm pooling and preempitble settings. Pooling will return later, but then for entire environments, rather than just vms.

## June
NEW FEATURES:
- Track creation wizard
- Add users to organization by e-mail address
- Allow invites to be used anonymously (configurable)

IMPROVEMENTS:
- Show more user details in invite overview

BUG FIXES:
- Fixed editor reload bug

## May
NEW FEATURES:
- AWS Account support. Ability to provision temporary AWS accounts and provide users with temporary credentials to these accounts.

IMPROVEMENTS:
- Removed editor mode toggle
- Allow HTML in notes and assignments
- Detect use of unsupported Docker images (old image manifest version)

## April
IMPROVEMENTS:
- Improved user profiles
- Change Web SDK from modal forms to to inline editing
- Inject arcade difficulty level into check scripts
- Allow ordering of arcade tracks

BUG FIXES:
- Fix problem with spaces in ENTRYPOINT/CMD for containers

## March
NEW FEATURES:
- Arcade management for organizations

IMPROVEMENTS:
- Add update command to CLI
- Allow tracks in topic to be sorted

## February
NEW FEATURES:
- Custom branding for organizations

IMPROVEMENTS:
- Revamp arcade version (including online option)
- Add verification for e-mail based accounts
- Various responsiveness fixes

## January
NEW FEATURES:
- Editor Tab
- Allow anonymous plays

IMPROVEMENTS:
- Make usernames optional
- Document API at docs.instruqt.com

## December
NEW FEATURES:
- API keys for organizations

## November:
NEW FEATURES:
- Invites: invite non-organization users to private tracks
- Statistics: track level statistics

IMPROVEMENTS:
- Merge play.instruqt.com with instruqt.com
 
## October
NEW FEATURES:
- Ability to restart tracks
- Arcade version of Instruqt (https://instruqt.com/arcade)
- Added organizations on Instruqt

IMPROVEMENTS
- Security fixes, based on security audit

BUGFIXES:
- Fixes in cleanup
- Limit number of tracks started to 1

## September 17, 2018
NEW FEATURES:
- Quizes: instead of a challenge, a track can contain quiz questions
 
CLI IMPROVEMENTS:
- Rework: use `push`/`pull` instead of `build`
- Added track logs functionality (`instruqt track logs`)
- Added delete track functionality (`instruqt track delete`)

## August 18, 2018
NEW FEATURES:
- Manage tracks, challenges and track config in the web interface
- Publish or unpublish a track in the web interface
- Manage notes, tabs in challenges in the web interface
- Automatically provision Google Cloud Projects for track players.
- Add quizzes to tracks.
- New notifications system to serve notifications throughout the application
- From now on, the Instruqt SDK CLI tool will automatically check for updates. Be sure to grab the lastest copy from [https://github.com/instruqt/cli/releases/latest](https://github.com/instruqt/cli/releases/latest), after that you will be able to enjoy automatic updates.
- Interface to manage tracks in topic
