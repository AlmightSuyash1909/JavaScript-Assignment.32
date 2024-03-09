#### Understanding copy by reference

```js
let brothers = ['John', 'Bran', 'Robb'];

let house = 'Stark';

let user = {
  name: 'Arya',
  house: house,
  brothers: brothers,
};

let user2 = {
  name: 'Arya',
  house: house,
  brothers: brothers,
};

let user3 = {
  name: 'Arya',
  house: 'Stark',
  brothers: ['John', 'Bran', 'Robb'],
};
```

1. After going through above code answer the following with reason:

user.house === user2.house; // output: ture
user.house == user2.house; // output: true
user.brothers === user2.brothers; // output: true
user.brothers == user2.brothers; // output: ture
user.name == user2.name; // output: true
user.name === user2.name; // output: true
user.brothers == user3.brothers; // output: false
user.brothers === user3.brothers; // output: false
user.house === user2.house; // output:  true
user.house === user3.house; // output: true
user.brothers[0] === user2.brothers[0]; // output: true
user.brothers[0] === user3.brothers[0]; // output: true

2. Copy the value of character variable into variable named characterOne and characterTwo.

```js
let character = {
  charactorName: 'Sansa',
  sisters: 1,
  brothers: 4,
};
```
// Your code
```js
let characterOne = character; 
let characterTwo = character; 
```

Check the output of below code after copying. The output of all of all of the below should be true

character === characterOne; // output: true
characterOne == characterTwo; // output: true
characterTwo == character; // output: true

3. Clone (no reference) the value of character variable into variables named characterThree and characterFour.

```js
let character = {
  charactorName: 'Sansa',
  sisters: 1,
  brothers: 4,
};
```
// Your code
```js
let characterThree = {
  charactorName: 'Sansa',
  sisters: 1,
  brothers: 4,
}
let characterFour = {
  charactorName: 'Sansa',
  sisters: 1,
  brothers: 4,
}
```

Check your result by comparing the values: All the below result should be false.

character === characterThree;
characterThree == characterFour;
characterFour == character;