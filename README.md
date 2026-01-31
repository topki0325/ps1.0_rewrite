# Photoshop 1.0 Rust Rewrite

This project is a clean-room reimplementation/rewrite of the original Photoshop 1.0 logic using Rust and the `egui` GUI library. It aims to recreate the visual style of Classic Mac OS (System 6/7) while running natively on modern Windows systems.

**Note:** This is an educational project exploring the architecture of early graphics software.

## ✨ Features

### 🖥️ UI & Experience
- **Classic Mac OS Aesthetic**: Custom-painted widgets mimicking the look and feel of System 6/7 (Chicago font style, beveled buttons, 1-bit icons).
- **Modern Backend**: Built with `egui` on top of OpenGL.
- **Responsive Canvas**: Zoomable and scrollable workspace with classic scrollbar styling.

### 📂 File Support
- **Legacy Formats**: 
  - Targa (`.tga`)
  - IFF/ILBM (`.iff`, `.lbm`)
  - MacPaint (`.mac`, `.pntg`)
- **Modern Formats** (via `image` crate):
  - PNG, JPEG, BMP, TIFF, WebP, ICO
- **Color Modes**:
  - RGB (True Color 24-bit)
  - Grayscale (8-bit)
  - Automatic format conversion on import.

### 🛠️ implemented Tools
| Tool | Status | Description |
|------|--------|-------------|
| ✏ **Pencil** | ✅ | 1px hard-edge continuous drawing. |
| 🖌 **Brush** | ✅ | Basic round brush drawing. |
| 🩹 **Eraser** | ✅ | White hard-edge eraser. |
| 🪣 **Bucket** | ✅ | Flood fill algorithm (supports RGB/Gray). |
| 🔍 **Zoom** | ✅ | Click to zoom in, Alt+Click to zoom out. |
| ✋ **Hand** | 🚧 | Visual only (Use scrollbars). |
| □ / ◯ **Select** | 🚧 | Visual only. |
| ✂ **Crop** | 🚧 | Visual only. |
| T **Text** | 🚧 | Visual only. |
| 🧹 **Smudge/Blur**| 🚧 | Visual only. |

## 🚀 How to Run

1. **Download**: Get the latest release `exe`.
2. **Run**: Double click `ps1_rewrite.exe`.
3. **Open Image**: File -> Open (or Ctrl+O) to select an image file.

## 🛠️ Build from Source

Requirements: [Rust Toolchain](https://rustup.rs/) (1.75+)

```bash
# Clone the repository
git clone https://github.com/yourusername/ps1-rewrite.git

# Enter directory
cd ps1-rewrite

# Build release version
cargo build --release
```

The executable will be generated in `target/release/ps1_rewrite.exe`.

## 📝 Status & Roadmap

- [x] Basic Window Shell & Layout
- [x] Custom "Classic" Widget Painter
- [x] Image Loading Pipeline
- [x] Basic Pixel Manipulation (Set Pixel, Line, Flood Fill)
- [ ] Save Functionality
- [ ] Selection System (Marching Ants)
- [ ] Filters (Blur, Sharpen, Edge Detect)
- [ ] Image Adjustments (Levels, Brightness/Contrast)

## ⚖️ License

This code is a rewrite and does not contain original source code from the Computer History Museum release.
