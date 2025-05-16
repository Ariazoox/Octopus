# Git Project Description - Octopus 3D Viewer

## Overview

This project is an **interactive 3D web viewer** for an octopus model created in Blender. It is a modern web application using Three.js and TypeScript to display and animate a GLTF 3D model in the browser.

## Project Goal

Create an interactive web viewer that allows visualization, exploration, and animation of a 3D octopus model with:
- Orbital navigation (rotation, zoom, pan)
- GLTF model loading and display
- Built-in animation support
- HDR environment for realistic lighting
- Responsive web interface

## Technical Stack

### Frontend
- **TypeScript** (v5.7.2) - Static typing for JavaScript
- **Three.js** (v0.175.0) - 3D library for the web
- **Vite** (v6.2.0) - Modern and fast build tool
- **HTML5 / CSS3** - Structure and styling

### Three.js Features
- **GLTFLoader** - Loading 3D models in GLTF format
- **RGBELoader** - Loading HDR environments
- **OrbitControls** - Interactive camera controls
- **AnimationMixer** - Model animation management

## Project Structure

```
Octopus/
├── public/
│   ├── models/gltf/PoulpeAnas/     # 3D octopus model (GLTF + textures)
│   │   ├── Anaspoulpev2.gltf       # Main model file
│   │   ├── Anaspoulpev2.bin        # Binary data
│   │   └── [textures].png          # Model textures
│   └── textures/
│       └── desert.hdr              # HDR environment for lighting
├── src/
│   ├── main.ts                     # Main entry point (3D scene)
│   ├── style.css                   # Application styles
│   └── counter.ts                  # (Unused - template file)
├── index.html                      # Main HTML page
├── package.json                    # Dependencies and npm scripts
└── tsconfig.json                   # TypeScript configuration
```

## Included 3D Model

The project includes an octopus model (`Anaspoulpev2.gltf`) with:
- Detailed octopus geometry
- PBR textures and materials
- Built-in animations (tentacles, movements)
- GLTF format optimized for the web

## Installation and Usage

### Prerequisites
- Node.js (modern version recommended)
- npm or yarn

### Installation
```bash
npm install
```

### Development
```bash
npm run dev
```
Starts the Vite development server (usually on http://localhost:5173)

### Production Build
```bash
npm run build
```
Generates optimized files in the `dist/` folder

### Preview Build
```bash
npm run preview
```
Previews the production build locally

## Implemented Features

1. **3D Model Loading**
   - Asynchronous GLTF model loading
   - Texture and material management
   - Automatic model scaling

2. **Environment and Lighting**
   - HDR background (desert.hdr) for realistic lighting
   - Environment mapping for reflections

3. **Interactive Controls**
   - Camera rotation with mouse
   - Zoom with mouse wheel
   - Pan with right-click (OrbitControls)

4. **Animations**
   - Automatic playback of built-in model animations
   - AnimationMixer for synchronization

5. **Performance**
   - Asynchronous model compilation to optimize rendering
   - Antialiasing enabled
   - ACES Filmic tone mapping for more realistic rendering

## Camera Configuration

- **Type**: PerspectiveCamera
- **FOV**: 45°
- **Clipping Planes**: 0.25 (near) to 20 (far)
- **Initial Position**: (-1.8, 0.6, 2.7)
- **Target**: (0, 0, -0.2)
- **Zoom Limits**: 2 (min) to 10 (max)

## Development Notes

- Project uses TypeScript in strict mode
- Vite configuration for fast development
- Model is scaled to 50% for better display
- Animations are updated at 50 FPS

## Possible Future Improvements

- User interface to control animations
- Loading multiple models
- Screenshot export
- Configurable lighting parameters
- Fullscreen mode
- Touch controls for mobile

## Credits

- 3D Model: Octopus created in Blender (PoulpeAnas/Anaspoulpev2)
- Technologies: Three.js, TypeScript, Vite
- Environment: Desert HDR texture

---

**Project Type**: 3D Web Application / Model Viewer  
**Domain**: Computer Graphics / WebGL / Three.js  
**Main Language**: TypeScript  
**3D Framework**: Three.js
