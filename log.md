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

## Day 3: February, 05, 2022

### Today's Progress:

> I'm driving up north today and started very early. I started with a code challenge very early this morning! My answer is below:

```
function noSpace(x){
return x.replace(/\s/g, '')
}
```

### Thoughts:

> This mornings code challenge was simple. We had to replace the white space of a string and then join the string. I originally thought or splitting and then joining, but I remember seeing it done in a bizarre way. I experimented with some combinations before finding my notes on the method above. I'm enjoying the fact that I'm recalling problems and their solutions!
> Even though I'm driving a lot today, I hope to do more work on my portfolio!

## Day 4: February, 06, 2022

### Today's Progress:

> Successfully made it back to the North! To start my morning I did not one, but two code challenges! I did not know there was an endsWith() method so I'm glad I learned that today! My challenges are below:

This was my solution for problem one:

```
function solution(str, ending){
  return ending === str.substring(str.length - ending.length)
}
```

This was the top solution for problem one:

```
function solution(str, ending){
  return str.endsWith(ending);
}
```

This was the solution for problem two:

```
function SeriesSum(n)
{
  for (i = 0, j =0; j < n; j++) {
    i += 1 / (1+j*3)
  }
  return String(i.toFixed(2))
}
```

### Thoughts:

> I graduated to the 7kyu level in CodeWars and my first problem was on the easier side, while the second problem was a lot trickier! I did need help to find out the solution. I was happy with how I was able to find the answers and use tools when I didn't know exactly what to do. It is teaching me that I still need a lot of practice.
> The rest of today will be dedicated to portfolio work and homework! I am implementing new photos and a page turning style that hopefully works!

## Day 5: February, 07, 2022

### Today's Progress:

> Happy Monday! Today had some great code wars challenges! I completed two. The answers and the top solutions are below. First problem had to make a positive number negative and if it was zero or already negative, do nothing. The second problem needed to validate a pin that was exactly 4 or 6 digits and could only contain digits. Have a look!

This was my solution for problem one:

```
function makeNegative(num) {
  if (num <=0) {
    return num
  } else {
    return num * -1
  }
}
```

This was the top solution for problem one:

```
function makeNegative(num) {
  return -Math.abs(num);
}
```

This was the solution for problem two:

```
function validatePIN (pin) {
  if (pin.length === 4 || pin.length === 6){
    if (pin.match(/^[0-9]+$/) != null){
      return true
    } else{
      return false
    }
  }else {
    return false
  }
}
```

This was the top solution for problem two:

```
function validatePIN(pin) {
  return /^(\d{4}|\d{6})$/.test(pin)
}
```

### Thoughts:

> I find myself wanting to know what each new method I see does. The curiosity I have been having for everything I've been working on is so great! I want to keep learning, understanding, and training!
> I have also been working on my portfolio. I hit a huge landmark last night / this morning where I was able to DRY up my portfolio and complete the draft of mobile and desktop versions. I need to now refactor the styling and adjust for ultra wide monitors!

## Day 6: February, 08, 2022

### Today's Progress:

> Happy Tuesday! I did one code challenge this morning that was tough! It allowed me to use the reducer method which I still need to practice with. Also, I will be continuing to refactor my portfolio. I also got my first interview today! I'm so excited!

This was my solution for problem one:

```
function findEvenIndex(arr){
  let left = 0;
  let right = 0;
  const reducer = (accumulator, currentValue) => accumulator + currentValue;

  if(arr.length == 0){
    return -1;
  }

  for(let i = 0; i < arr.length; i++){
    if(i == 0){
      right = arr.slice(1).reduce(reducer, 0);
      if(right === i){
        return i;
      }
    }else{
      left = arr.slice(0, i).reduce(reducer, 0);
      right = arr.slice(i+1).reduce(reducer, 0);
      if(left == right){
        return i;
      }
    }
  }

  return -1;
}
```

This was the top solution for problem one:

```
const sum = (a, from, to) => a.slice(from, to).reduce((a, b) => a + b, 0)
const findEvenIndex = a => a.findIndex((el, i) => sum(a, 0, i) === sum(a, i + 1));
```

### Thoughts:

> I had trouble this morning, but that could have been because I had other things on my mind. Sometimes it's hard to find where to start with a problem. I want to study all of the methods and figure them out on my own as well.
> It is now time to study everything for my upcoming interview!!
