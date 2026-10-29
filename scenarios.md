# Walkthrough Scenarios

English | [简体中文](zh-CN/scenarios.md)

Combined scenarios exercise several items and the handoffs between them at once, which surfaces problems more readily than checking items one by one. To verify the checklist, pick the scenarios relevant to the product and run them in a real environment.

**Guidelines**: Choose scenarios by product; full coverage of every platform, device, and input method combination is not required. For scenarios that involve killing processes, disconnecting storage, overwriting, migrating, or uninstalling, use disposable samples and an isolated environment. When recording results, distinguish between two cases: evidence seen in the implementation, and behavior actually tested in the stated environment. Mark anything that could not be tested as "not verified".

Each scenario lists steps, checkpoints, and related items.

**Choosing by user moment**: The table groups scenarios by the moment the user is in, which shows which kinds of moments have not been walked through yet. The grouping is only for choosing scenarios and does not indicate priority. A scenario can appear under more than one moment.

| Moment | Scenarios |
| --- | --- |
| First use | S21, S23, S27, S40 |
| Interruption | S05, S10, S32 |
| Leaving | S09, S11, S20, S41 |
| Returning | S04, S26, S34, S41 |
| Mistake | S42 |
| Environment change | S02, S07, S08, S12, S15, S16, S18, S22, S28, S29, S30, S33, S38 |
| System failure | S06, S13, S17, S31, S37 |
| Repetitive work | S19, S25 |
| After an update | S14, S24 |
| Migrating in / running alongside | S43 |

S01, S03, S35, S36, and S39 test properties that hold at every moment (IME input, accessibility, local interface security, untrusted content, multilingual input) and are not listed in the table.

---

### S01 · Chinese or Japanese IME: confirm a candidate, then test save, undo, and Esc

Enable a Chinese or Japanese IME, type pinyin or kana in an input field, and press Enter to confirm a candidate. With the IME still on but no longer composing, press Ctrl/Cmd + S, Ctrl/Cmd + Z, and Esc. Then type more pinyin or kana and press Esc while the candidate window is open.

Checkpoints: Enter did not submit the content; the candidate window stays next to the insertion point; after confirmation, shortcuts and Esc worked and were not swallowed by IME handling; Esc during composition only cancelled the composition and did not close a dialog or panel.

Related items: INPUT-06 IME composition; INPUT-01 Platform shortcuts and keyboard layouts; INPUT-02 Dialog conventions

### S02 · Enlarge text, snap to half screen, unplug the dock

Set system text size to 125% or higher, snap the window to half of the laptop screen, move the window to an external display, then unplug the dock.

Checkpoints: The main window, dialogs, menus, and key buttons can still be found and operated; the window returns to a visible area; the snap layout flyout can be opened, and the window fits into the selected zone.

Related items: DISPLAY-01 System scaling; DISPLAY-02 Runtime display changes; DISPLAY-03 Mixed DPI; DISPLAY-04 Window size adaptation; DISPLAY-06 Text enlargement and reflow; WINDOW-01 Position and size restoration; WINDOW-02 Window state and system window management; WINDOW-12 Placement and stacking of owned windows

### S03 · Complete the core workflow with only a keyboard and a screen reader

Without a mouse, with NVDA, Narrator, VoiceOver, or Orca running, complete "launch → open or create → core action → save → close". Along the way, enter and leave an editing area once and close a dialog. Finally, turn on voice control (Voice Access on Windows, Voice Control on macOS) and click a button by saying its on-screen label.

Checkpoints: Every object and state is understandable; there are no keyboard traps; after a dialog closes, focus returns to the control that opened it; voice control can click buttons by their on-screen labels.

Related items: A11Y-01 Core workflows by keyboard; A11Y-02 Visible focus, logical order, focus return; A11Y-03 Assistive technology semantics; A11Y-04 Announced state changes; INPUT-02 Dialog conventions

### S04 · Filter a list, open details, go back, then trigger a background refresh

