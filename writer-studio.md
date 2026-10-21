---
layout: default
title: Writer Studio
permalink: /writer-studio/
---

# Writer Studio

Writer Studio is a local-first writing and document-production application for
Android. It helps professional writers plan, draft, revise, organize,
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
When enabled, project safety copies can synchronize automatically after saves.
The [Privacy Policy, section 4.2.1](https://hafych.github.io/#writer-studio-google-data)
explains the Google account data, project data, uses, storage and deletion controls.

Ordinary Google Drive safety copies are readable `.writer` ZIP archives. Writer
Studio does not encrypt these archives before uploading them; anyone with access
to a downloaded archive can read the included text and attachments without the
app's local project key or a recovery secret.

## Dropbox collaboration access

Dropbox collaboration is optional and starts only after the user explicitly
chooses **Connect Dropbox** in the Library. Writer Studio uses Dropbox shared
folders to exchange project snapshots, manuscript changes, comments and
collaboration metadata. It
requests `account_info.read`, `files.metadata.read`, `files.content.read`,
`files.content.write`, `sharing.read`, and `sharing.write` so it can identify the
connected account, create and synchronize the project's shared resources,
invite collaborators, change an editor or reader role, and remove access.

The project owner controls each invitation and can change or revoke a
collaborator's access from Writer Studio. Users can disconnect Dropbox in the
app and can revoke the application's authorization from their Dropbox account
settings. Writer Studio does not connect to or access Dropbox until the user
initiates the OAuth authorization flow.

The integration requires Full Dropbox access because Dropbox's shared-folder
APIs do not support App Folder access. This permission technically allows access
across the connected account; the app directs project operations to its created
or joined project resources. Optional recovery also uses a separate
`/.writer-studio` folder for passphrase-encrypted key-recovery envelopes.

Ordinary Dropbox project snapshots, manuscript edits and comments are not
encrypted by Writer Studio before uploading them. The snapshot ZIP archives and
collaboration JSON files contain readable content; Dropbox and people with the
relevant file access can read it without the app's local project key or a recovery
secret. Read the
[Privacy Policy, sections 4.2.2 and 4.2.3](https://hafych.github.io/#writer-studio-dropbox-data)
for transferred data, participant access, credential storage and deletion controls.

## Encryption and recovery

- On Android, local project files and their locally stored attachments are
  encrypted using project keys kept in protected device storage. This local
  protection does not encrypt ordinary cloud archives or collaboration files.
- An explicitly exported `.writer-recovery` bundle is encrypted with a separate
  recovery secret. It is a snapshot at export time, not an automatically updated
  backup. Keep both the bundle and its matching secret, stored separately.
- Optional key backup protects project keys with a user-chosen passphrase. Its
  recovery envelopes contain keys, not manuscript backups; restoration requires
  a previously saved available envelope and the matching passphrase.

See the [Privacy Policy, section 4.2.4](https://hafych.github.io/#writer-studio-encryption-recovery)
for local encryption and recovery details. Ordinary cloud files are not
end-to-end encrypted by Writer Studio. HTTPS and the provider's own storage
protection are separate from these application encryption mechanisms.

## Support and legal information

- [Privacy Policy](https://hafych.github.io/#privacy-policy) — Version 1.7,
  effective 21 October 2026
- [Terms of Use](https://hafych.github.io/#terms-of-use) — Version 1.4,
  effective 29 July 2026
- [Business-to-Business Data Processing Addendum](https://hafych.github.io/dpa/)
- Support: [nazariihafych@gmail.com](mailto:nazariihafych@gmail.com)

Writer Studio is provided by Nazarii Hafych under the HAFYCH brand.
