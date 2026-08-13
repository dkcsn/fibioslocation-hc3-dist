# Apple Find My and iOS Geofencing for Fibaro HC3

This repository contains the sanitized Danish and UK English distribution
packages for **iCloud Location**. Development sources remain in a separate
private repository.

## Install with QA Dist Manager

Import `QA_Dist_Manager_iCloud_Location.fqa` for a preconfigured QA Dist Manager
with an empty `githubToken`. Alternatively, install the official QA Dist Manager
and add this manifest URL to a QuickApp variable whose name starts with
`manifest`:

```text
https://raw.githubusercontent.com/dkcsn/fibioslocation-hc3-dist/main/dist.json
```

Refresh QA Dist Manager, select **iCloud Location (Dansk)** or
**iCloud Location (English)**,
select **Create new instance**, choose the release, and press **Apply**.

Version 1.2.0 can emit native Fibaro `enter`/`leave` geofence events for Scenes
and EventRunner. Set `geofenceUserId` to the numeric HC3 user ID to enable
events. Each geofence child also exposes distance, GPS accuracy, and the latest
position timestamp. Events are disabled by default in the public packages.

No GitHub token is required for this public distribution repository.

The packages contain no Apple credentials, session information, controller
identifiers, local network addresses, or GitHub tokens. The QuickApps are not
encrypted or obfuscated; all Lua files can be inspected in the HC3 editor.

## Acknowledgements

Many thanks to **@jgab** for PLua, QA Dist Manager, and all the other excellent
tools, code, knowledge, and support he has generously shared with the Fibaro
community. His work and help were invaluable throughout development, testing,
packaging, and distribution.

Many thanks to **@Tinman** for the Lua implementation of SHA-2 used by the Apple
SRP sign-in process.

And for anyone who enjoys looking beneath the surface: see if you can find the
small hidden Star Wars tribute in the QuickApp's attributes. ;)
