# 🚨 Emergency Location SMS System using GPS and GSM (Arduino)

This project uses an Arduino board, a GPS module, and a GSM module to send an emergency text message with real-time GPS coordinates to a predefined phone number. It's particularly useful for sending help alerts in disaster zones, remote areas, or personal safety situations.

---

## 📦 Features

- Send an SMS with:
  - User name
  - GPS location (latitude & longitude)
  - Emergency message
- Live SMS monitoring option
- GPS data parsing using the `TinyGPS` library
- GSM communication using `SoftwareSerial`

---

## 🛠️ Hardware Required

- Arduino UNO (or compatible)
- GPS Module (e.g., NEO-6M)
- GSM Module (e.g., SIM800L, SIM900)
- Jumper wires
- External power supply (for GSM module)
- SIM card with active SMS plan

---

## 🔌 Wiring

| Component    | Arduino Pin |
|--------------|-------------|
| GSM RX       | Pin 10      |
| GSM TX       | Pin 9       |
| GPS TX       | Pin 0 (RX)  |
| GPS RX       | Not used    |

> ⚠️ Note: The GPS module communicates via the hardware serial port, so avoid connecting other serial devices while reading GPS.

---

## 💻 How It Works

1. **Startup:**
   - Initializes Serial Monitor and GSM module.
2. **Commands from Serial Monitor:**
   - Type `S` or `s` to send an emergency SMS.
   - Type `R` or `r` to receive live SMS on the GSM module.
3. **SMS Content:**
