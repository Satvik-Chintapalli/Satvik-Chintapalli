---
layout: post
title: 'CSES Introductory Problems' 
date: 2026-09-04 00:02:00 +0530
----

## 00:03

Well I've started out with CSES Problem sets accompained with the handbook. So let's start with the first problem which is basically Collatz conjecture(watched on veritasium)

## 00:19

Well I'm succesfully done with the first problem and it was a breeze except it gave me a result to just stick to using long long when huge n values could be taken. 

Also I hate this line highlighting. Ok so somehow just removing and putting it back made it set right

So let me start with the next problem 

# 00:22

using ll = long long, is something I'd like to incorporate in my further code. But I believe it's not that useful because putting that many values of n is not feasible

# 00:24

So the user would tell how many numbers are there(n), and the user would give n-1 numbers out of the first n natural numbers, and we need to find the missing number. So, if we manually check for each number in a loop, it's pretty tiring. The input of all the numbers would be in an array. 

Let's just try brute force and see what happens

## 00:29

I should think about how I'm going to check in the first place. So currently we have sequence of all the digits taken as input. I think a clever solution would be to take the sum of all those numbers given as input and subtract it from the sum of first n natural numbers. Yeah, that would give us the answer directly. Let me do that.

## 00:31

Well it's working for the example case. But let me think of cases where it might break. Since I've used long everywhere, there isn't any question of overflow or something like that. Also we could just remove the array. we can define a temporary variable.

Now that this is done, let me just submit and see , wait, I need to change j variable type to long long

Let's GO completed it in first attempt. This is actually quite fun to do.

Let me move to the next problem

## 00:36

So now that we have the DNA sequence as input, say ATTCGGGA. So my initial idea is that we set up counter variables for A,C,G and T, and then select the maximum value out of the 4.

This is a pretty simple again brute force idea. Let's think of something which might potentially be more "neat". 

I believe knowing vector might make the task easier i.e. avoiding these temporary variables and looping. But before that let me just solve the problem in the way I'm able to think, later I can learn vector and maybe solve it much more efficiently

I'll stop now I guess, I think the next best step would be to learn vector as you can make one without having to know the number of elements in it which I think is required for this problem. 

Bye.

## 17:07 

I'm back. Yesterday I said I might need to learn vectors. Well before that I think it's high time I read up some theory from the book, which might teach vectors. Even if it doesn't it's a good idea to finish theory so that I can do those introductory problems atleast without "lack of theory" , though I might have lack of coding skills

## 17:43

So I'm going to learn the dreaded recursion for the first time. I have actually refrained from learning about it before hand jus tto have the experience of learning it as there's a lot of hype about it. I'm gonna go buy milk and then start with it. 

## 18:20

I took an awful lot of time than I should. 

## 18:29

Well I tried the basic example on recursion it's not really that hard so to speak conceptually. It's like recursion in math where you have a function a(n) which depends on a(n-1) and stuff like that, and for that once you know required base cases, you can solve for the general. This is kind of like that. 

## 18:45

Recursion isn't even that deep as it was projected. I don't know what is so counter intuitive in it. I guess some math background previously gave me a heads up. 

## 19:07

I got a bit carried away by Riemann Hypothesis. It's really fascinating because the problem statement in itself sounds decently easy to understand, of course there's a lot of methods which I just don't understand, how the summation of n^s has been extended to entire complex plane using analytical continuation (I just memorized the word lol). So it's pretty interesting. I have two mathematical problems which I'm interested in. The first is to prove Riemann Hypothesis and the second is to be make an algorithm which will trade in market with immense efficiency. The second one doesn't sound mathematical but based on what I know, these quant firms and hedge funds like Jane Street, Rennaisance , they all use mathematical techniques. Those are pretty far fetched goals but I think they act as a light which gives direction to travel. And it would break my mind if there is any connection between those both problems, because then that would mean I was working on the same problem. Anyways let's get back to coding.

So I've stumbled on this "Maximum sub array sum". I'm going to take pen and paper and think about it on paper. 

## 19:26

I've worked over it on paper with an example and here's my algorithm statement(not very professional)

*We first calculate subarrays of each size 1,2,3,...,n. In subarrays of size i, 1<=i<=n, we calculate sum of elements in each subbaray and find the maximum, that will be the maximum sum of subarray i. We calculate for all i values and compare.*

So this is my initial algorithm. Now I'd like to code it up myself. Back to paper.

## 19:45

After working out the loops on paper in a really illegible format, I've figured out how to code it. So let me just jump into code editor and code it out. And this time I would have really less debugging I suppose because I've worked out the problem first on paper.

## 19:56

I've coded it up and I'm really excited to see if it works. I'm going to start with the example I made myself which I used to develop the algorithm and see if it works(it should tho).

I've screwed it big time. The answer is supposed to be 17. Time for some debugging I guess. 

So the part where we take the array as input is working just fine. So we messed it up afterwards. 

I understood. After the loop I'm supposed to set the current and temporary Sum to 0.

Alright I figured out the problem, I don't know why I was using we the whole time. It's a habit from reading math proofs I believe. Anyways, I finally cracked the code. 