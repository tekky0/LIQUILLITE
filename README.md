<!-- ~ header wave ~ -->
<img src="https://capsule-render.vercel.app/api?type=waving&height=240&color=0:7ee8d6,50:5fb8c9,100:f4d9c6&text=LIQUILLITE&fontColor=ffffff&fontSize=70&fontAlignY=36&desc=a%20little%20tide%20pool%20you%20can%20wear&descAlignY=56&descSize=18&animation=twinkling" width="100%" alt="LIQUILLITE" />

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=18&pause=1400&color=5FB8C9&center=true&vCenter=true&width=520&lines=tilt+it.+watch+it+slosh.;real-time+FLIP+fluid+on+an+STM32;liquid+light%2C+on+a+keyring+%F0%9F%90%9A" alt="tilt it. watch it slosh." />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/MCU-STM32L412-5fb8c9?style=for-the-badge&logo=stmicroelectronics&logoColor=white" alt="MCU STM32L412" />
  <img src="https://img.shields.io/badge/sensor-BMA400-7ee8d6?style=for-the-badge" alt="BMA400 accelerometer" />
  <img src="https://img.shields.io/badge/sim-FLIP%20fluid-8fd3c7?style=for-the-badge" alt="FLIP fluid simulation" />
  <img src="https://img.shields.io/badge/PCB-EasyEDA%20Pro-e8b4a0?style=for-the-badge" alt="EasyEDA Pro" />
</p>

<br />

<table align="center">
  <tr>
    <td align="center"><img src="media/trio_screen.png" alt="Three LIQUILLITE pendants glowing" width="380" /></td>
    <td align="center"><img src="media/trio_shell.png" alt="Three LIQUILLITE pendants in their shells" width="380" /></td>
  </tr>
</table>

<img src="https://capsule-render.vercel.app/api?type=rect&height=2&color=0:7ee8d6,50:5fb8c9,100:f4d9c6" width="100%" alt="" />

## 🐚 &nbsp;What is this?

LIQUILLITE is a tiny pendant with a sea of light inside it.

There's an LED matrix behind the glass and an STM32L412 running a FLIP fluid simulation in real time, so the light pools, sloshes and settles like water in a shell. A BMA400 accelerometer tells it which way is down, and a coin cell that charges over USB keeps it running on the go.

I built it because I saw mitxela's fluid pendant, couldn't stop thinking about it, and wanted to make my own from scratch: my own board, my own firmware, my own little enclosure. Everything is open, so if you want one, you can make one.

<br />

<div align="center">

<img width="200" alt="EasyEDA logo" src="https://github.com/user-attachments/assets/2f64c7bc-434b-4d77-b1a0-089d0a61b321" />

<sub>This project was kindly sponsored by <a href="https://easyeda.com/"><b>EasyEDA</b></a>, who covered the PCB design, manufacturing and prototyping.<br/>
You can explore and fork the full hardware design on <a href="https://oshwlab.com/ezekielchang31/project_aiwnxyiw">OSHWLab</a>.</sub>

</div>

<img src="https://capsule-render.vercel.app/api?type=rect&height=2&color=0:f4d9c6,50:5fb8c9,100:7ee8d6" width="100%" alt="" />

## 🌊 &nbsp;See it move

<p align="center">
  <a href="[https://youtube.com/shorts/2AIkvsZuiDc](https://youtu.be/ThHMOvxxm6c)">
    <img src="https://img.youtube.com/vi/2AIkvsZuiDc/hqdefault.jpg" alt="Watch the LIQUILLITE full demo on YouTube" width="420" />
  </a>
  <br /><br />
  <a href="https://youtube.com/shorts/2AIkvsZuiDc">
    <img src="https://img.shields.io/badge/watch_the_full_demo-YouTube-ff0000?style=for-the-badge&logo=youtube&logoColor=white" alt="Watch the full demo on YouTube" />
  </a>
  <br />
  <sub>or grab the clip straight from the repo: <a href="media/demo.mp4">media/demo.mp4</a></sub>
</p>

<img src="https://capsule-render.vercel.app/api?type=rect&height=2&color=0:7ee8d6,50:5fb8c9,100:f4d9c6" width="100%" alt="" />

## 🫧 &nbsp;Shells & colours

<p align="center"><i>Each one gets its own shade. So far there's amber, emerald and aqua.</i></p>

