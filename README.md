# Automator Workflows
Random OSX automator testbed. Home of PoC and unfinished, broken code fragments.

## Output Volume "as a Service"
Volume function keys in OSX are setting volume in steps >=5. Volume Up / Volume down + modifier keys (Shift+Alt) use a lower stepping. There is no easy way for the enduser to customize this key sequence (Shift+Alt+VolUp/Down). I tried hdiutil, but it seems to be limited to "switch Key A with Key B" and unable to "switch Key A with a sequence of keys".

I was looking something that can be configured in the keyboard shortcut preferences pane of OSX. Besides that, it should be as simple as possible. No additional software should be needed to install to get this up and running, let alone "compile" stuff.

**outputVolumeIncreaseBy2** and **outputVolumeDecreaseBy2** is just a PoC. It's a four-line Applescript wrapped in a Workflow to make it available in prefs pane. If you need something that has all the bells and whistles, try one of gazillion keyboard-shortcut-modifier-keypress-listening apps.

### Install
Download zip and place **outputVolumeIncreaseBy2** and **outputVolumeDecreaseBy2** in
```
~/Library/Services
```

### Configure
Open _Preferences -> Keyboard -> Shortcuts_ and select _Services_ in the left pane. Scroll down until you spot **outputVolumeIncreaseBy2** and **outputVolumeDecreaseBy2** and define your shortcuts.

![prefs_pane](https://user-images.githubusercontent.com/47872623/153690401-c4d1fdcd-58cb-40c2-880e-c283df31bdaa.png)

Some keys didn't work for me. Function keys didn't work without a modifier at all. So I ended up with cmd+F18 and cmd+F19 in my PoC.
