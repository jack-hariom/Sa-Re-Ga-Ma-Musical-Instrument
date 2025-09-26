# 🎵 SA RE GA MA Musical Instrument  

A simple **Arduino-based musical instrument** that plays Indian classical notes (**Sa Re Ga Ma Pa Dha Ni Sa**) using **LDR sensors** and **light exposure**.  

When a torch/flashlight is pointed inside any of the 8 pipes (each containing an LDR), the Arduino detects the light and plays the corresponding musical note through a speaker.  

---

## 🔧 Components Required
- Arduino Nano  
- 8 × LDR sensors  
- 8 × 10kΩ resistors (for voltage divider)  
- Speaker + Amplifier  
- 8 × PVC pipes (for note holders)  
- Jumper wires & Breadboard  

---

## 🎶 Notes & Frequencies
| Note | Name | Frequency (Hz) |
|------|------|----------------|
| सा   | Sa   | 240 Hz |
| रे   | Re   | 270 Hz |
| गा   | Ga   | 300 Hz |
| मा   | Ma   | 337 Hz |
| प    | Pa   | 360 Hz |
| धा   | Dha  | 400 Hz |
| नी   | Ni   | 450 Hz |
| सा   | Sa’  | 480 Hz |

---

## ⚙️ Circuit Description
- Each LDR forms a **voltage divider** with a 10kΩ resistor.  
- Output of the divider is fed to Arduino Nano **analog pins A0–A7**.  
- Arduino checks if the light intensity crosses a set **threshold**.  
- If yes → Arduino generates the respective frequency on **pin 11** using the `tone()` function.  
- An external amplifier + speaker plays the note.  

---


