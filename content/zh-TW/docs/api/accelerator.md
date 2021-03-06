# 快速鍵

> 定義鍵盤快速鍵。

Accelerators are Strings that can contain multiple modifiers and key codes, combined by the `+` character, and are used to define keyboard shortcuts throughout your application.

範例:

* `CommandOrControl+A`
* `CommandOrControl+Shift+Z`

Shortcuts are registered with the [`globalShortcut`](global-shortcut.md) module using the [`register`](global-shortcut.md#globalshortcutregisteraccelerator-callback) method, i.e.

```javascript
const {app, globalShortcut} = require('electron')

app.on('ready', () => {
  // Register a 'CommandOrControl+Y' shortcut listener.
  globalShortcut.register('CommandOrControl+Y', () => {
    // Do stuff when Y and either Command/Control is pressed.
  })
})
```

## Platform notice

On Linux and Windows, the `Command` key does not have any effect so use `CommandOrControl` which represents `Command` on macOS and `Control` on Linux and Windows to define some accelerators.

Use `Alt` instead of `Option`. The `Option` key only exists on macOS, whereas the `Alt` key is available on all platforms.

The `Super` key is mapped to the `Windows` key on Windows and Linux and `Cmd` on macOS.

## Available modifiers

* `Command` (or `Cmd` for short)
* `Control` (or `Ctrl` for short)
* `CommandOrControl` (or `CmdOrCtrl` for short)
* `Alt`
* `Option`
* `AltGr`
* `Shift`
* `Super`

## 能用的按鍵碼

* `` 到 `9`
* `A` 到 `Z`
* `F1` 到 `F24`
* `~`, `!`, `@`, `#`, `$` 等半型標點符號。
* `<code>Plus` (加號)</code>
* `<code>Space` (空白鍵)</code>
* `Tab`
* `<code>Backspace` (倒退)</code>
* `Delete (刪除)`
* `Insert (插入)`
* `Return` (也可寫成 `Enter`)
* `Up` (上), `Down` (下), `Left` (左) 及 `Right` (右)
* `Home` 及 `End`
* `PageUp` 及 `PageDown`
* `Escape` (或縮寫成 `Esc`)
* `VolumeUp`, `VolumeDown` 及 `VolumeMute`
* `MediaNextTrack`, `MediaPreviousTrack`, `MediaStop` 及 `MediaPlayPause`
* `PrintScreen`