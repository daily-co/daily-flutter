## 0.28.0

- Fixed various Android build issues seen with new versions of Gradle, Java, and AGP.
- Fixed a logging-related crash (stack overflow) that could occur when rapidly starting and stopping the SDK.
- Fixed an issue where missing fields in the domain/room permission config could cause a connection failure.
- Renamed `org.webrtc` package to `co.daily.webrtc` to avoid conflicts.
- Improved meeting move robustness by increasing the number of retries, to account for
  situations where the backend takes longer to complete the move.

## 0.22.0

### Added
- Added new metrics that will allow us to better understand the meeting quality.

### Fixed
- Preventing Flutter iOS from crashing when closing the app (via the user manually swiping away).
- Preventing Flutter Android from crashing when closing the app if the `surfaceTextureHelper` has not been properly initialized.
- Fixed an issue to show the correct state when the mic is muted remotely.
- Fixed an issue with meeting moves that could occur in an exceptional case where, for a short period of time, we didn't receive information about which worker server to connect to.

## 0.20.0

### Fixed
- Added support for Flutter 3.22 and Dart 3.4.
- Fixed multi-threading issue encountered when sending events.
- Resolved an issue where the videos sent had the wrong orientation when viewed on iOS mobile web.
- Fixed an issue where `joinedAt` value (participant info) could sometimes be zero.
- Fixed issue where `onParticipantUpdated()` didn't reflect the new state of the local participant's screen video 
  track, in cases where `leave()` was called while a screen share was active.
- Fixed an issue that could cause join to fail if recording/transcription/live
  stream was started from the REST API.
- Fixed an issue that would not allow join to succeed if a React Native client 
  was already in the room.

## 0.16.0-beta.1

Bringing the latest changes to daily-flutter, primarily focused on
fixing multiple issues that could cause deadlock during network reconnection,
enhancing performance, and reducing the bundle size for Android.

## 0.1.0-alpha.1

Initial alpha release.
