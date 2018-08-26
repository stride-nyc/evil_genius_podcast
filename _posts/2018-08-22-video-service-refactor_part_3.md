---
layout: default
title:  "Video Service Refactor: Part 3"
date:   2018-08-22
categories: episodes
excerpt: "What did Martin do?"
---
# Video Service Refactor: Part 3
<iframe style="border: none" src="//html5-player.libsyn.com/embed/episode/id/6951448/height/90/theme/custom/autoplay/no/autonext/no/thumbnail/yes/preload/no/no_addthis/no/direction/forward/render-playlist/no/custom-color/000000/" height="90" width="100%" scrolling="no"  allowfullscreen webkitallowfullscreen mozallowfullscreen oallowfullscreen msallowfullscreen></iframe>

## Talking Points

- What did Martin do?
- [Martin Fowler’s refactoring](https://martinfowler.com/articles/refactoring-external-service.html)
- Separating out things:
  - How to access to YouTube's API
  - How YouTube structures its data
  - Domain logic.
  - MF concludes with 4 objects: VideoService (coordinator), Video (domain object), YoutubeGateway (gateway), and YoutubeConnection (connection)
  - EG has 3 objects: VideoService, VideoRepo, YoutubeVideoClient
- MF’s code went from 26 - 54 lines. Discuss when longer = better
- Martin did not include accessing the file as something external to this thing
- The Legacy Code Dilemma:
> When we change code, we should have tests in place. To put tests in place, we often have to change code. [-- Michael Feathers](https://www.amazon.com/gp/product/0131177052?ie=UTF8&tag=martinfowlerc-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0131177052)
- Put Youtube call in a method and then stubbed it out
- Stubbed out Date - Why? Contrast with out EG dealt with Date
- *“Code that needs to change frequently should be separated from code that changes rarely, or simply changes for different reasons”*
- Sequence of named refactorings(extract method, move method, inline method)
- BIT BY BIT
**  > The point here is that by taking small steps, you end up going faster because you don't break anything and thus avoid debugging.
> I created the simplest behavior I could at this point, even though I don't intend to use the gateway's record method eventually, indeed unless I stop for a cup of tea I don't think it will last for half-an-hour.

Humble Object, Youtube Gateway

> I find that a good way to think about this is Eric Evans's notion of [Bounded Context](https://martinfowler.com/bliki/BoundedContext.html). YouTube organizes its data according to its context, while I want to organize mine according to a different one. Code that combines two bounded contexts gets convoluted because it's mixing two separate vocabularies together.



| **Martin**   | **VideoService** | **YoutubeConnection**| **YoutubeGateway** | **Video** |
| ------------ | ---------------- | -------------------- | ------------------ | --------- |
|              | init’d with: nothing <br> methods: <br> `video_list` | init’d with: nothing <br> methods:<br> `list_videos(ids)`        | init’d with: responseJson <br> methods:<br> `item(id)` | init’d with: aHash <br> methods:<br> `to_h`, `youtube_id`, `enrich_with_youtube(youtube_item)` |

| **Emmanuel** | **VideoService**| **YoutubeVideoClient** | **VideoRepo**|
| ------------ | ----------------------- | -------------------- | ------------------ | --------- |
|              | init’d with: `video_repo`, `video_client` <br> methods: <br> `video_list`, `monthlyViews(views, publishing_date)` | init’d with: nothing <br> methods <br> `video_stats(youtube_ids)` | init’d with: nothing <br> methods: <br> `videos`|