In a list, enter a filter, sort, and select several items. Open one item's details, return to the list, start renaming one item, and while typing, trigger an automatic refresh or sync.

Checkpoints: Filter, sort order, selection, scroll position, and tree expansion are unchanged; the refresh did not change the target under the pointer; an in-progress rename was not lost.

Related items: WINDOW-06 Workspace and view context restoration; DISPLAY-08 No flashing, no jumping, stable targets; INPUT-11 Multi-selection and batch actions; DATA-03 Protecting unsaved changes

### S05 · Out-of-order responses and account switching

Use throttling or a breakpoint so that the response to search A arrives after search B. In a networked product, switch accounts and then let a request from the previous account complete. Finally, start a search and close the window before the results arrive.

Checkpoints: The UI shows B's results; the previous account's response did not reach the new account's UI; no stale results appeared after the window closed.

Related items: TASK-11 Stale results do not override current intent; PRIVACY-05 Signing out and switching accounts or workspaces

### S06 · Save to an unwritable directory or full disk; test a forced kill separately

Using a sample document, make the target directory read-only or fill the disk, then save. Restore the condition and retry. In a separate round, edit past the autosave point, kill the process, and relaunch.

Checkpoints: The original file was not truncated to 0 bytes; in-memory content is still there and can be saved elsewhere; after the kill, the most recent autosave is recovered and the recovery UI shows its time. Record the two tests separately; killing a process does not simulate power loss.

Related items: DATA-06 Safe writes; DATA-02 Autosave and crash recovery; DATA-01 Visible save state; HELP-03 Actionable, copyable error messages

### S07 · External replace-saves and renames; opening a cloud placeholder offline

Use another editor to save an open file several times in a row (most editors write a temporary file and rename it), then rename the file and rename it back. Separately, take an online-only OneDrive or iCloud file, disconnect from the network, open it in the application, then index the whole folder.

Checkpoints: Every external save is detected, not just the first; after the rename, the application tracks the file or offers to relocate it; the placeholder is not reported as corrupt, there is no blocking without feedback, and no mass download is triggered.

Related items: DATA-07 External changes and conflicts; FILE-05 Network drives, removable media, and cloud placeholders; FILE-04 Feedback for move, rename, and delete

### S08 · Two clients edit the same content offline, then reconnect

Take two devices or two accounts offline at the same time. Edit different parts and the same part of one document on each, then reconnect. Also change an attachment and a setting on each side.

Checkpoints: Conflicts are surfaced and both versions can be recovered; conflict handling for attachments and settings is checked separately from text; the pending sync queue is visible before reconnecting.

Related items: DATA-07 External changes and conflicts; NETWORK-04 Visible sync queue; DATA-05 Version history and backup

### S09 · Recovering a background tool with notifications off, a hotkey conflict, and no tray

Turn off the application's notifications at the system level. Have another program take the application's global hotkey. Launch the application on a desktop without a tray (GNOME without extensions).

Checkpoints: The settings page does not show the hotkey as active; the application can still be reopened and quit through its icon, a menu, or the command line; the process can always be found and ended.

Related items: SYSTEM-04 Global shortcuts; SYSTEM-02 Tray or menu bar entry; SYSTEM-11 Alternatives when system features are unavailable; SYSTEM-03 System notifications and attention

### S10 · Cancelling, sleeping, switching networks, and interrupting a long task

Start a download, conversion, or recording and cancel it partway. Start it again, close the lid for a few minutes, and wake the machine. Start it again and switch Wi-Fi or toggle a VPN. Finally, forcibly interrupt a recording or generation task and open the output in a downstream application.

Checkpoints: The fate of partial output after cancellation is clear; after wake and network changes, the task either continues or fails clearly without a cascade of errors; the sleep prevention request is released when the task ends; the usability of the interrupted output and its secondary information are described separately.

Related items: TASK-03 Stop waiting, cancel the task, or revert the result; TASK-09 Sleep, wake, network, and device changes; TASK-12 Output after an interrupted long task; SYSTEM-08 Preventing sleep; TASK-05 Retry and idempotency

