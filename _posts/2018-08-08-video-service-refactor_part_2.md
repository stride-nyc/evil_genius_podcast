---
layout: default
title:  "Video Service Refactor: Part 2"
date:   2018-08-08
categories: episodes
excerpt: "More lines with Martin"
---
# Video Service Refactor: Part 2

<iframe style="border: none" src="//html5-player.libsyn.com/embed/episode/id/6895251/height/90/theme/custom/autoplay/no/autonext/no/thumbnail/yes/preload/no/no_addthis/no/direction/forward/render-playlist/no/custom-color/000000/" height="90" width="100%" scrolling="no"  allowfullscreen webkitallowfullscreen mozallowfullscreen oallowfullscreen msallowfullscreen></iframe>

## Talking Points

- What is the difference between mocks and stubs?
- Dependency injection allows you to test your functionality more thoroughly
- Refactoring next steps

## Commits

- [**Use YoutubVideoClient to abstract away talking to youtube**](https://github.com/stride-nyc/evil_genius_podcast_exercises/commit/7551b8d7ce5275fe506a8a5540bbbe1cceb47c57#diff-4c208c099901f939b08c104d82f72e60)
- [**Update test to use YoutubeVideoClientMock**](https://github.com/stride-nyc/evil_genius_podcast_exercises/commit/d6f75bf874a2b295e1b7b5fe8b1c754d48b7c7e3#diff-4c208c099901f939b08c104d82f72e60)
- [**Change TestStubs to Stubs**](https://github.com/stride-nyc/evil_genius_podcast_exercises/commit/7f05d312db498811d95ca0d70e6c7773922ef8cc)
- [**Make TestStubs able to return test specific canned responses**](https://github.com/stride-nyc/evil_genius_podcast_exercises/commit/abbf9cbe64c9b934d4738b8fc09376a9f44c0fea#diff-4c208c099901f939b08c104d82f72e60)
- [**Clean up and rename initial test**](https://github.com/stride-nyc/evil_genius_podcast_exercises/commit/72de92f8adfc52e212bbf965ac616b1c10f50101#diff-4c208c099901f939b08c104d82f72e60)
- [**Add another test case for when video has been published for less than 30 days**](https://github.com/stride-nyc/evil_genius_podcast_exercises/commit/1d38b335042b941f385c47a7db8e14af43aea2bb#diff-4c208c099901f939b08c104d82f72e60)
- [**Get test with two months since published days to pass, assume fractional views don’t mean anything**](https://github.com/stride-nyc/evil_genius_podcast_exercises/commit/53c30c03e3c7be9c1714482121e3a60f03c4b604#diff-4c208c099901f939b08c104d82f72e60)