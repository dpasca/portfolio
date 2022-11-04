# Davide Pasca's programmer portfolio

I consider programming computers the ultimate form of exploration and creativity, everything else is secondary. I'm an R&D guy at the core, although I also appreciate publishing products, because it's something that can have a direct impact on people.

I've been developing software and video games since the 90s, always with a focus in low level programming, 3D graphics and game engine development. Since 2018 I've been working mostly on algorithmic trading and created [ENZO-TS](https://www.enzobot.com), a complete trading system for cryptocurrencies.

I have a [YouTube channel](https://www.youtube.com/c/DavidePasca), mostly about algo-trading, sometimes Duolingo lessons or programming.

## Skills Summary

- **C/C++ programmer with 30 years work experience**
- Specialized in performance optimization, computer graphics, algorithmic trading, risk management, simulation, system programming, desktop applications and game development
- Published software on Windows, Linux, MS-DOS, Mac, mobile and game consoles
- Expert in **real-time 3D graphics**, **OpenGL**, **Direct3D**, software rendering, geometry and animation compression
- Good knowledge of **image processing and compression** (DCT, Wavelets, zero-tree encoding, progressive encoding)
- 5 years experience developing an **algorithmic trading systems** from the ground up, with machine-learning optimization, network connectivity, backtesting and reporting
- Experience writing complete **GUI systems** for desktop, mobile VR and avionics displays
- Some experience with **REST** API, PHP, **SQL**, Java, Python
- Some experience with **flight simulation** (flight dynamic models, avionics, auto-pilot, weapon systems)
- Languages: fluent **English**, native **Italian**, conversational **Japanese**, beginner Russian and Chinese

## Emplyoment History

{:style="font-size: 80%"}
| Start   | End  | Title  | Company  | Location  |
|:--------|:--------|:-------|:---------|:----------|
| 2010/11 | Current | Co-founder and CTO | NEWTYPE K.K. | Tokyo, Japan |
| 2006/11 | 2010/4 | Senior Software Engineer | Square Enix Co., Ltd. | Tokyo, Japan |
| 2001/8  | 2006/9 | Senior Software Engineer | Arika Co., Ltd. | Tokyo, Japan |
| 2000/5  | 2000/12 | Senior Software Engineer | Gama Internet Technology USA, Inc. | Costa Mesa, CA, USA |
| 1999/3  | 2000/3 | Software Engineer | SquareSoft, Inc. | Costa Mesa, CA, USA |
| 1995/9  | 1998/6 | Senior Programmer | Digital Dialect | West Hills, CA, USA |
| 1990/11 | 1995/8 | Programmer | Tabasoft, s.a.s. | Rome, Italy |

## Projects

<ol>
  {% for item in site.data.projects %}
    <li>
      <b><a href="#{{ item.id }}">{{ item.year_end }} - {{ item.title }}</a></b>
    </li>
  {% endfor %}
</ol>

{% for item in site.data.projects %}
---
<h3 id="{{ item.id }}">{{forloop.index}}. {{ item.year_end }} - {{ item.title }}</h3>
  {% if item.image %}
   {% if item.image_small %}
![]({{ item.image }}){:width="50%"}
   {% else %}
![]({{ item.image }})
   {% endif %}
  {% endif %}
  {% if item.image_local %}
   {% if item.image_small %}
![]({{ site.baseurl }}{{ item.image_local }}){:width="50%"}
   {% else %}
![]({{ site.baseurl }}{{ item.image_local }})
   {% endif %}
  {% endif %}
  {% if item.youtube_id %}
   {% include youtubePlayer.html id=item.youtube_id %}
  {% endif %}
  {% include_relative {{ item.src }} %}
{% endfor %}

