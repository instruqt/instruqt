# Changelog

All notable changes to the Instruqt platform will be documented in this file.
If you have any feature requests or bugs to report you can do so [here](https://github.com/instruqt/instruqt/issues).

If you have any questions regarding this changelog, feel free to reach out to us on [Slack](https://join.slack.com/t/instruqt/shared_invite/enQtMzcwNTY1OTQ5NzE2LTQ5YTgxODgzNTk4NzY0OWU0OTczZjlhNThlMGJjYmFlNTNiNTMxZTVhNjE4MTczYzkxNDNkNTc1NzYwN2RlY2M) or through [our website](https://instruqt.com).

## June 2020
NEW FEATURES:
- Added `show_timer` option to track.yml and track settings. When `true`, a timer will be shown on the assignment screen stating how long the participant has left untill the environment will expire.

IMPROVEMENTS:
- Added cooldown period for AWS accounts, so they will not be reused within the hour
- When the sandboxed environment expires, users will see a message that the environment has expired

BUG FIXES:
- Fixed bug where tracks with GCP projects would fail to start intermittently with error "Provider produced inconsistent result after apply"


## May 2020
NEW FEATURES:
- Enable pooling for tracks. This enables having hot standby environments, so tracks start faster for your users. The pooled phase of an environment is billed per minute. Contact us if you want to enable pooling for your account.

IMPROVEMENTS:
- `instruqt track test` now skips quiz type challenges

BUG FIXES:
- Fixed bug where any organization member could force push a track, even if they are not a developer
- Fixed bug when saving files after changing tabs in the editor
- Fixed bug when renaming a container/vm wouldn't also rename the corresponding scripts and tabs

## April 2020
NEW FEATURES:
- Organization level statistics of track plays
- Azure support (in private beta)
- Allow organization members to skip challenges (feature flagged)

BUG FIXES:
- Small css fixes for notes (overlapping images, indentation of code blocks)

INTERNALS:
- Add dynamic authentication to participant proxy
- Migrate to pub/sub for environment creation and cleanup

## March 2020
NEW FEATURES:
- Alibaba Cloud support (in private beta)

IMPROVEMENTS:
- Auto accept invite option

BUG FIXES:
- Fixed saving file in editor

## February 2020
IMPROVEMENTS:
- Make track/challenge teaser optional
- Filter track developers from statistics

## January 2020
NEW FEATURES:
- Added some options to embedding tracks (auto start on load, hiding the assignment on start, hiding the check button). View your track's embed page to see available options (More to come, let us know if you have any suggestions).

IMPROVEMENTS:
- Force challenge ID's to be empty when pushing a new track from CLI. This prevents overwriting existing challenges.
- The `instruqt track test` command now waits for the challenge cleanup script to be finished before going to the next challenge.
- The track creation wizard now automatically generates the track slug.

BUG FIXES:
- Fixed syntax highlighting in editor when switching files.
- Fixed incorrect expire dates in track invite overview.

## December 2019
IMPROVEMENTS:
- Added SCP Policy field to AWS config
- Removed deploy track from frontend & CLI because deploying tracks is not necessary anymore.

BUG FIXES:
- If the user token expires on the frontend, retry refreshing the token

## November 2019
NEW FEATURES:
- Users will see a median waiting time when the track environment is spinning up.
- Added track lifecycle scripts (cleanup only for now). With this lifecycle script you can execute code before the entire track environment is cleaned up.
- Added `instruqt track test` command to CLI. Read more about testing track on our [documentation page](https://docs.instruqt.com/#testing-amp-debugging)

IMPROVEMENTS:
- Improved polling of track status when the user is waiting for the environment spinning up.
- Sort tracks by title for invites
- The first challenge setup script will automatically start after the environment was created. Previously this was initiated by the frontend.
- You can now use `--slug <organzation-slug>/<track-slug>` shorthand with our CLI tool.

BUG FIXES:
- Fixed bug for removing tracks from topic

## October 2019
BUG FIXES:
- Instruqt file editor
  - A bug where there was a chance the file was not saved has been fixed

IMPROVEMENTS:
- Environments spinup performance increased
  - We've made some changes in the way we spin up environments for users which enables more concurrent spinups and better performance
- Instruqt file editor
  - Dramatically increased the performance of the editor
  - The file tree is now collapsed by default
  - You can now create new files and folders by clicking the + icons in the file tree
  - You can now select the language of the file in the bottom right corner to get syntax highlighting. The editor detects most file extensions
  - You can now change the width of the left panel (file tree)
  - When you click on another tab (for example a terminal tab) and create a file on the filesystem, the editor will now show the new files when you go back to the editor. (note that it will not change the contents of files that you already had opened)

## September 2019
NEW FEATURES:
- Added ability to skip to a challenge as a track developer
- Added challenge solve script (for use with skipping challenges)
- The track creation wizard will now save progress in the browser

BUG FIXES:
- Fixed user profile now working for some users
- Fixed a bug in the arcade where the input loses focus when entering your name

IMPROVEMENTS:
- Added validation for challenge scripts

## August 2019
NEW FEATURES:
- Embedded Instruqt
- Show track progress (attempts and number of challenges completed) in invite claims
- Limit accepting invites to certain email addresses only
- An estimate of how long it takes to spin up the environment is now shown when creating an environment

## July 2019
NEW FEATURES:
- Add option to override ENTRYPOINT/CMD of a container
- Add click-to-copy on code blocks in assignments
- Add option to put track into maintenance mode, so it is still visible, but temporarily not playable.

IMPROVEMENTS:
- Inject container/vm env vars into setup, check and cleanup scripts

INTERNALS:
- Complete upgrade to Terraform 0.12

DEPRECATIONS:
- Removed vm pooling and preempitble settings. Pooling will return later, but then for entire environments, rather than just vms.

## June 2019
NEW FEATURES:
- Track creation wizard
- Add users to organization by e-mail address
- Allow invites to be used anonymously (configurable)

IMPROVEMENTS:
- Show more user details in invite overview

BUG FIXES:
- Fixed editor reload bug

## May 2019
NEW FEATURES:
- AWS Account support. Ability to provision temporary AWS accounts and provide users with temporary credentials to these accounts.

IMPROVEMENTS:
- Removed editor mode toggle
- Allow HTML in notes and assignments
- Detect use of unsupported Docker images (old image manifest version)

## April 2019
IMPROVEMENTS:
- Improved user profiles
- Change Web SDK from modal forms to to inline editing
- Inject arcade difficulty level into check scripts
- Allow ordering of arcade tracks

BUG FIXES:
- Fix problem with spaces in ENTRYPOINT/CMD for containers

## March 2019
NEW FEATURES:
- Arcade management for organizations

IMPROVEMENTS:
- Add update command to CLI
- Allow tracks in topic to be sorted

## February 2019
NEW FEATURES:
- Custom branding for organizations

IMPROVEMENTS:
- Revamp arcade version (including online option)
- Add verification for e-mail based accounts
- Various responsiveness fixes

## January 2019
NEW FEATURES:
- Editor Tab
- Allow anonymous plays

IMPROVEMENTS:
- Make usernames optional
- Document API at docs.instruqt.com

## December 2018
NEW FEATURES:
- API keys for organizations

## November 2018
NEW FEATURES:
- Invites: invite non-organization users to private tracks
- Statistics: track level statistics

IMPROVEMENTS:
- Merge play.instruqt.com with instruqt.com

## October 2018
NEW FEATURES:
- Ability to restart tracks
- Arcade version of Instruqt (https://instruqt.com/arcade)
- Added organizations on Instruqt

IMPROVEMENTS
- Security fixes, based on security audit

BUGFIXES:
- Fixes in cleanup
- Limit number of tracks started to 1

## September 2018
NEW FEATURES:
- Quizes: instead of a challenge, a track can contain quiz questions

CLI IMPROVEMENTS:
- Rework: use `push`/`pull` instead of `build`
- Added track logs functionality (`instruqt track logs`)
- Added delete track functionality (`instruqt track delete`)

## August 2018
NEW FEATURES:
- Manage tracks, challenges and track config in the web interface
- Publish or unpublish a track in the web interface
- Manage notes, tabs in challenges in the web interface
- Automatically provision Google Cloud Projects for track players.
- Add quizzes to tracks.
- New notifications system to serve notifications throughout the application
- From now on, the Instruqt SDK CLI tool will automatically check for updates. Be sure to grab the lastest copy from [https://github.com/instruqt/cli/releases/latest](https://github.com/instruqt/cli/releases/latest), after that you will be able to enjoy automatic updates.
- Interface to manage tracks in topic