### S11 · Drag in from various sources; paste after closing the source; copy a secret, then plain text

Drag content in from a file manager, an email client, a screenshot tool, and a browser, and cancel one drag. Copy content in the application, close the window or quit, and paste elsewhere. Copy password or token A and wait for the clear timeout. Copy A again, then copy plain text B in another application, and wait for the timeout again.

Checkpoints: Every source produces drop feedback, and unsupported sources are explained; content can still be pasted after the source closes; target applications receive the correct format (test once each with a plain text editor, a document editor, and a chat application); in the first round A was cleared; in the second round B is still on the clipboard.

Related items: INPUT-09 Drag in; INPUT-10 Clipboard formats and lifetime; INPUT-13 Drag out; INPUT-21 Dragging within the application; PRIVACY-07 Displaying and copying sensitive content

### S12 · Moving a project to a new drive, user name, and machine; case-conflicting names

Move a project folder, together with the images, attachments, and fonts it references, to another drive or another computer with a different user name. Place `Readme.md` and `readme.md` in the folder and sync it to a case-insensitive file system.

Checkpoints: Resources can be relocated, a single relocation fixes the whole batch, and records for missing resources are not deleted; files that differ only by case are not silently overwritten, and the resolution is clear.

Related items: DATA-11 Relocating external resources; DATA-09 Transparent, movable data location; FILE-03 Paths, characters, and name collisions

### S13 · Back up during editing and restore to an empty directory; export a complex project

While editing is in progress, export using the application's backup feature, copy the result to an empty directory or another computer, and restore it. Separately, export a project with multiple layers or sheets to an open format and open it in the target application.

Checkpoints: Restored data includes the latest changes and attachments, and databases in use were exported through a backup interface; the scope and losses were stated before export; users can tell the full project apart from the delivered output.

Related items: DATA-05 Version history and backup; DATA-08 Import, export, and data portability

### S14 · Upgrade with the final release package; downgrade and open a copy of the data

Upgrade from the previous version using the installer that is actually distributed, then sign out and back in. Check launch at login, file associations, recent files, and sandbox grants. Then install the previous version and open a copy of the data. Separately, upgrade once with a copy of data that makes the migration fail.

Checkpoints: Registrations and grants work after the upgrade; a failed migration leaves the data as it was before the upgrade; when the older version opens newer data, it refuses clearly, opens read-only, or enters a recovery flow, and the data is not damaged; when a safe downgrade is not possible, the reason is given.

Related items: INSTALL-05 Program rollback and data downgrade; SETTINGS-08 Migration on upgrade; SYSTEM-01 Launch at login; FILE-01 Platform file dialogs and persistent access; DATA-10 Protection for bulk deletion and migration

### S15 · Switch keyboard layouts; browse remotely loaded items with arrow keys

Switch to a non-US keyboard layout (German, French, or Japanese) and test punctuation shortcuts and normal character input. Move between items in a list or tabs using only arrow keys, where each item's content loads remotely.

Checkpoints: Shortcuts are displayed for the current layout and can be triggered; arrow key browsing did not trigger external actions or irreversible changes, and previews loading with the selection did not block further movement.

Related items: INPUT-01 Platform shortcuts and keyboard layouts; INPUT-17 Separating browsing from activation; INPUT-04 Customizable shortcuts

### S16 · Change settings on another device and sync

For products with settings sync: on a desktop, change a local path, a device selection, and a shortcut, then check on a laptop.

Checkpoints: Machine-specific values did not overwrite each other; platform-specific shortcuts are kept separately; credentials were not synced.

Related items: SETTINGS-06 Exportable, editable, syncable configuration; SETTINGS-05 Clear scope

### S17 · Temporarily disable extensions to troubleshoot, restore, then export a diagnostic bundle

