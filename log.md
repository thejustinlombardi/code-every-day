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

## Day 7: February, 09, 2022

### Today's Progress:

> I started the day with another code challenge. I got very far in my first attempt at the question but my tests kept failing. I realized that I was trying to use forEach which kept breaking it. I also have never used .repeat() before and I saw that in the top solution. It's so great to see how others answer these questions!!

This was my solution for problem one:

```
function accum(s) {
  let arr = []
  for(let i=0; i<s.length; i++) {
    arr.push(upLow(s[i], i +1))
    }
    return arr.join('-')
  }
function upLow(s, num){
    let letter = s.toUpperCase()
    while (letter.length !== num) {
    letter += s.toLowerCase()
 }
 return letter
  }
```

This was the top solution for problem one:

```
function accum(s) {
  return s.split('').map((c, i) => (c.toUpperCase() + c.toLowerCase().repeat(i))).join('-');
}
```

### Thoughts:

> I got very close with my first attempt but did need to look up additional methods on how I could do this differently. I think my first mistake was trying to do this in a forEach rather then a regular for loop.
> I have been studying and also trying to teach myself Angular. I'm still in the early days of it, but the concept and way that it's structured is very interesting! I'll comment more on that when I get further along.

## Day 8: February, 10, 2022

### Today's Progress:

> I started the day with about an hour of my Udemy course on Angular. I have really been liking Angular and learning how to use it! I also really enjoy the Udemy course! I feel like I'm getting an incredibly deep understanding of framework! This morning's CodeWars challenge was on the simple side, but my solution used a method I learned from yesterday's challenge! This is what I'm talking about where you learn so much by just seeing how something else is done. It was also the top solution!

This was my solution for problem one:

```
function repeatStr (n, s) {
  return s.repeat(n);
}
```

### Thoughts:

> I'm loving Angular and learning a new language on my own. With GA coming to a close, I want to implement Angular in our Project 4 and I also want to have an understanding of it so I can chat about it in interviews.
> My focus today in class is authentication in django. I look forward to that because I would love to implement it in our project four as well! We are incredibly ambitious, but I really feel like we can pull this off!

## Day 9: February, 11, 2022

### Today's Progress:

> I started the day with about an hour of my Udemy course on Algorithms and Data Structures and then some code challenges. The challenges were on the easier side. The more practice I get, the better I am at remembering how to get to each problem. That plus Google helps when I need to remember the parameters of a method.

This was my solution for problem one:

```
var isSquare = function(n){
  return n >= 0 && Math.sqrt(n) % 1 === 0;
}
```

This was my solution for problem two:

```
function getCount(str) {
  var vowelsCount = 0;
  let vowels = ['a', 'i','e','o','u']
  for (let char of str) {
    if (vowels.includes(char)) {
      vowelsCount += 1
    }
  }

  return vowelsCount;
}
```

### Thoughts:

> I have full faith that we can pull off this project four! Angular has been fun and if we each tackle sections, it won't be so daunting! That will be most of my updates for the next week, plus some small challenges as well!

## Day 10: February, 12, 2022

### Today's Progress:

> Today was great! I id more work in my Udemy course and also had my first coding interview today!! It was so much fun and, no matter the outcome, It was such a great learning experience! I also tried to debug some of our backend problems for our Project 4. I wasn't completely successful, but I got a lot closer! Not much code to share today

### Thoughts:

> Today proved that I truly do love to code and love to learn how to code. I feel like I've been on the best path and I'm only going to continue to grow! Code snippets will be shared tomorrow!

## Day 11: February, 13, 2022

### Today's Progress:

> Today was an easy day. Fixed a few bugs for our Project 4 backend and worked on some Codewars challenges. Felt a little tired, but was still able to put in some work.

This was my solution for problem one:

```
function booleanToString(b){
  return b ? 'true' : 'false'
}
```

This was my solution for problem two:

```
function removeSmallest(numbers) {
  let smallestNum = Math.min.apply(Math,numbers);
  let index = numbers.indexOf(smallestNum)
  numbers.splice(index, 1)
  return numbers
}
```

### Thoughts:

> I am so close to getting some of these answers. I know what needs to be done, but now it's time to study and refine my skills so I can call upon these methods without having to Google the methods.

## Day 12: February, 14, 2022

### Today's Progress:

