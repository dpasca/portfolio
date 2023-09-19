---
---
# Davide Pasca's programmer portfolio

I consider programming computers the ultimate form of exploration and creativity, everything else is secondary. I'm an R&D guy at the core, although I also appreciate publishing products, because it's something that can have a direct impact on people.

I've been developing software and video games since the 90s, always with a focus in low-level programming, **3D graphics** and **game engine development**. Since 2018 I've been working mostly on algorithmic trading with **machine-learning** (neural networks, genetic algorithms), and created [ENZO-TS](https://www.enzobot.com), a complete trading system for cryptocurrencies. 

I have a [YouTube channel](https://www.youtube.com/c/DavidePasca), mostly about algo-trading and programming.

I can be reached at **dpasca@gmail.com**

## Quick Links
- **[ENZO-TS: Cryptocurrency Trading System](https://www.enzobot.com)**
- **GitHub: [profile](https://github.com/dpasca) / [portfolio](https://github.com/stars/dpasca/lists/portfolio)**
- **[YouTube: Algo-Trading & Programming](https://www.youtube.com/c/DavidePasca)**
- **Contact: dpasca@gmail.com**

## Skills Summary

- **C/C++ Programmer with 30+ Years of Experience**
- Specialized in:
  - **Performance Optimization**
  - **Real-Time 3D Graphics**
  - **Video Game Development**
  - **Machine Learning & Algorithmic Trading**
  - **System Programming & Desktop Applications**
- Platforms: Windows, Linux, MS-DOS, Mac, iOS, Android, Game Consoles

### Strong Experience
- **Real-Time 3D Graphics**: OpenGL, Direct3D, Software Rendering, Geometry Processing
- **Image Processing & Compression**: DCT, Wavelets, Zero-Tree Encoding
- **Video Games & Simulation Development**: Including physics and AI
- **Automated Trading Systems**: AI-Based Algorithms, Data Collection, Backtesting, Portfolio Management
- **GUI Systems**: Desktop, Mobile, VR, Avionics
- **Mobile Platforms**: Published software on major mobile platforms

### Moderate Experience
- **AI / Machine Learning**: Neural Networks, Neuroevolution, in C++ and Python
- **Python & ML Libraries**: PyTorch/Libtorch
- **Flight Simulation**: Flight Dynamics, Avionics, Weapon Systems

### Limited Experience
- JavaScript, REST, PHP, SQL, Java

### Leadership & Language Skills
- **Management**: Capable of running a small business and leading a development team
- **Languages**: Italian (Native), English (Fluent), Japanese (Conversational), Russian & Chinese (Beginner)

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

