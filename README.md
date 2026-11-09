# Lowpoly – Android app (play on the same Wi-Fi)

One phone taps **HOST GAME** (it runs the game server inside the app).
Everyone else taps **JOIN** and types the IP address the host sees (e.g. 192.168.1.23).
Works on a shared router Wi-Fi or on the host's phone hotspot. No PC, no internet needed.

## Build the APK
1. Install Android Studio, choose **Open** and select this folder.
2. Let Gradle sync (needs internet once).
3. **Build > Build APK(s)** -> app/build/outputs/apk/debug/app-debug.apk
4. Copy to each phone and install (allow "install unknown apps").

## Notes
- app/src/main/assets/index.html is your game, unchanged.
- RelayServer.kt is a Kotlin port of mp.php and also serves index.html on port 8080.
- If JOIN can't connect: same network? Router "client/AP isolation" off? Host still in game?
