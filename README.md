# Loops Lab

## Instructions for lab submission

1. Fork the assignment repo
1. Clone your Fork to your machine
1. Complete the lab
1. Push your changes to your Fork
1. Submit a Pull Request back to the assignment repo
1. Paste a link to of your Fork on Canvas and submit


## Question 1

Write code that prints all the numbers from 1 to 150, **inclusive.**

```
var range1 = 1...150
var numberList = 0

for _ in range1{
    numberList += 1
    print(numberList)
}   
```

***
## Question 2

Write code that prints all the numbers from 142 to 159, **exclusive.**

```
var range1 = 141..<158
var numberList = 0

for i in range1{
    numberList = i + 1
    print(numberList)
}
```
***
## Question 3

Write code that prints only the even numbers from 15 to 80, **inclusive.**

```
var range1 = 15...80
var numberList = 0

for i in range1 where i % 2 == 0{
    numberList = i
    print(numberList)
}
```

***
## Question 4

Write code that prints only the odd numbers from 19 to 51, **inclusive.**

```
var range1 = 18...51
var numberList = 0

for i in range1 where i % 2 == 0{
    numberList = i + 1
    print(numberList)
}
```

***
## Question 5

Write code that prints all the numbers that end in a **5** from 1 to 100, **exclusive.**
```
var range1 = 1...100
var numberList = 0

for i in range1 where i % 5 == 0 && !(i % 2 == 0){
    numberList = i
    print(numberList)
}
```
***
## Question 6

Write code that prints all the numbers that end in a 7 from 1 to 40, **inclusive.**

```
var range = 1...40

for i in range where i % 10 == 7{
    print(i)
}
```

***
## Question 7

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 3`

```
var range = 20...150
var Num = 1
for i in range where i % 3 == 0{
print(i)
}
```
***
## Question 8

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 2 and 3`
```
var range = 20...150
var Num = 1
for i in range where i % 3 == 0 && i % 2 == 0{
print(i)
}
```
***
## Question 9

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that end with a 4`

```
var range = 20...150

for i in range where i % 10 == 4{
    print(i)
}
```
***
## Question 10

Given a range of numbers from 20 to 150, print out all the numbers that follows these conditions:

`Print out numbers: 31, 35, 40 to 60.`

```
var range = 20...150

for i in range  {
    if i == 31 {
        print(i)
    }
    if i == 35 {
        print(i)
    }
    if i <= 60 && i >= 40 {
        print(i)
    }
}
```

***
## Question 11

Without using Xcode, how many times will the loop below run?  Explain why.

```swift
var i = 5

while (i > 3) {
    i += 1
}

// This is an infinite loop. The loop is saying "As long as the value of i is greater than 3, add 1 to it." Since i was declared as 5 above the loop, and since 5 (and everything higher than 5) is greater than 3, the loop will continue to add 1 to i forever. If i was declared as 3 or below, the loop would not even run.
```

***
## Question 12

Change the code below to make the loop stop executing when i reaches 9.

```swift
var i = 5

while (i < 9) {
    i += 1
}
```

***
## Question 13

Change the code below to make the loop stop executing after it has run 1,000 times.

```swift
var i = 0

while (i < 1000) {
    i += 1
}
```

***
## Question 14

Change the code below to make the loop stop executing after it has run 1,000 times and also make it print out the current value of i **only if i is an even number.**

```swift
var i = 5

while (i > 1005) {
    i += 1
}
if i % 2 == 0{
    print(i)
}

```

***
## Question 15

What's the difference in syntax between the following two while loops?  Will their outputs be different?  Explain why or why not.

```swift
var i = 1
//loop one
while i <= 10 {
    print("i = \(i)")
    i += 1
}

//loop two
var i = 1

repeat {
    print("i = \(i)")
    i += 1
} while i <= 10
```
Loop one uses the `while` condition (`i <= 10`) to hold the rest of the loop's algorithm inside (`print` and add 1 to `i`)
Loop two starts off with a `repeat` to execute the algorithm and leaves the `while` condition at the end.

The outputs for both are exactly the same because the algorithms for both do the same thing: Adds 1 to `i` if it is less then or equal to 10 and prints.

***
## Question 16

What's the difference between `break` and `continue`?  Give an example that demonstrates their differences.

`break` is used to end the execution of a loop. `continue` is used to skip over an iteration and to go on to the next one.

```

var range = 0...10
var yaBoi = 0

// break example

for i in range{
    yaBoi = i + 1

    if yaBoi == 8{
        break
    }
    print(yaBoi)
}

// continue example

while yaBoi <= 10{
    yaBoi += 1
    if yaBoi == 8 {
        continue
        }
    print(yaBoi)
}
```


***
## Question 17

Without using Xcode, what will the loop below print? Select all that apply.

```swift
for i in 1...10 {
    if (i >= 4 && i <= 7){
        continue
    }
    print(i)
}
```

[O]1
[O]2
[O]3
[]4
[]5
[]6
[]7
[O]8
[O]9
[O]10

***
## Question 18

Without using Xcode, what will the loop below print? Select all that apply.

```swift
for i in 1...10 {
    if (i >= 4 && i <= 7){
        break
    }
    print(i)
}
```

[O]1
[O]2
[O]3
[]4
[]5
[]6
[]7
[]8
[]9
[]10

***
## Question 19

Without using Xcode, what will the loop below print?  Explain below.

```swift
outerloop: for x in 1...3 {
    innerloop: for y in 1...3 {
        if y == 2{
            continue outerloop
        }
        print("x = \(x), y = \(y)")
    }
}
```
x = 1, y = 1
x = 2, y = 1
x = 3, y = 1

There is a range of 1...3 for both x in the first loop and y in the second nested loop. Because the range in the first loop is from 1 to 3, the code will only print out 3 lines, with x going from 1 to 2 to 3. Within the second loop, the condition `if y == 2{continue outerloop}` prevents y from ever reaching number 2 or even number 3, because `continue outerloop` restarts everything from the outer loop. y will always be 1.
***







I'm really sorry, I did not have the time (or the brain power) to finish these questions in time tonight. But I will sumbit the finished version tomorrow! 

## Question 20

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** x and y are both integers.


***
## Question 21

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** the difference of x and y is at least 5, and x and y are both integers.

```

```

***
## Question 22

Print the first `N` square numbers. A **square number**, also called perfect square, is an integer that is obtained by squaring some other integer; in other words, it is the product of some integer with itself (ex. 1 = 1*1, 4 = 2 * 2, 9 = 3* 3 …).

Example:
Input: `var N = 5`

Output:
```swift
1
4
9
16
25
```

***
## Question 23

Given an integer N draw a square of N x N asterisks. Look at the examples.

Example 1:
Input: `var N = 2`

Output:
```swift
**
**
```

Example 2:
Input: `var N = 3`

Output:
```swift
***
***
***
```

Hint 1
Try printing a single line of * first.

Hint 2
You can use print("") to print an empty line.

***
