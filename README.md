# VIRTUAL-PLM
## A visual, interactive tool for understanding optical mineralogy

VIRTUAL-PLM is a lightweight HTML tool designed to help you understand how visible interference colors relate to retardation, mineral thickness, birefringence, and indicatrix orientation.

The idea for this project came from my experience teaching Optical Mineralogy to undergraduate students, many of whom struggled with concepts such as the indicatrix and birefringence. This tool aims to make these topics more intuitive through an interactive, visual environment.
The entire application runs as a single, self-contained webpage.
You can download it and open it in any modern browser - on a computer, tablet, or even a phone (although I strongly recommend using a larger screen).

---

## 1. Indicatrix

<img width="931" height="459" alt="image" src="https://github.com/user-attachments/assets/65fcc31f-5bf6-4dc9-9507-78289965f490" />

The first section of the tool shows the 3D indicatrix generated from the mineral’s refractive indices.
Currently, the tool supports isotropic and uniaxial indicatrices (biaxial support may be added later). 
This view also displays:
- the ordinary and apparent extraordinary vibration directions,
- the cutting plane representing the mineral’s orientation in thin section,
- the basal and principal reference sections,
- the optic axis,
- a 2D preview of the current cut, shown in the small window in the upper-right corner.

The 2D preview updates dynamically as you modify the cut angle or rotate the microscope stage.
For convenience, you can zoom the entire 3D setup using the slider below the 3D view.

---

## 2. Michel-Lévy Chart

<img width="938" height="453" alt="image" src="https://github.com/user-attachments/assets/1a37bb5a-f423-4ea3-9815-1d61f30d8426" />

The bottom-left section contains an interactive Michel-Lévy interference color chart, calculated following Sørensen ( 2012).
This chart has a red marker that dynamically shows you the current interference color visible in the mineral.
This module helps visualize how birefringence and thickness combine to produce observable colors.

---

## 3. Mineral Parameters

<img width="927" height="126" alt="image" src="https://github.com/user-attachments/assets/58c90570-fec1-4be5-a8d1-8e45bc2114af" />

Here you can choose from several built-in uniaxial minerals:
- Quartz
- Calcite
- Tourmaline
- Zircon
- Beryl

Each preset provides refractive indices and different mineral appearances in the microscope view (relief, PPL colors, and pleochroism).
For demonstration purposes, you can also manually customize nω and nε values.
<img width="927" height="122" alt="image" src="https://github.com/user-attachments/assets/f026c8c3-d959-4b83-8b3a-9b42d401f795" />

In this section, you can also change the indicatrix cut angle and thickness. These two sliders are the most important controls in this tool, and will and will help demonstrate what kind of interference colors you can see in the mineral you choose. 

---

## 4. Microscope Simulation (PPL & XPL)
Two visualization panels simulate the appearance of a mineral grain under Plane- and Cross-Polarized Light. 
The crosshairs here represent the allowed light vibration directions in the polarizer and analyzer.
<img width="925" height="234" alt="image" src="https://github.com/user-attachments/assets/5bba03b8-2945-4321-9953-08db8a270600" />

For better experience, I aimed to make it close to realistic observations in a polarized microscope: 
- PPL color (if the mineral has it) can change with stage rotation (pleochroism)
- Relief varies with the difference between the mineral RI and mounting medium
- Grain shape changes based on the crystal system and cut angle
- Interference colors are computed from current retardation value
- Minerals have extinction (parallel for uniaxial minerals in this tool)
- Minerals have lower thickness close to the grain boundary to approximate real interference color behavior
- An accessory plate (540 nm) insertion button that can show you enhancement or compensation effects on interference colors
<img width="456" height="201" alt="image" src="https://github.com/user-attachments/assets/f69749c2-1a94-4182-9c1d-7586c2926548" />

The slider below allows you to rotate the virtual stage.
<img width="925" height="48" alt="image" src="https://github.com/user-attachments/assets/3a629784-b6cf-4557-a242-554c0c1e2733" />

---

## 5. Calculated Data

<img width="927" height="187" alt="image" src="https://github.com/user-attachments/assets/e8b9c2fb-f098-418f-afb0-b570df76296d" />

The last panel displays real-time computed parameters:
- Apparent birefringence (δ′ for your cut)
- Maximum birefringence (|nε − nω|)
- Retardation (Γ (nm) = thickness × birefringence × 1000)

These values update instantly whenever you change thickness, cut angle, or refractive indices.
This panel also has equations that you need to explain the numbers you get. 

---

## 6. References
Bjørn Eske Sørensen; A revised Michel-Lévy interference colour chart based on first-principles calculations. European Journal of Mineralogy 2012;; 25 (1): 5–10. doi: https://doi.org/10.1127/0935-1221/2013/0025-2252

---

## 7. Behind the Scenes
The initial structure of this tool was prompt-engineered with the assistance of several large language models, but the optical mineralogy theoretical base was manually revised and validated to make sure it behaves exactly as it should.
