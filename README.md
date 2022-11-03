# Davide Pasca's programmer portfolio

I consider programming computers the ultimate form of exploration and creativity, everything else is secondary. I'm an R&D guy at the core, although I also appreciate publishing products, because it's something that can have a direct impact on people.

I've been developing software and video games since the 90s, always with a focus in low level programming, 3D graphics and game engine development. Since 2018 I've been working mostly on algorithmic trading and created [ENZO-TS](https://www.enzobot.com), a complete trading system for cryptocurrencies.

I have a [YouTube channel](https://www.youtube.com/c/DavidePasca), mostly about algo-trading, sometimes Duolingo lessons or programming.

Skills summary:
- **30 years of work experience as a C/C++ programmer**, specialized in performance optimization, computer graphics, algorithmic trading, simulation, system programming, deskptop applications and game development
-	Published software on PC, Mac, mobile and game consoles
- Expert in **real-time 3D graphics**, OpenGL, Direct3D, software rendering, geometry and animation compression
- Good knowledge of **image processing and compression** (DCT, Wavelets, zero-tree encoding, progressive encoding)
-	5 years experience developing an **algorithmic trading** system from the ground up, with machine-learning optimization, network connectivity, backtesting and reporting
-	Some experience with **flight simulation** (flight dynamic models, avionics, auto-pilot, weapon systems)
-	Languages: fluent **English**, native **Italian**, conversational/informal-business **Japanese**. Beginner Russian and Chinese.

## Projects

<ul>
  {% for item in site.data.projects %}
    <li>
      <b><a href="#{{ item.id }}">{{ item.title }}</a></b>
    </li>
  {% endfor %}
</ul>

{% for item in site.data.projects %}
---
  <h3 id="{{ item.id }}">{{ item.title }}</h3>
  {% include_relative {{ item.src }} %}
{% endfor %}