Install a plugin that fails or breaks the layout, confirm the problem in safe mode or with temporary isolation, then leave temporary mode and return to the original environment. Export a diagnostic bundle, extract it, and review it.

Checkpoints: Temporary mode did not change the original configuration; plugin states are restored after troubleshooting; the bundle describes its contents and can be previewed before sending; test markers placed in file names, paths, and the personal dictionary do not appear in the bundle.

Related items: HELP-07 Safe mode and self-recovery; HELP-05 Diagnostic logs and bundles; SETTINGS-07 Reset by category

### S18 · Sign in, download, and update behind a proxy; cancel one authentication

In a supported proxy environment, sign in, call the core API, load images, download a file, and check for updates, in that order. Cancel a browser sign-in partway through, then complete a full sign-in.

Checkpoints: Every path goes through the proxy, and failures identify which service failed; after cancelling sign-in, the user returns to the original screen with input intact; after signing in, the user returns to the correct window and task.

Related items: NETWORK-05 Proxies and corporate networks; NETWORK-07 Sign-in return path; NETWORK-01 Connection state

### S19 · Repeated successes and repeated failures

Run a batch save twenty times in a row. Let reconnection fail ten times in a row. Repeat an action that produces the same error.

Checkpoints: Success feedback is lightweight and local, with no twenty toasts; failure messages are grouped, and the important one is still findable with an actionable option after the toast disappears.

Related items: SYSTEM-03 System notifications and attention; HELP-03 Actionable, copyable error messages; WINDOW-08 No focus stealing

### S20 · Resource usage when hidden and idle

Minimize the window or hide it in the tray for thirty minutes. Separately, leave it visible but untouched for ten minutes.

Checkpoints: CPU usage is near zero, memory does not keep growing, and there is no pointless disk or network activity; unnecessary animation and polling have stopped or slowed down. The resource budget is set by the product; monitoring products are exempt for their necessary work.

Related items: TASK-08 Idle resource budget; SYSTEM-02 Tray or menu bar entry

### S21 · Open an unfamiliar project: view read-only first, then grant trust

Download a project or document containing build scripts or macros, open it directly, and read it. Then grant trust once. Then open another new file in the same folder.

Checkpoints: No script ran on open, and the UI explained which capabilities were suspended; the grant stated whether it covers this time, this file, or this folder; the new file in the same folder was not trusted along with it unless the grant stated that it covers the folder; hovering over external links in the document shows the real target.

Related items: TRUST-01 Restricted view first; TRUST-02 Clear scope of trust; TRUST-04 Verifiable link targets

### S22 · License expired and the old device is gone

Launch with an expired trial or subscription account. Then simulate an unreachable license server. Finally, activate on a new device while the old device is unavailable.

Checkpoints: After expiration, users can still view and export their work and know which parts cannot be exported; with the server unreachable, network failure is distinguished from an invalid license, and the application did not close in the middle of a save; the new device can be activated through remote deactivation or a support path.

Related items: LICENSE-01 License state and available scope; LICENSE-02 Retrieving existing work after expiration; LICENSE-03 Handling failed verification; LICENSE-04 Changing or losing devices; DATA-08 Import, export, and data portability

### S23 · Silent deployment on an isolated network, then a policy lock

On a machine without internet access, deploy using the administrator's silent install command. Then push a policy that locks "Automatic updates". Sign in as a standard user and use the application.

Checkpoints: Installation did not stall on a hidden dialog, and the administrator received the result and any failure reason; the first launch did not require downloading a runtime or activating online; the locked setting shows that it is managed, and the user's change is not shown as saved; configuration is written to the standard user's own directory.

Related items: MANAGED-01 Unattended deployment; MANAGED-02 User and machine scope; MANAGED-03 Visible policy control; MANAGED-04 Complete path for isolated networks; SETTINGS-05 Clear scope; INSTALL-03 Update preferences

### S24 · Recovering from a failed extension update

Install several extensions. Let one of them update automatically to an incompatible version. Then disable it, roll it back, and uninstall it.

