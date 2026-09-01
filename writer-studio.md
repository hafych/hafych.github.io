---
layout: default
title: Writer Studio
permalink: /writer-studio/
---

# Writer Studio

Writer Studio is a local-first writing and document-production application for
Android and macOS. It helps professional writers plan, draft, revise, organize,
compile, and export long-form projects.

## How the app works

- Projects and drafts are stored locally on the user's device by default.
- Users can compile and export their work in supported document and publishing
  formats.
- Optional Google Drive integration lets a user back up and synchronize Writer
  Studio project files through their own Google Account.
- Optional Dropbox integration lets a project owner invite editors and readers,
  synchronize shared project data, change collaborator roles, and revoke access.
- Optional Pro subscriptions are purchased and managed through the applicable
  app store.
- Writer Studio can prepare copy-ready prompts for use with an external AI
  service; it does not represent those prompts as built-in AI processing.

## Google Drive access

Google Drive access is optional and starts only after the user chooses to sign
in and enable synchronization. Writer Studio requests the
`https://www.googleapis.com/auth/drive.file` scope. This scope allows the app to
see and manage only the Drive files that the user creates or opens with Writer
Studio, rather than all files in the user's Drive.

Users can disconnect Google Drive from Writer Studio and can revoke the app's
Google Account access at any time from their Google Account settings.

## Dropbox collaboration access

Dropbox collaboration is optional and starts only after the user explicitly
chooses **Connect Dropbox** in the Library. Writer Studio uses Dropbox shared
folders to exchange encrypted project snapshots and collaboration metadata. It
requests `account_info.read`, `files.metadata.read`, `files.content.read`,
`files.content.write`, `sharing.read`, and `sharing.write` so it can identify the
connected account, create and synchronize the project's shared resources,
invite collaborators, change an editor or reader role, and remove access.

The project owner controls each invitation and can change or revoke a
collaborator's access from Writer Studio. Users can disconnect Dropbox in the
app and can revoke the application's authorization from their Dropbox account
settings. Writer Studio does not connect to or access Dropbox until the user
initiates the OAuth authorization flow.

## Support and legal information

- [Privacy Policy](https://hafych.github.io/#privacy-policy) — Version 1.3,
  effective 29 July 2026
- [Terms of Use](https://hafych.github.io/#terms-of-use) — Version 1.3,
  effective 29 July 2026
- [Business-to-Business Data Processing Addendum](https://hafych.github.io/dpa/)
- Support: [nazariihafych@gmail.com](mailto:nazariihafych@gmail.com)

Writer Studio is provided by Nazarii Hafych under the HAFYCH brand.
