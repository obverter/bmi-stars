# BMI-Stars

To the casual observer, baseball isn’t an impressive sport. There’s lots of standing around. Games can sometimes take five hours. And the action — if or whenever any occurs — is over in a few seconds.

Further influencing the sport’s non-athletic perception is the truth that many — if not most — professional baseball players don’t look like freakish athletes. When a non-baseball enthusiast asks me about the game, one comment often surfaces in some form or another:

Why are these guys millionaires? None of what they’re doing looks difficult. And it looks like some of these guys are in worse shape than me.

And even as someone who’s spent about thirty years studying the game — that perception tracks.

Compare these bodies:

![bmi_comparison](/Users/bean/Dropbox/code/_projects/baseball/bmi-stars/images/bmi_comparison.png)

Everyone would agree that at least one of these people is in stupendous shape. But if you said I’d win twenty bucks if I could correctly identify which (if any) of these folks were professional athletes — I might not pick the guys on sides.

> !From left to right, these folks are Prince Fielder, Antonio Brown, and Cecil Fielder. Prince and his dad, Cecil, were big stars in the MLB. Antonio Brown is and/or was an NFL superstar — depending on the week, alignment of the planets, or some other catalyst that the universe has yet to discern.

## Baseball Players Come in One Shapes and Sizes

One of the wonderful things about baseball is that there are about an eleventy-zillion different ways to quantify what’s going on during a game. And since 1871, folks have been tabulating and aggregating an enormous amount of data about the game, organizing it, and offering it up for baseball fans to digest.

Height and weight are among the metrics that we know for over 99% of all ballplayers.

<iframe title="Here's How Every MLB Player in History Shapes Up" aria-label="Table" id="datawrapper-chart-kyZDp" src="https://datawrapper.dwcdn.net/kyZDp/1/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="376"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(e){if(void 0!==e.data["datawrapper-height"]){var t=document.querySelectorAll("iframe");for(var a in e.data["datawrapper-height"])for(var r=0;r<t.length;r++){if(t[r].contentWindow===e.source)t[r].style.height=e.data["datawrapper-height"][a]+"px"}}}))}();
</script>

But in a sport where plenty of the players in its pantheon look sort of like this:

![babe_ruth](/Users/bean/Dropbox/code/_projects/baseball/bmi-stars/images/babe_ruth.jpeg)

An itchy question begins to instantiate itself about one inch behind my forehead.

*How terrible would the all-time highest-BMI team really be?*

### Caveat: BMI is a blunt scalpel

Before we go further, I’ve gotta take a moment to front-load some caveats about body mass index (BMI) before I start throwing the term around in analysis.

Foremost, body mass index (BMI) by itself is a terrible indicator. Here’s how you’d describe it pythonically:

```python
body[‘BMI’] == body[‘weight_in_KG’] / body[‘height_in_meters’] ** 2
```

Ostensibly, mass-to-height ratio that’s useful when broadly classifying a person as underweight, normal weight, overweight, or obese. For nutritionists, trainers, and doctors, BMI can be a facet of an overall snapshot of a person’s health.

But because BMI is ignorant of body composition, it’s not a great barometer for whether someone’s in shape. 

Here's a picture of Arnold Schwarzenegger in 1974 — the year he won his fifth Mr. Olympia.

![Arnold_Schwarzenegger_1974_32.1](/Users/bean/Dropbox/code/_projects/baseball/bmi-stars/images/Arnold_Schwarzenegger_1974_32.1.jpeg)

At the time of this photo, his BMI was around 32.

And just so we're clear: any BMI over 30 is classified as some flavor of obese.

So when I talk about BMI, know that I’m using it with other sprint-speed related statistics to quickly filter for baseball players that are probably of the specific body type that I'm trying to find. Past that, I’m looking at pictures of our candidates to help make a final determination of whether a player’s body looks more like Arnold Schwarzenegger’s or more like me.

Basically: I’m interested in assembling a roster of me-types and then seeing how they’d stack up. I’m not here to single out any of these champions in the pejorative.

## Selection Process

### Roster Construction

