App Update Process Explained in Detail

1. Current App Version
- The application has a built-in APP_VERSION (e.g., 1.0.0).
- This version is hardcoded in the app and represents what the user currently has installed.

2. version.txt File
- This is a remote file (usually hosted on a server or CDN).
- It contains the latest available version number (e.g., 1.0.1).
- When the app runs, it reads this file and compares it to APP_VERSION.
  - If version.txt > APP_VERSION → app triggers update prompt.
  - If version.txt == APP_VERSION → app does not update.

3. UPDATE_EXE_URL
- This is the URL pointing to a ZIP archive that contains the new app version.
- The ZIP file must contain the next version as defined in version.txt.
Example:
- If APP_VERSION is 1.0.0:
  - version.txt must say 1.0.1
  - UPDATE_EXE_URL should link to a ZIP file that contains 1.0.1

4. Contents of the ZIP File
- The ZIP should include the executable and supporting files for version 1.0.1.
- After downloading and extracting, the new app version replaces the old one.
- Once launched, the app now runs APP_VERSION = 1.0.1.

5. Next Update Cycle
- After the user is on version 1.0.1, the cycle repeats:
  - Update version.txt to 1.0.2
  - Upload a new ZIP to UPDATE_EXE_URL containing 1.0.2
- This ensures users on 1.0.1 will be prompted to upgrade to 1.0.2 next time.

Example Timeline:
App State    APP_VERSION    version.txt    ZIP Content (UPDATE_EXE_URL)
Initial      1.0.0          1.0.1          Version 1.0.1 files
After update 1.0.1          1.0.2          Version 1.0.2 files
Next         1.0.2          1.0.3          Version 1.0.3 files

Key Rules:
- version.txt must always show a version higher than the current APP_VERSION.
- UPDATE_EXE_URL must point to a ZIP file matching the version in version.txt.
- The app checks for updates only if version.txt > APP_VERSION.
