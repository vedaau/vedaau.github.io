---
title: Power Budget
---
## Overview
Here is the the power budget for my Lid motor subsystem. When I analyzed the power budget, I saw that the 5 V rail needs about 0.7 A after adding a 25% safety margin, and the 9 V rail normally draws around 0.2–0.3 A but can spike to about 0.5–1 A when the motor starts. Since both rails ultimately pull from the 9 V supply, I estimated the total system demand to be roughly 1.0–1.3 A during normal operation, with short peaks reaching close to 2 A. Based on that, I concluded that a 1 A fuse would probably blow during motor startup, while a 2 A slow-blow fuse would handle both the steady load and the momentary surges without nuisance tripping. So from the power budget, I determined that a **2 A slow-blow fuse** is the safest and most reliable choice.

<br><br>

 ![](xlsmotor1.jpg)
 ![](xlsmotor2.jpg)
The power budget as a PDF download is available [*here*](PowerBudgetVedaamotor1.pdf), and a Microsoft Excel Sheet [*here*](PowerBudgetVedaamotor1.xlsx).
