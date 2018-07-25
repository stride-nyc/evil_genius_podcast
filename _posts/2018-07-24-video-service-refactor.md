---
layout: default
title:  "Video Service Refactor: Part 1"
date:   2018-07-24
categories: episodes
excerpt: "We go line by line with Martin Fowler"
---

# Video Service Refactor: Part 1

<iframe style="border: none" src="//html5-player.libsyn.com/embed/episode/id/6846815/height/90/theme/custom/autoplay/no/autonext/no/thumbnail/yes/preload/no/no_addthis/no/direction/forward/render-playlist/no/custom-color/000000/" height="90" width="100%" scrolling="no"  allowfullscreen webkitallowfullscreen mozallowfullscreen oallowfullscreen msallowfullscreen></iframe>


- Introducing… a new problem! We talk about how Emmanuel ran across this problem. [**Martin Fowler's blog post**](https://martinfowler.com/articles/refactoring-external-service.html)
- We talk about the problem itself: What is an external service?
- We dive into the code

## Commits

- [**Add description of functionality**](https://github.com/stride-nyc/evil_genius_podcast_exercises/commit/50936a97682499d713c5d071eaaaffede8abba1a#diff-4c208c099901f939b08c104d82f72e60)
  - Commenting the heck out of this code.

- [**Note where external services are being used to potentially mock out**](https://github.com/stride-nyc/evil_genius_podcast_exercises/commit/67b206820e5571329e9458e22d8d8a1d29d80789#diff-4c208c099901f939b08c104d82f72e60)
  - What makes this stuff an "external service" ?

- [**Use Minitest so that I can stub**](https://github.com/stride-nyc/evil_genius_podcast_exercises/commit/378111784790c0d6882db132e599787985c7016d#diff-4c208c099901f939b08c104d82f72e60)
  - Why minitest over test unit?

- [**Remove unnecessary comments. Stub out method that loads up video list**](https://github.com/stride-nyc/evil_genius_podcast_exercises/commit/5a1e53792e0ad95b14350e24a043d1d36696349b#diff-4c208c099901f939b08c104d82f72e60)
  - Why is `@video_list` an ivar?

- [**Extract external service dependencies into method calls, get first real test**](https://github.com/stride-nyc/evil_genius_podcast_exercises/commit/c2fe51c5dffa0efa5d2cb84a66ec555473146692#diff-4c208c099901f939b08c104d82f72e60)
  - Why doesn't `get_current_video_list` method get its own test?

- [**Extract getting the current list into its own object that is injected**](https://github.com/stride-nyc/evil_genius_podcast_exercises/commit/625667c365b050293fbdf8b99154f2617bbf1f45#diff-4c208c099901f939b08c104d82f72e60)
  - Introduction of new object! How did you decide to name this VideoRepo and make it responsible for parsing the json?
