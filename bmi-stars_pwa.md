BMI-Stars
To the casual observer, baseball isn’t an impressive sport. There’s lots of standing around. Games can sometimes take five hours. And the action — if or whenever any occurs — is over in a few seconds.
Further influencing the sport’s non-athletic perception is the truth that many — if not most — professional baseball players don’t look like freakish athletes. When a non-baseball enthusiast asks me about the game, one comment often surfaces in some form or another:
Why are these guys millionaires? None of what they’re doing looks difficult. And it looks like some of these guys are in worse shape than me.
And even as someone who’s spent about thirty years studying the game — that perception tracks.
Compare these bodies:
[[image: Fielders + AB]]
Everyone would agree that at least one of these people is in great shape. But if you said I’d win twenty bucks if I could correctly identify which (if any) of these folks were professional athletes — I might not pick the guys on sides.
(From left to right, these folks are Prince Fielder, Antonio Brown, and Cecil Fielder. Prince and his dad, Cecil, were big stars in the MLB. Antonio Brown is and/or was an NFL superstar — depending on the week, alignment of the planets, or some other catalyst that the universe has yet to discern.)
Overview of baseball players’ size
One of the wonderful things about baseball is that there are about an eleventy-zillion different ways to quantify what’s going on during a game. And since 1871, folks have been tabulating and aggregating an enormous amount of data about the game, organizing it, and offering it up for baseball fans to digest.
Height and weight are among the metrics that we know for over 99% of all ballplayers.
[[everyone height and weight table]]
But in a sport where plenty of the players in its pantheon look sort of like this:
[[babe ruth]]
And some of its most spectacular statistical failures involve folks who look like this:
An itchy instantiates itself about one inch behind my forehead.
How terrible would the all-time highest-BMI team really be?
Caveat: BMI is a blunt scalpel
Before we go further, I’ve gotta take a moment to front-load some caveats about body mass index (BMI) before I start throwing the term around in analysis.
Foremost, body mass index (BMI) by itself is a terrible indicator. Here’s how you’d describe it pythonically:
body[‘BMI’] == body[‘weight_in_KG’] / body[‘height_in_meters’] ** 2
Ostensibly, mass-to-height ratio that’s useful when broadly classifying a person as underweight, normal weight, overweight, or obese. For nutritionists, trainers, and doctors, BMI can be a facet of an overall snapshot of a person’s health.
But because BMI is ignorant of body composition, it’s not a great barometer for whether someone’s in shape. For example, both in men in this picture have a BMI over 40, which the chart on the wall at your doctor’s office might classify as “morbidly obese”

