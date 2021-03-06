# Tennison : 45 points
[See Online](https://www.facebook.com/hackercup/problems.php?pid=373965339404375&round=598486203541358)

[Download Input File](https://www.facebook.com/hackercup/problems.php?pid=373965339404375&round=598486203541358#)

You may be familiar with the works of Alfred Lord Tennyson, the famous English
poet. In this problem we will concern ourselves with Tennison, the less famous
English tennis player. As you know, tennis is not so much a game of skill as a
game of luck and weather patterns. The goal of tennis is to win **K** sets
before the other player. However, the chance of winning a set is largely
dependent on whether or not there is weather.

Tennison plays best when it's sunny, but sometimes of course, it rains. Tennison
wins a set with probability p<sub>s</sub> when it's sunny, and with probability
p<sub>r</sub> when it's raining. The chance that there will be sun for the first
set is p<sub>i</sub>. Luckily for Tennison, whenever he wins a set, the
probability that there will be sun increases by p<sub>u</sub> with probability
p<sub>w</sub>. Unfortunately, when Tennison loses a set, the probability of sun
decreases by p<sub>d</sub> with probability p<sub>l</sub>. What is the chance
that Tennison will be successful in his match?

Rain and sun are the only weather conditions, so P(rain) = 1 - P(sun) at all
times. Also, probabilities always stay in the range [0, 1]. If P(sun) would ever
be less than 0, it is instead 0. If it would ever be greater than 1, it is
instead 1.

## Input
Input begins with an integer **T**, the number of tennis matches that Tennison
plays. For each match, there is a line containing an integer **K**, followed by
the probabilities p<sub>s</sub>, p<sub>r</sub>, p<sub>i</sub>, p<sub>u</sub>,
p<sub>w</sub>, p<sub>d</sub>, p<sub>l</sub> in that order. All of these values
are given with exactly three places after the decimal point.

## Output
For each match, output "Case #i: " followed by the probability that Tennison
wins the match, rounded to 6 decimal places (quotes for clarity only). It is
guaranteed that the output is unaffected by deviations as large as 10<sup>-8</sup>.

## Constraints
 * 1 ≤ **T** ≤ 100
 * 1 ≤ **K** ≤ 100
 * 0 ≤ **p<sub>s</sub>, p<sub>r</sub>, p<sub>i</sub>, p<sub>u</sub>, p<sub>w</sub>, p<sub>d</sub>, p<sub>l</sub>** ≤ 1
 * **p<sub>s</sub>** > **p<sub>r</sub>**

### Example input · Download
    5
    1 0.800 0.100 0.500 0.500 0.500 0.500 0.500
    2 0.600 0.200 0.500 0.100 1.000 0.100 1.000
    1 1.000 0.000 1.000 1.000 1.000 1.000 1.000
    25 0.984 0.222 0.993 0.336 0.207 0.084 0.478
    58 0.472 0.182 0.418 0.097 0.569 0.816 0.711

### Example output · Download
    Case #1: 0.450000
    Case #2: 0.352000
    Case #3: 1.000000
    Case #4: 0.999956
    Case #5: 0.000000