Checkpoints: When the update fails, the main application and other extensions still work; the UI shows which extension updated and when; after disabling, its background tasks have stopped, or the UI stated that a restart is needed; uninstalling did not delete content the user created; data and settings compatibility was stated before rollback.

Related items: EXTEND-02 Identifiable origin and dependencies; EXTEND-03 Controlled updates; EXTEND-04 Effects of disabling and removal; HELP-07 Safe mode and self-recovery

### S25 · Unattended batch conversion with one failure

Use the command line or scripting interface to convert a batch of files into a specified directory, with one deliberately corrupted input file. Have the caller judge the result by exit code. Then run it again.

Checkpoints: Success or failure of each file can be determined from the exit code or a result file, not only from printed text; no hidden dialog is waiting for input; the rerun did not duplicate the previous run's successful output; steps requiring interaction are documented.

Related items: AUTOMATE-01 Composable entry points for repetitive tasks; AUTOMATE-03 Determinable input, output, and completion; TASK-05 Retry and idempotency; TASK-03 Stop waiting, cancel the task, or revert the result

### S26 · Searching for something that exists and finding nothing

In a previous session, set a search scope or exclusion (current folder only, exclude a type, regex enabled). Close the application. After reopening, search for an object within the scope, then for an object that is excluded, then widen the scope as suggested and search again.

Checkpoints: The object within the scope is found; the current scope and active mode are shown near the search field; with no results, the UI suggests widening the scope or checking the conditions, and after widening, the excluded object appears in the results; the result list can be traversed with the keyboard and returns to the original position.

Related items: FIND-01 Visible scope and exclusions; FIND-02 Recognizable matches, navigable results; FIND-03 Visible matching mode; HELP-02 Empty states that suggest a next step

### S27 · First core task on a fresh system; decline a component download once

On a supported system with no development tools or extra runtimes, install the final release package as a standard user. Use a feature that needs an external component for the first time, then decline the component download once.

Checkpoints: No hidden dependency on PATH or the development environment; the missing component has a name, purpose, and download path; after declining, the user can quit or keep using other features.

Related items: INSTALL-09 Runtime dependencies on a fresh system; COMPONENT-02 Acquiring and removing on-demand resources; INSTALL-01 Installation scope and first launch; INSTALL-12 Signing, source verification, and system gatekeeping

### S28 · Launch from a DMG or read-only share and save; then move the program

Launch from a read-only share or a mounted DMG, read and save once; where the platform allows, move the running program, then trigger a helper feature that has not loaded yet.

Checkpoints: Nothing is forced into the program directory; the data location is clear; lazily loaded resources and helpers are still found, or a clear restart prompt appears.

Related items: INSTALL-10 Running from a read-only or protected location; COMPONENT-01 Coexistence with system copies; DATA-09 Transparent, movable data location

### S29 · Stable and beta side by side; switch system user; uninstall one

Install the stable and beta releases side by side, launch each and open a file externally; switch to another system user and launch again; finally uninstall one of the two.

Checkpoints: Instance locks and open routing are not confused; no cross-version configuration is overwritten without notice; user data stays isolated; uninstalling does not affect the other version.

Related items: WINDOW-04 Multi-window and multi-instance rules; WINDOW-05 Routing on relaunch and external open; MANAGED-02 User and machine scope; INSTALL-06 Uninstallation scope

### S30 · Incompatible tool of the same name on PATH; paths with spaces and non-BMP characters

Place an incompatible FFmpeg, Python, or download engine of the same name on PATH; give the user directory, temp directory, and resource directory names with spaces, emoji, and non-Latin characters.

Checkpoints: The application uses the intended component; no wrong copy is called, no command is split, no characters are mangled; component versions are identifiable.

Related items: COMPONENT-01 Coexistence with system copies; FILE-03 Paths, characters, and name collisions; INPUT-07 Standard text editing behavior

### S31 · Kill the conversion helper; then quit normally and kill the main program

