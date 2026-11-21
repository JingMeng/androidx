# CardView AAR validation on Windows

This entry compiles the existing checkout's complete CardView production Java and resources with Gradle8.5, AGP8.2.1, SDK34 and Java11. Original AndroidXConfig minSdk19 and original module dependencies are retained. No placeholder library or copied binary is used.

From the AndroidX checkout root: `gradlew.bat -p apk-aar-validation assembleRelease --no-daemon --max-workers=1`.

The original AOSP root build needs external tools/prebuilts absent from this checkout. This entry deliberately has its own settings and does not load the AOSP buildSrc. Only CardView is validated; it does not establish that the whole AndroidX source tree is upgraded or buildable. No test tasks are run.