Without getting into the weeds, let’s agree that a modern baseball roster comprises 26 players — 13 pitchers and 13 not-pitchers.

[^1]: For a long time, rosters were capped at 25 people during the first five months of the regular season — after which they’d expand to 40 people through the end of the playoffs. During World War I, the Great Depression, and World War II, rosters were exactly 24 people. Before then, it was “up to 25”. Since 2020, rosters have been set at 26, and then expanded to 28 from August 1.

  For pitchers, teams generally carry five starting pitchers and seven relief pitchers who are brought into games at opportune moments, or when the starting pitcher is worn out, or when the current pitcher starts throwing batting practice to the other team.

For not-pitchers, most rosters include:

- Two catchers.
- Five outfielders.
- One each of Shortstop and First, Second, and Third Basemen.
- Two utility players, who can do a lot of things decently well.

So if I’m looking to fill a 26-person roster of the least-athletic-looking players out of the 20,000-odd people who have played professional baseball during the last ~150 years, I need to come up with a height/weight/BMI filter to apply to the entire set of players that will yield the smallest subset of players such that I can fill employ enough high-weight-low-height players at every position on the roster.

### Filter 99th BMI, 25th height

After some noodling, I ended up finding that filtering the set of all players for 99th weight and 25th height yielded this result:

<iframe title="Open Tryouts for the Wonkaville Huskies" aria-label="Scatter Plot" id="datawrapper-chart-TQbiM" src="https://datawrapper.dwcdn.net/TQbiM/1/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="600"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(e){if(void 0!==e.data["datawrapper-height"]){var t=document.querySelectorAll("iframe");for(var a in e.data["datawrapper-height"])for(var r=0;r<t.length;r++){if(t[r].contentWindow===e.source)t[r].style.height=e.data["datawrapper-height"][a]+"px"}}}))}();
</script>

From these, grouping players by position and sorting by descending weight yields this as the inaugural roster of the Wonkaville Huskies.

<iframe title="The 2022 Wonkaville Huskies" aria-label="Table" id="datawrapper-chart-tvkRI" src="https://datawrapper.dwcdn.net/tvkRI/1/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="1134"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(e){if(void 0!==e.data["datawrapper-height"]){var t=document.querySelectorAll("iframe");for(var a in e.data["datawrapper-height"])for(var r=0;r<t.length;r++){if(t[r].contentWindow===e.source)t[r].style.height=e.data["datawrapper-height"][a]+"px"}}}))}();
</script>

### And here's how they compare to our aforementioned 20,000-player historical means.

<iframe title="This is What Peak Performance Looks Like" aria-label="Range Plot" id="datawrapper-chart-jDZzI" src="https://datawrapper.dwcdn.net/jDZzI/1/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="146"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(e){if(void 0!==e.data["datawrapper-height"]){var t=document.querySelectorAll("iframe");for(var a in e.data["datawrapper-height"])for(var r=0;r<t.length;r++){if(t[r].contentWindow===e.source)t[r].style.height=e.data["datawrapper-height"][a]+"px"}}}))}();
</script>

<iframe title="The Lightest Husky is Heavier Than MLB's Historical Mean" aria-label="Range Plot" id="datawrapper-chart-Vud7Q" src="https://datawrapper.dwcdn.net/Vud7Q/1/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="119"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(e){if(void 0!==e.data["datawrapper-height"]){var t=document.querySelectorAll("iframe");for(var a in e.data["datawrapper-height"])for(var r=0;r<t.length;r++){if(t[r].contentWindow===e.source)t[r].style.height=e.data["datawrapper-height"][a]+"px"}}}))}();
</script>

<iframe title="Pro Baseball Players Are Roughly the Same Size" aria-label="Stacked Bars" id="datawrapper-chart-1ILqv" src="https://datawrapper.dwcdn.net/1ILqv/2/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="469"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(e){if(void 0!==e.data["datawrapper-height"]){var t=document.querySelectorAll("iframe");for(var a in e.data["datawrapper-height"])for(var r=0;r<t.length;r++){if(t[r].contentWindow===e.source)t[r].style.height=e.data["datawrapper-height"][a]+"px"}}}))}();
</script>

