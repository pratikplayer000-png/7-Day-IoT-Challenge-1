# Day 2: 3-Stage Hardware Combination Lock

## Overview
Built a pure 3-button hardware combination lock using 7474 Dual D-Type and 7476 Dual JK Flip-Flop ICs without a microcontroller. Successfully verified the correct `1 -> 2 -> 3` button sequence triggers the green output LED.

## Breadboard Circuit Setup
![Day 2 Circuit Setup](mini_project_day2_photo.jpeg)

## Logic Configuration
* **Stage 1 (7474):** $D_1$ tied to +5V. Button 1 provides a rising-edge clock to set $Q_1$ HIGH.
* **Stage 2 (7474):** $D_2$ connected to $Q_1$. Button 2 clocks $Q_2$ HIGH only after Stage 1.
* **Stage 3 (7476):** Wired $J = Q_2$ and $K = \overline{Q}_2$. Clock (Pin 1) configured active-LOW with a 10kΩ pull-up to prevent level-latching. Button 3 triggers $Q_3$ HIGH to light the Green LED.
* **Master Reset Line:** Shared active-LOW line tied to +5V via 10kΩ pull-up resistor; grounded via Reset push button.

## Status & Day 3 Tasks
- [x] Verified 1 -> 2 -> 3 unlock sequence on hardware.
- [ ] Fix sequence bypass bug (`2 -> 1 -> 3`, `2 -> 3`, or direct `3`) caused by contact bounce and floating states.
