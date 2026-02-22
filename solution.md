# 🧠 SECTION 1: Core Logic (No built-ins mindset)

## Reverse a string without using built-in methods
```js

const name = 'rahul'
let res =''
for (let i = name.length - 1; i >= 0; i--) {
    res+=name[i]
}
console.log(res)

```
##  Check if a number is prime

```js

let n = 10;
let isPrime = true;

if (n <= 1) {
    isPrime = false;
} else {
    for (let i = 2; i < n; i++) {
        if (n % i === 0) {
            isPrime = false;
            break;
        }
    }
}

console.log(isPrime ? `${n} is a prime number.` : `${n} is not a prime number.`);

```
##  Remove prime number from an array

```js

let n = [1, 2, 3, 61, 47]

let isPrime = true
let prime = []

for (const elem of n) {
    if (elem <= 1) {
        isPrime = false
    } else if (elem % 2 === 0) {
        isPrime = false
    } else {
        prime.push(elem)
    }
}

console.log(prime)
```
## Check if a number is a perfect square

```js

let a = 10

for (let i = 1; i <= a; i++) {
    for (let j = 1; j * j <= a; j++) {
        if (j * j === i) {
            console.log(i)
        }
    }
}

```
## flat nested array and filter unique and duplicate value
```js

let arr = [1, 2, [3, 4], [3, [4, 7]]];

let flat = arr.flat(Infinity)

let dupli = []
let unique = []


for (let i = 0; i <= flat.length - 1; i++) {
    let isDuplicate = false
    for (let j = i + 1; j <= flat.length - 1; j++) {
        if (i !== j && flat[i] === flat[j]) {
            isDuplicate = true
            break;
        }
    }
    if (isDuplicate) {
        if (!dupli.includes(flat[i])) {
            dupli.push(flat[i])
        }
    } else {
        unique.push(flat[i])
    }
}


console.log(dupli)
console.log(unique)


```
## Find smallest number in an array
```js

let arr = [7, 2, 4, 5, 8, 0]

let smallest = arr[0]

for (let i = 0; i <= arr.length - 1; i++) {
    if (arr[i] < smallest) {
        smallest=arr[i]
    }
}

console.log(smallest);
```

## Find factorial of a number

```js

let num = 5;
let fact = 1
for (let i = 1; i <= num; i++) {
    res = fact*=i
}
console.log(res)
```
## Find largest number in an array
```js
let arr = [1, 33, 4, 67, 77]

let large = arr[0]


for (const element of arr) {
    if (element > large) {
        large = element
    }
}

console.log(res)

```
## Remove duplicate elements from an array
```js

let arr = [1, 33, 4, 67, 77, 77, 33, 1, 4]

let dupli =[]

for (const element of arr) {
    if (!dupli.includes(element)) {
        dupli.push(element)
    }
}

console.log(`Duplicate elements : ${dupli}`)

```
## Check if a string is a palindrom

```js
let name = "madam";

let isPalindrome = true;

for (let i = 0; i <= (name.length - 1) / 2; i++) {

  for (let j = name.length - 1 - i; j >= name.length - 1 - i; j--) {

    if (name[i] === name[j]) {
      isPalindrome = true;
    }else{
        isPalindrome=false
    }
  }

  if (!isPalindrome) break;
}

console.log(isPalindrome ? "Palindrome" : "Not Palindrome");

```
 
 # 📦 SECTION 2: Array & Object (Startup favorite ❤️)
 ## Sum of all numbers in an array

 ``` js
 let arr = [1, 2, 4, 6, 7]

let sum = 0
let total = []
for (let i = 0; i <= arr.length - 1; i++) {
    sum += arr[i]
}

total.push(sum)
console.log(total)
 ```

## Count how many even & odd numbers in an array
```js
let arr = [1,2,4,6,7,3,9]

let even = 0
let odd = 0

for(let i =0;i<=arr.length-1;i++){
    if(arr[i]%2===0){
        even ++
    }else{
        odd ++
    }
}

console.log("even count",even)
console.log("odd count",odd)
```
## Find frequency of elements in an array
```js
let arr = [1, 2, 2, 6, 7, 3, 3, 3, 9];

let freq = {}

for (let i = 0; i <= arr.length - 1; i++) {

    let num = arr[i]

    if (freq[num] === undefined) {
        freq[num] = 1
    } else {
        freq[num] = freq[num] + 1
    }

}

console.log(freq)
```
## Find frequency of elements in an string
```js
let str = 'rahul kumar'

let freq = {}

for (let i = 0; i <= str.length - 1; i++) {
    let chr = str[i]
    if(freq[chr]===undefined){
        freq[chr] = 1
    }else{
        freq[chr]=freq[chr]+1
    }
}
console.log(freq)
```


## Filter users whose age > 25 from an array of objects
```js
let users = [
    { name: "rahul", age: 20 },
    { name: "ajay", age: 18 },
    { name: "karan", age: 25 },
    { name: "akash", age: 15 },
    { name: "papa", age: 45 },
]

let teen = []
for (const user of users) {
    if (user.age > 25) {
        teen.push(user)
    }
}
console.log(teen)
```
## Convert array of strings to uppercase
```js
let str = ['rahul','ajay']

let uppercase = []

for (const element of str) {
    uppercase.push(element.toUpperCase())
    console.log(element)
}

console.log(uppercase)
```

## Find total price from cart items
```js


let cart = [
    { name: "Shirt", price: 500, qty: 2 },
    { name: "Jeans", price: 1200, qty: 1 },
    { name: "Shoes", price: 2000, qty: 1 }
];



var total = 1000
for (let i = 0; i <= cart.length - 1; i++) {
    total = total + (cart[i].price * cart[i].qty)
    console.log(total)
}

```

