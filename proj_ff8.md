While employed at [SquareSoft](https://en.wikipedia.org/wiki/Square_(video_game_company)), USA,
I worked on the Windows port of the **Final Fantasy VIII** PlayStation game.

My main job was that of creating an abstraction layer between the PSX code and SquareSoft's graphics library, which was based on DirectX.
This drastically reduced porting time, as most code continued to compile as it were on the PlayStation.

Some code still needed fixing, in a few cases due to memory access bugs that did not appear on the original platform, due to lack of an MMU unit in the first PlayStation.

![]({{ site.baseurl }}/images/ff8_korean_mag_kp150_cut.jpg)

#### My work on the project

- Writing the abstraction layer that simulated PlayStation APIs and hardware on PC
- Alternative software rendering path for special effect, normally not possible via DirectX
- Adapt rendering code for the wild variety of graphics accelerators of the era
- Develop techniques to improve rendering quality with original (low res) assets

#### What I learned

- I built a deeper understanding of the PlayStation hardware
- Game code of Japanese RPG games
- Work in a mixed Japanese/international environment
