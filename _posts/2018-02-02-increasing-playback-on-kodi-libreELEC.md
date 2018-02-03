---
title: Increasing Playback Speed on Kodi LibreELEC on Raspberry Pi
layout: post
date: 2018-02-02
tags: kodi raspberry-pi
---

Increasing the playback speed of a video has never been easier with Kodi on your Raspberry Pi.  To enable this, we must do two things. First, we need to enable playback syncing.

This can be done by enabling the setting under:

General Settings > Player > Videos > Sync playback to display

Then we have to upload our new `keymap.xml` to `/storage/.kodi/userdata/keymaps/`. We can do this however works for you (I find using SSH or SFTP is easiest)

Create the `keyboard.xml` file with the following content:

```
<?xml version="1.0" encoding="UTF-8"?>
<keymap>
  <FullscreenVideo>
    <keyboard>
      <opensquarebracket>PlayerControl(TempoDown)</opensquarebracket>
      <closesquarebracket>PlayerControl(TempoUp)</closesquarebracket>
    </keyboard>
  </FullscreenVideo>
  <VideoMenu>
    <keyboard>
      <opensquarebracket>PlayerControl(TempoDown)</opensquarebracket>
      <closesquarebracket>PlayerControl(TempoUp)</closesquarebracket>
    </keyboard>
  </VideoMenu>
</keymap>
```

Now just restart your Pi and you should be able to use the `[` key on your keybaord to decrease the playback speed, and `]` to increase the playback speed!

