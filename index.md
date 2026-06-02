---
layout: default
---
# Davide Pasca's programmer portfolio

<img src="images/dav_front_shot_cropped.jpg" alt="Davide Pasca" style="width: 120px; float: right; margin-left: 5px; margin-bottom: 10px; border-radius: 10px; position: relative; top: 20px;"/>

Programming represents the pinnacle of exploration and creativity for me. I'm deeply involved in R&D, constantly pursuing innovative ideas and technologies. Over the years I also found significant satisfaction in developing impactful software, particularly in gaming, interactive media, quantitative trading, and developer tools.

I speak Italian, English, Japanese, and occasionally touch on some other languages.

## Career

My current focus lies in [AI Research & Development](#ai-rnd), AI-native products, and developer tools. I work both at the low level with **C++** and **PyTorch**, and at the higher level with LLM APIs, model routing, tool orchestration, and agent-based architectures.

I am actively developing my own AI-based IDE called [Little Control Room](#little-control-room). I believe that the ability to rapidly develop tools for development is essential to accelerating productivity. It has the potential to build a competitive hedge and to future-proof this business by building alternative solutions, rather than relying on a single LLM provider.

Before the new AI wave that started with ChatGPT, I've successfully applied **AI / ML** to **financial market forecasting** ([ENZO-TS](#enzo-trading-system)) and **autopilot** for airframes ([XPSVR](#xpsvr-experimental-flight-simulator)).

Since the mid-90s I've been working on **game development** and **real-time 3D graphics**, gaining experience in major gaming corporations as well as spearheading projects at my own [development studio](https://oykgames.com).

## Programming in the AI era

I'm not a terribly nostalgic person, and while I do appreciate how programming used to be and the personal benefits I received from doing it manually, I also realize that my passion for technology and the will to build more and better is stronger than the pure activity of writing code. Writing code itself has changed a lot over the years, from the daunting task of writing terse assembly code trying to shave every cycle to high-level languages and package systems that allow for rapid development of fairly complex applications.

LLMs as they are today in 2026 have completely revolutionized the process, although having a strong foundation as a software engineer is still essential to build robust products.

Recent projects such as **AskMei.ai**, **Little Control Room**, and **Fractal Strike** are fully developed with AI tools as a normal part of the engineering process. They are built with programming languages that I have never formally learned, but that now feel less like barriers and more like abstraction layers over the process of development.

|  Quick Links              |                                           |
|:--------------------------|:------------------------------------------|
| 💻 My GitHub Profile      | [github.com/dpasca](https://github.com/dpasca)      |
| 📚 My GitHub Portfolio    | [dpasca.github.io/portfolio](https://dpasca.github.io/portfolio) |
| 📈 My Trading System      | [ENZO-TS](https://www.enzobot.com)        |
| 📺 My YouTube Channel     | [DavidePasca](https://www.youtube.com/c/DavidePasca) |
| ✍️ My Blog                | [xpsvr.com](https://xpsvr.com)            |
| 📧 Contact                | dpasca@gmail.com                          |


## Skills Summary

- **Software Engineer with 30+ Years of Experience**
- **Performance Optimization**: C/C++, assembly
- **AI / Machine Learning**: neural networks from the ground up, PyTorch, LLMs via APIs
- **AI Product Development**: assistants, agentic workflows, memory systems, image generation, developer tools
- **Algorithmic Trading**: strategy development, backtesting, portfolio management
- **Video Game Development**: 3D engine, physics, game logic, UI
- **Real-Time 3D Graphics**: OpenGL, Direct3D, software rendering
- **Image Processing & Compression**: DCT, Wavelets, Zero-Tree Encoding
- **Flight Simulation**: flight dynamics, avionics, weapon systems
- Platforms: desktop, mobile, consoles

### Leadership & Language Skills

- **Management**: Capable of running a small business and leading a development team
- **Languages**: Italian, Japanese, English

## Employment History

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
![{{ item.title }} screenshot]({{ item.image }}){% if item.image_small %}{:width="50%"}{% endif %}
{% endif %}
{% if item.image_local %}
![{{ item.title }} screenshot]({{ site.baseurl }}{{ item.image_local }}){% if item.image_small %}{:width="50%"}{% endif %}
{% endif %}
{% if item.youtube_id %}
  {% include youtubeplayer.html id=item.youtube_id %}
{% endif %}
{% include_relative {{ item.src }} %}
{% endfor %}