While editing a document and running a conversion, kill the conversion helper; then test a normal quit and a forced kill of the main program, checking for leftover processes, lock files, and ports.

Checkpoints: The local failure does not lose other edits; the failed object and recovery entry are clear; no child processes, capture, or ports remain after exit; the next launch is not blocked by a stale lock file.

Related items: TASK-14 Fault isolation of subsystems in use; COMPONENT-03 Identity and lifetime of helper processes; FILE-08 File locks and stale lock files; WINDOW-03 Clear close, minimize, and quit behavior; DATA-02 Autosave and crash recovery

### S32 · Two applications competing for media control

Play music first, then play an attachment in the application under test; use the headset media keys and the system media controls; adjust per-application volume; stop the attachment and press the media key once more.

Checkpoints: Now-playing information and the controlled target are correct; no unprompted exclusive access or changes to other applications' audio; system volume applies; media keys are not captured after playback ends.

Related items: MEDIA-01 System media controls and now-playing information; MEDIA-02 Volume, mixing, and exclusive access; COMPONENT-03 Identity and lifetime of helper processes

### S33 · Confirm the capture source, then lose the capture target

Select a muted or signal-less input, check the preview, then switch to a working input; capture a single window, close that window, then stop capturing.

Checkpoints: The missing signal is visible before starting; the actual capture state is shown throughout; the vanished window does not widen capture to the full screen; stopping releases the device.

Related items: MEDIA-03 Confirming the capture source; MEDIA-04 Actual capture state and stop control; MEDIA-05 Confirming the screen capture scope

### S34 · Source changed before resume; problematic names, checksums, and disk space

Quit halfway through a download, replace the file at the same server address with another version, then launch and resume. Separately: download the same file twice, use a suggested file name containing path fragments and a reserved name, download a file with a wrong checksum; fill the target disk and the temp disk in turn.

Checkpoints: The two versions are not spliced together; resume information is kept; name handling stays inside the target directory and does not overwrite silently; partial files are not treated as final results; a wrong checksum is not shown as success; running out of space keeps the recovery context.

Related items: TASK-04 Pause and resume; TRANSFER-01 Integrity verification; TRANSFER-02 Boundary between partial files and final results; FILE-03 Paths, characters, and name collisions; DATA-06 Safe writes

### S35 · Reach the local interface from unexpected callers

In an authorized test environment, try to reach the application's local service and IPC entry points from another device on the LAN, from an ordinary web page, and from another system user.

Checkpoints: Sample data cannot be read and unauthorized actions cannot be triggered; listening on loopback alone is not treated as the whole authorization mechanism; legitimate callers still work.

Related items: PRIVACY-09 Access boundaries of local services and IPC; AUTOMATE-04 Delegation that can be enabled, stopped, and reviewed; MANAGED-02 User and machine scope

### S36 · Import an archive with escaping paths; export a sample with hidden information

Import an archive containing `../` paths and symbolic links; share and export a sample containing author, location, comments, and hidden content.

Checkpoints: The import stays inside the target directory; private metadata is identifiable and removed as chosen; required content and dependencies are not removed by mistake.

Related items: TRUST-05 Directory boundary on archive import; PRIVACY-11 Hidden information in exports and shares; DATA-08 Import, export, and data portability

### S37 · Launch with a corrupted data file; shut down while editing and downloading

Corrupt a few bytes of the data file with a hex editor and launch. Separately, shut down or sign out while an edit and a download are in progress, then check after the restart.

Checkpoints: The corrupted file is not overwritten with defaults, a recovery or export path is offered, and there is no crash loop; state is saved quickly on shutdown and any shutdown block states its reason; the session is restored after the restart.

Related items: DATA-13 Handling corrupted data files; SYSTEM-12 Shutdown, sign-out, and system restart; DATA-02 Autosave and crash recovery

### S38 · IPv6-only network; certificate failure; clock change during a task

On an IPv6-only test network, sign in, make core requests, and download; use a test certificate to force identity verification to fail; move the system clock forward and back while a task runs.

