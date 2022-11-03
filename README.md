# Davide Pasca's programmer portfolio

I consider programming computers the ultimate form of exploration and creativity, everything else is secondary. I'm an R&D guy at the core, although I also appreciate publishing products, because it's something that can have a direct impact on people.

I've been developing software and video games since the 90s, always with a focus in low level programming, 3D graphics and game engine development. Since 2018 I've been working mostly on algorithmic trading and created [ENZO-TS](https://www.enzobot.com), a complete trading system for cryptocurrencies.

Some pointers:
- My favorite programming language is C++ (for better or for worse), and I follow the best-practices (exceptions, `auto`, labmdas, etc.).
- I don't like weakly-typed languages. Their flexibility can quickly lead to ambiguity and bugs.
- Italian is my mother tongue, English second, Japanese a distant third.
- In 2022 I started learning Russian and Chinese on Duolingo ([my profile](https://www.duolingo.com/profile/TheCrib)).
- I have a [YouTube channel](https://www.youtube.com/c/DavidePasca), mostly about algo-trading, sometimes Duolingo lessons or programming.

## Projects

    {% for item in site.data.projects %}
        {% include_relative item.src %}
    {% endfor %}

