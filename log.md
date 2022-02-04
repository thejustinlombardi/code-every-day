# 100 Days of code - Log

## Day 0: February, 02, 2022

### Today's Progress:

> Set up this repo to keep track of all of my progress.
> I also worked on creating a database for my portfolio so I could store my projects outside of my frontend project. Worked on a separate Code Wars challenge with Landon and Michel.
> The challenge was to convert a string into a number. My answer is below:

```
var stringToNumber = function(str){
  return parseInt(str);
}
```

### Thoughts:

> Working on the Code Challenge was fun! It was on the easier side, but I believe that getting the reps in is important. I also am having fun creating the backend for my portfolio. I can't wait to implement this into the frontend and connect all of the dots!

## Day 1: February, 03, 2022

### Today's Progress:

> I was able to deploy my backend that holds the data for my portfolio and link the backend to the frontend! My portfolio is now a full-stack application.
> I also did another code challenge! The challenge was to take a non-negative number and turn it into an array in reverse order. My answer is below:

```
function digitize(n) {
  return Array.from(String(n), Number).reverse();
}
```

### Thoughts:

> This mornings code challenge was fun and I challenged myself by trying to solve the problem in a single statement. Sometimes I separate the steps when they can be done in one go. I believe I succeeded in this today! I also love that my portfolio is functioning from front and backend. The next step is creating a superuser and incorporating User Auth so I can do all my additions to my portfolio from the portfolio itself!

## Day 2: February, 04, 2022

### Today's Progress:

> I played around with styling for my portfolio and fixed some of the image issues on mobile. I also had a broken image link so I fixed that as well. .
> I also did another code challenge! The challenge was to calculate bmi and then have different return statements depending on the bmi calculation. My answer is below:

```
function bmi(weight, height) {
  let bmi = weight / height ** 2
  if (bmi <= 18.5){
    return "Underweight"
  } else if (bmi <= 25) {
    return "Normal"
  } else if (bmi <= 30) {
    return "Overweight"
  } else {
    return "Obese"
  };
}
```

Someone else's answer I really liked the look of:

```
const bmi = (w, h, bmi = w/h/h) =>
bmi <= 18.5 ? "Underweight" :
bmi <= 25 ? "Normal" :
bmi <= 30 ? "Overweight" : "Obese";
```

### Thoughts:

> This mornings code challenge was interesting. I have done these before and completed how I know how to. I did see another example that I really liked the look of. I like the use of ternary statements and like the implementation above. I will have to try that next time.
> For my portfolio, I used axios to get the data from my API instead of the standard fetch. I like the syntax a lot better and it looks cleaner along with the async/await function.