> Today was a lot. We deployed our backend and have been swamped in Angular. It is so much fun, but a very different way to approach things. This has been teaching us so much and I'm so glad we decided to challenge ourselves this way.

### Thoughts:

> We are currently learning how to fetch data with Angular! Wish us luck!

## Day 13-16: February, 17, 2022

### This Week's Progress and Thoughts:

> This week was a lot. We did our best to get Angular working, but not being able to pass data was hurting us and we needed to make a decision...Do we continue with possibility of failure, or do we keep it safe and go back to React? We decided to go back to React so we could deliver something great for our final project. It has come along so well. I've been coding a lot the past few days and have been burning the midnight oil. Needless to say, I haven't had much time for code challenges, but I have been coding every day! Today is also my last work day in General Assembly's coding boot camp. What a crazy 3 months! I went from zero coding experience to wanting to know as much as I can! I loved this experience and cannot wait for what my future has in store!

## Day 17: February, 18, 2022

### Today's Progress:

> I graduated from General Assembly today! What a surreal feeling and I couldn't be happier!! Our project four turned out amazing and I'm so proud of my teammates and all of my classmates for doing so well during this course!! I still managed to get in a Codewar challenge and I did spend part of the morning getting out code ready for presentation. Codewar challenge below!

The solution for the problem was:

```
function comp(array1, array2){
  if (array1 === null || array2 === null) return false;
  array1.sort((a, b) => a - b);
  array2.sort((a, b) => a - b);
  return array1.map(v => v * v).every((v, i) => v == array2[i]);

}
```

### Thoughts:

> I had to evaluate whether the values in the first array squared equaled the values in the second array. This was definitely tricky and I got pretty far on my own but I kept running into a snag when figuring how to return it. I did consult Google as I'm still getting used to these types of problems. My main focus is to just get the reps in as much as I can.

## Day 18: February, 19, 2022

### Today's Progress:

> Started the day with some Code wars challenges and will be studying more of the Data Structures and Algorithms course as well.

The solution for the problem was:

```
function lovefunc(flower1, flower2){
  if ((flower1 + flower2) % 2 === 1) {
    return true
  } else {
    return false
  }
}
```

### Thoughts:

> Maybe it was because I'm still coming down from graduating and the intensity of the past three months, but make sure you read the directions of the prompts! I was curious as to why my function wasn't working and it was simply because I didn't fully read the prompt. Check every detail!!

## Day 19: February, 20, 2022

### Today's Progress:

> Today was filled with the Data Structures and Algorithms course from Udemy and some Code wars challenges!

The solution for the problem was:

```
function numberToString(num) {
  return num.toString();
}
```

### Thoughts:

> Practicing challenges in Code wars is still fun and I keep learning from them. I definitely like watching the DS&A videos with my fiance and having to explain what is happening. This method is proving more and more what concepts I understand and what concepts I need more work on. She is picking up these methods really quickly, too! She's a natural!

## Day 20: February, 21, 2022

### Today's Progress:

> Today was filled with the Data Structures and Algorithms course and Angular course from Udemy and some Code wars challenges! The problem was finding the unique value in an array. I thought I was on the right track, but my approach was wrong.

This is what I was trying to do:

```
function findUniq(arr) {
  let uniq = {},
      result;
  arr.forEach(function(item) {
    uniq[item] = uniq[item] + 1 || 1;
  });
  Object.keys(uniq).forEach(function(key) {
    if (uniq[key] == 1) {
      result = key;
    }
  });

  return parseFloat(result);
}
```

The solution for the problem was:

```
function findUniq(arr) {
  return +arr.filter( (value) => { return arr.indexOf(value) == arr.lastIndexOf(value) } );
}
```

The solution I understood more was:

```
function findUniq(arr) {
  arr.sort((a,b)=>a-b);
  return arr[0]==arr[1]?arr.pop():arr[0]
}
```

### Thoughts:

> I try my hardest in the Code Challenges. Even if I don't get the answer, the thing that I'm proud of is that I understand what needs to be done, but I don't know the exact method yet. That's why I'm looking at the problems, understanding them, looking for examples, studying the answers, and then writing about them so I can keep track of how it is all done. I used to think of it as cheating, but if I don't know how to do something, it shows I need more practice and more understanding.

## Day 21: February, 22, 2022 (My Fiance's Birthday!!!)

### Today's Progress:

