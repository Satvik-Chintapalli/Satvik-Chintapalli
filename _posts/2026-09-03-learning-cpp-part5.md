---
layout: post
title: 'Learning C++ Part 5' 
date: 2026-09-03 16:48:00 +0530
----

## 16:49

Well I finally got the boilerplate for markdown and some customization up and running. I haven't seen people who stop line highlighting and now it feels like I'm writing on a blank slate. Which feels kind of good not gonna lie, as I'm pretty habituated on writing on blank paper over ruled ones.

Anyways let's just get started with learning some more C++. And instead of starting at night and calling it a day quite early, I'm starting at the evening and I'm hoping I'll be working longer. 

I'm in the bedroom even today so fingers crossed the wifi doesn't mess up stuff like last time. I checked the vod of last night's stream and it was incomplete

## 16:56

My idea for the problem is that we need to find the digits, and once we find them then we can sum them up. So suppose the input was 4538, what would I do. Well if I divide it 1000, since it's integer division, it's going to give 4. Then what I can do is subtract 4*1000 from 4538 and then repeat this operation for division by 100 and so on. By this I get all the digits in the number. For this I'll need to know the number of digits, which I can potentially find by dividing it by various 10 powers in a loop until I hit a value, by which when I divide, the quotient is less than 1, or maybe since we are doing integer division, it'll be zero. So let's start.

## 17:10

Took a chocolate break. Diary milk 10 Rs melted.

## 17:16

Completed problem 7. It was a breeze. So the next problem is to find gcd. So we are using the euclidean division algorithm here. We divide the bigger number by smaller number and then replace the bigger number with the remainder. We repeat this until the smaller number becomes zero and then we'll have our answer. So let me first check this by hand. 

gcd(48,18) = gcd(12,18) = gcd(12,6) = gcd(0,6) = 6

Well the algorithm is working pretty well, so it's time to code it up.

## 17:22

The challenge I'm facing right now is to find the variable with lower value in a and b. And my simple approach is to just brute force the modulo and if one of them leads a number which is not the numerator itself, then that's the one we'll be using.

## 17:27

Ok, we ran into some unknown error, so it's time to do debugging.

SO as far as my diagnosis goes, it went into the while loop 4 times. So let me just be printing the live values of a and b, that would give me some idea.

## 17:33

Interesting observation. Somehow I got the value of a and b exactly as I wanted, but it's messing up the return value. 

It's quite counter intuitive as the conditional statements are quite straightforward. let me see if the a and b values have updated outside of the while loop

Made a really rookie mistake. It's a==0. That's the reason why it's directly going into else statement I believe

## 17:43

It gave me problem when dealing with negative numbers as the % operator gives negative numbers I believe. Actually let me check. Ok so it's giving 0 I believe, and that would cause error. My simple idea is to just use a-(a/b) , as it would be integer division, so we'll be left with remainder.

## 18:00
 
I'll admit it's really dumb from my side. I could have just taken modulus value of all of them and just called it a day. Let me just do that

## 18:04

Time to buy milk. I'll be right back. 

## 18:59

The break was longer than expected. I got a bit side track. Anyways let's just continue with the next problem

## 20:04

I'm back again after wasting some more time.