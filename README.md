# VIRTUAL-PLM
## A visual, interactive tool for understanding optical mineralogy

VIRTUAL-PLM is a lightweight HTML tool designed to help you understand how visible interference colors relate to retardation, mineral thickness, birefringence, and indicatrix orientation.

The idea for this project came from my experience teaching Optical Mineralogy to undergraduate students, many of whom struggled with concepts such as the indicatrix and birefringence. This tool aims to make these topics more intuitive through an interactive, visual environment.
The entire application runs as a single, self-contained webpage.
You can download it and open it in any modern browser - on a computer, tablet, or even a phone (although I strongly recommend using a larger screen).

<!-- Image: [Overview of the Workspace Layout] -->

---

## 0. Installation and launch
Online:  
[LINK](https://yakovyermakov.github.io/VIRTUAL-PLM/)  
  
Offline:
1. [Download](https://github.com/YakovYermakov/VIRTUAL-PLM/blob/main/indicatrix_v1.0.html) .html file from repository for offline use.
2. Open in any browser.
3. Enjoy!
4. May not open properly on iPad, so it is recommended to use a laptop.

---

## 1. Mineral Parameters

<!-- Image: [Mineral Parameters Window] -->

Here you can customize the mineral optical properties or choose from built-in uniaxial minerals:
- Zircon
- Quartz
- Calcite
- Tourmaline
- Apatite
- Nepheline
- Custom

Each preset provides refractive indices and realistic mineral appearances in the microscope view (relief, PPL colors, and pleochroism).
- **Refractive Index Sliders:** Smooth sliders for $n_\omega$ (Ordinary RI) and $n_\varepsilon$ (Extraordinary RI) ranging from 1.000 to 2.000 (step 0.001) with live numerical readouts and optic sign detection (Uniaxial (+), Uniaxial (−), or Isotropic).
- **Thickness Slider:** Adjust sample thickness from 5 to 50 µm with quick presets for 20 µm, 30 µm (Standard thin section), and 50 µm.

---

## 2. Indicatrix

<!-- Image: [Indicatrix View] -->

The 3D Indicatrix window displays the 3D indicatrix generated from the mineral’s refractive indices.
Currently, the tool supports isotropic and uniaxial indicatrices (biaxial support will be added in upcoming updates). 
This view also displays:
- the ordinary ($n_\omega$) and apparent extraordinary ($n_\varepsilon'$) vibration directions,
- the cutting plane representing the mineral’s orientation in thin section,
- the basal and principal reference sections,
- the optic axis ($c$-axis),
- an interactive collapsible **Legend** on the upper-left,
- a 2D preview of the current cut, shown in the small circular window in the upper-right corner.

The 2D preview updates dynamically as you modify the cut angle or rotate the mineral stage.
Below the 3D scene, you can adjust the **Indicatrix Cut Angle** (from 0° to 90° with quick presets for Basal 0°, 45° Cut, and Principal 90°), zoom the setup with the slider, or click **Reset View** to return to the default 3D camera angle.

---

## 3. Michel-Lévy Chart

<!-- Image: [Michel-Lévy Chart Window] -->

The Michel-Lévy Chart window features an interactive interference color chart calculated following Sørensen (2012).
Key features include:
- A dynamic cursor (red dot and reference crosslines) showing the exact retardation and birefringence coordinates for the current mineral state.
- Dynamic responsive axis scaling (retardation from 0 to 1800 nm, thickness from 0 to 50 µm).
- In-chart legend indicating the current state, birefringence line, and accessory plate shift.
- A live metrics panel below the chart displaying:
  - Color swatch and interference order name (e.g., *Light yellow 1st order*)
  - Apparent Birefringence ($\delta'$)
  - Retardation ($\Gamma$)
  - Maximum Birefringence ($|n_\varepsilon - n_\omega|$)

This module helps visualize how birefringence and thickness combine to produce observable colors.

---

## 4. Microscope Simulation (PPL & XPL)

<!-- Image: [Microscope View] -->

The Microscope View simulates the appearance of a mineral grain under polarized light microscopy:
- **PPL & XPL Modes:** A toggle button switches seamlessly between Plane-Polarized Light (PPL) and Cross-Polarized Light (XPL).
- **Virtual Stage Rotation:** Smooth rotation slider (0° to 360°) as well as direct interactive click-and-drag rotation on the microscope canvas.
- **Pleochroism & PPL Color:** Mineral grain color dynamically reflects pleochroic absorption during stage rotation.
- **Relief:** Grain boundary relief adjusts according to the refractive index contrast with the mounting medium.
- **Grain Geometry & Extinction:** Realistic crystallographic grain shapes with parallel extinction for uniaxial minerals.
- **Boundary Taper:** Thickness tapers near the grain boundary to reproduce realistic edge interference fringes.
- **Accessory Plate (Gypsum 540 nm):** Toggle button inserts a first-order red accessory plate with an animated visual indicator to observe interference color addition (enhancement) and subtraction (compensation).
- **Zoom to Grain Boundary:** Toggle switch to inspect grain boundary color transitions in high magnification.

---

## 5. Theory & Lab Notes

<!-- Image: [Optics Theory & Lab Notes Windows] -->

VIRTUAL-PLM includes built-in learning and observation tools accessible from the sidebar:
- **Optics Theory:** A dedicated reference panel detailing key equations:
  - Apparent birefringence: $\delta' = |n_\varepsilon' - n_\omega|$
  - Retardation: $\Gamma = d \times \delta' \times 1000$
  - Fast vs. Slow rays (velocity vs. refractive index)
  - Accessory plate rules for interference color shift
  - Variable color coding directly mapped to the 3D indicatrix rays and Michel-Lévy metrics.
- **Lab Notes:** A digital laboratory notebook allowing you to record observations. Click **Log Current Reading** to instantly append all current mineral parameters, rotation angle, and retardation values. Notes are automatically saved in local browser storage.
- **Window Management:** Movable, resizable, and minimizable windows with **Tile Windows** and **Reset Workspace** buttons to optimize screen layout.

---

## 6. References
Bjørn Eske Sørensen; A revised Michel-Lévy interference colour chart based on first-principles calculations. European Journal of Mineralogy 2012;; 25 (1): 5–10. doi: https://doi.org/10.1127/0935-1221/2013/0025-2252

---

## 7. Behind the Scenes
The initial structure of this tool was prompt-engineered with the assistance of several large language models, but the optical mineralogy theoretical base was thoughtfully revised and validated to make sure it behaves exactly as it should and simulate real-life world of optical mineralogy!