Checkpoints: No hidden IPv4 dependency; a failed verification does not turn into an insecure connection; errors are distinguishable; the clock jump causes no retry storm or absurd durations.

Related items: NETWORK-09 IPv6 networks; NETWORK-08 Transport encryption and server identity; NETWORK-01 Connection state; TASK-09 Sleep, wake, network, and device changes

### S39 · Multilingual input and authentication forms

Type composed emoji, combining marks, and Arabic file names; enter numbers in a decimal-comma region; enter several quantities and switch languages; paste a complete password and verification code from a credential manager; submit a form with one invalid field.

Checkpoints: Editing does not split characters; the real identity of file names is clear; number parsing matches display; plural grammar is correct; authentication needs no manual transcription; the error points to the field and valid input is kept.

Related items: INPUT-07 Standard text editing behavior; LOCALE-03 Dates, numbers, units, and currency; LOCALE-06 Right-to-left scripts; INPUT-18 Input constraints and inline correction; INPUT-19 Assisted authentication

### S40 · Purchases, license materials, and policy access

Go through a trial and purchase flow in a store sandbox or with a test account and check the final charge terms; restore the purchase after reinstalling; look up third-party licenses and the accepted terms while offline.

Checkpoints: Cost and renewal terms are complete before purchase; entitlements can be restored or the identity mismatch is explained; license materials and policy text are reachable.

Related items: FAIR-05 Clear pricing, trial, and renewal terms; LICENSE-04 Changing or losing devices; COMPONENT-04 Third-party licenses and notices; PRIVACY-12 Terms and privacy policy remain accessible

### S41 · Leave mid-draft, close, and relaunch; finish reading on another device

Write a draft in two objects without submitting, then switch to a third object. Close the window and relaunch, then wait longer than the autosave interval, force-quit, and relaunch again. On another device, read the new content in one of the objects, then return to this machine.

Checkpoints: The list or a central entry point shows which two objects have unfinished work; the drafts survive the relaunch and the forced quit, and the marker disappears after submitting; content read on the other device shows as read here, and the badge updates.

Related items: DATA-14 Unfinished work is discoverable after leaving; SYSTEM-14 Accurate unread and pending state; DATA-02 Autosave and crash recovery; DATA-07 External changes and conflicts

### S42 · Recovering from a wrong deletion, overwrite, or click

Delete several objects in a batch, restore one with undo, and recover the rest from the trash or the application's restore entry point. Import a file that overwrites existing content, then undo. Make a change in each of two windows, switch focus, and press Ctrl/Cmd + Z. Mess up a group of settings and reset that category. Perform a frequent action that takes effect immediately (move, archive, or send), then undo it.

Checkpoints: Deleted objects can be recovered with their location and properties unchanged; the import can be undone, and manual edits made before the import remain; undo affects only the object that has focus; the reset stated its scope before running, and settings in other categories were unaffected; the immediate action could be undone within the undo period, and the UI showed where to undo.

Related items: INPUT-14 Undo over confirmation; DATA-04 Undo and redo targets; DATA-10 Protection for bulk deletion and migration; FILE-04 Feedback for move, rename, and delete; SETTINGS-07 Reset by category

### S43 · Migrating from a similar product

In the shortcut settings, choose the scheme preset that matches a comparable product. Export a batch of tagged or categorized objects from the similar product and import them. In a submit-style input, press the send key that was habitual in the previous product. After installing a new major version, import settings from the previous version.

Checkpoints: The preset is available, and after applying it a key lookup returns the right action; the import offers a choice of how tags are merged, and the result states what was discarded; the send key can be switched and is not reverted by "reset all shortcuts"; the imported settings take effect, and obsolete ones are explained.

Related items: INPUT-04 Customizable shortcuts; DATA-08 Import, export, and data portability; INPUT-22 Configurable send key in submit-style inputs; SETTINGS-08 Migration on upgrade