> Today was again filled with Data Structures and Algorithms work in my Udemy course. We focused on Linear Search and Binary Search. Both extremely wonderful topics and I enjoyed diving deeper into these concepts.

### Thoughts:

> I posted about this on LinkedIn, but I want to say it here, too. I feel like I'm very close to this content sometimes. For example, this morning when we were working on binary search, my code kept returning values that were so close to the answer, but still wouldn't pass their tests. I wasn't understanding why until my fiance took a look at it and said, "Wait, shouldn't that be <= instead of just <"? I was floored. Today I learned that I need to take a step back when I've been in a problem for too long.

## Day 22: February, 23, 2022

### Today's Progress:

> Today was again filled with Data Structures and Algorithms work in my Udemy course. We focused on Bubble Sort and I got an assessment to take home for another interview. Hopefully it goes well! Below is a solution to today's code challenge.

```
function findOdd(arr) {
for(let i = 0; i < arr.length; i++){
const count = arr.filter(value => value === arr[i]).length;
if(count % 2 == 1){
return arr[i];
}
}
return -1;
}
```

### Thoughts:

> I'm thrilled with the progress I'm making with the Data Structures and also the different projects I'm working on. I also love being a TA and helping people in class! Today was a truly wonderful day.

## Day 23: February, 24, 2022

### Today's Progress:

> I went on a little tear with CodeWars today. I was getting in the zone and feeling really good about the challenges so I kept going. I continuously want to get better and keep working hard towards a higher kyu! I also worked on my portfolio, made small edits to our Project 4, and applied to a few jobs. Below are my solutions to the challenges I did.

```
function grow(x){
return x.reduce((acc, curr) => acc * curr, 1)
}
```

```
function squareDigits(num){
let newNum = num.toString()
let numArr = newNum.split('')
let sqArr = [];
numArr.forEach((e)=>{
sqArr.push(e**2)
})
return parseInt(sqArr.join(''))
}
```

```
function duplicateEncode(word){
let chars=[...word.toLowerCase()];
let dupList = chars.filter((char,index,chars)=>chars.indexOf(char)!==index);
let dupSet = new Set(dupList);
let uniqueDupList = [...dupSet];
let resultString = "";
for (let i=0, n=chars.length; i < n; ++i ) {
if(uniqueDupList.includes(chars[i])) {
resultString += ")";
} else {
resultString += "(";
}
}
return resultString;
}
```

```
function DNAtoRNA(dna) {
return dna.split('T').join('U');
}
```

```
function betterThanAverage(classPoints, yourPoints) {
let sum = 0;
for(i = 0; i < classPoints.length; i++ ){
sum += classPoints[i]
}
let avg = sum / classPoints.length;
return yourPoints > avg ? true : false;
}
```

```
function squareSum(numbers){
return numbers.reduce((acc, curr)=> acc + (curr ** 2), 0)
}

```

### Thoughts:

> I was so glad I got to use the reduce method so much today because I do prefer to use it and I wanted more practice with it anyway. It feels great to be able to recall the syntax from memory now!

## Day 24-29: March, 1, 2022

### Today's Progress:

> It has been an insane weekend. Unfortunately, I lost my streak on GitHub this weekend. I was away and mostly was listening to DS&A lectures but did not commit any code. Then I started on Monday with college again so I've been a little all over the place. But! I have been steady with my DS&A lectures while also diving back into Java!! This new course I'm working on has been teaching me so much! Java is a very interesting language once you get used to it. I will keep up to date on everything I've been learning! For today, I focused mostly on Java and setting up methods! I finally understand what static and void mean! After all of this time!

## Day 30-37: March, 9, 2022

### Today's Progress:

> I have been continuing to practice my DS&A skills through Udemy and it has been going very smooth. The course has been informative and practicing Doubly Linked Lists and Binary Search Trees in JavaScript has been my focus. I'm feeling more comfortable with the formats and thinking of the real-world applications of the data structures.

I also finished my first week back to Southern New Hampshire University in my Operating Platforms course where I'm designing UML Diagrams based off of Java code. I've been working through a complete Java course in Udemy as well to get a refresher which has been a blast!

I'm starting a personal project for my poetry as well! I'm looking to design a blog style site that I can display all of my poems on. With over 200 poems I've written in the past few years, I finally can showcase them in a central place! I'll keep you posted on this as well!