So when I talk about BMI, I’m know that I’m using it with other sprint-speed related statistics to quickly filter for baseball players that are probably of a specific body type. Past that, I’m looking at pictures of our candidates to help make a final determination of whether a player’s body looks more like Arnold Schwarzenegger’s or more like me.
I’m interested in assembling a roster of me-types and then seeing how they’d stack up. I’m not here to single out any of these champions in the pejorative.
Selection Process
Roster Construction
Without getting into the weeds, let’s agree that a modern baseball roster comprises 26 players — 13 pitchers and 13 not-pitchers.
[1]  For a long time, rosters were capped at 25 people during the first five months of the regular season — after which they’d expand to 40 people through the end of the playoffs. During World War I, the Great Depression, and World War II, rosters were exactly 24 people. Before then, it was “up to 25”. Since 2020, rosters have been set at 26, and then expanded to 28 from August 1.
For pitchers, teams generally carry five starting pitchers and seven relief pitchers who are brought into games at opportune moments, or when the starting pitcher is worn out, or when the current pitcher starts throwing batting practice to the other team.
For not-pitchers, most rosters include:
Two catchers.
Five outfielders.
One each of Shortstop and First-, Second-, and Third-basemen.
Two utility players, who can do a lot of things decently well.
So if I’m looking to fill a 26-person roster of the least-athletic-looking players out of the 20,000-odd people who have played professional baseball during the last ~150 years, I need to find a height/weight/BMI filter to apply to the entire set of players that will yield the smallest subset of players such that I can fill employ enough players at every position on the roster.
Filter 99th BMI, 25th height
After some noodling, I ended up finding that filtering the set of all players for 99th weight and 25th height yielded this result:
[[Tryouts table]]
Sort by weight, cut
From these, grouping players by position and sorting by descending weight yields this as the inaugural roster of the Wonkaville Huskies.
WAR — What is it good for? Absolutely Everything.
When you start any sort of comparative analysis between baseball players, the good news is that you’ve got about a zillion ways to see how they measure up. Some of these are super simple.
How many homers did someone hit in a given time period?
And some of these are not simple:
SIERA = 6.145 - (16.986 * (SO/PA)) + (11.434 * (BB/PA)) - (1.858 * ((GB - FB - PU) / PA)) + (7.653 8 ((SO / PA) ** 2)) +/- (6.664 * (((GB - FB - PU) / PA) ** 2)) + (10.130 * (SO / PA) * ((GB - FB - PU) / PA)) - 5.195 * (BB / PA) * ((GB - FB - PU) / PA)
There are, however, a few specific shiny, golden metrics that cut through much of the statistical noise and simply quantify a player’s value relative to their contemporaries.
For our analysis, we’ll be relying on one of these: Wins Above Replacement (WAR)
Breakdown WAR
WAR measures the totality of a player’s value across all aspects of the game by quantifying how many more wins they’re worth compared to a replacement-level player at his same position.
Replacement-level players can be thought of as folks like Minor Leaguers who are still trying to make a Major League roster, or a journeyman free agent who’s better than nothing, but not by much.
To be even more reductive, think of replacement-level players as extras in a movie. Yeah, they’re there — and you notice if they weren’t. But at the same time, if you notice them at all, then something’s probably wrong.
WAR is adjusted for position, too. Some positions on the field — often referred to as “premium positions” — are comparatively more difficult to play than others. The premium positions are:
Catcher
Shortstop
Center field
And since it’s much harder to play these positions, team owners are happy to employ folks that might not hit the ball as well as, say, a First Baseman — who don’t need to be ~gymnasts in order to play great defense.
Show different players with same WAR
Here are two Hall of Famers:
[[brouthers/smith]]
Dan Brouthers was a big, powerful guy who hit very well. But he played First Base. And not very well. His success was earned almost entirely with his bat.
Ozzie Smith is the greatest defensive shortstop that professional baseball has ever seen. Nobody really cared about whether he hit the ball. Which is handy for Ozzie — because he sure couldn’t hit.
Pitchers and Batters Can Both Be Described with WAR
Pitchers don’t hit.
This isn’t true, but it’s near to the truth — speaking both literally and figuratively.
There are exceptions to this generalization, but for now we’re going to ignore Mr. Ruth and Mr. Ohtani et al. and agree that it’s reasonable to say that pitchers’ value doesn’t hinge on how well they swing the bat.
But it’s not all bad news.
We can still calculate WAR for pitchers, and the resultant numbers are just as valid as any calculation for any batter.
In sum: WAR is simple.
If I’ve got a WAR of 1, then it’s reasonable to say that out of my team’s 162-game season, one of those wins is because of my contributions in the aggregate. Had an ‘extra’ been wearing my uniform, playing my position, and taking my at-bats — the team would’ve won one fewer game over the course of the season.
Show Huskies WAR
So! Here are the Wonkaville Huskies. Or WARriors, as I almost named them.
[[huskies WAR]]
Are you surprised? I was surprised.
Having gone into this assuming that I’d end up with a roster of folks that didn’t really amount to much over the course of their probably brief baseball careers, it surprised me to find that this team is...
Not bad!
Actually, it’s better than not-bad.
Hell, it’s better than average.
How the Huskies Compare to All-time, League-wide Historical Means
Finding an analogue: The 1995 Seattle Mariners
In fact, if we’re searching for an analogous historical team that produced similar numbers, our Huskies are about as good as the 1995 Seattle Mariners, who won 79 games and finished first in their division.
Explain bbref 162-avg
In order to search for and compare our Huskies and the ‘95 Mariners, I made a few assumptions:
For each Husky, I set their stats at Baseball Reference’s 162-game average, which is a statistically sound quantification of what you statistics you could expect from that player in a hypothetical 162-game season. They derive these numbers from the player’s historical performances.
While most players’ performance over the course of their career looks something like a normal distribution, a significant minority have had careers that started or finished extremely strong — and normalizing for the presence and/or severity of this sort of deviation is beyond what we’re looking at, here.
Compare Huskies :: ‘95 Mariners

WAR, OPS+, ERA+

Compare “Huskies” to historically good/poor teams
In the future, I’ll revisit this article and simulate the Huskies’ season. But since we have an analogue handy in the 1995 Mariners, let’s look at how these Faux-Huskies compare to some historically good and bad teams.
The 2001 Seattle Mariners won 116 games and then shat the bed in the first round of the playoffs. But their single-season wins record still stands.
It has been said that the 1962 Mets were mathematically eliminated from the playoffs in late April — which is about one-sixth of the way through the season.
This isn’t true. But on a gut-level, it isn’t not true. Those Mets were bad, bad, bad.
Wrap-up
So what did we learn today?
In truth, not much.
We already know that BMI is nigh-useless in a vacuum.
Also, we know that baseball is asynchronously balanced in myriad ways. The game needs in equal parts fast players and powerful players, reactive improvizationalists and steely nerved, crocodile-blooded players, and also First Basemen.
And since we’re sifting through some 20,000 players — some of whom had careers lasting over two decades, and some of whom had careers lasting less than two hours — the fact that we’re able to fill a decent roster with the largest guys we can find shouldn’t be a surprise.
Because baseball is as self-selective as it is fickle. When considering baseball contracts, “What have you done for me lately?” is the first and last question. And if the answer in response is “not much,” then there’s the door.
In that way, anyone who made this roster is already probably good enough to play pro ball — regardless of what they look like.
Except Edwar Colina.
Poor guy got shelled in his debut and was out of the league the next day.