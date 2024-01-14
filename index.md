---
---
# Davide Pasca's programmer portfolio

Programming represents the pinnacle of exploration and creativity for me. I'm deeply involved in R&D, constantly pursuing innovative ideas and technologies. In the years I also found significant satisfaction in developing impactful software, particularly in the realms of gaming and interactive media, used and enjoyed by millions worldwide.

My native language is Italian 🇮🇹, I'm fluent in English 🇺🇸, decent in Japanese 🇯🇵, and I can catch some words in Russian 🇷🇺 and Chinese 🇨🇳.

## Career

My current focus is on **AI**, encompassing both the technical depths of **C++ and PyTorch** and the strategic aspects of **Python, LLM APIs, and prompt engineering**.

My journey into AI and machine-learning began in 2017 working on the [XPSVR flight sim](https://dpasca.github.io/portfolio/#xpsvr-experimental-flight-simulator), progressing with the development of [ENZO-TS](https://www.enzobot.com), an **algorithmic trading** system for cryptocurrencies.

Prior to this, I dedicated over two decades to **game development** and **real-time 3D graphics**, gaining experience in major gaming corporations as well as spearheading projects at my own [development studio](https://oykgames.com).

## A programmer in 2024

I'm not a terribly nostalgic person, and while I do appreciate how programming used to be, I very much welcomed the benefits recently brought by AI tools such as *ChatGPT* and *Copilot*. I've always wished for more time and more brain power to explore and implement many ideas that I had, and these tools are a giant leap in that direction.

I believe (hope ?) that as much as an equalizer these AI tools are, they will continue to work as a force multiplier, expecially for those of us that have extensive experience in software engineering.

|  Quick Links              |                                           |
|:--------------------------|:------------------------------------------|
| 💻 My GitHub Profile      | [profile](https://github.com/dpasca)      |
| 📚 My GitHub Portfolio    | [portfolio](https://dpasca.github.io/portfolio) |
| 📈 My Trading System      | [ENZO-TS](https://www.enzobot.com)        |
| 📺 My YouTube Channel     | [channel](https://www.youtube.com/c/DavidePasca) |
| ✍️ My Blog                | [xpsvr.com](https://xpsvr.com)            |
| 📧 Contact                | dpasca@gmail.com                          |


## Skills Summary

- **Software engineer with 30+ Years of Experience**
- **Performance Optimization**: C/C++, assembly
- **Fluent in C/C++, Python, JavaScript**
- **AI / Machine Learning**: neural networks from ground up, PyTorch
- **Algorithmic Trading**: strategy development, backtesting, portfolio management
- **Video Game Development**: PC, console, mobile, 3D engine, physics, game logic, UI
- **Real-Time 3D Graphics**: OpenGL, Direct3D, software rendering
- **Image Processing & Compression**: DCT, Wavelets, Zero-Tree Encoding
- **Flight Simulation**: flight dynamics, avionics, weapon systems
- **System Programming & Desktop Applications**
- Platforms: Windows, Linux, MS-DOS, Mac, iOS, Android, Game Consoles

### Leadership & Language Skills
- **Management**: Capable of running a small business and leading a development team
- **Languages**: Italian, English (fluent), Japanese (conversational), Russian & Chinese (beginner)

## Emplyoment History

{:style="font-size: 85%"}
| Start   | End  | Title  | Company  | Location  |
|:--------|:--------|:-------|:---------|:----------|
| 2010/11 | Current | Co-founder and CTO | NEWTYPE K.K. | Tokyo, Japan |
| 2006/11 | 2010/4 | Senior Software Engineer | Square Enix Co., Ltd. | Tokyo, Japan |
| 2001/8  | 2006/9 | Senior Software Engineer | Arika Co., Ltd. | Tokyo, Japan |
| 2000/5  | 2000/12 | Senior Software Engineer | Gama Internet Tech. USA, Inc. | Costa Mesa, CA, USA |
| 1999/3  | 2000/3 | Software Engineer | SquareSoft, Inc. | Costa Mesa, CA, USA |
| 1995/9  | 1998/6 | Senior Programmer | Digital Dialect | West Hills, CA, USA |
| 1990/11 | 1995/8 | Programmer | Tabasoft, s.a.s. | Rome, Italy |

## Projects

The following list of projects is limited to major milestones or more
recent products. My professional experience started in 1990, however, the first listed project is from 1994, for the sake of brevity.

<table style="font-size: 85%">
<thead><tr>
<th style="text-align: left"></th>
<th style="text-align: left">Year</th>
<th style="text-align: left">Name</th>
<th style="text-align: left">Type</th>
<th style="text-align: left">Company</th>
</tr></thead>
<tbody>
{% for item in site.data.projects %}
<tr>
<td style="text-align: left">{{forloop.index}}</td>
<td style="text-align: left">{{item.year_end}}</td>
<td style="text-align: left; font-weight: bold"><a href="#{{ item.id }}">{{item.title}}</a></td>
<td style="text-align: left">{{item.type}}</td>
<td style="text-align: left">{{item.company}}</td>
</tr>
{% endfor %}
</tbody>
</table>

{% for item in site.data.projects %}
---
<h3 id="{{ item.id }}">{{forloop.index}}. {{ item.year_end }} - {{ item.title }}</h3>
{% if item.image %}
![]({{ item.image }}){% if item.image_small %}{:width="50%"}{% endif %}
{% endif %}
{% if item.image_local %}
![]({{ site.baseurl }}{{ item.image_local }}){% if item.image_small %}{:width="50%"}{% endif %}
{% endif %}
{% if item.youtube_id %}
  {% include youtubeplayer.html id=item.youtube_id %}
{% endif %}
{% include_relative {{ item.src }} %}
{% endfor %}

