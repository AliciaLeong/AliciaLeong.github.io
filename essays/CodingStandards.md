---
layout: essay
type: essay
published: true
title: "Guidelines to Coding"
date: 2019-02-05
labels:
  - ICS 314
  - Coding
---
# My Thoughts on ESLint
In my opinion ESLint reminds me of that one aunty that you have that is very critical of everything. According to ESLint, there needs to be spaces between everything but in some areas you can't have any spaces. To me it the spacing seems trivial. It is similar to when your aunty comments on why you forgot you jacket at home when it summer. However, just like your aunty has her moments, ESLint has its benefits. While the spacing and quote guidelines seems tedious, the way ESLint has your format your code is very useful. For example if you coded the following:
```
Before ESLint:
const temp = 'World';
console.log("Hello" + temp); // using concatenation
After ESLint:
const temp = 'World';
console.log(`Hello ${temp}`);// using template literals
```
ESLint would scold you with that red error message saying "strings must use single quotes", which really should not make a difference in my opinion. But then the error message "unexpected string concatenation" would pop up too. This is where I feel ESLint proves that its useful. It forces everyone to conform to one standardized way. Programming is so veristle there are numerous ways to do the same thing, this means if one person does it one way someone else may not understand that syntax. ESLint allows you to only do it one way so everyone can understand, this helps a lot when working collaboratively.

# Speaking From Experience
I am currently working on a project where I must edit code that has been passes down for years. From what I can tell there is some attempt at documentation in some parts but other parts has no formatting or documentation. Sticking to some sort of guideline here would have been very useful. I would use less time sifting though all the code trying to find that one function I need thats implemented in a syntax I can only half understand. One of our goals is to fix the code so it follows the [Google Coding Syle Guideline](https://google.github.io/styleguide/cppguide.html) that way it will help the future team understand the syntax and formatting. 