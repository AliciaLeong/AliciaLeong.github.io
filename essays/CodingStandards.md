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


<img class="ui medium right floated image" src="../images/ESLint_logo.png">

## My Thoughts on ESLint
In my opinion ESLint reminds me of that one aunty that you have that is very critical of everything. According to ESLint, spacing matters and single quotes should be used rather then double quotes. It is similar to when your aunty comments your own personal style. However, just like your aunty has her moments, ESLint has its benefits. While the spacing and quote guidelines seems tedious, the way ESLint has your format your code is very useful. For example if you coded the following:
Before ESLint:
```
const temp = 'World';
console.log( "Hello" + temp ); // using concatenation
```
After ESLint:
```
const temp = 'World';
console.log(`Hello ${temp}`);// using template literals
```
ESLint would scold you with that red error message saying "strings must use single quotes", which really should not make a difference in my opinion. But then the error message "unexpected string concatenation" would pop up too. This is where I feel ESLint proves that its useful. It forces everyone to conform to one standardized way. Programming is so versatile there are numerous ways to do the same thing, this means if one person does it one way someone else may not understand that syntax. ESLint allows you to only do it one way so everyone can understand, this helps a lot when working collaboratively.

## Speaking From Experience
I am currently working on a project where I must edit code that has been passed down for years. From what I can tell, there are some attempts at documentation in some parts but, other parts have no formatting or documentation. Sticking to some sort of guideline here would have been very useful. I would use less time sifting though all the code trying to find that one function I need. (If only their aunty came to scold them on their documentation.) Coding guidelines can be so useful that one of our goals, this semester, is to fix the code so it follows the [Google Coding Syle Guideline](https://google.github.io/styleguide/cppguide.html). This way we can help the future team have an easier time working collaboratively. 

## Last Remarks
In conclusion, just as you love your aunty anyway, I believe that ESLint is a good thing. I have only been using it for a week and I am already seeing the benefits. I guess the spacing and quote errors are not as terrible as they seem. They make my code look more organized and readable which I respect after experiencing semi-readable code. Overall, the feature I like the most is that ESLint makes us standardize how some syntax is used. In the example code above, we now have to use template literals rather then concatenation. ESLint is forcing us to learn good coding habits which can reflect on all our code regardless if it is in JavaScript or not. In the future, ESLint will allow me to work more efficiently with my peers as we can collaboratively understand and work together.