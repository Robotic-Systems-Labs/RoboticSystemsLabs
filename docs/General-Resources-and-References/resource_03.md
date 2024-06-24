---
layout: default
title: LCD Screen Information
parent: General Resources and References
nav_order: 23
---

{: .fs-2 }
This document was last modified: <scr id="demo">.

<script>
let text = document.lastModified;
document.getElementById("demo").innerHTML = text;
site.last_edit_timestamp= text;
</script>

# LCD Screen Information
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Wiring/Pin Connections

| LCD Pin<br>Number | LCD Pin<br>Abbreviations | LCD Function       | PSoC 5LP Pin<br>Number |
|:-------|:---------|:---------------------------------|:---------|
| 1	 | V<sub>SS</sub>|	GND                     | GND    |
| 2	 | V<sub>dd</sub>	 | 3V or +5V	                       | V<sub>dd</sub> |
| 3  | V<sub>o</sub>   | Contrast Adjustment	            |   GND    |
| 4  | RS	 | H/L Register Select Signal      |  2.5 |
| 5	 | R/W  | H/L Read/Write Signal	       |  2.6  |
| 6	 | E	 | H → L Enable Signal	           |  2.4 |
| 7  |	DB0  | H/L Data Bus Line	               |  n/a |
| 8  | DB1  | H/L Data Bus Line                |  n/a |
| 9  |	DB2	 | H/L Data Bus Line	 | n/a |
| 10 | DB3	 | H/L Data Bus Line	 | n/a |
| 11  | DB4	 | H/L Data Bus Line	| 2.0 |
| 12  | DB5  | H/L Data Bus Line	| 2.1 |
| 13  | DB6  | H/L Data Bus Line	| 2.2 |
| 14  |	DB7  | H/L Data Bus Line	| 2.3 |
| 15  | A/V<sub>ee</sub>	| + 4.2V for LED/Negative Voltage Output	| V<sub>dd</sub> |
| 16  |	K	| Power Supply for B/L (OV)	| GND |


## Data Sheet

<strong>DFRobot's LCD datasheet:</strong> <https://image.dfrobot.com/image/data/FIT0127/datasheet.pdf>

