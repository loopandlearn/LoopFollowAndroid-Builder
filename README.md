# LoopFollow Android Builder

Build your own [LoopFollow for Android](https://github.com/loopandlearn/LoopFollowAndroid) in GitHub, in your own
private repository. Nothing to install, no terminal, works from an Android phone.

> **No fork needed.** You do not fork LoopFollowAndroid. The source code is downloaded from
> [loopandlearn/LoopFollowAndroid](https://github.com/loopandlearn/LoopFollowAndroid) at every build and signed with
> your own key.

## 👉 New here?

Follow the setup steps in the LoopFollow documentation:
**[LoopFollow for Android](https://loopfollowdocs.org/android/lf-android/)**.

Step 1 creates your own **private copy** of this repository (GitHub's "Use this template"). Do not fork it: a fork is
public, and everything a public repository builds can be downloaded by anyone.

## 🔧 Already have your own copy?

These links always open **this** repository, whatever you named it:

| | |
|---|---|
| 🔑 **[Add your key](../../settings/secrets/actions/new)** | Name: `KEYSTORE_SET` · Secret: the long code from the setup steps (step 3) |
| ▶️ **[Build LoopFollow](../../actions/workflows/build.yml)** | Run workflow → Run workflow |
| 📦 **[My builds](../../actions)** | Open a finished build → tap **📱 Download LoopFollow** |

> **On a phone, use the web browser (Chrome), not the GitHub app.** The app cannot download your builds.

**New LoopFollow version?** Press **Build LoopFollow** → **Run workflow** again. `latest` always builds the newest
release. Your repository never builds anything by itself.

**Following more than one person?** Choose `Second` or `Third` under **Which app**. Each is a separate app with its own
settings, next to the first one. Use the same key for all of them.

## How it works

`.github/workflows/build.yml` in your copy is short: it runs the build steps in
[`loopfollow-builder.yml`](.github/workflows/loopfollow-builder.yml) on the `release` branch of
loopandlearn/LoopFollowAndroid-Builder, so improvements reach you without any change to your repository. A build
downloads only the LoopFollow source and GitHub's own build tools, signs the app with the key in your `KEYSTORE_SET`
secret, and keeps the APK on the build page for 14 days.

`KEYSTORE_SET` is one base64 code holding `keystore (base64)|keystore password|alias|key password`. The setup steps
create it in your browser; nothing is sent anywhere except into the secret you paste it into.

Based on [AAPS Builder](https://github.com/nightscout/aaps-builder) (AGPL-3.0). LoopFollow is not a medical device and
is not a substitute for advice from your care team.
