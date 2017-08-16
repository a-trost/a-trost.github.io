---
title: "Nearest Monday Problem"
date: 2017-08-16
layout: post
---

Last night at a coding get together with a couple friends I was working on a small problem inside a larger script. I called it finding the “Nearest” Monday, but that’s not exactly it.
Essentially the problem was:
* If today is monday, return today’s date.
* If today is Tuesday through Friday, go /backward/ to the previous Monday and return that date.
* If today is Saturday or Sunday, go /forward/ to the upcoming Monday and return that date.

I set to work on the problem and came up with this pseudo code:
```
# With datetime get the number for the day of the week ('%w')
# (Sun = 0, Mon=1, ...Sat=6)
# If num = 1, return today's date
# If num in range(2,6): today-timedelta(days=(num-(num-1)))
# If num ==6, today+timedelta(days=2)
# If num == 0, today+timedelta(days=1)
```
I really didn’t like the solution for Saturdays or Sundays, but I couldn’t think of much more of an elegant solution because of the awkward rollover from 6 to 0.
Pitching it to friends for cleaning up, they had a couple ideas dealing with modulus, and looking at the entire year and finding the Mondays, and working that way.

Then another friend recommended I take what I have and just use a dictionary, which was definitely the easiest way to go about it. Here’s what I ended up with.
```
DAY_DICT = {0:1, 1:0, 2:-1, 3:-2, 4:-3, 5:-4, 6:2,}
todays_date= datetime.date.today()
days_away = datetime.timedelta(days=DAY_DICT[int(todays_date.strftime('%w'))])
mondays_date = todays_date + days_away
```

A quick solution that would be easy to change if I ever want to start making Fridays round forward.
