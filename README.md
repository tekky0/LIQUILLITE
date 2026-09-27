<!-- ~ header wave ~ -->
<img src="https://capsule-render.vercel.app/api?type=waving&height=220&color=0:7ee8d6,50:5fb8c9,100:f4d9c6&text=LIQUILITE&fontColor=ffffff&fontSize=64&fontAlignY=38&desc=a%20little%20tide%20pool%20you%20can%20wear&descAlignY=58&descSize=18&animation=fadeIn" width="100%" alt="LIQUILITE" />

<p align="center">
  <img src="https://img.shields.io/badge/MCU-STM32L412-5fb8c9?style=flat-square" alt="MCU STM32L412" />
  <img src="https://img.shields.io/badge/sim-FLIP%20fluid-7ee8d6?style=flat-square" alt="FLIP fluid simulation" />
  <img src="https://img.shields.io/badge/PCB-EasyEDA%20Pro-f4d9c6?style=flat-square" alt="EasyEDA Pro" />
  <img src="https://img.shields.io/badge/hardware-open%20source-e8b4a0?style=flat-square" alt="Open source hardware" />
</p>

<br />

<table align="center">
  <tr>
    <td align="center"><img src="media/trio_screen.png" alt="Three LIQUILITE pendants glowing" width="380" /></td>
    <td align="center"><img src="media/trio_shell.png" alt="Three LIQUILITE pendants in their shells" width="380" /></td>
  </tr>
</table>

<br />

## 🐚 &nbsp;What is this?

LIQUILITE is a tiny pendant with a sea of light inside it.

There's an LED matrix behind the glass and an STM32L412 running a FLIP fluid simulation in real time, so the light pools, sloshes and settles like water in a shell. I built it because I saw mitxela's fluid pendant, couldn't stop thinking about it, and wanted to make my own from scratch: my own board, my own firmware, my own little enclosure.

Everything is open. The PCB, the schematic, and the firmware are all in this repo, so if you want one, you can make one.

<br />

<!-- sponsor -->
<div align="center">

<img width="200" alt="EasyEDA logo" src="https://github.com/user-attachments/assets/2f64c7bc-434b-4d77-b1a0-089d0a61b321" />

<sub>This project was kindly sponsored by <a href="https://easyeda.com/"><b>EasyEDA</b></a>, who covered the PCB design, manufacturing and prototyping.<br/>
You can explore and fork the full hardware design on <a href="https://oshwlab.com/ezekielchang31/project_aiwnxyiw">OSHWLab</a>.</sub>

</div>

<br />

## 🌊 &nbsp;See it move

https://github.com/user-attachments/assets/YOUR-VIDEO-ID

<br />

## 🫧 &nbsp;Shells & colours

Each one gets its own shade. So far there's amber, emerald and aqua.

<table align="center">
  <tr>
    <td align="center"><img src="media/amber.jpeg" alt="Amber pendant" width="240" /></td>
    <td align="center"><img src="media/amber%20(2).jpeg" alt="Amber pendant, another angle" width="240" /></td>
    <td align="center"><img src="media/amber%20(3).jpeg" alt="Amber pendant, another angle" width="240" /></td>
  </tr>
  <tr>
    <td align="center" colspan="3"><sub><i>amber</i></sub></td>
  </tr>
  <tr>
    <td align="center"><img src="media/emerald.jpeg" alt="Emerald pendant" width="240" /></td>
    <td align="center"><img src="media/emerald%20(2).jpeg" alt="Emerald pendant, another angle" width="240" /></td>
    <td align="center"><img src="media/aqua.jpeg" alt="Aqua pendant" width="240" /></td>
  </tr>
  <tr>
    <td align="center" colspan="2"><sub><i>emerald</i></sub></td>
    <td align="center"><sub><i>aqua</i></sub></td>
  </tr>
</table>

<p align="center">
  <img src="media/enclosure.png" alt="Enclosure design" width="420" /><br/>
  <sub><i>the enclosure</i></sub>
</p>

<br />

## 🪸 &nbsp;What's inside

| | |
|:--|:--|
| **Brain** | STM32L412CBTx |
| **Display** | LED matrix |
| **Simulation** | FLIP fluid, following Matthias Müller's approach |
| **PCB tool** | [EasyEDA Pro](https://pro.easyeda.com/) |
| **Hardware files** | [OSHWLab project page](https://oshwlab.com/ezekielchang31/project_aiwnxyiw) |

<br />

## 🗂️ &nbsp;Finding your way around

```
LIQUILITE/
├── ProDoc_liquilite_.epro2   → PCB + schematic (EasyEDA Pro)
├── liquilite.ioc             → STM32CubeMX configuration
├── Core/                     → firmware source
├── Drivers/                  → STM32 HAL drivers
└── media/                    → photos, renders and the demo video
```

<br />

## 🔍 &nbsp;Opening the design

1. Grab [EasyEDA Pro](https://pro.easyeda.com/) (desktop or web).
2. Go to **File → Open → EasyEDA File** and pick `ProDoc_liquilite_.epro2`.
3. Or skip the download and view, fork, or order boards straight from the [OSHWLab page](https://oshwlab.com/ezekielchang31/project_aiwnxyiw).

<br />

## 🤍 &nbsp;Thank you

- **[mitxela](https://mitxela.com/)**, whose fluid pendant started all of this.
- **Matthias Müller**, for the maths behind the FLIP simulation.
- **[EasyEDA](https://easyeda.com/)**, for sponsoring the PCB design, manufacturing and prototyping.

<br />

<img src="https://capsule-render.vercel.app/api?type=waving&height=120&section=footer&color=0:f4d9c6,50:5fb8c9,100:7ee8d6" width="100%" alt="" />
