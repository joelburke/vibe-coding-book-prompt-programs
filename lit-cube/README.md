# Lit Cube

A 3D cube lit by a colored point light, with sliders to change the cube's orientation and the light's color, position and brightness. One HTML file using plain WebGL, with no libraries.

## Prompt

> Write a JavaScript program that shows a cube with a colored light source. Create slider parts that can change the orientation of the polygon.

## Features

- **Cube orientation:** three sliders set Pitch (X), Yaw (Y) and Roll (Z) rotation from −180° to 180°. You can also drag on the cube to turn it, and the sliders follow. A reset button restores the starting angle.
- **Light color:** a color picker plus six preset swatches.
- **Light position:** an Orbit slider moves the light around the cube; a Height slider moves it up or down. A small glowing marker shows where the light is.
- **Intensity:** a slider from 0 to 2.
- **Shading:** Blinn-Phong lighting (ambient + diffuse + specular highlight) with gamma correction. Faces turned away from the light stay dim.

## How it works

- **Shaders:** a vertex shader transforms each vertex into world and screen space; a fragment shader computes per-pixel Blinn-Phong lighting from the light position, light color and camera position.
- **Geometry:** the cube is 6 faces × 4 vertices, each face with its own normal, so faces shade flat. The light marker reuses the same mesh at 8% size, drawn unlit in the light's color.
- **Math:** a minimal column-major 4×4 matrix helper (multiply, rotate X/Y/Z, translate, perspective), with no math library.
- **Rendering:** draws only on demand (when a control changes or the window resizes), batched through `requestAnimationFrame`, and scales the canvas for high-DPI screens.

## Run it

Open `index.html` in any WebGL-capable browser. It works offline.
