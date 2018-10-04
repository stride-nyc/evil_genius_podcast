---
layout: default
title:  "A First Example Part 1"
date:   2018-09-19
categories: episodes
excerpt: "We go into the Refactoring book and try our hand at a first example."
---

# A First Example Part 1
<iframe style="border: none" src="//html5-player.libsyn.com/embed/episode/id/7111261/height/90/theme/custom/autoplay/no/autonext/no/thumbnail/yes/preload/no/no_addthis/no/direction/forward/render-playlist/no/custom-color/000000/" height="90" width="100%" scrolling="no"  allowfullscreen webkitallowfullscreen mozallowfullscreen oallowfullscreen msallowfullscreen></iframe>

## Talking Points

- Present the problem
- You have to add tests. Assume that the application works as is; change no current behavior

## Commits

- [**Add test cases for statement method**](https://github.com/stride-nyc/evil_genius_podcast_exercises/commit/7a45e9baff1e3e67b6ba28d87fc62600389a1011)
  - What did you add that wasn’t in the book?
  - Curious. Why did you choose minitest over rspec?
  - I'm noticing some patterns.
    - In #setup, you create your Customer and 3 instances of Movie. #setup is the only place that directly class those classes.
    - Later, you use @joe in every single test. Cool. You then pass a movie object to the Rental on the first line -- for example: Rental.new(@child_movie, 3) and then add the rental to @joe.
  - Each test calls #add_rental then looks at @joe.statement.
    - How do you feel about this? Is it a good test pattern to call one method (#add_rental) and test its correctness by calling another method (#statement)?
  - What do the test names mean? test_2day_new_4day_child_3day_reg
  - Can you summarize the objects here and their responsibilities?
- [**add notes from book stating the problem**](https://github.com/stride-nyc/evil_genius_podcast_exercises/commit/cece5872ac35a32ab41fdd04def53ae3201cbdd9)
  - Can you summarize for our listeners?
