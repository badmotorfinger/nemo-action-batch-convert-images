# Nemo Batch Convert Images

A Nemo file manager action extension that provides batch image conversion functionality directly from the context menu.

## Features

- **Batch conversion** of multiple image files to various formats
- **PDF support** - Convert PDF pages to images
- **Animated GIF creation** from multiple images
- **Progress tracking** with visual progress bar
- **Multi-language support** with internationalization
- **Format validation** to skip unsupported files

## Supported Formats

### Input Formats
- All common image formats (JPEG, PNG, GIF, BMP, TIFF, WebP, HEIC, AVIF, etc.)
- PDF documents
- SVG vector graphics
- PSD files (first layer only)

### Output Formats
- APNG, AVIF, BMP, GIF, HEIC, HEIF, ICO, JPEG, JP2, PDF, PNG, SVG, TIFF, WebP

## Installation

1. Copy the `batch-convert-images@badmotorfinger.nemo_action` file to:
   - `~/.local/share/nemo/actions/` (user-specific)
   - `/usr/share/nemo/actions/` (system-wide)

2. Copy the `batch-convert-images/` directory to the same location

3. Restart Nemo file manager

## Dependencies

The following packages must be installed:
- `zenity` - GUI dialogs
- `imagemagick` (provides `convert` command)
- `file` - File type detection
- `poppler-utils` (provides `pdftoppm` and `pdfinfo`)
- `librsvg2-bin` (provides `rsvg-convert` for SVG)

Install on Ubuntu/Debian:
```bash
sudo apt install zenity imagemagick file poppler-utils librsvg2-bin
```

## Usage

1. Select one or more image files or PDFs in Nemo
2. Right-click and choose "Batch convert images to another format"
3. Select the desired output format from the dialog
4. Conversion starts automatically with progress tracking

### Special Features

- **PDF to Images**: Converts each PDF page to a separate image file in a new directory
- **Animated GIF**: When converting multiple images to GIF format, creates a single animated GIF
- **PSD Support**: Extracts the first layer from Photoshop files
- **SVG Handling**: Uses proper SVG converter for vector graphics

## File Structure

```
batch-convert-images@badmotorfinger.nemo_action  # Nemo action definition
batch-convert-images/
├── batch-convert-images.sh                     # Main conversion script
├── icon.png                                    # Action icon
└── metadata.json                              # Extension metadata
```

## Localization

The extension supports multiple languages including:
- English, Spanish, French, Italian, German
- Portuguese, Dutch, Finnish, Hungarian
- Czech, Ukrainian, Catalan, Basque

## Author

Created by **badmotorfinger**

## Version

1.0.0