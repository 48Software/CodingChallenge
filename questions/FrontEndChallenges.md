# Front-end Code Challenges

## Part 1
Given the below code snippet, solve the problems that follow:

```html
<div id="firstDiv" class="red-card">
<div id="secondDiv" class="red-card">

<style>
    #secondDiv {
        background: orange;
    }

    div {
        height: 150px;
        width: 150px;
        background: green;
    }

    .red-card {
        background: red;
    }

    .yellow-card {
        background: yellow;
    }
</style>
```

1. What will the colour of both div elements be?
2. How would you dynamically target ```firstDiv``` and make it's colour pink? (provide the code snippet)
3. How would you dynamically target ```secondDiv``` and add the ```yellow-card``` class to its class list? (provide the code snippet)

## Part 2
### Section 1
Given the below JavaScript snippet, solve the problems that follow:

```javascript
var data = [
    {
        name: "Sandals",
        country: "Jamaica",
        holidayRanking: 9
    },
    {
        name: "Auckland",
        country: "New Zealand",
        holidayRanking: 5
    },
    {
        name: "Suva",
        country: "Fiji",
        holidayRanking: 6
    },
    {
        name: "Apia",
        country: "Somoa",
        holidayRanking: 4
    },
    {
        name: "Nuku'alofa",
        country: "Tonga",
        holidayRanking: 10
    },
];
```

1. Given the data array, process the array returning another array containing only the name of each destination.
2. Given the same data array, process the array again this time returning only the destination objects where the holidayRanking > 4.
3. Extend your solution to problem 2 to return an array of holiday rankings where holidayRanking > 4 then sum all the holiday rankings

### Section 2
Consider the ```compareIt``` function definition

```javascript
function compareIt(num1, num2) {
    return num1 == num2;
}

compareIt(5, "5");
```

1. Why will the function call return true? 
2. How could one change this function so that data types are checked as well as values?

### Section 3
Consider the function below:

```javascript
function legal(x) {
    console.log(x);
    var x;
}
```

1. Why will the function be parsed correctly? 
2. How could you introduce a stricter syntax to variable/function declaration and avoid this behaviour?

## Part 3
1. How would you make a web page mobile friendly (i.e responsive)? 
   * Provide examples of this.
2. What is the benefit of bundling .js scripts into one file? 
3. What needs to be done to ensure the browser understands Sass styling?
4. What should be done to ensure browser compatibility with newer flavours of JavaScript like ES6/7?
