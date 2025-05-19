# 🎬 Open Source Media Player

A modern, lightweight, and highly customizable HTML5 media player built with no external dependencies. Ideal for embedding video/audio playback with advanced features in any web application.

## 🚀 Features

- ✅ **Video & Audio Support**: Native HTML5 `<video>` and `<audio>` support (optimized for video).
- 📝 **Subtitles Support**: Load `.vtt` subtitles via `data-subtitle-src`.
- ⚙️ **Modular Design**: Enable/disable features with a simple config.
- 📜 **Context Menu**: Custom right-click context menu.
- 📺 **Picture-in-Picture (PiP)**: Built-in PiP support.
- 🖥️ **Fullscreen Toggle**: Fullscreen support for immersive playback.
- 🎞️ **Cinematic Mode**: Dims background elements to reduce distraction.
- 🎛️ **Settings Panel**: UI for toggling player options (e.g. subtitles, cinematic mode).
- ➕ **Addon Support**: Plug and play additional JavaScript modules.
- 🖼️ **SVG / Unicode Icons**: Easily switch or customize icons.
- 📱 **Vertical video fill**: Fills vertical videos with blured video background.
- 🖱️ **Mouse events**: Hides ui when playing
- 📟 **Plug**: Shows a custom message before a video plays with manual or timed close window.
- ⌛**Preload**: Preloads resources like Svg icons from `preload.js`

## 📸 Preview
![show](https://github.com/user-attachments/assets/04ec3ab0-eb2b-401a-924e-209732c358ea)


## 🛠️ Quick Start

### 1. Include the CSS

```html
<link rel="stylesheet" href="css/OpenSourcePlayer.css">
```

### 2. Add the HTML Structure

```html
<div class="osp-player">
  <video data-subtitle-src="subtitles.vtt">
    <source src="video.mp4" type="video/mp4">
  </video>
</div>
```

### 3. Initialize the Player in JS

```javascript
import { initializePlayer } from './js/modules/OpenSourcePlayer.js';

document.addEventListener('DOMContentLoaded', () => {
  initializePlayer();
});
```

## 📚 Documentation

### Configuration

Customize the player by modifying addons in `js/modules/OpenSourcePlayer.js`:

```javascript
const config = {
  usePreload: true,           // Preloads Svg icons
  mouseEvent: true,           // Show/hide UI on mouse move
  useSvgIcons: true,          // Use SVG instead of Unicode
  useMediaSource: false,      // Enable MediaSource streaming
  useSubtitles: true,         // Load VTT subtitles
  useSettings: true,          // Show settings UI menu
  useContextMenu: true,       // Enable right-click menu
  useVerticalVidFill: true,   // Adds vertical video background
  useCinematicMode: true,     // Dim background
  useFastForward: true,       // Skip 10s forward in video
  debugger: false             // Toggle console logs
};
```

### Adding Subtitles

To add subtitles, include the `data-subtitle-src` attribute in the video tag:

```html
<video data-subtitle-src="path/to/subtitles.vtt">
```

### Changing icons

Set each icons in `controls.js -> svgIcons` from a singe icons.svg file.

Currently using **Streamline Remix** icons. Supports both inline SVG and fallback Unicode.

### Plug message

To enable a plug message, include the `data-plugId` attribute in the video tag and set it to the corresponding id from `videoPlug.js`. You can change the content, duration and auto-close in `videoPlug.js` for each id.

## 🤝 Contributing

Contributions are welcome just submit a pull request or donate a coffee.

<a href='https://ko-fi.com/X8X11DTGJQ' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://storage.ko-fi.com/cdn/kofi6.png?v=6' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>

## 📄 License

This project is licensed under the GNU General Public License - see the [LICENSE](LICENSE) file for details.

---
This all started because i just wanted to style the default play/pause icons..

Happy coding! 🎉
