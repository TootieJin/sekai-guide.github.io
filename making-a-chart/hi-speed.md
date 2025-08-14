---
description: >-
  "Where did the note go!?" - Hi-Speed: How it works and common effects using
  Hi-Speed.
icon: angles-up
---

# Hi-Speed

## Quick Overview

<figure><img src="../.gitbook/assets/image (9).png" alt="" width="403"><figcaption><p>Hi-Speed option</p></figcaption></figure>

Hi-Speeds (soflan) change the speed of notes and the distance between them. **They don't change the timings of the notes.**\
\
You can place the Hi-Speed event by pressing <img src="../.gitbook/assets/image (7).png" alt="" data-size="line"> (or <mark style="color:blue;">`9`</mark> by default) in Timeline Tools and place it anywhere.

### \[Advanced] Calculating the Note Distance between Hi-speeds

* The distance between any two notes is the sums of each hi-speed and their lengths.
  * e.g. A 2/16th measure @ <mark style="color:red;">x5</mark>, 2/16ths @ <mark style="color:red;">x2</mark>, and 6/16ths @ <mark style="color:red;">x1</mark> would look like a 20/16th distance. (5\*2/16 + 2\*2/16 + 1\*6/16 = 20/16)
* At <mark style="color:red;">x0.001</mark>, an entire measure (1) would look like a distance of 1/1000th. (0.001\*1 measure = 1/1000 measures) This effectively makes the notes stop completely.
  * Inversely, at <mark style="color:red;">x1000</mark>, a 1/16th would look like a distance of 62.5 measures. (1000\*1/16th measure = 62.5 measures) This effectively makes all the notes so fast they're invisible.

### Negative Hi-Speeds

Hi-Speeds value can also go below <mark style="color:red;">x0</mark>. Instead of going towards the judgement line, notes will go _backwards._

* A <mark style="color:red;">x-1000</mark> and a <mark style="color:red;">x1000</mark> of equal lengths will not cancel out to a <mark style="color:red;">x1</mark> distance; it will cancel out to a <mark style="color:red;">x0</mark>. (-1000 + 1000 = 0 measures)
  * A <mark style="color:red;">x1</mark> distance is made with a <mark style="color:red;">x1000</mark> and <mark style="color:red;">x-998</mark>. (1000\*1/2 measures + -998\*1/2 measures = 2\*1/2 = 1 measure)

***

## Common Effects

### Notes Come from the Bottom and Fall Down

1. Place 3 Hi-Speeds:&#x20;
   1. <mark style="color:red;">x10000</mark> (or higher) before the last two Hi-Speeds (to teleport the note to under the judgement line)
   2. A negative value Hi-Speed.
   3. A positive value Hi-Speed.

<div align="center"><figure><img src="../.gitbook/assets/image (1) (1) (1) (1).png" alt="" width="375"><figcaption><p>Step 1</p></figcaption></figure></div>

2. Interpolate Hi-Speeds between the last 2 Hi-Speeds. (This step can be done easily in [MMW4CC](https://github.com/sevenc-nanashi/MikuMikuWorld4CC) like so.)

<div><figure><img src="../.gitbook/assets/image (2) (1) (1) (1).png" alt=""><figcaption><p>Interpolate Hi-Speeds in MMW4CC</p></figcaption></figure> <figure><img src="../.gitbook/assets/Screenshot 2024-09-09 204941.png" alt=""><figcaption><p>After interpolation</p></figcaption></figure></div>

### Different Hi-Speeds in Different Notes ([MMW4CC](https://github.com/sevenc-nanashi/MikuMikuWorld4CC))

* Place 2 simultaneous notes, one on a separate timeline with a different speed (called "Layers" in MMW4CC).

### Notes Suddenly Turns Invisible

**\[For Beginners]** Place a <mark style="color:red;">x-9999</mark> Hi-speed on each note you want to make disappear, and a <mark style="color:red;">x10000</mark> Hi-Speed halfway between each note. Do this for every other notes _(remember to add separate Layers per notes for this effect)_.\
\
&#xNAN;**\[Advanced]** Original: [lawneater](https://discordid.netlify.app/?id=579413915197505537) ([message link](https://discord.com/channels/1060525567797112832/1060553867496018000/1167671018735800370))

1. Place a <mark style="color:red;">x1000</mark> on the point where you want your notes to go invisible, and on each note during that time. (You can stop after about half a measure.)
2. Take note of your division. The smaller the better. Try to use a number that is divisible by the division your notes are on.
   * (e.g notes are on 16ths -> use 1600 division; notes on 24ths - > use 1200 division)
3. Place a Hi-speed 1 step after the <mark style="color:red;">x1000</mark> Hi-speed.
4. Set value for the Hi-speed to `(d*n - 1000)/(d*n -1)`
   * where `d` is your division
   * and `n` is the reciprocal of the distance between this <mark style="color:red;">x1000</mark> and the next <mark style="color:red;">x1000</mark> Hi-speed in measures (e.g. 1/16, 17/24)
5. Repeat Steps 3 and 4 for each note. Your chart should look something like this.

<figure><img src="../.gitbook/assets/image (6) (1).png" alt="" width="563"><figcaption></figcaption></figure>