<table align="center">
  <tr>
    <td align="center"><img src="media/amber.jpeg" alt="Amber pendant" width="240" /></td>
    <td align="center"><img src="media/amber%20(2).jpeg" alt="Amber pendant, another angle" width="240" /></td>
    <td align="center"><img src="media/amber%20(3).jpeg" alt="Amber pendant, another angle" width="240" /></td>
  </tr>
  <tr>
    <td align="center" colspan="3"><sub><i>🟠 amber</i></sub></td>
  </tr>
  <tr>
    <td align="center"><img src="media/emerald.jpeg" alt="Emerald pendant" width="240" /></td>
    <td align="center"><img src="media/emerald%20(2).jpeg" alt="Emerald pendant, another angle" width="240" /></td>
    <td align="center"><img src="media/aqua.jpeg" alt="Aqua pendant" width="240" /></td>
  </tr>
  <tr>
    <td align="center" colspan="2"><sub><i>🟢 emerald</i></sub></td>
    <td align="center"><sub><i>🔵 aqua</i></sub></td>
  </tr>
</table>

<p align="center">
  <img src="media/enclosure.png" alt="Enclosure design" width="420" /><br/>
  <sub><i>the enclosure</i></sub>
</p>

<img src="https://capsule-render.vercel.app/api?type=rect&height=2&color=0:f4d9c6,50:5fb8c9,100:7ee8d6" width="100%" alt="" />

## 🪸 &nbsp;How it works

**🧠 The brain.** An STM32L412 reads the accelerometer at a high rate, runs the FLIP simulation (particles carry the fluid, a grid keeps it incompressible) and redraws the LED matrix every frame.

**🧭 The sense of down.** A Bosch BMA400 streams 3-axis acceleration over I²C/SPI. That vector becomes gravity inside the simulation, so the fluid always falls toward the real floor, and tilting, turning or shaking the pendant moves it instantly.

**🔋 The power.** A Microchip MCP73871 power-path charger takes 5V from USB, runs the board and charges the coin cell at the same time, then hands over to the battery when you unplug.

<br />

| | |
|:--|:--|
| **MCU** | STM32L412CBTx |
| **Motion sensor** | Bosch BMA400, ultra-low-power 3-axis accelerometer |
| **Power / charging** | Microchip MCP73871 power-path Li-ion charger |
| **Input** | 5V over USB |
| **Battery** | LIR1654 (16 mm) or LIR2050 (20 mm), 3.6V rechargeable coin cell |
| **Display** | LED matrix |
| **Simulation** | FLIP fluid, following Matthias Müller's method |

<img src="https://capsule-render.vercel.app/api?type=rect&height=2&color=0:7ee8d6,50:5fb8c9,100:f4d9c6" width="100%" alt="" />

## 🛠️ &nbsp;Building your own

The Gerber, BOM and CPL files are on the [OSHWLab page](https://oshwlab.com/ezekielchang31/project_aiwnxyiw). Build from those, since the original design file is missing some traces.

To open the design:

1. Grab [EasyEDA Pro](https://pro.easyeda.com/) (desktop or web).
2. Go to **File → Open → EasyEDA File** and pick `ProDoc_liquilite_.epro2`.
3. Or view, fork, or order boards straight from [OSHWLab](https://oshwlab.com/ezekielchang31/project_aiwnxyiw).

> [!WARNING]
> **Rechargeable cells only.** Use a 3.6V LIR1654 or LIR2050. Never fit a disposable CR2032 or CR1632: the MCP73871 will try to charge it, which can damage the cell or make it leak.

> [!TIP]
> The BMA400 (LGA) and MCP73871 (QFN) are tiny, so use hot air or a fine-tip iron. Before plugging in USB for the first time, check the STM32 and power pins for solder bridges under a magnifier.

<img src="https://capsule-render.vercel.app/api?type=rect&height=2&color=0:f4d9c6,50:5fb8c9,100:7ee8d6" width="100%" alt="" />

## 🗂️ &nbsp;Finding your way around

```
LIQUILLITE/
├── ProDoc_liquilite_.epro2   → PCB + schematic (EasyEDA Pro)
├── liquilite.ioc             → STM32CubeMX configuration
├── Core/                     → firmware source
├── Drivers/                  → STM32 HAL drivers
├── media/                    → photos, renders and the demo clip
└── kicad/                    → KiCAD Archived files
```

<img src="https://capsule-render.vercel.app/api?type=rect&height=2&color=0:7ee8d6,50:5fb8c9,100:f4d9c6" width="100%" alt="" />

## 🤍 &nbsp;Thank you

- **[mitxela](https://mitxela.com/)**, whose fluid pendant started all of this.
- **Matthias Müller**, for the maths behind the FLIP simulation.
- **[EasyEDA](https://easyeda.com/)**, for sponsoring the PCB design, manufacturing and prototyping.

<br />

<img src="https://capsule-render.vercel.app/api?type=waving&height=140&section=footer&color=0:f4d9c6,50:5fb8c9,100:7ee8d6&text=made%20with%20%F0%9F%A4%8D%20by%20tekky0&fontSize=18&fontColor=ffffff&fontAlignY=72" width="100%" alt="made by tekky0" />
