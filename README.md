 Hello

=========
* 1. Who is going to pay for the wall?
(https://www.codewars.com/kata/58bf9bd943fadb2a980000a7)
```javascript
function whoIsPaying(name){
   return (name.length > 2) ? ([name, name.substr(0,2)]):[name];
}
```
* 2. Numerical Palindrome #1
(https://www.codewars.com/kata/numerical-palindrome-number-1/train/javascript)
```javascript
  function palindrome(num) { 
    if (typeof num !== 'number' || num < 0){
      return 'Not valid';
    }
    const arr = +(num.toString().split('').reverse().join(''));
    return arr === num;
  } 
```
Another solution
``` javascript
function palindrome(num) { 
  let str = ""; 
  if (typeof num !== 'number' || num < 0) {
    return "Not valid";
  }  
  str = num + '';  
  for (let i = 0; i < Math.floor(str.length / 2); i++) {
    if (str[i] !== str[str.length - i - 1]) {
      return false;   
    }
  } 
  return true;
}
```
* new solution to TOG 
to master
* new solution into TOG
* second commit into TOG

* 3. 6 kata Simple reversed parenthesis
https://www.codewars.com/kata/simple-reversed-parenthesis/train/javascript
``` javascript
function solve(s){
  if (s.length%2) return -1;
  while (/\(\)/g.test(s)) s = s.replace(/\(\)/g, "");
  let cnt = 0;
  for (let i = 0; i < s.length -1; i += 2) {
    s[i] !== s[i + 1] ? cnt+=2 : cnt++;
  }
  return cnt;
}
```
* 4. Two fighters, one winner.
(https://www.codewars.com/kata/577bd8d4ae2807c64b00045b/solutions/java)
``` javascript
public class Kata {
    public static String declareWinner(Fighter fighter1, Fighter fighter2, String firstAttacker) {
      Fighter a=fighter1, b=fighter2;
      if (firstAttacker.equals(fighter2.name)) {
        a = fighter2; b = fighter1;
      }    
      while (true) {      
        if ((b.health -= a.damagePerAttack) <= 0) return a.name;  // a wins
        if ((a.health -= b.damagePerAttack) <= 0) return b.name;  // b wins
      }
    }
  }
```
* 5. Sum of a Beach 
(https://www.codewars.com/kata/5b37a50642b27ebf2e000010)
``` javascript
function sumOfABeach(beach) {
  let reg = /sand|water|fish|sun/gi;
  let arr = beach.match(reg);
  return !arr ? 0 : arr.length;
}
```
* 6. Array Leaders (Array Series #3)
(https://www.codewars.com/kata/5a651865fd56cb55760000e0)
```javascript
var arrayLeaders = num => {
  let arr = [];
  for(let i = 0; i < num.length; i++){
    let sum = 0;
    for(let j = i + 1  ; j < num.length; j++){
      sum += num[j];
    }
    if(num[i] > sum){
      arr.push(num[i]);
    }
  }
  return arr;
}
```
* 7. Building blocks
(https://www.codewars.com/kata/55b75fcf67e558d3750000a3)
```java
public class Block{
  private int width;
  private int length;
  private int height;
  private int volume;
  private int surface_area;
  
  // Constructor
  public Block(int[] params) {
    width = params[0];
    length = params[1];
    height = params[2];
    
    volume = width * length * height;
    surface_area = 2 * (width * length + width * height + length * height);
  }
  
  public int getWidth() {
    return width;
  }
  
  public int getLength() {
    return length;
  }
  
  public int getHeight() {
    return height;
  }
  
  public int getVolume() {
    return volume;
  }
  
  public int getSurfaceArea() {
    return surface_area;
  }
}
```
* 8. Playing with cubes
(https://www.codewars.com/kata/55c0a79e20be94c91400014b)
```java
public class Cube{
  
  private int Side;
  
  public void setSide(int num){
    this.Side = num;
  }
  
  public int getSide(){
    return this.Side;
  }
}
```
* 9. Fibonacci
```java
public class Fibonacci {
  public static long fib (int n){
    long f1 = 0;
    long f2 = 1;
    long f3 = 1; 
    for(int i = 1; i < n; i++){
      f3 = f1 + f2;
      f1 = f2;
      f2 = f3;
    }
    return f3;
  }
}
```
* 10. Convert number to reversed array of digits
```javascript
function digitize(n) {
  return n.toString().split('').reverse().map(el => +el);
}
```
* 11. Maximum Multiple
(https://www.codewars.com/kata/5aba780a6a176b029800041c)
```javascript
function maxMultiple(divisor, bound){
  let res = 0;
  for(let i = divisor; i <= bound; i += divisor){
    res = i;
  }
return res;
}
```
* 11.1 Maximum Multiple
```java
public class MaxMultiple {
  public static int maxMultiple(int divisor, int bound) {
    int res = 0;
    for(int i = divisor; i <= bound; i += divisor){
      res = i;
    }
    return res;
  }
}
```
* 12. Square(n) Sum
(https://www.codewars.com/kata/515e271a311df0350d00000f)
```java
public class Kata
 {
  public static int squareSum(int[] n)
  { 
   int sum = 0;
   for (int i = 0; i < n.length; i++){
     sum += n[i] * n[i];
   }
   return sum;
  }
 }
 ```
 * 13. Lario and Muigi Pipe Problem
 ```JavaScript
 (https://www.codewars.com/kata/56b29582461215098d00000f)
function pipeFix(num){
  let res = [];
  for(let i = num[0]; i <= num[num.length - 1]; i++){
      res.push(i);
  }
  return res;
}
```
* 14. Sort Out The Men From Boys
(https://www.codewars.com/kata/5af15a37de4c7f223e00012d)
```JavaScript
function menFromBoys(arr){
let arrMan = [];
let arrBoys = [];
  for(let i = 0; i < arr.length; i++){
    if(arr[i] % 2 === 0){
      arrMan.push(arr[i]);
    } else arrBoys.push(arr[i]);
  }
  arrMan.sort((a,b) => a-b);
  arrBoys.sort((a,b) => b-a);
  let res = [...new Set([...arrMan, ...arrBoys])];
  return res;
}
```
* 15. Discover The Original Price
(https://www.codewars.com/kata/552564a82142d701f5001228)
```JavaScript
function discoverOriginalPrice(discountedPrice, salePercentage){
  return +(discountedPrice /(100 - salePercentage) * 100).toFixed(2);
}
```
* 16. Sum of Multiples
(https://www.codewars.com/kata/57241e0f440cd279b5000829)
```JavaScript
function sumMul(n,m){
  let res = 0;
  for ( let i = n; i < m; i += n) res += i;  
  return res > 0 ? res : 'INVALID';
}
```
```javascript
function sumMul(n,m){
  let sum = 0;
  if(m <= 0) return 'INVALID';
  for(let i = n; i < m ; i+=n){
   sum += i 
  }
  return sum;
}
```
* 17. Number of People in the Bus
(https://www.codewars.com/kata/5648b12ce68d9daa6b000099)
```JavaScript
var number = function(busStops){
  return busStops.reduce((accum, [a,b]) => accum + a - b, 0)
}
```
* 18. Sum of Array Averages
```JavaScript
const sumAverage = (arr) => {
return Math.floor(arr.reduce((a,b)=>a+b.reduce((c,d)=>c+d)/b.length,0));
}
```
* 19. Discover The Original Price
```JavaScript
function discoverOriginalPrice(discountedPrice, salePercentage){
  return +(discountedPrice /(100 - salePercentage) * 100).toFixed(2);
}
```
* 20. Sum of Multiples
```JavaScript
function sumMul(n,m){
  let res = 0;
  for ( let i = n; i < m; i += n) res += i;  
  return res > 0 ? res : 'INVALID';
}
```
```javascript
function sumMul(n,m){
  let sum = 0;
  if(m <= 0) return 'INVALID';
  for(let i = n; i < m ; i+=n){
   sum += i 
  }
  return sum;
}
```
* 21. Sum of Multiples
```JavaScript
function sumMul(n,m){
  let sum = 0;
  if(m <= 0) return 'INVALID';
  for(let i = n; i < m ; i+=n){
   sum += i;
  }
  return sum;
}
```
* 22.Number of People in the Bus
(https://www.codewars.com/kata/5648b12ce68d9daa6b000099)
```JavaScript
var number = function(busStops){
  return busStops.reduce((accum, [a,b]) => accum + a - b, 0)
}
```
*. 23 Sum of Array Averages
(https://www.codewars.com/kata/56d5166ec87df55dbe000063)
```JavaScript
const sumAverage = (arr) => {
return Math.floor(arr.reduce((a,b)=>a+b.reduce((c,d)=>c+d)/b.length,0));
}
```
```javascript
const sumAverage = (arr) => {
  return Math.floor(arr.map(el => el.reduce((accum, current) => accum + current, 0)/el.length).reduce((accum, current) => accum + current, 0));
}
```
```JavaScript
const sumAverage = (arr) => {
  let res = 0;
  for(let i = 0; i < arr.length; i++){
    let sum = 0;
    for(let j = 0; j < arr[i].length; j++){
      sum += arr[i][j];
      console.log(sum)
    }
    res += sum/arr[i].length;
    console.log(res);
  }
  return Math.floor(res);
}
```
*. 24 Balanced Number (Special Numbers Series #1 )
https://www.codewars.com/kata/5a4e3782880385ba68000018
```JavaScript
function balancedNum(number){
  let numArr = number.toString().split('').map((d) => +d);
  let sumF = 0, sumB = 0;
  if(numArr.length <= 2) return 'Balanced';
console.log(numArr, Math.floor(numArr.length / 2));
  if(numArr.length%2 === 0){
    for(let i = 0; i < Math.floor(numArr.length / 2) - 1; i++){
      sumF += numArr[i];
      sumB += numArr[numArr.length-1-i];
console.log(sumF, sumB);
    }
  } else {
      for(let i = 0; i < Math.floor(numArr.length / 2); i++){
        sumF += numArr[i];
        sumB += numArr[numArr.length-1-i];
  console.log(sumF, sumB);
    }
  }
  return (sumF === sumB) ? 'Balanced' : 'Not Balanced';
}
```
*. 25 Who's Online?
https://www.codewars.com/kata/5b6375f707a2664ada00002a
```JavaScript
const whosOnline = (friends) => {
 let obj = {};
 for (let i = 0; i < friends.length; i++){
   if(friends[i].status === 'online' && friends[i].lastActivity <= 10){
     if(!obj.online){
       obj.online = [];
     }
       obj.online.push(friends[i].username);
   }
   if(friends[i].status === 'offline'){
     if(!obj.offline){
       obj.offline = [];
     }
       obj.offline.push(friends[i].username);
   }
   if(friends[i].status === 'online' && friends[i].lastActivity > 10){
     if(!obj.away){
       obj.away = [];
     }
       obj.away.push(friends[i].username);
   }
 }
 return obj;
}
```
*. 26 Player Contact Manager
(https://www.codewars.com/kata/5b203de891c7469b520000b4)
```JavaScript
function playerManager(players) {
  if(players === null || players.length === 0 ) {
    return [];
  }
  let arr = players.split(', ');
  let res = [];
  for(let i = 0; i < arr.length; i+= 2){
    let obj = {
      player: arr[i],
      contact: +arr[i+1]
    };
    res.push(obj);
  }
  return res;
}
```
*.27 The Office I - Outed
https://www.codewars.com/kata/57ecf6efc7fe13eb070000e1
```JavaScript
function outed(meet, boss){
const num = Object.values(meet);
num.push(meet[boss]);
let amount = Object.keys(meet).length;
let s = num.reduce((acc, curr) => acc + curr, 0);
return (s / amount <= 5) ? 'Get Out Now!' : 'Nice Work Champ!';
}
```
*. 27'1 The office I - Outed (another solution)
```javascript
function outed(meet, boss){
  let sum = 0;
  let count = 0;
  for (let key in meet){
    if(key === boss){
      sum = sum + meet[key] * 2;
    } else {
      sum = sum + meet[key];
    }
    count++;
  }
  if(sum/count <=5) {
    return 'Get Out Now!';
  } else {
    return 'Nice Work Champ!';
  }
}
```
*. 28 The Office II - Boredom Score
(https://www.codewars.com/kata/57ed4cef7b45ef8774000014)
```JavaScript
function boredom(staff){
  let sum = 0;
  let dep = {
    accounts: 1,
    finance: 2,
    canteen: 10, 
    regulation: 3, 
    trading: 6,
    change: 6,
    IS: 8,
    retail: 5,
    cleaning: 4,
    'pissing about': 25
  } 
  for (let key in staff){
    sum += dep[staff[key]];
  }
  if(sum <= 80){ return 'kill me now';}
  if(sum < 100 && sum > 80){ return 'i can handle this';}
  if(sum >= 100){return 'party time!!';}
}
```
*. 29 Last
```JavaScript
function last(...list){
let  str = list.join();
if(str.includes(',')) str = str.split(',');
return !isNaN(+str[str.length-1]) ? +str[str.length-1] : str[str.length-1];
}
```
*. 30 The Office II - Boredom Score
(The Office II - Boredom Score)
```JavaScript
function boredom(staff){
  let sum = 0;
  let dep = {
    accounts: 1,
    finance: 2,
    canteen: 10, 
    regulation: 3, 
    trading: 6,
    change: 6,
    IS: 8,
    retail: 5,
    cleaning: 4,
    'pissing about': 25
  } 
  for (let key in staff){
    sum += dep[staff[key]];
  }
  if(sum <= 80){ return 'kill me now';}
  if(sum < 100 && sum > 80){ return 'i can handle this';}
  if(sum >= 100){return 'party time!!';}
}
```
* 30. Breaking chocolate problem
(https://www.codewars.com/kata/534ea96ebb17181947000ada/train/javascript)
```JavaScript
function breakChocolate(n,m) {
  if( n === 0 || m === 0) return 0;
  return n * m - 1;
}
```
* 31. Simple Fun #1: Seats in Theater
(https://www.codewars.com/kata/588417e576933b0ec9000045)
```JavaScript
function seatsInTheater(nCols, nRows, col, row) {
  let x = nRows - row;
  let y = nCols - col + 1
  return x * y;
}
```
* 32. Sum of angles
https://www.codewars.com/kata/5a03b3f6a1c9040084001765
```JavaScript
function angle(n) {
  return 180 * (n - 2);
}
```
* 33. DNA to RNA Conversion
https://www.codewars.com/kata/5556282156230d0e5e000089
```JavaScript
function DNAtoRNA(dna) {
  let rna = dna.replace(/t/gi, 'U');
  return rna;
}
```
* 34. Grasshopper - Order of operations
https://www.codewars.com/kata/560ecf0cb040de130e00007d
```JavaScript
function orderOperations () {
  return (2 + 2) * (2 + 2) * 2;
}
```
* 35. Century From Year
https://www.codewars.com/kata/5a3fe3dde1ce0e8ed6000097/train/javascript
```JavaScript
function century(year) {
  return Math.ceil(year/100); //using ceiling method to round up to nearest century (100)
}
```
* 36. Fix the Bugs (Syntax) - My First Kata
https://www.codewars.com/kata/56aed32a154d33a1f3000018/train/javascript
```JavaScript
function myFirstKata(a, b) {
  if (typeof(a) !== "number" || typeof(b) !== "number") {
    return false;
  } else {
    return a % b + b % a;
  }
}
```
* 37. Convert a Number to a String!
https://www.codewars.com/kata/5265326f5fda8eb1160004c8/train/javascript
```JavaScript
function numberToString(num) {
  return num.toString();
}

function numberToString(num) {
  return ''+num;
}

function numberToString(num) {
  return String(num);
}
```
* 38. Number toString
https://www.codewars.com/kata/53934feec44762736c00044b/train/javascript
```JavaScript
let a = String(123);

```
* 39.Well of Ideas - Easy Version
https://www.codewars.com/kata/57f222ce69e09c3630000212/train/javascript
```JavaScript
function well(x){
  let a = x.filter(el => el === 'good').length;
  return (a > 2) ? 'I smell a series!' : (a >= 1) ? 'Publish!' : 'Fail!'
}
```
* 40. Keep Hydrated!
https://www.codewars.com/kata/582cb0224e56e068d800003c/solutions/javascript
```JavaScript
function litres(time) {
  return Math.floor(time * 0.5);
}
```
 * 41. Rock Paper Scissors!
https://www.codewars.com/kata/5672a98bdbdd995fad00000f/train/javascript
```JavaScript
 const rps = (p1, p2) => {
  if(p1===p2) return 'Draw!';
  if (p1==='rock' && p2==='scissors' || p1==='scissors' && p2==='paper' || p1==='paper' && p2==='rock') return 'Player 1 won!';
  else return 'Player 2 won!'
};
```
* 42. L1: Set Alarm
https://www.codewars.com/kata/568dcc3c7f12767a62000038/train/javascript
```JavaScript
function setAlarm(employed, vacation){
  return employed && !vacation;
}
```
* 42. Student's Final Grade
https://www.codewars.com/kata/5ad0d8356165e63c140014d4/train/javascript
```JavaScript
function finalGrade (exam, projects) {
  if (exam > 90 || projects > 10) return 100;
  if (exam > 75 && projects >= 5) return 90;
  if (exam > 50 && projects >=2) return 75;
  return 0;
}
```
* 43. Plural
https://www.codewars.com/kata/52ceafd1f235ce81aa00073a/solutions/javascript
```JavaScript
function plural(n) {
  return n !== 1;
}
```
* 44. Days in the year
https://www.codewars.com/kata/56d6c333c9ae3fc32800070f/train/javascript
```JavaScript
function yearDays(y) {
  return (y%400===0 && Number.isInteger(y/100) || y%4===0 && !Number.isInteger(y/100))  ? `${y} has 366 days` : `${y} has 365 days`;
}
```
* 45. Be Concise I - The Ternary Operator
https://www.codewars.com/kata/56f3f6a82010832b02000f38/train/javascript
```JavaScript
function describeAge(age) {
  return "You're a(n) " + (age<=12? 'kid' : age<=17? 'teenager' : age<=64? 'adult' : 'elderly');
}
```
```JavaScript
function describeAge(age) {
  return `You're a(n) ${age<13 ? 'kid' : age<18 ? 'teenager' : age<65 ? 'adult' : 'elderly'}`;
}
```
* 46. 101 Dalmatians - squash the bugs, not the dogs!
https://www.codewars.com/kata/56f6919a6b88de18ff000b36/
```JavaScript
function howManyDalmatians(n) {
  var d = ["Hardly any", "More than a handful!", "Woah that's a lot of dogs!", "101 DALMATIANS!!!"];
  var respond = (n<=10 ? d[0] : n<=50 ? d[1] : n==101 ? d[3] : d[2]);
  return respond;
}
```
* 48. Training JS #7: if..else and ternary operator
https://www.codewars.com/kata/57202aefe8d6c514300001fd/solutions/javascript
```JavaScript
function saleHotdogs(n){
  return (n<5 ? n*100 : (n>=5 && n<10) ? n*95 : n>=10 ? n*90 : '');
}
```
* 49. Testing, Testing! Return and concatenate a string.
https://www.codewars.com/kata/5977387e131c07082b000098/train/javascript
```JavaScript
function getRes(myScore) {
  return `${myScore>=70 ? "Congratulations, you have passed!" : "Sorry, you have failed. Better luck next time!"} Thank you for taking part.`
}
```
* 50. GCD sum
https://www.codewars.com/kata/5dd259444228280032b1ed2a/train/javascript
```JavaScript
function solve(x, y) {
  return x % y ? -1 : [y, x - y];
}
```
 * 51. Какой день недели
 ```JavaScript
//  Дни недели пронумерованы так: 0 - 'Sunday', 1 - 'Monday', 2 - 'Tuesday', 3 - 'Wednesday', 4 - 'Thursday', 5 - 'Friday', 6 - 'Saturday'.

// Дано целое число k (от 1 до 365). Определите название дня недели для k-го дня года, если считать, что 1 января был понедельник.

// Напишите функцию с именем dayOfWeek, которая принимает число k в качестве аргумента (число от 1 до 365 - номер дня года) и возвращает название дня недели.

// Примеры:

// функция dayOfWeek(3) должна возвратить "Wednesday";
// функция dayOfWeek(14) должна возвратить "Sunday".
function dayOfWeek(k){
    switch(k%7) {
    case 0:
      return 'Sunday';
      break;
    case 6:
      return 'Saturday';
      break;
     case 5:
      return 'Friday';
      break;
     case 4:
      return'Thursday';
      break;
     case 3:
      return 'Wednesday';
      break;
    case 2:
      return 'Tuesday';
      break;
    case 1:
      return 'Monday';
      break;
  }
}

