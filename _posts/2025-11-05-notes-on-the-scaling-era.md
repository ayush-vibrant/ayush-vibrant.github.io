---
layout: post
title: "Notes on 'The Scaling Era: An Oral History of AI, 2019-2025'"
date: 2025-11-05
categories: ai
---

# Notes on 'The Scaling Era: An Oral History of AI, 2019-2025'

Dwarkesh Patel's oral history captures a pivotal moment in AI development—the era when scaling became the primary driver of progress.

## Key Insights

[Add your notes here]
The core point which is being discussed or raised in this chapter is - (most probably) scaling is the answer to reach AGI.
Scaling is the answer - this conclusion has been reached at from multiple angles. As if, the starting point could be different but at the end they have reached the point that proves scaling is the answer. 
Why?
EpochAI paper -- two-thirds of the gains come from increasing data and compute.
The compute needed to train a leading model is now 10 billion times higher than it was in 2010.
The compute needed to train each frontier model doubled every six months.



# Chapter-2
"_all intelligence is, search over turing machine_"
Another way to say this: intelligence is just trying different algorithms (Turing machines) until you find one that solves your problem.

Turing Machine:
is a theoretical computer which is the mathematical foundation of all computation.
Simple description:
* An infinitely long tape with squares
* A read/write head that can move left or right
* A set of rules: "If you see X, write Y and move left/right"
* That's it!
Key insight: This simple device can compute ANYTHING that any computer can compute - from your iPhone to ChatGPT.

Details:
This was done essentially in order to define what a computer is or what essentially a computation is. If you think about on pen and paper when you add two numbers what you are essentially doing is you are looking at some symbols which are those numbers you are following certain rules you carry one and then you write new symbols that is the addition of those two numbers and then you move on to the next position. That's exactly the algorithmic approach that you follow when you are adding two numbers on pen and paper. This is exactly what the Turing machine does. Essentially it follows a very simple algorithm and the algorithm is something which we defined in the simple description. Now here comes the most interesting part. We are saying that Turing machine can essentially compute anything so long as it is computable. Well what are the things that Turing machine cannot compute? Might be interesting to look into. But essentially we are saying that iPhone to chat GPT or anything that is also a Turing machine but that Turing machine is significantly faster. So intelligences you have a very long tape and you can move right and left and you can keep doing this. You can keep doing this. This is what essentially intelligences. So you keep on applying the Turing machine algorithm to get the answer that you want. 
Think of it like this:

-Each Turing machine is a different program/algorithm
-Intelligence is the process of searching through all possible programs to find the right one
-When you "learn" or "figure something out," you're essentially finding the right algorithm

---
GWERN BRANWEN statements:
1. There is no magic transfer to all tasks. There is no intelligence fluid. It’s just a tremendous number of special cases that we learn and encode in our brains.
2. You can always extract a small solution to a specific problem from any learned model or brain, because all the large brain is doing with the extra compute is finding it.

This defination is essentially proving the _ratant vidya_ model of intelligence right.
By a statement 2, it is saying that all the learning that you are essentially doing or all the understanding that you are essentially doing, sort of the reasoning traces that are visible whenever a reasoning model's output is there, sort of saying that those are of no use. If you can build a machine which can learn all the possible cases, it's essentially memorizing there is no derivation there, then that's intelligence. In my gut, I disagree with this because this cannot be intelligence. Back in the day when I was preparing for IIT JEE, the difference between a smart student and a dumb student used to be that both of them have gone through the same material but given a new unseen question, a smart student is able to solve it and a dumb student is not able to solve it. So, wrote memorization cannot be learning. However, their definition of Turing machine or stacking Turing machines is that the smart student theoretically is able to search over a larger spaces of Turing machines and pick the one Turing machine with that particular algorithm which will solve this problem statement but the dumb student is not able to do so. Now, this begs the question, the ability for a smart student to search over a larger space and the inability and the inability of the dumb student to not being able to search over the large space is what is separating them. Now, is it a compute problem that the smart student has more compute, more processing power? No, both of them theoretically have the same brain. So, this definition of stacking Turing machines is not sitting right with me. If it is not sitting right with me, does it mean that the scaling law will not give us AGI? 


---
FRANÇOIS CHOLLET
General intelligence is the ability to approach any problem, any skill, and very quickly master it using very little data. This is what makes you able to face anything you might ever encounter. Generality is not specificity scaled up. It is the ability to apply your mind to anything at all, to arbitrary things. This fundamentally requires the ability to adapt, to learn on the fly
efficiently.

Essentially, I guess he is talking about 1. transfer learning, 2. the same analogy that I gave earlier (smart kid vs dumb kid during jee prep), the ability to learn more from the limited data. That is, general intelligence. And the third point is, the third point is somehow related to Miyamoto Mushashi's quote about the way you do one thing is the way you do everything. As in when you go deep into any one domain, just by the fact that you went deep into a particular domain, you learn a lot of system-2 thinking or meta skills which you can quickly apply to new domain and ramp up yourself quickly in it. Ramping up yourself quickly in it is 1. Ramping yourself up with limited data. 2. If you have a lot of compute, then sure you have faster processors. That is also ramping up quickly. 

---
llms not having tree seach in them. is one of the limitation sthat yan lee cunn talks about. Becuase it can not backtrack and it's just greedy hence you can nver get the best solution and you are ta the mercey of probabality. and since it is probablity, if you amke one mistak and since you are not allowed to go back, you will never reach the optimal (correct) answer. 