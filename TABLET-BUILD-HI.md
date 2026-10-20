# StaySathi APK build from an Android tablet

This project is a prototype WebView wrapper. It does not add real hotel inventory, login, payments, or a booking backend.

## Tablet-only build using GitHub Actions
1. Download and extract this ZIP on your tablet.
2. Open https://github.com/new in your browser and create a repository named `staysathi-android` (Public is easiest for the first test). Do not initialize with README/license/gitignore.
3. Open the new repository, choose **Add file → Upload files**. Upload the *contents* of this extracted folder, including `.github/workflows/build-apk.yml`, `app/`, `build.gradle.kts`, `settings.gradle.kts`, and `gradle.properties`. If `.github` is hidden in the file picker, upload the other files first, then use **Add file → Create new file** and create `.github/workflows/build-apk.yml` with the workflow contents from this ZIP.
4. Commit the files to `main`.
5. Open the repository's **Actions** tab. Select **Build StaySathi APK**. If prompted, enable workflows. Tap **Run workflow → Run workflow**.
6. Wait until the run shows a green check. Open that run, scroll to **Artifacts**, and download `StaySathi-debug-apk`.
7. Extract the downloaded artifact ZIP. It contains `app-debug.apk`. Tap it to install; Android may ask you to allow installs from that browser/files app.

If the build fails, open the failed run and copy the first red error section. Do not paste any passwords, tokens, or secret keys.

Note: This workflow builds in GitHub's cloud, so Java does not need to run in Acode Terminal. A debug APK is for testing, not Play Store release.