Alright. So now we've got our roster.

How good is this team?

## WAR — What is it good for? Absolutely Everything.

When you start any sort of comparative analysis between baseball players, the good news is that you’ve got about a zillion ways to see how they measure up. Some of these are super simple.

> How many homers did someone hit in a given time period?

And some of these are not simple:

```latex
SIERA = 6.145 - (16.986\times\frac{SO}{PA}) + (11.434\times\frac{BB}{PA}) - 1.858\times\frac{GB - FB - PU}{PA} + 7.653\times\frac{SO}{PA}{^2} \pm 6.664\times\frac{GB - FB - PU}{PA}{^2} + 10.130\times\frac{SO}{PA} \times\frac{GB - FB - PU}{PA} - 5.195 \times \frac{BB}{PA} \times \frac{GB - FB - PU}{PA}
```



There are, however, a few specific shiny, golden metrics that cut through much of the statistical noise and simply quantify a player’s value relative to their contemporaries.

For our analysis, we’ll be relying on one of these: **Wins Above Replacement (WAR)**
### WAR Defined

WAR measures the totality of a player’s value across all aspects of the game by quantifying how many more wins they’re worth compared to a replacement-level player at his same position.

Replacement-level players can be thought of as folks like Minor Leaguers who are still trying to make a Major League roster, or a journeyman free agent who’s better than nothing, but not by much.

To be even more reductive, think of replacement-level players as extras in a movie. Yeah, they’re there — and you notice if they weren’t. But at the same time, if you notice them at all, then something’s probably wrong.

WAR is adjusted for position, too. Some positions on the field — often referred to as “premium positions” — are comparatively more difficult to play than others. The premium positions are:

- Catcher
- Shortstop
- Center field

And since it’s much harder to play these positions, team owners are happy to employ folks that might not hit the ball as well as, say, First Baseman — who don’t need to be ~gymnasts in order to play great defense.

### Why WAR is Great in One Example or Less

Here are two Hall of Famers:

<iframe title="In Professional Baseball, Size Isn't Everything" aria-label="Table" id="datawrapper-chart-GOfCX" src="https://datawrapper.dwcdn.net/GOfCX/1/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="338"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(e){if(void 0!==e.data["datawrapper-height"]){var t=document.querySelectorAll("iframe");for(var a in e.data["datawrapper-height"])for(var r=0;r<t.length;r++){if(t[r].contentWindow===e.source)t[r].style.height=e.data["datawrapper-height"][a]+"px"}}}))}();
</script>

Dan Brouthers was a big, powerful guy who hit very well. But he played First Base. And not very well. His success was earned almost entirely with his bat.

Ozzie Smith is the greatest defensive shortstop that professional baseball has ever seen. Nobody really cared about whether he hit the ball. Which is handy for Ozzie — because he sure couldn’t hit.

### Pitchers and Batters Can Both Be Described with WAR

Pitchers don’t hit.

This isn’t true, but it’s near to the truth — speaking both literally and figuratively.

[^2]: There are exceptions to this generalization, but for now we’re going to ignore Mr. Ruth and Mr. Ohtani et al. and agree that it’s reasonable to say that pitchers’ value doesn’t hinge on how well they swing the bat.

But it’s not all bad news.

We can still calculate WAR for pitchers, and the resultant numbers are just as valid as any calculation for any batter.

In sum: WAR is simple.

If I’ve got a WAR of 1, then it’s reasonable to say that out of my team’s 162-game season, one of those wins is because of my contributions in the aggregate. Had an ‘extra’ been wearing my uniform, playing my position, and taking my at-bats — the team would’ve won one fewer game over the course of the season.

## So How 'Bout Them Huskies?

So! Here are the Wonkaville Huskies.

[^3]: Or *WARriors*, as they were nearly named.

[[huskies WAR]]

Are you surprised? I was surprised.

Having gone into this assuming that I’d end up with a roster of folks that didn’t really amount to much over the course of their probably-brief Major League careers, it surprised me to find that this team is...

**Not bad!**

Actually, it’s *better* than not-bad.

Hell, they're better than average.

