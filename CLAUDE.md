# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a single-file HTML application that creates triangle mesh (low-poly) art effects from images using Delaunay triangulation. The entire application is contained in `index.html` with embedded CSS and JavaScript.

## Architecture

### Key Components

1. **Delaunay Triangulation Implementation** (index.html:266-425)
   - Custom JavaScript implementation of Bowyer-Watson algorithm
   - Creates optimal triangle meshes from point sets
   - Handles edge cases and supertrangle removal

2. **Edge Detection** (index.html:702-734)
   - Simplified Sobel filter implementation
   - Detects image edges to place vertices at important features
   - Used to preserve detail in the triangulated output

3. **Point Generation Strategy** (index.html:647-700)
   - Fixed corner points for full coverage
   - Edge-based points for detail preservation
   - Random points for overall distribution

4. **SVG Export** (index.html:462-499)
   - Generates scalable vector graphics from triangle mesh
   - Preserves vector format for infinite scaling

## Development Commands

Since this is a standalone HTML file, no build process is required:

- **Run locally**: Simply open `index.html` in a web browser
- **Deploy**: Upload the single HTML file to any web server
- **Test**: Open in browser and use the demo image that auto-loads

## Key Algorithms

- **Delaunay Triangulation**: Ensures optimal triangle shapes (avoiding skinny triangles)
- **Edge Detection**: Uses Sobel filter to identify important image features
- **Color Averaging**: Samples pixels within each triangle to determine fill color

## User Interface Features

- Image upload support
- Adjustable triangle count (10-3000)
- Edge detection sensitivity control
- SVG export functionality
- Side-by-side comparison view
- Automatic demo image generation on load

## Language

The interface and documentation within the HTML file are in Japanese. Key UI elements:
- "画像を選択" - Select image
- "三角形の数" - Number of triangles  
- "エッジ検出感度" - Edge detection sensitivity
- "変換実行" - Execute transformation
- "SVGダウンロード" - Download SVG