# Santa_2020_Jehan
My submission to the Santa 2020 - The Candy Cane Contest Kaggle Competition
https://www.kaggle.com/c/santa-2020/



I've added a bunch of algorithms here
The TS and UCB were copied from some pretty useful startercode notebooks uploeaded by other people in the competition.

I've adapted them otherwise to produce greedy, e-greedy, D-UCB and even a D-linear UCB (the linear algebra with this one was a lot of fun).

So far, the Thompson Sampling (slightly adapted to have a discount factor) from https://www.kaggle.com/ilialar/simple-multi-armed-bandit
seems to play the best!



D-Linear UCB I found here:
https://arxiv.org/pdf/0805.3415.pdf
It's still non-contextual (we don't have any contextual info), so really it was more just a matter of implementing it for fun, than it was for actually using it.

I also added a fun little ensemble, thinking that an early run of greedy might give normal TS a little boost near the end! 
I got the idea from this paper here: 

https://arxiv.org/pdf/2002.10121.pdf
(The Unreasonable Effectiveness of Greedy Algorithms inMulti-Armed Bandit with Many Arms)

I tested how greedy performs as opposed to TS and up until about 50-75 rounds, greedy does better (makes sense if you think about it)
But it was of no avail, unfortunately. Although it did better in the beginning, regular TS outperformed it at every turn. I never could figure out why this was!



Further research:
I could also implement Sliding-Window UCB and see how that fares, or learn more about tuning UCB to specific situations
I could also implement D-Randomized-Linear UCB but I do not believe it will perform better than Thompson Sampling.
Maybe there's some ingenious idea that I didn't think of - maybe there *are* contextual features I haven't considered, or perhaps I didn't tune my hyperparams for UCB/e-greedy enough
MAYBE there's even a way to capture prior information about the arms that I haven't considered! (although I'm guessing not - it makes more sense to randomize the true arm distributions)

Either way, this was fun!
Highly recommend. 10/10