### Yes, But How Good Are They?

They're about this good:

<iframe title="The Huskies Are Actually Not That Bad" aria-label="Table" id="datawrapper-chart-tezgG" src="https://datawrapper.dwcdn.net/tezgG/2/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="1170"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(e){if(void 0!==e.data["datawrapper-height"]){var t=document.querySelectorAll("iframe");for(var a in e.data["datawrapper-height"])for(var r=0;r<t.length;r++){if(t[r].contentWindow===e.source)t[r].style.height=e.data["datawrapper-height"][a]+"px"}}}))}();
</script>

### Finding an analogue: The 1995 Seattle Mariners

In fact, if we’re searching for an analogous historical team that produced similar numbers, our Huskies are about as good as the **1995 Seattle Mariners**, who won 79 games and finished first in their division.

### You're Making This Up

In order to search for and compare our Huskies and the ‘95 Mariners, I made a few assumptions:

1. For each Husky, I set their stats at Baseball Reference’s 162-game average, which is a statistically sound quantification of what you statistics you could expect from that player in a hypothetical 162-game season. They derive these numbers from the player’s historical performances.
2. While most players’ performance over the course of their career looks something like a normal distribution, a significant minority have had careers that started or finished extremely strong — and normalizing for the presence and/or severity of this sort of deviation is beyond what we’re looking at, here.

### Fine. They're the 1995 Mariners. But How 1995-Marinersy Are They?

They're about this Marinersy:

<iframe title="The 2022 Huskies Won the American League West in 1995" aria-label="Table" id="datawrapper-chart-7N0fL" src="https://datawrapper.dwcdn.net/7N0fL/1/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="268"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(e){if(void 0!==e.data["datawrapper-height"]){var t=document.querySelectorAll("iframe");for(var a in e.data["datawrapper-height"])for(var r=0;r<t.length;r++){if(t[r].contentWindow===e.source)t[r].style.height=e.data["datawrapper-height"][a]+"px"}}}))}();
</script>

## Extrapolating Away from Reason

In the future, I’ll revisit this article and simulate the Huskies’ season. But since we have an analogue handy in the 1995 Mariners, let’s look at how these Faux-Huskies compare to some historically good and bad teams.

<iframe title="The Huskies Are a Lot Better Than Bad" aria-label="Interactive line chart" id="datawrapper-chart-Fr56a" src="https://datawrapper.dwcdn.net/Fr56a/1/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="400"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(e){if(void 0!==e.data["datawrapper-height"]){var t=document.querySelectorAll("iframe");for(var a in e.data["datawrapper-height"])for(var r=0;r<t.length;r++){if(t[r].contentWindow===e.source)t[r].style.height=e.data["datawrapper-height"][a]+"px"}}}))}();
</script>

The 2001 Seattle Mariners won 116 games and then shat the bed in the first round of the playoffs. But that team's single-season wins record still stands.

It has been said that the 2003 Tigers were mathematically eliminated from the playoffs in late April — which is about one-sixth of the way through the season.

This isn’t true. But on a gut-level, it isn’t not true. Those Tigers were bad, bad, bad.

## Wrap-up

So what did we learn today?

In truth, not much.

We already know that BMI is nigh-useless in a vacuum.

Also, we know that baseball is asynchronously balanced in myriad ways. The game needs in equal parts fast players and powerful players. And just as much as it needs outfielders who can throw a baseball into a shopping cart from 300 feet away, it needs steely nerved, crocodile-blooded pitchers who can mow down the heart of a lineup without breaking a sweat. And also it needs First Basemen.

And since we’re sifting through some 20,000 players — some of whom had careers lasting over two decades, and some of whom had careers lasting less than two hours — the fact that we’re able to fill a decent roster with the largest guys we can find shouldn’t be a surprise.

Because baseball is as self-selective as it is fickle. 

“What have you done for me lately?” is the first and last question in a Major League front office.

And if the answer is “not much,” then you can see yourself out.

In that way, anyone who made this roster is already probably good enough to play pro ball — regardless of what they look like.

Except Edwar Colina.

Poor guy got shelled in his debut and was out of the league the next day.