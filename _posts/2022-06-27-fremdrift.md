---
layout: post
title: Drivkraft
author: Christoffer Kleven Berg
categories: rcbåt
math: true
image: /drivkraft_blueprint.jpg
date: 2022-06-26
last_modified_at: 2022-06-28 22:42:00 +0200
---

# Motor

Mange av komponentene i båten må tilpasses motoren og den er derfor et godt utgangspunkt. Standaren i elektriske, radiokontrollerte fartøy er børsteløse motorer. Der er det hovedsakelig 3 egenskaper som er relevante.

### Størrelse

Hvor stor motor man trenger kommer an på hvor stor båt man har. Flere kilder er enige om at båter rundt 0.8m lange burde ha en motor med 36mm diameter. Vi er begrenset av regel nr. 2 til å holde oss under 1 meter, dermed virker en motor med Ø36mm helt kurant.

### KV rating

KV betyr rpm/V, altså turtall per volt. KV ratingen bestemmer hvor mye spenning motoren trenger for å nå et ønsket turtall når den ikke er under belastning. En motor med Ø36mm burde ligge på rundt 40000rpm og standard LiPo batterier har maksimalt 4.2V per celle. Med utgangspunkt i det får vi følgende alternativer:

| Celler | Spenning $[\text{V}]$ | KV $[\frac{\text{rpm}}{\text{V}}]$ |
| -----: | --------------------: | ---------------------------------: |
|      1 |                   4.2 |                               9500 |
|      2 |                   8.4 |                               4800 |
|      3 |                  12.6 |                               3200 |
|      4 |                  16.8 |                               2400 |
|      5 |                  21.0 |                               1900 |
|      6 |                  25.2 |                               1600 |

_Her er det brukt at $KV = \frac{\omega}{U}$ hvor $\omega$ er rotasjonshastighet og $U$ er spenning._

### Maks strøm

Maks strøm forteller deg hvor mye strøm motoren tåler. Dette er viktig å ta hensyn til når man velger en ESC(hastighetsregulator) og når man velger en propell. Uten belastning trekker ikke motoren mye strøm, men når den belastes av en propell, øker strømmen som trekkes fra ESC'en og batteriet. Motoren og hastighetsregulatoren kan overopphete dersom propellen gjør mer motstand enn de er bygget for å tåle.

# Hastighetsregulator (ESC)

En ESC konverterer batteriets likestrøm til 3-faset vekselstrøm som motoren trenger. Hvor mye spenning som leveres til motoren kan reguleres med et PWM signal. Det er vanlig at ESC'ene kommer med innebygget BEC (Battery Eliminator Circuit) som kan levere redusert spenning til RC-komponentene slik at de ikke trenger eget batteri. Når man velger ESC burde man sørge for at den tåler omtrent like mye strøm som motoren, på den måten blir ikke den ene komponenten en flaskehals for den andre. Samtidig bør BEC'en levere en spenning som samsvarer med det du trenger til RC-komponentene.

# Nedkjøling

Som nevnt ovenfor, er ytelsen til motoren i stor grad begrenset av varmedannelse. Om man får ledet bort mye av den varmen, så kan motoren yte bedre. En båt har særdeles god tilgang til kaldt vann, så vannkjøling er naturlig.

## Motorvalg

| Motor Spec      |
| --------------- | ------: |
| Motor Type      |    2948 |
| KV              |  3000KV |
| Max Amps        |     55A |
| Max Voltage     |     18V |
| Max Power       |   1000W |
| Weight          |    145g |
| No load current |    1.5A |
| Max RPM         |     60K |
| Motor shaft     | 3.175mm |
| Banana plug     |   4.0mm |

| ESC Spec      |
| ------------- | ---------------- |
| ESC Type      | BS50             |
| Cont. Current | 50A              |
| Burst Current | 60A              |
| Battery Cell  | 5-18NiMH/2-6lipo |
| BEC Output    | 5.5V/5A          |
| Weight        | 75g              |
| Size          | 56x30x19mm       |

# Batteri

## Kilder

1. https://rchobbytips.com/what-size-brushless-motor-for-rc-boat/
2. https://www.radiocontrolinfo.com/rc-electric-boats/brushless-boat-motor/
3. https://rcboatbitz.com/guides/choosing-a-brushless-motor/
4. http://www.blackbird-rc.net/index.php?option=com_zoo&task=item&item_id=17&Itemid=20
5. https://en.m.wikipedia.org/wiki/Electronic_speed_control
