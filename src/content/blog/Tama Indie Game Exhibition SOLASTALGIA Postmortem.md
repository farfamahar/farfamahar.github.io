---
title: 'Tama Indie Game Exhibition Postmortem for SOLASTALGIA'
description: ''
pubDate: 'Oct 22 2026'
heroImage: ''
---

In July I exhibited [SOLASTALGIA](https://farfama.itch.io/solastalgia) as part of the [TAMA INDIE GAME EXHIBITION DISSONANCE #1](https://www.dissonance.tokyo/en/). This was organized by [futurala](https://x.com/yasukiwatanabe) and [.iris](https://x.com/thisisdotiris). Along with them, 12 others exhibited works under the theme of 不穏 -unrest-. The event was organized as an art gallery-like exhibition. A small maze arrangement encouraged attendees to explore the space where games were displayed both in the open but also hidden around darker corners. A lot of thought went into making the space feel interesting to navigate, with each game given its own area to get immersed in. I appreciated that this wasn't a typical game expo setup with countless tables, games, and bright lights. It was quieter, slower, and fit the themes atmosphere well.

<img  src="/dissonance/website_homepage.png"/>

Developing SOLASTALGIA for this exhibition was more difficult than I thought. I had to make some changes to the build so that it would restart after completion, and also create a title screen so those walking by could start the experience, set the language, and read the intro quote. I already had a previous exhibition build (without the title screen) that would reset on finish, but after testing that build I found a bug. There's a section in the game when time slows down. When the game resets, some time related code doesn't reset properly which causes a performance issue with all the particle effects in the game. This would lead to some type of memory leak that caused small freezes whenever you entered the fire forest area (where the most particles lived). I was able to locate the problem by using Unity's built-in profiler tools and solve the problem with a few code changes after that.

<img  src="/dissonance/unity-profiler.png"/>

Some other additions to the experience were new visuals added to the poem section. As the poem finishes, it starts to display word and sentence fragments randomly. To match the ramp up towards the chaotic back and forth flashing, I added a shaky effect to the text which gradually gets more wobbly and disorienting. I also added more deers in the environment during this section which slowly appear around you. Eventually at the peak of this chaotic moment, the deers will float towards you and start to spin rapidly around like a vortex. In the fire section I also included a hazy blur shader so you can get a visual sense of the heat. Some additional spark and fire particles were added in this environment too.

<video src="/dissonance/solastalgia-text-wobble.mp4" autoplay loop muted playsinline controls style="width:100%"></video>

The biggest thing I added was a Japanese translation done by [nicolith](https://nicolith.crd.co/). It took some back and forth to make sure the meaning was still preserved. I imagine poetry is difficult to translate and requires some interpretation, localization, and creative liberties. It was great collaborating and they asked a lot of questions to ensure the poem turned out well. If you need your game translated to Japanese, I highly recommend working with nicolith. They specialize in short-form experimental indie games and has worked on both big and large scale projects. By including a Japanese translation, the experience now supports translations of any language via a .csv file that gets parsed. It was also translated into French for another exhibition that happened in August. If you have experience translating poetry from English, please get in touch if you would like to help.

<img  src="/dissonance/solastalgia-title.webp"/>

Exhibiting the game was wonderful. I was given a space with a large wall and projector. The seat to play was always occupied by someone. So I would say maybe 3 - 5 people played the whole game every hour, and there were 4 seats behind for anyone that wanted to watch. At the end of the first day, we also had a performance of the game where Sivani would read the poem out loud, and I would play it. We hooked up some synthesizers to play live noise music during the end poem section. Our friend [Kaho](https://www.kahoabe.net/) also helped out with controlling the game while we messed around on the instruments. I was inspired to do this after seeing a [playformance](https://www.souslesneons.com/playformance/en/) in Barcelona by art collective [Sous les Néons](https://www.souslesneons.com/fr/) as well as seeing [Qualia](https://2026.amaze-berlin.de/performances/) (Philip Wölk & Moshe Linke) perform at A MAZE Berlin this year. The whole performance was a lot of fun, and I think added a nice creative twist to the event. I was really happy that the organizers allowed me to do this with short notice. There was a decent sized audience too (since there was also a talk event happening after). You can watch the full performance [here](https://youtu.be/qn8DX6MlqoI).

<img  src="/dissonance/performance-2.jpeg"/>

On the last day of the event I was interviewed by Fuji TV. A lot of the questions seemed to be framed around a Japanese context of how the game is experienced. I forgot my answers, but I remember steering away from trying to make any broad generalizations or interpretations of how a Japanese audience played it. I just hope that nothing got lost in translation or used to build a negative narrative I didn't agree to. I don't know much about television in Japan other than NHK which seems like the chill PBS style educational broadcasting. I believe Fuji TV is a private broadcasting service focused more on entertainment. Will look into finding the episode of the show it aired on.

I want to thank [futurala](https://x.com/yasukiwatanabe) and [.iris](https://x.com/thisisdotiris) for organizing such a thoughtful event and letting me be part of it in such a big way. And thanks to all exhibitors that showed their unique games that keep me inspired, and all the attendees for supporting the event.



