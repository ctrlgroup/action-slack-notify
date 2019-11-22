This is a fork of [action-slack-notify](https://github.com/rtCamp/action-slack-notify) with adaptations to support our desired release notifications.

Here is an example use from the blackwell-android application.
```
  - name: Slack Notification
    uses: ctrlgroup/action-slack-notify@master
    env:
      SLACK_CHANNEL: releases
      SLACK_ICON: https://img.icons8.com/material/48/000000/android-os--v1.png
      SLACK_PRETEXT: New Android Fora Health Release
      SLACK_FOOTER: With love from the Android team
      SLACK_TITLE: ${{ steps.version-name.outputs.version_name_readable }}
      SLACK_USERNAME: Android Deployer
      CHANGELOG_URL: https://github.com/ctrlgroup/blackwell-android/blob/master/CHANGELOG.md
      RELEASES_URL: https://github.com/ctrlgroup/blackwell-android/releases
      VARIANTS: staging, release
      SLACK_WEBHOOK: ${{ secrets.SLACK_WEBHOOK }}
```

See the original repo for further documentation.
