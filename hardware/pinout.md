# Hardware Architecture
<img width="280" height="350" alt="Screenshot 2026-08-29 233512" src="https://github.com/user-attachments/assets/1b5894c7-3a8c-45c2-8654-ab1ad8a20b89" />

## Pinout Table
| Device | Device Pin | Destination | Destination Pin |
|---|---|---|---|
| DE-1O | GND | Battery | - |
| DE-1O | GPIO-Pin-1 | L298N | ENA |
| Battery | + | L298N | +12V |
| Battery | - | DE-10 | GND |
| Battery | - | L298N | IN1 |
| L298N | +5V | L298N | IN2 |
| L298N | OUT3 | Motor | 1 |
| L298N | OUT4 | Motor | 2 |

WARNING: Make sure the L298N ground and the DE-10 Lite ground are shared.