## Sort an array without using sort()
```js
let arr = [1, 8, 2, 6, 10];

for (let i = 0; i <= arr.length - 1; i++) {
    for (let j = 0; j <= arr.length - 1; j++) {
        if (arr[i] < arr[j]) {
            let temp = arr[i];
            arr[i] = arr[j];
            arr[j] = temp;
        }
    }
}
console.log(arr)
```

## Merge two arrays without duplicates
```js
let arr = [1, 2, 3, 4];
let arr1 = [5, 6, 7, 8];

let set = new Set()

for(let i=0;i<=arr.length-1;i++){
    set.add(arr[i])
}

for(let i=0;i<=arr1.length-1;i++){
    set.add(arr1[i])
}

let merged = [...set]
console.log(merged)
```

## Find second largest number in array
```js
let arr = [1, 2, 3, 4, 5];

let scndlrg = -Infinity
let largest = -Infinity

for (let i = 0; i <= arr.length - 1; i++) {
    if (arr[i] > largest) {
        scndlrg = largest
        largest = arr[i]
    }
}
console.log(scndlrg)
```
## Find largest number in array
```js
let arr = [1, 2, 3, 4, 5,20];

let largest = arr[0]

for (let i = 0; i <= arr.length - 1; i++) {
    if (arr[i] > largest) {
        largest = arr[i]
    }
}
console.log(largest)
```

## Group objects by a key (basic)
```js
let users = [
    { name: "Rahul", city: "Delhi" },
    { name: "Aman", city: "Mumbai" },
    { name: "Rohit", city: "Delhi" },
    { name: "Rohit", city: "Mumbai" },
];

let grouped = {};

for (const elem of users) {
    let key = elem.city;

    if (!grouped[key]) {
        grouped[key] = [];
    }

    grouped[key].push(elem);
}

console.log(grouped);
```

<!-- # 🖱️ SECTION 3: DOM & Events (REAL JOB SKILL) -->


# 🧠 SECTION 5: String + Number Logic (Very common)


## Count words in a sentence

```js
let arr = "I Love JavaScript"

let word = arr.split(" ")

console.log(word.length)
```
## Find first non-repeating character in a string

```js
let str = "aabbcde"

let freq = {}

for (let i = 0; i <= str.length - 1; i++) {
    let chr = str[i]
    if (freq[chr] === undefined) {
        freq[chr] = 1
    } else {
        freq[chr] += 1
    }
}
let ans = null
for (const ch of str) {
    if (freq[ch] === 1) {
        ans = ch
        break
    }
}
console.log(ans)
```

## Check if two strings are anagrams

```js
let str1 = "silent"
let str2 = "listen"

if (str1.length !== str2.length) {
    console.log("It's not an Anagram")
} else {
    let freq = {}
    for (let i = 0; i <= str1.length - 1; i++) {
        let ch = str1[i]
        if (freq[ch]) {
            freq[ch]++
        } else {
            freq[ch] = 1
        }
    }

    for (let j = 0; j <= str2.length - 1; j++) {
        let ch = str2[j]
        if (!freq[ch]) {
            console.log("It's not an Anagram")
            return
        } else {
            freq[ch]--
        }
    }
    console.log("It's an Anagram")
}
```
Main pehle dono strings ki length check karunga.
Phir first string ke characters ka frequency count banaunga.
Second string traverse karke frequency minus karunga.
Agar koi character missing ho ya count negative ho jaye to wo anagram nahi hai.

----
## Convert string to title case

```js
let str = "hello world from javascript"

let strArr = str.split(" ")

let res = []
for (let i = 0; i <= strArr.length - 1; i++) {
    let upper = strArr[i][0].toUpperCase()
    let remain = strArr[i].slice(1).toLowerCase()
    res.push(upper + remain)
}
console.log(res.join(" "))
```
## Count digits in a number

```js
let num = 12345

let digit = 0

while (num !== 0) {
    num = Math.floor(num / 10)
    digit++
}
console.log(digit)
```
## Reverse a number without built-in
```js
let num = 12345

let reverse = 0 

while (num !== 0) {
    let remainder = Math.floor(num % 10)
    reverse = reverse * 10 + remainder
    num = Math.floor(num / 10)
}
console.log(reverse)
```
## Find sum of digits of a number

```js
let num = 12345

let sum = 0

while (num !== 0) {
    let digit = num % 10
    sum += digit
    num = Math.floor(num / 10)
}
console.log(sum)
```
## Check if number is Armstrong
```js
let num = 153;
let original = num;

let digits = num.toString().length;
let sum = 0;

while (num !== 0) {
    let digit = num % 10;
    sum += digit ** digits;
    num = Math.floor(num / 10);
}

if (sum === original) {
    console.log("Armstrong Number");
} else {
    console.log("Not Armstrong");
}
```
## Remove spaces from a string
```js
let str = "hello world from js";

let res = ''
for (let i = 0; i <= str.length - 1; i++) {
    if (str[i] !== " ") {
        res += str[i]
    }
}
console.log(res)
```

## Check if number is Armstrong
```js
let num = 1533;
let original = num;

let digits = num.toString().length;  // total digits
let sum = 0;

while (num !== 0) {
    let digit = num % 10;          // last digit
    sum += digit ** digits;        // digit ^ totalDigits
    num = Math.floor(num / 10);    // remove last digit
}

if (sum === original) {
    console.log("Armstrong Number");
} else {
    console.log("Not Armstrong");
}
```
## Find longest word in a sentence

```js
let str = "Hello Javascript"

let newArr = str.split(" ")

let longest = newArr[0]


for (let i = 0; i <= newArr.length - 1; i++) {
    if (newArr[i].length > longest.length) {
        longest = newArr[i]
    }
}
console.log(longest) // output: Javascript
```