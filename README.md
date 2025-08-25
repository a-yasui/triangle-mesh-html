# 🎨 Triangle Mesh Image Transformer

A web-based image transformation tool that creates artistic low-poly triangle mesh effects using Delaunay triangulation.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

## ✨ Features

- **Real-time Image Processing**: Transform images into triangle mesh art instantly
- **Adjustable Parameters**: 
  - Control the number of triangles (10-3000)
  - Adjust edge detection sensitivity for detail preservation
- **Smart Vertex Placement**: Automatically places more triangles at image edges and details
- **SVG Export**: Download results as scalable vector graphics
- **No Dependencies**: Pure HTML/CSS/JavaScript implementation
- **Responsive Design**: Works on desktop and mobile devices

## 🚀 Quick Start

### Online Demo
Simply open `index.html` in any modern web browser. The application will automatically load with a demo image.

### Local Development
```bash
# Clone the repository
git clone https://github.com/yourusername/triangle-mesh-html.git

# Navigate to the project
cd triangle-mesh-html

# Open in browser (macOS)
open index.html

# Or use a local server
python -m http.server 8000
# Then visit http://localhost:8000
```

## 🎯 How to Use

1. **Load an Image**: Click "📷 画像を選択" to upload your image, or use the auto-loaded demo
2. **Adjust Settings**:
   - **三角形の数 (Triangle Count)**: More triangles = more detail
   - **エッジ検出感度 (Edge Sensitivity)**: Higher values preserve more details at edges
3. **Process**: Click "変換実行" to generate the triangle mesh
4. **Export**: Click "SVGダウンロード" to save as SVG

## 🔧 Algorithm Details

### Delaunay Triangulation
The core algorithm uses Bowyer-Watson implementation to create optimal triangle meshes:
- Ensures no skinny triangles
- Maximizes minimum angles
- Creates aesthetically pleasing results

### Vertex Placement Strategy
1. **Fixed Vertices**: Four corners for complete coverage
2. **Edge-Based Vertices**: Placed at detected edges using Sobel filter
3. **Random Vertices**: Fill remaining space uniformly

### Color Approximation
Each triangle is filled with the average color of pixels within its boundaries, creating the characteristic low-poly aesthetic.

## 📊 Performance

- Processes images up to 500x500px in real-time
- Supports up to 3000 triangles
- SVG export maintains vector quality at any scale

## 🎨 Example Use Cases

- **Artistic Effects**: Create unique low-poly art from photos
- **Design Assets**: Generate geometric backgrounds and patterns
- **Image Compression**: Represent images with fewer primitives
- **Educational**: Demonstrate computational geometry concepts

## 🛠️ Technical Details

- **Language**: Pure JavaScript (ES6+)
- **Rendering**: HTML5 Canvas API
- **Export Format**: SVG (Scalable Vector Graphics)
- **Browser Support**: Chrome, Firefox, Safari, Edge (modern versions)

## 📝 License

This project is open source and available under the MIT License.

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests

## 🙏 Acknowledgments

- Delaunay triangulation algorithm by Boris Delaunay
- Bowyer-Watson algorithm implementation
- Sobel edge detection filter

## 📧 Contact

For questions or suggestions, please open an issue on GitHub.

---

Made with ❤️ using vanilla JavaScript