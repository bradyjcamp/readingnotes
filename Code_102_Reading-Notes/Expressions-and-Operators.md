# Expressions and operators

- JS expressions and operators include **assignment**, **comparison**, **arithmetic**, **bitwise**, **logical**, **sting**, and **ternary**.
- Assignment operator
  - An assignment operator assigns a value to its left operand based on the value of its right operand.
  - A simple assignment operator is equal (=) `x = f()` this assigns the value of `f()` to `x`.

# Loops with programs

- A loop is a set of operations that you need to run more than once.
- It gives a multiple pathways
- Syntax: looks a lot like function signatures, instead of parameters, there are a couple options.
- 3 types: for loop, while loop, do while loop

 ```js

// for loop

//3 things that go here

// first is a variable
// second is a condition - if condition is false, then loop will stop
// third is update to the initializer (incrementer)

// i stands for initializer 
// times equals i

for (let times=0; times < 50; times ++) {
    // this block will run as many times needed for loop
    console.log('this loop has run ' + times + 'many times')
}

//while loops!
//the parentheses only contrain a condition

let likeWatermelons = confirm('Do you like watermelons?');

while(!likesWatermelons) {
//console.log('I will never stop running)
likesWatermelons = confirm('Do you like watermelons?');
}


let answer = prompt('yes or no, do you like watermelons?');

while(answer != 'yes') {
answer = prompt(do you like watermelons?);}

let num = 10


let num = 10;
while(num < 10) {
console.log(num);
num++}


// loop 10 times. incriment or depliment

//for loops

for (let times = 5; times > 0; times --) {
    // this block will run as many times needed for loop
    console.log('this loop has run ' + times + 'many times');

}


for (let times=0; times < 50; times ++) {
    // this block will run as many times needed for loop
    console.log('this loop has run ' + times + 'many times')};

    let likeWatermelons = confirm('Do you like watermelons?');

    while(!likesWatermelons) {
    //console.log('I will never stop running)
    likesWatermelons = confirm('Do you like watermelons?');
    }
  ```
  