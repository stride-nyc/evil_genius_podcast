---
layout: default
title:  "A First Example Part 2"
date:   2018-10-03
categories: episodes
excerpt: "We actually do the refactoring this time."
---

# A First Example Part 2

## Talking Points

- Where do you start the refactoring? What do you do first?
- How do you decide what methods belong where?
- Where do you stop?

## Commits

- [**rename element to rental**](https://github.com/stride-nyc/evil_genius_podcast_exercises/commit/2bb71cf34ad8eebcf80897523b159b3623c7aad6)
  - Why did you choose rental over element?
- [**extract base_cost_of_movie concept**](https://github.com/stride-nyc/evil_genius_podcast_exercises/commit/a17cb0e17c4e38bdbf91df6aee747c4e853fcb80)
  - For our listeners: what did you do here? Why move this into a method?
- [**remove duplicate base_cost_of_movie calls**](https://github.com/stride-nyc/evil_genius_podcast_exercises/commit/2ccc5b58eea9843e3f41d71058a25d35c8aa5cf7)
  - why don't you have to call this in every "when" piece now?
- [**rename method to tell a more accurate story**](https://github.com/stride-nyc/evil_genius_podcast_exercises/commit/1a18543952ea80360fb3aa469bee1ab1aad9d4ef)
  - Can you TOL (tell our listeners) what method you renamed and why rental is more accurate than movie?
- [**extract the #extra_charge_for_rental method**](https://github.com/stride-nyc/evil_genius_podcast_exercises/commit/45081a0bc9a13e4b37bcb0c39f86fd56d9baef07)
  - Why did you have to add a new test? What is being tested here?
  - How is extra_charge_for_rental different in its shape from base_cost_of_rental?
- [**remove duplicate extra_charge_for_rental calls**](https://github.com/stride-nyc/evil_genius_podcast_exercises/commit/c3fa29b1662670d6f57f4cc1ad2caf371d17ac84)
  - why did you add this logic to the case statement inside extra_charge_for_rental instead of somewhere inside statement ?