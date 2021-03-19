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
```
* 52. Basic Calculator
https://www.codewars.com/kata/5296455e4fe0cdf2e000059f/train/javascript
```JavaScript
function calculate(n1, operation, n2) {
   switch(operation) {
       case '+':
         return n1 + n2;
         break;
       case '-':
         return n1 - n2;
         break;
       case '*':
         return n1 * n2;
         break;
       case '/':
         return n2 !== 0 ? n1 / n2 : null;
         break;
       default:
          return null;
   }
}
```
* 53. No zeros for heros
https://www.codewars.com/kata/no-zeros-for-heros
```JavaScript
function noBoringZeros(n) {
  while (n % 10 === 0 && n !==0){
    n /= 10;
  } 
  return n;
}
```
* 54. Going to the cinema
https://www.codewars.com/kata/562f91ff6a8b77dfe900006e/solutions/javascript
```JavaScript
function movie(card, ticket, perc) {
  let count = 0,
      a = 0,
      b = card,
      ticketB = ticket;
  
  while(Math.ceil(a) <= Math.ceil(b)) {
    a = a + ticket;
    ticketB = ticketB * perc;
    b += ticketB;
    count++;
  }
  return count;
};
```
* 55. Power of two
https://www.codewars.com/kata/534d0a229345375d520006a0
```JavaScript
function isPowerOfTwo(n){
  while(n>=2) {
    n = n/2;
  } return n === 1;
}
```
* 56. Draw stairs
https://www.codewars.com/kata/5b4e779c578c6a898e0005c5/train/javascript
```JavaScript
function drawStairs(n) {
  let a = '';
  for (let i = 0; i < n; i++){
    if(i < n-1) {
      a += ' '.repeat(i) + 'I\n';
    } else {
      a += ' '.repeat(i) + 'I';
    }
  }
  return a;
}
```
* 57. The Skiponacci Sequence
https://www.codewars.com/kata/580777ee2e14accd9f000165/train/javascript
```JavaScript
function skiponacci(n) {
  let fib = [1,1];
  for(let i = 2; i < n; i++){
    fib.push(fib[i-2] + fib[i-1]);
  }
  return n === 1 ? '1' : fib.map((el,i) => i % 2 ? 'skip' : el).join(' ');
}
```
* 57. Money, Money, Money
https://www.codewars.com/kata/563f037412e5ada593000114/train/javascript
```JavaScript
function calculateYears(principal, interest, tax, desired) {
    // your code
    var years = 0;
    while(principal < desired){
      principal += (principal * interest) * (1 - tax);
      years++;
    }
    return years;
}
```
* 58. The wheat/rice and chessboard problem
https://www.codewars.com/kata/5b0d67c1cb35dfa10b0022c7/train/javascript
```JavaScript
function squaresNeeded(grains){
  let s = 0;
  while(2 ** s - 1 < grains) {
    s++;
  }
  return s;
}
```
* 59. Find the divisors!
https://www.codewars.com/kata/544aed4c4a30184e960010f4/solutions/javascript
```JavaScript
function divisors(integer) {
  var divs = [];
  
  for(var i = 2; i < integer; i++) {
    if(integer % i === 0) {
      divs.push(i);
    }
  }
  
  return divs.length ? divs : integer + ' is prime';
};
```
* 60. Round up to the next multiple of 5
https://www.codewars.com/kata/55d1d6d5955ec6365400006d/train/javascript
```JavaScript
function roundToNext5(n){
  while(n % 5){
    n++;
  }
  return n;
}
```
* 61. Training JS #9: loop statement --while and do..while
https://www.codewars.com/kata/57216d4bcdd71175d6000560/train/javascript
```JavaScript
function padIt(str,n){
  let i = 1;
  while (i <= n) {
    if(i % 2) {
      str = '*' + str;
    } else {
      str = str + '*';
    }
    i++;
  }
  return str;
}
=======
ffunction padIt(str,n){
  // while
  if (n % 2 === 0) {
    return '*'.repeat(n/2) + str + '*'.repeat(n/2);
  } else {
    return '*'.repeat((n+1)/2) + str + '*'.repeat((n-1)/2);
  }
}
```
* 62. Halving Sum
https://www.codewars.com/kata/5a58d46cfd56cb4e8600009d/train/javascript
```JavaScript
function halvingSum(n) {
  let sum = n;
  while(n >= 1) {
    n = Math.trunc(n/2);
    sum += n;
  }
  return sum;
}
```
* 63.Array Leaders (Array Series #3)
https://www.codewars.com/kata/5a651865fd56cb55760000e0/train/javascript
```JavaScript
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
* 64. Draw stairs
https://www.codewars.com/kata/5b4e779c578c6a898e0005c5/train/javascript
```JavaScript
function drawStairs(n) {
  let a = '';
  for (let i = 0; i < n; i++){
    if(i < n-1) {
      a += ' '.repeat(i) + 'I\n';
    } else {
      a += ' '.repeat(i) + 'I';
    }
  }
  return a;
}
```
* 65. DNA to RNA Conversion
https://www.codewars.com/kata/5556282156230d0e5e000089
```JavaScript
function DNAtoRNA(dna) {
  let rna = dna.replace(/t/gi, 'U');
  return rna;
}
```
* 66. Difference Of Squares
https://www.codewars.com/kata/558f9f51e85b46e9fa000025
```JavaScript
function differenceOfSquares(n){
  let sqS = 0,
      sSq = 0,
      i = 1;
  while(i <= n) {
    sqS += i;
    sSq += i**2;
    i++
  }
  return sqS**2 - sSq;
}
```
* 67. Power of 3
https://www.codewars.com/kata/57be674b93687de78c0001d9
```JavaScript
function largestPower(n){
  let k = 0;
  while(3**k < n){
    k++;
  }
  return k-1;
}
```
* 68. Round up to the next multiple of 5
https://www.codewars.com/kata/55d1d6d5955ec6365400006d
```JavaScript
function roundToNext5(n){
  while(n % 5 !== 0){
    n++;
  }
  return n;
}
```
* 69. Training JS #10: loop statement --for
https://www.codewars.com/kata/5721a78c283129e416000999
```JavaScript
function sum1_100(){
  var sum=0,num=1
  while (num<=100){
    sum+=num;
    num++;
  }
  return sum;
}
```
* 70. Find the divisors!
https://www.codewars.com/kata/544aed4c4a30184e960010f4
```JavaScript
function divisors(integer) {
  var arr = [];
  
  for(let i = 2; i < integer; i++) {
    if(integer % i === 0) {
      arr.push(i);
    }
  }
  return arr.length ? arr : integer + ' is prime';
};
```
```JavaScript
function isPrime(n){
  if(n <= 1) return false;
  for(let i = 2; i < Math.round(Math.sqrt(n) + 1); i++){
    if(n % i === 0) return false;
  }
  return true;
}
function divisors(integer) {
  let arr = [];
  if(isPrime(integer)) return integer + ' is prime';
  for(let i = 2; i < integer; i++){
    if(integer % i === 0) {
      arr.push(i);
    }
  }
  return arr;
};
```
* 71. Halving Sum
https://www.codewars.com/kata/5a58d46cfd56cb4e8600009d
```JavaScript
function halvingSum(n) {
  let sum = n;
  while(n >= 1) {
    n = Math.trunc(n/2);
    sum += n;
  }
  return sum;
}

* 72. Power
https://www.codewars.com/kata/562926c855ca9fdc4800005b
function numberToPower(number, power){
  let res = 1;
  let i = 1;
  while (i <= power) {
   res = number * res;
   i++;
  } 
  return res;
}
// 2d solution
function numberToPower(number, power){
  let res = 1;
  let i = 1;
  while (i <= power) {
   res = number * res;
   i++;
  } 
  return res;
}
// 3d solution
function numberToPower(number, power){
  let mult = 1;
  for(let i = 1; i <= power; i++){
    mult = mult * number;
  }
  return mult;
}

* 73. Training JS #9: loop statement --while and do..while
https://www.codewars.com/kata/57216d4bcdd71175d6000560
function padIt(str,n){
  // while
  if (n % 2 === 0) {
    return '*'.repeat(n/2) + str + '*'.repeat(n/2);
  } else {
    return '*'.repeat((n+1)/2) + str + '*'.repeat((n-1)/2);
  }
}
* 74. "Very Even" Numbers.
https://www.codewars.com/kata/58c9322bedb4235468000019
function isVeryEvenNumber(n) {
  n = String(n);
  while(n.length > 1) {
    let sum = 0;
    for(let i = 0; i < n.length; i++){
      sum += +n[i];
    }
    n = sum + '';
  }
  return !(+n%2);
}

* 75. Total amount of points
https://www.codewars.com/kata/5bb904724c47249b10000131
function points(games) {
  let s = 0;
  games.forEach((el,i) => el[0] > el[2] ? s +=3 : el[0] === el[2] ? s +=1 : s);
  return s;
}

* 76. GCD sum
https://www.codewars.com/kata/5dd259444228280032b1ed2a
function solve(s,g){
   return ((s-g)%g===0 && g%g===0) ? [g, s-g] : -1;
}

* 77. Round up to the next multiple of 5
https://www.codewars.com/kata/55d1d6d5955ec6365400006d
function roundToNext5(n){
  while(n % 5 !== 0){
    n++;
  }
  return n;
}

* 78. Money, Money, Money
https://www.codewars.com/kata/563f037412e5ada593000114
function calculateYears(principal, interest, tax, desired) {
  let y = 0;
    while(principal < desired){
      principal = principal + principal * interest - principal * interest * tax;
      y++;
    }
  return y;
}

* 79. Help the Fruit Guy
https://www.codewars.com/kata/557af4c6169ac832300000ba/solutions/javascript
function removeRotten(arr){
    return arr ? arr.map(x=>x.replace('rotten', '').toLowerCase()) : [] ;
}

* 80. 
// Напишите функцию с именем numericalTable, которая принимает число n в качестве аргумента и возвращает таблицу чисел от 1 до n. Каждая строка содержит 5 чисел, разделенных пробелом. Все строки кроме последней, заканчиваются символом \n перевода строки.

// Например, для n = 4 должна быть получена строка:

// "1 1 1 1 1\n2 2 2 2 2\n3 3 3 3 3\n4 4 4 4 4"

function numericalTable(n){
  let res = '';
  for (let i = 1; i <= n; i++){
    for (let j = 1; j <= 5; j++) {
      res = res + i + ' ';
    }
    // res = res.trim();
    res = res.slice(0,-1);
    res += '\n';
  }
  return res.trim();
}
console.log(numericalTable(4));

// Нарисовать числовой треугольник
// "1
// 2 2
// 3 3 3
// 4 4 4 4
// 5 5 5 5 5"
function numericalTriangle(n){
  let res = '';
  for (let i = 1; i <= n; i++) {
    res = res + ((i + ' ').repeat(i)).trim() + '\n';
  }
  return res.trim();
}

//let s = 'hello'.repeat(5);

// "*
// **
// ***
// ****
// *****
// ******
// *******"
function starTriangle(n){
  let res = '';
  for(let i = 1; i <= n; i++){
    res += '*'.repeat(i) + '\n';
  }
  return res.trim();
}
console.log(starTriangle(7));

// ****
// ***
// **
// *
function triangle(n){
  let res = '';
  for (let i = n; i > 0; i--){
    res += '*'.repeat(i) + '\n';
  }
  return res.trim();
}
console.log(triangle(5));

function triangle(n){
  let arr = [];
  for (let i = n; i > 0; i--){
    arr.push('*'.repeat(i));
  }
  return arr;
}
console.log(triangle(5));

* 81. Start with a Vowel
function vowelStart(str){
  return str.toLowerCase().replace(/[^0-9a-z]/g, '').replace(/[auioe]/g, el=>' ' + el).trim();
}

* 82. Fake Binary
https://www.codewars.com/kata/57eae65a4321032ce000002d
function fakeBin(x){
  return x.replace(/[0-4]/g, '0').replace(/[5-9]/g, '1');
}

* 83. Help the Fruit Guy
function removeRotten(bagOfFruits){
  return bagOfFruits && bagOfFruits.length ? bagOfFruits.join(',').replace(/rotten/g, '').toLowerCase().split(',') : [];
}

* 84. Fake Binary
function fakeBin(x){
  return x.replace(/[0-4]/g, '0').replace(/[5-9]/g, '1');
}

* 85. vowel remover
function shortcut(string){
  return string.replace(/[auioe]/g, '');
}

* 86. Function 2 - squaring an argument
https://www.codewars.com/kata/523b623152af8a30c6000027/train/javascript
function square(x){
  return x**2;
}

* 87. Get the mean of an array
https://www.codewars.com/kata/563e320cee5dddcf77000158/train/javascript
function getAverage(marks){
  let sum = 0;
  for(let i = 0; i < marks.length; i++){
    sum += marks[i];
  }
  return Math.floor(sum/marks.length);
}

* 88. Split Strings
https://www.codewars.com/kata/515de9ae9dcfc28eb6000001
function solution(str){
  if(str.length % 2 !== 0 ){
     str += '_';
   }
  let arr = str.split('');
  let res = [];
  for(let i = 0; i < arr.length; i=i+2){
    res.push(arr[i] + arr[i+1]);
  }
  return res;
}

* 89. Round up to the next multiple of 5
https://www.codewars.com/kata/55d1d6d5955ec6365400006d
function roundToNext5(n){
  while(n % 5 !== 0){
    n++;
  }
  return n;
}

* 90. 
// Во многих школах применяется цифровая пятибалльная система оценки успеваемости учащихся:

// 5 - Excellent
// 4 - Good
// 3 - Satisfactory
// 2 - Unsatisfactory
// 1 - Bad
// Дана отметка (цифра). Получить словесное значение отметки.

// Создайте переменную mark и присвойте ей значение целого числа от 1 до 5. Создайте переменную name, в которой получите словесное значение отметки. Используя оператор switch, получите в переменной name значения:

// 'Excellent', если mark = 5,
// 'Good', если mark = 4,
// 'Satisfactory', если mark = 3,
// 'Unsatisfactory', если mark = 2,
// 'Bad', если mark = 1,
// 'Error', в противном случае.
// Приведем пример, который принципиально похож на то, что нужно сделать, но адаптируйте его к требованиям задачи:

const mark = 4;
let name;
switch (mark) {
  case 1:
    name = 'Bad';
    break;
  case 2:
    name = 'Unsatisfactory';
    break;
  case 3:
    name = 'Satisfactory';
    break;
  case 4:
    name = 'Good';
    break;
  case 5:
    name = 'Excellent';
    break;
  default:
    name = 'Error';
}

// // Количество планет в Солнечной системе – 8, в порядке удаления от Солнца они располагаются так: Меркурий, Венера, Земля, Марс, Юпитер, Сатурн, Уран и Нептун. По номеру планеты получить ее название.

// Создайте переменную id и присвойте ей значение целого числа от 1 до 8 (номер планеты). Создайте переменную name. Используя оператор switch, получите в переменной name значения:

// 'Mercury', если id = 1
// 'Venus', если id = 2
// 'Earth', если id = 3
// 'Mars', если id = 4
// 'Jupiter', если id = 5
// 'Saturn', если id = 6
// 'Uranus', если id = 7
// 'Neptune', если id = 8
const id = 6;
let name;
switch (id) {
  case 1: name = 'Mercury'; break;
  case 2: name = 'Venus'; break;
  case 3: name = 'Earth'; break;
  case 4: name = 'Mars'; break;
  case 5: name = 'Jupiter'; break;
  case 6: name = 'Saturn'; break;
  case 7: name = 'Uranus'; break;
  case 8: name = 'Neptune'; break;
}

* 90. Quarter of the year
codewars.com/kata/5ce9c1000bab0b001134f5af/train/javascript
const quarterOf = (month) => {
  console.log(month)
  if(month === 1 || month === 2 || month === 3) {
    return 1;
  } else if(month === 4 || month === 5 || month === 6) {
    return 2;
  } else if(month === 7 || month === 8 || month === 9) {
    return 3;
  } else {
    return 4
  }
}

* 91. How much water do I need?
function howMuchWater(water, load, clothes){
 return clothes > load * 2 ? 
  'Too much clothes' : 
  (clothes < load ? 'Not enough clothes' : 
  Number(( water * 1.1 ** (clothes - load)).toFixed(2))
  )
}

* 92. 
// Найдите сумму чисел 0.1 + 0.2 + 0.3 + ... + 5

let sum = 0;
let x = 0.1;
while (x <= 5) {
  sum = sum + x;
  x = x + 0.1;
}

* 93 . Найдите сумму 1 + 1/2 + 1/3 + 1/4 + ... + 1/10.
let sum = 0;
let x = 1;
while (x <= 10) {
  sum = sum + 1/x;
  x = x + 1;
}

* 94. Найдите сумму элементов массива, содержащего четные числа от 2 до 20
const arr = [2, 4, 6, 8, 10, 12, 14, 16, 18, 20];
let sum = 0;
let i = 0;
while (i < arr.length) {
  sum = sum + arr[i];
  i++;
}

* 95. Найдите произведение чисел 0.3 * 0.6 * 0.9 * ... * 3
let product = 1;
let x = 0.3;
while (x <= 3) {
  product = product * x;
  x = x + 0.3;
}

* 96. Вычислите 2 в степени 15
let power = 1;
for (let x = 1; x <= 15; x++) {
  power = power * 2;
}

* 97. Найдите факториал числа 7.
Факториал числа — это произведение натуральных чисел от 1 до самого числа (включая данное число). Обозначается факториал восклицательным знаком «!». Например, 5! = 1*2*3*4*5

Создайте переменную с именем factorial, используйте ключевое слово let, присвойте начальное значение: 1. Создайте цикл for, в котором заголовок цикла содержит:

начальное значение переменной x = 1;
условие цикла x <= 7;
шаг x++ (переменная x увеличивается на 1 после каждого выполнения тела цикла) В теле цикла запишите:
команду, которая умножает значение переменной factorial на число x;
Приведем пример, который принципиально похож на то, что нужно сделать, но адаптируйте его к требованиям задачи:
let factorial = 1;
for (let x = 1; x <= 7; x++) {
  factorial = factorial * x;
}

* 98. Найдите сумму четных чисел от 2 до 200.
let sum = 0;
for (let i = 2; i <= 200; i += 2) {
  sum = sum + i;
}

* 99. Найдите сумму чисел, кратных 3, в диапазоне от 12 до 120.
Создайте переменную с именем sum, используйте ключевое слово let, присвойте начальное значение: 0. Создайте цикл for, в котором заголовок цикла содержит:

начальное значение переменной i = 12;
условие цикла i <= 120; (конечное значение переменной i)
шаг i+=3 (переменная i увеличивается на 3 после каждого выполнения тела цикла) В теле цикла запишите:
команду, которая увеличивает значение переменной sum на число i;
Приведем пример, который принципиально похож на то, что нужно сделать, но адаптируйте его к требованиям задачи:
let sum = 0;
for (let i = 12; i <= 120; i += 3) {
  sum = sum + i;
}

* 100. Создайте массив из двадцати нулей
const arr = [];
for (let i = 0; i < 20; i++) {
  arr.push(0);
}

* 101.Создайте массив, содержащий десять чисел, являющихся степенями числа 2.
const power = [];
for (let i = 0; i < 10; i++) {
  power.push(2**i);
}

* 102. Сколько получится, если число 2020 десять раз делить на 2?
let number = 2020;
for (let i = 1; i <= 10; i++) {
  number = number / 2;
}

* 103. Как Клавдия покупала конфеты.
У Клавдии было 200 долларов. В первый день она купила конфет на сумму 3 доллара, во второй день - на 6 долларов, и каждый день сумма покупки увеличивалась на 3 доллара. Так она поступала 10 дней, пока не посмотрела на себя в зеркало. Сколько денег осталось у Клавдии после 10 покупок?

Создайте переменную с именем money, используйте ключевое слово let, присвойте начальное значение: 200. Создайте переменную с именем candy, используйте ключевое слово let, присвойте начальное значение: 3.

Создайте цикл for, в котором заголовок цикла содержит:

начальное значение счетчика цикла i = 1;
условие цикла i <= 10; (покупки делались в течение 10 дней)
шаг i++ (переменная i увеличивается на 1 после каждого выполнения тела цикла) В теле цикла запишите:
команду, которая уменьшает значение переменной money на стоимость покупки candy;
команду, которая увеличивает значение переменной candy на 3.
Приведем пример, который принципиально похож на то, что нужно сделать, но адаптируйте его к требованиям задачи:
let cash = 150;                 // начальное количество денег
let cost = 3;                     // стоимость покупки в первый день
for (let i = 1; i <= 10; i++){  // покупки продолжаются в течение 10 дней
 cash = cash - cost;          // количество денег уменьшается каждый день на стоимость покупки
 cost = cost + 3;               // стоимость покупки каждый день увеличивается на 3
}

let money = 200;
let candy = 3;
for (let i = 1; i <= 10; i++) {
  money = money - candy;
  candy = candy + 3;
}

* 104. Получить строку "Abc Abc Abc Abc"
Создайте переменную с именем result, используйте ключевое слово let, присвойте значение пустой строки: ''. Создайте переменную (счетчик цикла) с именем i, используйте ключевое слово let, присвойте значение 0. Создайте цикл do, который выполняется 4 раза. Для этого после слова do в фигурных скобках напишите команды тела цикла:

команду, увеличивающую значение переменной i на 1;
команду, которая изменяет значение переменной result, прибавляя к строке result строку 'Abc '; После слова while в скобках напишите условие (i < 4).
Приведем пример, который принципиально похож на то, что нужно сделать, но адаптируйте его к требованиям задачи:

let result = '';
let i = 0;
do {
  i = i + 1;
  result = result + 'Abc ';
} while (i < 4)

* 105. Получить строку "12345"
Создайте переменную с именем result, используйте ключевое слово let, присвойте значение пустой строки: ''. Создайте переменную с именем i, используйте ключевое слово let, присвойте значение 0. Создайте цикл do, который выполняется 5 раз. Для этого после слова do в фигурных скобках напишите команды тела цикла:

команду, увеличивающую значение переменной i на 1;
команду, которая изменяет значение переменной result, прибавляя к строке result число i; После слова while в скобках напишите условие (i < 5).
Приведем пример, который принципиально похож на то, что нужно сделать, но адаптируйте его к требованиям задачи:

let str = '';
let i = 0;
do {
  i = i + 1;
  str = str + i; // результатом будет строка "12345678910"
} while (i < 10);

let result = '';
let i = 0;
do {
  i = i + 1;
  result = result + i;
} while (i < 5)

* 106. Получить массив [1, 2, 3, 4, 5, 6, 7, 8]
Создайте переменную с именем arr, используйте ключевое слово const, присвойте значение пустого массива [].

Создайте переменную цикла с именем i, используйте ключевое слово let, присвойте значение 0.

Создайте цикл do, который выполняется 8 раз.

Для этого после слова do в фигурных скобках напишите команды тела цикла:

команду, увеличивающую значение переменной i на 1;
команду, которая добавляет значение i в конец массива. После слова while в скобках напишите условие (i < 8).
Приведем пример, который принципиально похож на то, что нужно сделать, но адаптируйте его к требованиям задачи:

const array = [];
let i = 0;
do {
  i = i + 1;
  array.push(i); // результатом будет массив [1, 2, 3, 4, 5]
} while (i < 5);

const arr = [];
let i = 0;
do {
  i = i + 1;
  arr.push(i);
} while (i < 8)

* 107. Получить массив [1, 0, 1, 0, 1, 0, 1, 0, 1, 0]
Создайте переменную с именем arr, используйте ключевое слово const, присвойте значение пустого массива [].

Создайте переменную (счетчик цикла) с именем i, используйте ключевое слово let, присвойте значение 0.

Последовательность чисел 1, 0 повторяется в массиве 5 раз, поэтому организуем цикл do, который выполняется 5 раз.

Для этого после слова do в фигурных скобках напишите команды тела цикла:

команду, увеличивающую значение переменной i на 1;
команду, которая добавляет числа 1, 0 в конец массива.
после слова while в скобках напишите условие (i < 5).
Приведем пример, который принципиально похож на то, что нужно сделать, но адаптируйте его к требованиям задачи:

const array = [];
let i = 0;
do {
  i = i + 1;
  array.push(2, 1);    // результатом будет массив [2, 1, 2, 1, 2, 1, 2, 1]
} while (i < 4);
Write your solution here
unit
const arr = [];
let i = 0;
do {
  i = i + 1;
  arr.push (1,0);
} while (i < 5)
const arr = [];
let i = 0;
do {
  i = i + 1;
  arr.push (1,0);
} while (i < 5)


* 108. Считаем овец перед сном.
Говорят, что когда не можешь заснуть, надо считать овец. Составьте строку, которая "посчитает" 30 овец: "1 sheep...2 sheep...3 sheep..."

Создайте строку str, присвойте значение пустой строки ''. Создайте переменную (счетчик цикла) с именем i, используйте ключевое слово let, присвойте значение 0.

Создайте цикл do, который будет выполняться 30 раз.

Для этого после слова do в фигурных скобках напишите команды тела цикла:

команду, увеличивающую значение переменной i на 1;
команду, которая прибавляет к переменной str строку ${i} sheep...
После слова while в скобках напишите условие (i < 30).

Приведем пример, который принципиально похож на то, что нужно сделать, но адаптируйте его к требованиям задачи:

let s = '';
let i = 0;
do {
  i = i + 1;
  s = s + `${i} monkey...`
} while (i < 10);
Write your solution here
unit
let str = '';
let i = 0;
do {
  i = i + 1;
  str = str + `${i} sheep...`;
} while (i < 30)

* 109. Cекунды до старта
Составьте строку, которая "отсчитывает" секунды до старта ракеты: "10 seconds...9 seconds...8 seconds...7 seconds...6 seconds...5 seconds...4 seconds...3 seconds...2 seconds...1 second"

Создайте строку timer, присвойте значение пустой строки ''. Создайте переменную (счетчик цикла) с именем i, используйте ключевое слово let, присвойте значение 10.

Создайте цикл do, который будет выполняться 9 раз (прибавление числа и слова "seconds...")

Для этого после слова do в фигурных скобках напишите команды тела цикла:

команду, которая прибавляет к переменной timer строку {i} seconds...
команду, уменьшающую значение переменной i на 1; После слова while в скобках напишите условие (i > 1). После цикла допишите команду, добавляющую к значению строки timer слово '1 second'.
Приведем пример, который принципиально похож на то, что нужно сделать, но адаптируйте его к требованиям задачи:

let s = '';
let i = 20;
do {
  s = s + `${i} sheeps...`
  i = i - 1;
} while (i > 1);
s = s + '1 sheep';
Write your solution here
unit
let timer = '';
let i = 10;
do {
  timer = timer + `${i} seconds...`;
  i = i - 1;
} while (i > 1)
timer = timer + '1 second';

* 110.Найдите количество элементов массива, у которых последняя цифра - 0.
question
Создайте массив с именем arr, содержащий произвольное количество чисел. Создайте переменную countMultOf10, используйте ключевое слово let, присвойте начальное значение 0.

Создайте цикл for, в котором заголовок цикла содержит:

начальное значение переменной i = 0; (i - индекс элемента массива);
условие цикла i < arr.length;
шаг i++ (переменная i увеличивается на 1 после каждого выполнения тела цикла).
В теле цикла запишите команду if - else в которой проверьте выполнение условия arr[i] % 10 === 0. В случае выполнения условия, увеличьте значение переменной countMultOf10 на 1.

Приведем пример, который принципиально похож на то, что нужно сделать, но адаптируйте его к требованиям задачи:

const ar = [1, -9, 0, -8, 50, -20, -5, 7, 9, 11];
let res = 0;
for (let i = 0; i < ar.length; i++){
  if (ar[i] % 3 === 0) {
    res++;
  }
}

const arr = [2, 4, 6, 70];
let countMultOf10 = 0;
for (let i = 0; i < arr.length; i++) {
  if (arr[i] % 10 === 0) {
    countMultOf10++
  }
}

* 111 .Найдите количество целых чисел в массиве.

Создайте массив с именем arr, содержащий произвольное количество чисел (целых и нецелых, т.е. десятичных дробей).

Целые числа - числа, которые делятся на 1 без остатка.

Создайте переменную countOfInteger, используйте ключевое слово let, присвойте начальное значение 0.

Создайте цикл for, в котором заголовок цикла содержит:

начальное значение переменной i = 0; (i - индекс элемента массива);
условие цикла i < arr.length;
шаг i++ (переменная i увеличивается на 1 после каждого выполнения тела цикла).
В теле цикла запишите:

команду if - else в которой проверьте выполнение условия arr[i] % 1 === 0. В случае выполнения условия, увеличьте значение переменной countOfInteger на 1.
Приведем пример, который принципиально похож на то, что нужно сделать, но адаптируйте его к требованиям задачи:

const array = [0, 4.56, 2, 3.14, -0.5, 15, -3,6, 5];
let count = 0;
for (let i = 0; i < array.length; i++){
  if (array[i] % 1 === 0) {
    count++;
  }
}

const arr = [2, 4.1, 79];
let countOfInteger = 0;
for (let i = 0; i < arr.length; i++) {
  if (arr[i] % 1 === 0) {
    countOfInteger++;
  }
}

* 112.Расстояние от точки до начала координат.

Напишите функцию distance, которая принимает два числа x,y (координаты точки на плоскости) и возвращает расстояние от этой точки до начала координат. Расстояние от точки с координатами (x, y) до начала координат равно (x**2 + y**2) ** 0.5.

Примеры:

функция distance(3, 4) должна возвратить 5;
функция distance(0, 3) должна возвратить 3;
функция distance(2, 0) должна возвратить 2;
функция distance() должна возвратить 0.
Write your solution here
unit
function distance(x = 0, y = 0){
  return (x**2 + y**2) ** 0.5;
}

* 113.Расстояние между двумя точками на плоскости.

Напишите функцию distance, которая принимает четыре аргумента: x1, y1 (координаты первой точки на плоскости) и x2, y2 (координаты второй точки на плоскости) и возвращает расстояние между точками.

Расстояние между точками (x1, y1) и (x2, y2) равно ((x2 - x1)**2 + (y2 - y1)**2) ** 0.5.

Примеры:

функция distance(0, 0, 3, 4) должна возвратить 5;
функция distance(1, 1, 7, 9) должна возвратить 10.
Write your solution here
unit
function distance(x1, y1, x2, y2){
  return ((x2 - x1)**2 + (y2 - y1) ** 2) ** 0.5;
}

* 114 .Процент от числа
В ресторане принято оставлять чаевые 15% от суммы заказа. Напишите функцию percentageValue, которая принимает два аргумента: number и percent и возвращает процент от числа.

Примеры:

функция percentageValue(100, 15) возвращает 15% от числа 100, т.е. 15;
функция percentageValue(200, 15) должна возвратить 30.
Write your solution here
function percentageValue(number, percent){
  return number * percent / 100;
}

* 115. Индекс массы тела.

Индекс массы тела рассчитывается путем деления массы тела (в килограммах) на квадрат роста (в метрах квадратных).

Напишите функцию bodyMassIndex, которая принимает два аргумента: weight и height и возвращает индекс массы тела.

Пример:

функция bodyMassIndex(60, 1.65) должна возвратить 22.03856749311295.
Write your solution here
unit
function bodyMassIndex(weight, height){
  return weight / (height**2);
}

* 115. Степень числа
Напишите функцию powerOfNumber, которая принимает два аргумента: number и power и возвращает значение степени числа.

Примеры:

функция powerOfNumber(2, 2) должна возвратить 4;
функция powerOfNumber(2, 3) должна возвратить 8;
функция powerOfNumber(2, -2) должна возвратить 0.25;
функция powerOfNumber(2, -3) должна возвратить 0.125;
функция powerOfNumber(10, 0) должна возвратить 1.
Write your solution here
unit
function powerOfNumber(number, power){
  return number ** power;
}

* 116.Hello Name!

Напишите функцию с именем greetings, которая возвращает фразу "Hello Name!" для данного name. Если имя не дано или равно пустой строке, вернуть "Hello!"

Примеры:

функция greetings('Alice') должна возвратить приветствие 'Hello Alice!';
функция greetings('Tom') должна возвратить приветствие 'Hello Tom!';
функция greetings('') должна возвратить приветствие 'Hello!'.
функция greetings() должна возвратить приветствие 'Hello!'.
Приведем пример, который принципиально похож на то, что нужно сделать, но адаптируйте его к требованиям задачи:

function hi(str){
  if (!str) return 'Hi!';
   else return `Hi ${str}!`;
}

function greetings(name){
  if(!name) return 'Hello!';
   else return `Hello ${name}!`;
}

* 117.Всегда отрицательный результат
Напишите функцию с именем negative, которая принимает число и возвращает его отрицательным. Если число является отрицательным, то возвращается само число. Примеры:

функция negative(1) должна возвратить -1;
функция negative(0) должна возвратить 0.
функция negative(-2) должна возвратить -2.
Приведем пример, который принципиально похож на то, что нужно сделать, но адаптируйте его к требованиям задачи:

function reverse(num){
 if (num <= 0) return num;
 else return -num;
}
function negative(num){
  if (num <= 0) return num;
  else return -num;
}

* 118.Среднее геометрическое двух положительных чисел

Среднее геометрическое двух положительных чисел
question
Чтобы найти среднее геометрическое двух чисел, нужно перемножить эти числа и извлечь из них корень.

Напишите функцию geometricMean, которая принимает два числа: num1 и num2 и возвращает среднее геометрическое этих чисел.

Примеры:

функция geometricMean(2, 2) должна возвратить 2;
функция geometricMean(3, 12) должна возвратить 6;
функция geometricMean(2, 8) должна возвратить 4.
Write your solution here
unit
function geometricMean(num1, num2){
  return (num1 * num2) ** 0.5;
}

* 119. Сумма углов n-угольника

Мы знаем из школьного курса, что сумма углов треугольника равна 180 градусам, сумма углов квадрата или прямоугольника равна 360 градусам. Сумма углов n-угольника равна 180 * (n − 2).

Напишите функцию anglesOfPolygon, которая принимает аргумент n (число углов) и возвращает сумму углов n-угольника.

Примеры:

функция anglesOfPolygon(5) должна возвратить 540;
функция anglesOfPolygon(4) должна возвратить 360;
функция anglesOfPolygon(3) должна возвратить 180;
функция anglesOfPolygon(2) должна возвратить 0.
Write your solution here
unit

function anglesOfPolygon(n){
  return 180 * (n - 2);
}

* 120. Периметр треугольника
Напишите функцию perimeterOfTriangle, которая принимает три аргумента a, b, c (стороны треугольника) и возвращает периметр треугольника, если треугольник существует, или сообщение "The triangle does not exist", в противном случае.

Треугольник существует, если каждая из его сторон меньше суммы двух других сторон:

a < b + c && b < a + c && c < a + b

Примеры:

функция perimeterOfTriangle(4, 5, 6) должна возвратить 15;
функция perimeterOfTriangle(3, 2, 10) должна возвратить сообщение "The triangle does not exist".
Write your solution here
function perimeterOfTriangle(a, b, c){
  if(a < b + c && b < a + c && c < a + b) return a + b + c;
  else return "The triangle does not exist";
}

* 121 .Площадь треугольника
question
Напишите функцию areaOfTriangle, которая принимает три аргумента a, b, c (стороны треугольника) и возвращает площадь треугольника, если треугольник существует, или сообщение "The triangle does not exist", в противном случае.

Треугольник существует, если каждая из его сторон меньше суммы двух других сторон:

a < b + c && b < a + c && c < a + b.

Площадь треугольника вычисляется по формуле Герона:

s = (p * (p - a) * (p - b) * (p - c)) ** 0.5; где p = (a + b + c) / 2.

Примеры:

функция areaOfTriangle(3, 4, 5) должна возвратить 6;
функция areaOfTriangle(3, 2, 10) должна возвратить сообщение "The triangle does not exist".
Write your solution here
function areaOfTriangle(a, b, c){
  let p = (a + b + c) / 2;
  let s = (p * (p - a) * (p - b) * (p - c)) ** 0.5;
  if(a < b + c && b < a + c && c < a + b) return s;
  else return "The triangle does not exist";
}

* 122. Последняя цифра числа
question
Напишите функцию lastDigit, которая принимает аргумент number и возвращает его последнюю цифру.

Примеры:

функция lastDigit(43) должна возвратить 3;
функция lastDigit(52128) должна возвратить 8;
функция lastDigit(5) должна возвратить 5.
Write your solution here
function lastDigit(number){
  return number % 10;
}

* 123. Факториал числа
question
Факториал числа — это произведение натуральных чисел от 1 до самого числа (включая данное число). Факториал нуля и единицы равен 1.

Напишите функцию factorial, которая принимает число number и возвращает факториал этого числа.

Примеры:

функция factorial(0) должна возвратить 1;
функция factorial(1) должна возвратить 1;
функция factorial(2) должна возвратить 2 (т.к. 1 * 2 = 2);
функция factorial(4) должна возвратить 24 (т.к. 1 * 2 * 3 * 4 = 24).
функция factorial(5) должна возвратить 120 (т.к. 1 * 2 * 3 * 4 * 5 = 120).
Write your solution here
function factorial(number){
  let result = 1;
  for (let i = 1; i <= number; i++) {
    result = result * i;
  }
  if(number === 0) return 1;
  return result;
}

* 124 .question
Напишите функцию max, которая принимает три аргумента (числа) x, y и z и возвращает большее число.

Примеры:

функция max(30, 8, 17) должна возвратить 30;
функция max(1, 9, 3) должна возвратить 9;
функция max(1, 9, 26) должна возвратить 26;
функция max(2, 2, 8) должна возвратить 8;
функция max(20, 20, 6) должна возвратить 20.
Write your solution here
unit
function max(x, y, z){
  return Math.max(x,y,z);
}

* 126. Количество цифр в числе.

Напишите функцию numberOfDigits, которая принимает аргумент number и возвращает количество цифр в этом числе.

Примеры:

функция numberOfDigits(93) должна возвратить 2;
функция numberOfDigits(346821) должна возвратить 6;
функция numberOfDigits(5) должна возвратить 1.
Идея решения: чтобы найти количество цифр числа, мы будем отбрасывать по одной цифре с конца, до тех пор, пока число не станет равным нулю. Количество таких действий равно количеству цифр в числе.

Приведем пример, который принципиально похож на то что нужно сделать, но адаптируйте его к требованиям задачи:

let number = 342167;
let count = 0;
let last;
while (number !== 0){
  last = number % 10; //последняя цифра
  number = (number - last) / 10; //отбрасывание последней цифры
  count++;  //подсчет числа повторений цикла (количество цифр числа)
}
Write your solution here
function numberOfDigits(number){
  let count = 0;
  let last;
  while (number !== 0) {
    last = number % 10;
    number = (number - last) / 10;
    count++;
  }
  return count;
}

* 127. Quarter of the year
https://www.codewars.com/kata/5ce9c1000bab0b001134f5af
const quarterOf = (month) => {
  console.log(month)
  if(month === 1 || month === 2 || month === 3) {
    return 1;
  } else if(month === 4 || month === 5 || month === 6) {
    return 2;
  } else if(month === 7 || month === 8 || month === 9) {
    return 3;
  } else {
    return 4
  }
}
* 128.Split Strings
https://www.codewars.com/kata/515de9ae9dcfc28eb6000001 
function solution(str){
  if(str.length % 2 !== 0 ){
     str += '_';
   }
  let arr = str.split('');
  let res = [];
  for(let i = 0; i < arr.length; i=i+2){
    res.push(arr[i] + arr[i+1]);
  }
  return res;
}

129. Cумма чисел от n до m.
question
Дано два числа n и m. Найдите сумму всех целых чисел от n до m включительно.

Напишите функцию с именем sumFromNToM, которая принимает два числа n, m и возвращает сумму чисел от n до m. В решении используйте цикл for.

Примеры:

функция sumFromNToM(5, 5) должна возвратить 5;
функция sumFromNToM(5, 2) должна возвратить 0;
функция sumFromNToM(12, 13) должна возвратить 25;
функция sumFromNToM(5, 7) должна возвратить 18.
Write your solution here
unit

function sumFromNToM(n, m){
  let sum = 0;
  for(let i = n; i <= m; i++){
    sum += i;
  }
  return sum;
}

* 130. question
Дано два числа n и m. Найдите сумму целых чисел от n до m включительно, кратных числу n.

Напишите функцию с именем sumMultN, которая принимает два числа n, m и возвращает сумму чисел от n до m, кратных числу n. В решении используйте цикл for.

Примеры:

функция sumMultN(5, 5) должна возвратить 5; // 5 = 5
функция sumMultN(5, 2) должна возвратить 0;
функция sumMultN(2, 9) должна возвратить 20; // 2 + 4 + 6 + 8 = 20
функция sumMultN(5, 19) должна возвратить 30. // 5 + 10 + 15 = 30
Write your solution here

function sumMultN(n, m){
  let sum = 0;
  for (let i = n; i <= m; i=i+n){
    sum += i;
  }
  return sum;
}
* 131. Сумма дробей
question
Дано число n > 0. Найдите сумму: 1 + 1/2 + 1/3 + 1/4 + ... + 1/n

Напишите функцию с именем sumOfFractionals, которая принимает число n и возвращает сумму дробей, у которых в числителе 1, а в знаменателе - числа от 1 до n. В решении используйте цикл for. Сумму округлите до двух десятичных знаков.

Примеры:

функция sumOfFractionals(1) должна возвратить 1;
функция sumOfFractionals(5) должна возвратить 2.28;
функция sumOfFractionals(10) должна возвратить 2.93.
Write your solution here
unit

function sumOfFractionals(n){
  let divisor = 1;
  let sum = 1;
  for(let i = 1; i < n; i++) {
    divisor += 1;
    sum += 1/divisor;
  }
  return +sum.toFixed(2);
}

* 132. question
Дано число n > 0. Найдите значение дроби:

fractional

Напишите функцию с именем fractional, которая принимает число n и возвращает значение дроби. В решении используйте цикл for. Значение дроби округлите до трех десятичных знаков.

Примеры:

функция fractional(1) должна возвратить 1; // 1 / 1 = 1
функция fractional(2) должна возвратить 1.5; // 3 / 2 = 1.5
функция fractional(3) должна возвратить 1. // 6 / 6 = 1
функция fractional(4) должна возвратить 0.417. // 10 / 24 = 0.41666666... = 0.417
Write your solution here
unit

function fractional(n){
  let sum = 0;
  let divisor = 1;
  for (let i = 1; i <= n; i++) {
    sum += i;
    divisor *= i;
  }
  return +(sum/divisor).toFixed(3);
}

* 133 .Количество делителей числа.
question
Дано число n > 0. Найдите количество делителей этого числа. Делитель - это число, на которое данное число делится без остатка.

Напишите функцию с именем numberOfDividers, которая принимает число n и возвращает количество делителей этого числа.

Примеры:

функция numberOfDividers(1) должна возвратить 1; // один делитель - число 1
функция numberOfDividers(2) должна возвратить 2; // 2 делителя - числа 1 и 2
функция numberOfDividers(3) должна возвратить 2; // 2 делителя - числа 1 и 3
функция numberOfDividers(4) должна возвратить 3; // 3 делителя - числа 1, 2, 4
функция numberOfDividers(12) должна возвратить 6. // 6 делителей - числа 1, 2, 3, 4, 6, 12

function numberOfDividers(n){
  let count = 0;
  for(let i = 1; i <= n; i++){
    if(n % i === 0) count++;
  }
  return count;
}

* 134. Создайте массив делителей
question
Дано число n > 0. Найдите все делители этого числа. Делитель - это число, на которое данное число делится без остатка.

Напишите функцию с именем dividers, которая принимает число n и возвращает делители этого числа в виде массива.

Примеры:

функция dividers(1) должна возвратить [1];
функция dividers(2) должна возвратить [1, 2];
функция dividers(3) должна возвратить [1, 3];
функция dividers(4) должна возвратить [1, 2, 4];
функция dividers(12) должна возвратить [1, 2, 3, 4, 6, 12].
function dividers(n){
  let divArr = [];
  for (let i = 1; i <= n; i++) {
    if(n % i === 0) divArr.push(i);
  }
  return divArr;
}

* 135. Простое число.
question
Дано число n > 0. Определите, является ли данное число n простым.

Число называется простым, если оно делится только на 1 и на самого себя (т.е. число делителей числа равно 2). Например, числа 2, 3, 5, 5, 7, 11, 13, 17, 19 – простые. Число 1 не является ни простым, ни составным.

Напишите функцию с именем isPrime, которая принимает число n и возвращает true, если число простое, и false - в противном случае.

Примеры:

функция isPrime(1) должна возвратить false;
функция isPrime(2) должна возвратить true;
функция isPrime(29) должна возвратить true;
функция isPrime(30) должна возвратить false.

function isPrime(n){
  let count = 0;
  for(let i = 1; i <= n; i++){
    if(n % i === 0) count++;
  }
  return count === 2;
}

* 136. question
Не пользуясь операцией возведения в степень, возвести число a в степень n.

power

Напишите функцию с именем power, которая принимает числa a и n в качестве аргументов и возвращает значение a в степени n (a и n - целые неотрицательные числа). В решении используйте цикл for. В этом задании нельзя использовать операцию возведения в степень и методы объекта Math.

Примеры:

функция power(3, 3) должна возвратить 27;
функция power(3, 0) должна возвратить 1;
функция power(0, 0) должна возвратить 1;
функция power(2, 5) должна возвратить 32.
function power(a, n){
  let res = 1;
  for(let i = 1; i <= n; i++) {
    res *= a;
  }
  return res;
}

* 137. Последовательность Фибоначчи
question
Числа Фибоначчи - последовательность, в которой первые два числа равны 0 и 1, а каждое последующее число равно сумме двух предыдущих чисел: 0, 1, 1, 2, 3, 5, ...

Напишите функцию с именем fibonacciNumbers, которая принимает число n (n >= 2) в качестве аргумента и возвращает массив из n чисел Фибоначчи.

Примеры:

функция fibonacciNumbers(2) должна возвратить [0, 1];
функция fibonacciNumbers(5) должна возвратить [0, 1, 1, 2, 3];
функция fibonacciNumbers(7) должна возвратить [0, 1, 1, 2, 3, 5, 8].

function fibonacciNumbers(n){
  let arr = [0, 1];
  for (let i = 2; i < n; i++) {
    arr.push(arr[i-2] + arr[i-1]);
  }
  return arr;
}

* 138. Sum of Triangular Numbers
https://www.codewars.com/kata/580878d5d27b84b64c000b51
function sumTriangularNumbers(n) {
  let trNumber = 1;
  let sum = 1;
  for(let i = 2; i <= n; i++){
    trNumber += i;
    sum += trNumber;
  }
  return n < 0 ? 0 : sum;
}

* 139.Cумма всех двухзначных чисел.
question
Найдите сумму всех положительных целых двухзначных чисел.

Напишите функцию с именем sumOfTwoDigitsNumbers, которая возвращает сумму чисел от 10 до 99 включительно. В решении используйте цикл do while.

Write your solution here
unit
function sumOfTwoDigitsNumbers(){
  let i = 10;
  let sum = 0;
  do {
    sum += i;
    i++;
  } while (i <= 99)
  return sum;
}
* 140. Царевна-лягушка
question
Царевна-лягушка съедает ежедневно на 3 комара больше, чем в предыдущий день. Определите, в какой день количество съеденных комаров превысит 1000, если в первый день было съедено n комаров.

Напишите функцию с именем frogPrincess, которая принимает число n (количество комаров в первый день) и возвращает количество дней, в течение которых лягушка съест 1000 комаров.

В решении используйте цикл do while.

Примеры:

функция frogPrincess(1) должна возвратить 26;
функция frogPrincess(12) должна возвратить 23;
функция frogPrincess(99) должна возвратить 10.
функция frogPrincess(100) должна возвратить 9.
функция frogPrincess(1000) должна возвратить 1.

function frogPrincess(n){
  let days = 0;
  let i = n;
  let sum = 0;
  do {
    days++;
    sum += i;
    i += 3;
  } while (sum < 1000)
  return days;
}
 * 141. Спортивный бег.
question
Начав тренировки, спортсмен в первый день занятий пробежал n км. Каждый последующий день он увеличивал норму на 10% от нормы предыдущего дня. Определите, сколько километров пробежит спортсмен в 10-й день занятий.

Результат округлите до целого с помощью Math.round().

Напишите функцию с именем running, которая принимает число n (количество километров в 1 день) и возвращает количество километров в 10-й день занятий.

В решении используйте цикл do while.

Примеры:

функция running(1) должна возвратить 2;
функция running(5) должна возвратить 12;
функция running(10) должна возвратить 24.
Write your solution here
function running(n){
  let norma = n;
  let days = 1;
  do {
    days++;
    norma *= 1.1;
  } while (days < 10)
  return Math.round(norma);
}

* 142. Вклад в банк (простой процент)
question
Вкладчик положил 1000 долларов в банк. Ежегодно эта сумма увеличивается на p (p > 0) процентов от начальной суммы вклада. Через сколько лет на счету будет 1500 долларов?

Напишите функцию с именем bankPercent, которая принимает число p (банковский процент) и вычисляет, через сколько лет на счету будет 1500 долларов.

В решении используйте цикл do while.

Примеры:

функция bankPercent(10) должна возвратить 5;
функция bankPercent(5) должна возвратить 10;
функция bankPercent(13) должна возвратить 4.

function bankPercent(p){
  let sum = 1000;
  let year = 0;
  let increase = sum * (p / 100);
  do {
      year++;
      sum += increase;
  } while (sum < 1500)
  return year;
}

* 143. Вклад в банк (капитализированный процент)
question
Вкладчик положил некоторое количество денег в банк. Ежегодно эта сумма увеличивается на percent (percent > 0) процентов от текущей суммы вклада. Определите, какая сумма денег будет на счету через period лет?

Напишите функцию с именем bankPercent, которая принимает в качестве аргументов три числа:

money (начальная сумма вклада);
percent (капитализированный банковский процент);
period (количество лет),
и возвращает сумму денег на вкладе через period лет. Результат округлите до двух десятичных энаков.

При этом виде вкладов ежегодно сумма увеличивается на p процентов от имеющейся (текущей) суммы:

В решении используйте цикл do while.

Примеры:

функция bankPercent(1000, 10, 1) должна возвратить "1100.00".
функция bankPercent(1000, 10, 2) должна возвратить "1210.00".
функция bankPercent(1000, 10, 3) должна возвратить "1331.00".
функция bankPercent(1000, 10, 5) должна возвратить "1610.51".
Write your solution here

function bankPercent(money, percent, period){
  let year = 0;
  let sum = money;
  do {
    year++;
    sum += sum * (percent / 100);
  } while (year < period)
  return sum.toFixed(2);
}

* 144. "Переверните" число
question
Дано целое положительное число. Получите другое целое число, полученное из исходного числа путем чтения его справа налево. Используйте операции умножения, деления и нахождения остатка от деления. Запрещено использование методов строк и массивов. В решении используйте цикл do while.

Напишите функцию с именем invertNumber, которая принимает в качестве аргумента число n и возвращает перевернутое число.

Если в результате переворачивания числа первой цифрой становится цифра 0, число следует выводить без нуля в начале.

Примеры:

функция invertNumber(123) должна возвратить 321.
функция invertNumber(15670) должна возвратить 7651.
функция invertNumber(11) должна возвратить 11.
функция invertNumber(1000) должна возвратить 1.

function invertNumber(n){
  let num = '';
  let last;
  do {
    last = n % 10;
    num += last;
    n = (n - last) / 10;
  } while (n > 0)
  return +num;
}

* 145. Массив из цифр числа, записанных в обратном порядке.
question
Дано целое положительное число. Получите массив его цифр, записанных в обратном порядке (от последней цифры к первой).

Напишите функцию с именем arrayOfDigits, которая принимает в качестве аргумента число n и возвращает массив его цифр в обратном порядке. Запрещено использование методов split, reverse. В решении используйте цикл do while.

Примеры:

функция arrayOfDigits(123456) должна возвратить [6, 5, 4, 3, 2, 1];
функция arrayOfDigits(1000) должна возвратить [0, 0, 0, 1];
функция arrayOfDigits(1) должна возвратить [1].

function arrayOfDigits(n){
  let arr = [];
  let last;
  do {
    last = n % 10;
    arr.push(last);
    n = (n - last) / 10;
  } while (n > 0)
  return arr;
}

* 146. Содержит ли число цифру "2"?
question
Дано целое положительное число. Определите, содержит ли данное число цифру "2".

Напишите функцию с именем doesNumberContain2, которая принимает в качестве аргумента число n и возвращает true, если число содержит цифру 2, и false - в противном случае. Запрещено использование методов строк и массивов. В решении используйте цикл do while.

Примеры:

функция doesNumberContain2(1520) должна возвратить true;
функция doesNumberContain2(114876) должна возвратить false;
функция doesNumberContain2(22222) должна возвратить true.

function doesNumberContain2(n){
  let last;
  do {
    last = n % 10;
    if (last === 2) return true;
    n = (n - last) / 10;
  } while (n > 0)
  return false;
}

* 147.question
Дано целое положительное число. Получите массив, состоящий из четных цифр этого числа.

Напишите функцию с именем evenDigits, которая принимает в качестве аргумента число n и возвращает массив четных цифр. Если таких цифр в числе нет, возвратить пустой массив. Запрещено использование методов строк и массивов. В решении используйте цикл do while. Порядок цифр в массиве должен совпадать с порядком цифр в исходном числе.

Примеры:

функция evenDigits(12345) должна возвратить [2, 4];
функция evenDigits(110325) должна возвратить [0, 2];
функция evenDigits(22222) должна возвратить [2, 2, 2, 2, 2];
функция evenDigits(131) должна возвратить [].

function evenDigits(n){
  const arr = [];
  let last;
  do {
    last = n % 10;
    if (last % 2 === 0) {
      arr.unshift(last);
    }
    n = (n - last) / 10;
  } while (n > 0)
  return arr;
}

* 148. Определите, есть ли в массиве отрицательный элемент.
question
Напишите функцию с именем isNegativeInArray, которая принимает массив arr в качестве аргумента и возвращает true, если в массиве есть хотя бы один отрицательный элемент, и false в противном случае. В решении необходимо использовать оператор break.

Указание. Присвойте некоторой переменной значение false. Пройдите по массиву в цикле, и если встретится отрицательный элемент, присвойте этой переменной значение true и выполните прерывание цикла.

Примеры:

функция isNegativeInArray([1, 2, 3, 9, 0]) должна возвратить false;
функция isNegativeInArray([2, 1, -3, 4, 3]) должна возвратить true;
функция isNegativeInArray([2, 1, -3, -4, 3]) должна возвратить true.

function isNegativeInArray(arr){
  let a = false;
  for (let i = 0; i < arr.length; i++) {
    if(arr[i] < 0) {
      a = true;
      break;
    }
  }
  return a;
}

* 149. Найдите в массиве первый четный элемент и его индекс.
question
Напишите функцию с именем firstEvenElement, которая принимает массив arr в качестве аргумента и возвращает первый четный элемент и его индекс в виде массива [element, index]. Если в массиве нет ни одного четного элемента, вернуть пустой массив []. В решении необходимо использовать оператор break.

Примеры:

функция firstEvenElement([1, 2, 3, 4, 9, 0]) должна возвратить [2, 1];
функция firstEvenElement([2, 1, -3, 4, 3]) должна возвратить [2, 0];
функция firstEvenElement([9, 1, -3, -4, 12, 6]) должна возвратить [-4, 3];
функция firstEvenElement([9, 1, -3, 3, 11]) должна возвратить [].

function firstEvenElement(arr){
  let ar = [];
  for (let i = 0; i < arr.length; i++) {
    if(arr[i] % 2 === 0) {
      ar.push(arr[i], i);
      break;
    }
  }
  return ar;
}

* 150. Определите, содержит ли массив заданное значение.
question
Напишите функцию с именем isElementIncluded, которая принимает числовой массив arr и число x в качестве аргументов и возвращает true, если в массиве есть элемент x, и false в противном случае.

В решении необходимо использовать оператор break.

Примеры:

функция isElementIncluded([10, 0, 4, 5, 9, 30], 0) должна возвратить true;
функция isElementIncluded([2, 1, -3, 1, 4, 3], 1) должна возвратить true;
функция isElementIncluded([2, 1, -3, -4, 3], 0) должна возвратить false.

function isElementIncluded(arr, x){
  let result = false;
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] === x) {
      result = true;
      break;
    } 
  }
  return result;
}

* 151. 
Содержит ли строка данный символ?
question
Напишите функцию с именем iSymbInString, которая принимает строку str и символ symb в качестве аргументов и возвращает true, если в строке встречается хотя бы один символ symb, и false в противном случае.

В решении необходимо использовать оператор break. Запрещено использование методов строк.

Указание. Пройдите циклом по строке, и если встретится искомый символ, присвойте некоторой переменной значение true и выполните прерывание цикла.

Примеры:

функция iSymbInString("abcd", "b") должна возвратить true;
функция iSymbInString("abcd", "f") должна возвратить false.

function iSymbInString(str, symb){
  let result = false;
  for (let i = 0; i < str.length; i++) {
    if (str[i] === symb) {
      result = true;
      break;
    }
  }
  return result;
}

* 152. Получить массив из целых чисел от 1 до n, за исключением данного числа x.
question
Напишите функцию с именем fillArray, которая принимает числа n (n >= 1) и x (1 <= x <= n) в качестве аргументов и возвращает массив из целых чисел от 1 до n включительно, за исключением числа x.

В решении необходимо использовать оператор continue.

Примеры:

функция fillArray(5, 2) должна возвратить [1, 3, 4, 5]; // числа от 1 до 5, за исключением числа 2.
функция fillArray(10, 5) должна возвратить [1, 2, 3, 4, 6, 7, 8, 9, 10]; // числа от 1 до 10, за исключением числа 5.
функция fillArray(3, 1) должна возвратить [2, 3]; // числа от 1 до 3, за исключением числа 1.
функция fillArray(5, 5) должна возвратить [1, 2, 3, 4]; // числа от 1 до 5, за исключением числа 5.
функция fillArray(1, 1) должна возвратить []; // числа от 1 до 1, за исключением числа 1, т.е. пустой массив
function fillArray(n, x){
  const arr = [];
  for (let i = 1; i <= n; i++) {
    if(i === x) {
      continue;
    }
    arr.push(i);
  }
  return arr;
}


* 153. Получить массив из четных чисел от 2 до n, за исключением чисел, кратных 3.
question
Напишите функцию с именем fillArray, которая принимает число n (n >= 2) в качестве аргумента и возвращает массив из четных чисел от 2 до n, за исключением чисел кратных 3.

В решении необходимо использовать оператор continue.

Примеры:

функция fillArray(10) должна возвратить [2, 4, 8, 10]; // четные числа от 2 до 10, за исключением числа 6 (6 кратно 3).
функция fillArray(20) должна возвратить [2, 4, 8, 10, 14, 16, 20]; // четные числа от 2 до 20, за исключением чисел 6, 12, 18 (чисел, кратных 3).
функция fillArray(7) должна возвратить [2, 4]; // четные числа от 2 до 7, за исключением числа 6.
функция fillArray(3) должна возвратить [2]; // четные числа от 1 до 3, за исключением числа 3.
функция fillArray(2) должна возвратить [2].

function fillArray(n){
  const arr = [];
  for (let i = 2; i <= n; i++) {
    if(i % 3 === 0) continue;
    if(i % 2 === 0) arr.push(i);
  }
  return arr;
}

* 154. Quarter of the year
https://www.codewars.com/kata/5ce9c1000bab0b001134f5af
const quarterOf = (month) => {
  console.log(month)
  if(month === 1 || month === 2 || month === 3) {
    return 1;
  } else if(month === 4 || month === 5 || month === 6) {
    return 2;
  } else if(month === 7 || month === 8 || month === 9) {
    return 3;
  } else {
    return 4
  }
}

* 155. How much water do I need?
https://www.codewars.com/kata/575fa9afee048b293e000287
function howMuchWater(water, load, clothes){
 return clothes > load * 2 ? 
  'Too much clothes' : 
  (clothes < load ? 'Not enough clothes' : 
  Number(( water * 1.1 ** (clothes - load)).toFixed(2))
  )
}
* 156.Help the Fruit Guy
function removeRotten(bagOfFruits){
  return bagOfFruits && bagOfFruits.length ? bagOfFruits.join(',').replace(/rotten/g, '').toLowerCase().split(',') : [];
}

* 157. Get the mean of an array
function getAverage(marks){
  let sum = 0;
  for(let i = 0; i < marks.length; i++){
    sum += marks[i];
  }
  return Math.floor(sum/marks.length);
}

* 158. Halving Sum
function halvingSum(n) {
  let sum = 0;
  do {
    sum += n;
    n = Math.floor(n / 2);
  } while (n >= 1)
  return sum;
}

* 159. Quarter of the year
const quarterOf = (month) => {
  console.log(month)
  if(month === 1 || month === 2 || month === 3) {
    return 1;
  } else if(month === 4 || month === 5 || month === 6) {
    return 2;
  } else if(month === 7 || month === 8 || month === 9) {
    return 3;
  } else {
    return 4
  }
}

* 160. Get the mean of an array
function getAverage(marks){
  let sum = 0;
  for(let i = 0; i < marks.length; i++){
    sum += marks[i];
  }
  return Math.floor(sum/marks.length);
}

* 161. Exclamation marks series #2: Remove all exclamation marks from the end of sentence
function remove(s){
  return s.replace(/!+$/, '');
}
* 162. Fake Binary
https://www.codewars.com/kata/57eae65a4321032ce000002d
function fakeBin(x){
  return x.replace(/[0-4]/g, '0').replace(/[5-9]/g, '1');
}

* 162. Halving Sum
function halvingSum(n) {
  let sum = n;
  while(n >= 1) {
    n = Math.trunc(n/2);
    sum += n;
  }
  return sum;
}
* 163. Training JS #9: loop statement --while and do..while
function padIt(str,n){
  // while
  if (n % 2 === 0) {
    return '*'.repeat(n/2) + str + '*'.repeat(n/2);
  } else {
    return '*'.repeat((n+1)/2) + str + '*'.repeat((n-1)/2);
  }
}
*164. Round up to the next multiple of 5
function roundToNext5(n){
  while(n % 5 !== 0){
    n++;
  }
  return n;
}
* 165.
function fillArray(n, x) {
  const arr = [];
  for(let i = 1; i <= n; i++) {
    if(i === x) continue;
    arr.push(i);
  }
  return arr;
}
console.log(fillArray(10,5));

* 166.Split Strings
 function solution(str){
  if(str.length % 2 !== 0 ){
     str += '_';
   }
  let arr = str.split('');
  let res = [];
  for(let i = 0; i < arr.length; i=i+2){
    res.push(arr[i] + arr[i+1]);
  }
  return res;
}

* 167. Таблица из чисел: n строк по 5 чисел
Напишите функцию с именем numericalTable, которая принимает число n в качестве аргумента и возвращает таблицу чисел от 1 до n. Каждая строка содержит 5 чисел, разделенных пробелом. Все строки кроме последней, заканчиваются символом \n перевода строки.

Например, для n = 4 должна быть получена строка:

"1 1 1 1 1\n2 2 2 2 2\n3 3 3 3 3\n4 4 4 4 4"

При выводе в консоль такая строка отображается как таблица:
"1 1 1 1 1
2 2 2 2 2
3 3 3 3 3
4 4 4 4 4"

function numericalTable(n){
  let str = '';
  for (let i = 1; i <= n; i++) {
    for (let j = 1; j <= 5; j++) {
      if (j !== 5) str = str + i + ' ';
      else str = str + i ;
    }
    i !== n ? str = str + `\n` : str;
  }
  return str;
}

* 168. Еще одна таблица из чисел: `n` строк по `m` чисел в каждой строке
Напишите функцию с именем numericalTable, которая принимает числа n и m в качестве аргументов и возвращает таблицу чисел от 1 до n. Каждая строка содержит m чисел, разделенных пробелом. Все строки кроме последней, заканчиваются символом \n перевода строки.

Например, для n = 4, m = 3 должна быть получена строка:

"1 1 1\n2 2 2\n3 3 3\n4 4 4"

При выводе в консоль такая строка отображается как таблица: (выводятся 4 строки, содержащие числа от 1 до 4, по 3 числа в каждой строке).
Напишите функцию с именем numericalTable, которая принимает числа n и m в качестве аргументов и возвращает таблицу чисел от 1 до n. Каждая строка содержит m чисел, разделенных пробелом. Все строки кроме последней, заканчиваются символом \n перевода строки.

Например, для n = 4, m = 3 должна быть получена строка:

"1 1 1\n2 2 2\n3 3 3\n4 4 4"

При выводе в консоль такая строка отображается как таблица: (выводятся 4 строки, содержащие числа от 1 до 4, по 3 числа в каждой строке).

Напишите функцию с именем numericalTable, которая принимает числа n и m в качестве аргументов и возвращает таблицу чисел от 1 до n. Каждая строка содержит m чисел, разделенных пробелом. Все строки кроме последней, заканчиваются символом \n перевода строки.

Например, для n = 4, m = 3 должна быть получена строка:

"1 1 1\n2 2 2\n3 3 3\n4 4 4"

При выводе в консоль такая строка отображается как таблица: (выводятся 4 строки, содержащие числа от 1 до 4, по 3 числа в каждой строке).
"1 1 1
2 2 2
3 3 3
4 4 4"

function numericalTable(n, m){
  let str = '';
  for (let i = 1; i <= n; i++) {
    for (let j = 1; j <= m; j++) {
      j !== m ? str = str + i + ' ' : str = str + i;
    }
    i !== n ? str = str + `\n` : str;
  }
  return str;
}

* 169. Числовой треугольник
question
Напишите функцию с именем numericalTriangle, которая принимает число n в качестве аргумента и возвращает треугольник из чисел от 1 до n, разделенных пробелом. Все строки кроме последней, заканчиваются символом \n перевода строки.

Например, для n = 5, должна быть получена строка:

"1\n2 2\n3 3 3\n4 4 4 4\n5 5 5 5 5"

При выводе в консоль такая строка отображается как "треугольник" из чисел:
"1
2 2
3 3 3
4 4 4 4
5 5 5 5 5"
function numericalTriangle(n){
  let str = '';
  for (let i = 1; i <= n; i++) {
    for (let j = 1; j <= i; j++) {
      j !== i ? str += i + ' ' : str += i;
    } 
    i !== n ? str += `\n` : str;
  }
  return str;
}

* 170. Треугольник из звездочек
question
Напишите функцию с именем starTriangle, которая принимает число n в качестве аргумента и возвращает треугольник из n строк, состоящих из звездочек (*). Все строки кроме последней, заканчиваются символом \n перевода строки.

Например, для n = 7, должна быть получена строка:

"*\n**\n***\n****\n*****\n******\n*******"

При выводе в консоль такая строка отображается как "треугольник":

"*
**
***
****
*****
******
*******"

function starTriangle(n){
  let str = '';
  for (let i = 1; i <= n; i++) {
    for (let j = 1; j <= i; j++) {
      str = str + '*';
    }
    i !== n ? str = str + `\n` : str;
  }
  return str;
}

* 171. Суммы элементов в двухмерном массиве.
question
Напишите функцию с именем sumsInArray, которая принимает двухмерный массив arr в качестве аргумента и возвращает массив, содержащий суммы элементов вложенных массивов.

Примеры:

функция sumsInArray([[1, 2], [2, -3, 1, 1], [3, 5, 10], [3, 7]]) должна возвратить [3, 1, 18, 10];
функция sumsInArray([[1, 0, 0], [2, 2]]) должна возвратить [1, 4];
функция sumsInArray([[], [2, 2], [0]]) должна возвратить [0, 4, 0].

function sumsInArray(arr){
  const res = [];
  for (let i = 0; i < arr.length; i++) {
    let sum = 0;
    for (let j = 0; j < arr[i].length; j++) {
      sum += arr[i][j];
    }
    res.push(sum);
  }
  return res;
}

* 172. Перевернутый треугольник из звездочек
question
Напишите функцию с именем upsideDown, которая принимает число n в качестве аргумента и возвращает треугольник из n строк, состоящих из звездочек (*). В первой строке n звездочек, во второй - (n-1) звездочка, ... , в последней строке 1 звездочка.

Все строки кроме последней, заканчиваются символом \n перевода строки.

Например, для n = 5, должна быть получена строка:

"*****\n****\n***\n**\n*"

При выводе в консоль такая строка отображается как "перевернутый треугольник":

"*****
****
***
**
*"
Замечание: при проверке решения в тестах символ перевода строки не отображается.

Примеры:

функция upsideDown(1) должна возвратить: "*";
функция upsideDown(3) должна возвратить: "***\n**\n*".
function upsideDown(n){
  let str = '';
  for (let i = n; i >= 1; i--) {
    str = str + '*'.repeat(i) + `\n`;
  }
  return str.trim();
}

* 173. Coding Practice
Дан двухмерный массив. Найти количество строк, в которых есть отрицательные элементы.
question
Напишите функцию с именем countLinesWithNegativeElements, которая принимает двухмерный массив arr в качестве аргумента и возвращает количество строк, содержащих хотя бы один отрицательный элемент.

Примеры:

функция countLinesWithNegativeElements([[1, 2], [2, -2, -3], [3, 5], [3, 4, 5, -1, 8]]) должна возвратить 2; (так как только две строки (два элемента массива) имеют отрицательные элементы: [2, -2, -3], [3, 4, 5, -1, 8].

функция countLinesWithNegativeElements([[1, -2], [2, -2, -3], [3, 5], [3, 4, 5, -1, 8], [-3, -1]]) должна возвратить 4; (так как четыре элемента массива имеют отрицательные элементы: [1, -2], [2, -2, -3], [3, 4, 5, -1, 8], [-3, -1].

функция countLinesWithNegativeElements([[1, 3], [2, 7, 8], [3, 5]]) должна возвратить 0; (так как нет ни одного элемента массива с отрицательными элементами.

function countLinesWithNegativeElements(arr){
  let count = 0;
  for (let i = 0; i < arr.length; i++) {
    for (let j = 0; j < arr[i].length; j++) {
      if(arr[i][j] < 0) {
        count++;
        break;
      }
    }
  }
  return count;
}

* 174. Pack Some Chocolates
https://www.codewars.com/kata/5f5daf1a209a64001183af9b/train/javascript
function makeChocolates(small, big, goal) {
  for (let b = big; b >= 0; b--){
    for (let s = small; s >= 0; s--){
      if ((b*5 + s*2) === goal) return s;
    }
  }
  return -1;
}

* 175. ATM
https://www.codewars.com/kata/5635e7cb49adc7b54500001c/train/javascript
function solve(n) {
  let count = 0;
  if(n % 10) return -1;
  while(n>=500){
    count++;
    n -= 500;
  }
  while(n>=200){
    count++;
    n -= 200
  }
  while(n>=100){
    count++;
    n -= 100
  }
  while(n>=50){
    count++;
    n -= 50
  }
   while(n>=20){
    count++;
    n -= 20
  }
   while(n>=10){
    count++;
    n -= 10
  }
  return count;
}

function solve(n) {
  let count = 0;
  const arr = [500,200,100,50,20,10];
  for(let banknote of arr){
    while(n >= banknote){
      count++;
      n -= banknote;
    }
  }
  return n ? -1 : count;
  
}

* 176. Pack Some Chocolates
https://www.codewars.com/kata/5f5daf1a209a64001183af9b
function makeChocolates(small, big, goal) {
  for(let i = big; i >= 0; i--){
    for(let j = small; j >= 0; j--){
      if(i * 5 + j * 2 === goal) return j;
    } 
  }
  return -1;
}

* 177. Heads and Legs
function animals(heads, legs){
  let cows = (legs - heads * 2) / 2;
  let chickens = (heads * 4 - legs) / 2;
  
  if(heads === 0 && legs === 0) return [0,0];
  if(chickens < 0 || cows < 0 || legs > 1000 || heads > 1000 || (legs < 0 && heads < 0) || Math.round(chickens) != chickens || Math.round(cows) != cows) return "No solutions";
  return [chickens, cows];
}

* 178. Figurate Numbers #2 - Pronic Number
function isPronic(n){
  for(let i = 0; i <= n; i++){
    if(n === i*(i+1)) return true;
  }
  return false;
}

* 179. How much water do I need?
function howMuchWater(water, load, clothes){
 return clothes > load * 2 ? 
  'Too much clothes' : 
  (clothes < load ? 'Not enough clothes' : 
  Number(( water * 1.1 ** (clothes - load)).toFixed(2))
  )
}

* 180. Help the Fruit Guy
https://www.codewars.com/kata/557af4c6169ac832300000ba
function removeRotten(bagOfFruits){
  return bagOfFruits && bagOfFruits.length ? bagOfFruits.join(',').replace(/rotten/g, '').toLowerCase().split(',') : [];
}

* 181. Split Strings
function solution(str){
  if(str.length % 2 !== 0 ){
     str += '_';
   }
  let arr = str.split('');
  let res = [];
  for(let i = 0; i < arr.length; i=i+2){
    res.push(arr[i] + arr[i+1]);
  }
  return res;
}

* 182.Fake Binary
function fakeBin(x){
  return x.replace(/[0-4]/g, '0').replace(/[5-9]/g, '1');
}

* 184.
multiplicationTable = function(size) {
  const arr = [];
  for(let i = 1; i <= size; i++){
    let s = [];
    for(let j = 1; j <= size; j++){
      s.push(i*j);
    }
    arr.push(s);
  }
  return arr;
}

* 185. Complete The Pattern #6 - Odd Ladder
function pattern(n){
  let str = '';
  for(let i = 1; i <= n; i += 2){
    str = str + i.toString().repeat(i) + '\n';
  }
  return str.trim()
}

* 186.Complete The Pattern #2
https://www.codewars.com/kata/55733d3ef7c43f8b0700007c
function pattern(n){
 let str='';
  for(let i = 1; i<= n; i++){
    let s = '';
    for(let j = n; j >= i; j--){
      s += j;
    }
    str += s + '\n';
  }
 return str.trim();
}

* 187. Sum of Triangular Numbers
function sumTriangularNumbers(n) {
  let trNumber = 1;
  let sum = 1;
  for(let i = 2; i <= n; i++){
    trNumber += i;
    sum += trNumber;
  }
  return n < 0 ? 0 : sum;
}

* 188. ATM
function solve(n) {
  let count = 0;
  const arr = [500,200,100,50,20,10];
  for(let banknote of arr){
    while(n >= banknote){
      count++;
      n -= banknote;
    }
  }
  return n ? -1 : count;
  
}

* 189.Coefficients of the Quadratic Equation
function quadratic(x1, x2){
  return [1, -(x1+x2), x1*x2];
}

* 190. Rock off
function solve(a, b) {
  let countA = 0;
  let countB = 0;
  for(let i = 0; i < 3; i++){
    if(a[i] > b[i]) countA++;
    if(a[i] < b[i]) countB++;
  }
  if(countA === countB) return `${countA}, ${countB}: that looks like a "draw"! Rock on!`;
  if(countA > countB) return `${countA}, ${countB}: Alice made "Kurt" proud!`;
  if(countA < countB) return `${countA}, ${countB}: Bob made "Jeff" proud!`
  
}

* 191. What is type of variable?
function type(value) {
  console.log(value)
  if(value === null) return 'null';
  if(value === undefined) return 'undefined';
  return value.constructor.name.toLowerCase();
}

* 192. Plus - minus - plus - plus - ... - Count
https://www.codewars.com/kata/5bbb8887484fcd36fb0020ca
const catchSignChange = arr => {
  let count = 0;
  for(let i = 0; i < arr.length; i++){
    if(arr[i] >= 0 && arr[i+1] < 0 || arr[i] < 0 && arr[i+1] >=0) count++;
  }
  return count;
}
*193.
Напишите функцию changeMaxAndMin, которая принимает массив arr в качестве аргумента и возвращает массив, в котором максимальный и минимальный элементы поменялись местами. Если в массиве несколько максимальных или несколько минимальных элементов, поменять местами первые из них. Во всех тестах массив содержит минимум два элемента.

Используйте в решении циклы. Не разрешается использование методов Math.min() и Math.max().

function changeMaxAndMin(arr){
  let min = arr[0];
  let minInd = 0;
  
  let max = arr[0];
  let maxInd = 0;
  
  for(let i = 1; i < arr.length; i++){
    if(arr[i] > max) {
      max = arr[i];
      maxInd = i;
    }
    if(arr[i] < min) {
      min = arr[i];
      minInd = i;
    }
  }
  
  console.log(max, min);
  console.log(maxInd, minInd);

  arr[maxInd] = min;
  arr[minInd] = max;
  return arr;
}
console.log(changeMaxAndMin([3, 4, 8, 4, 1, 2, 1,8 ])); // [3, 4, 1, 4, 8, 2, 1,8]

// // c помощью методов
function changeMaxAndMin(arr) {
  let min = Math.min(...arr);
  let max = Math.max(...arr);
  let minInd = arr.indexOf(min);
  let maxInd = arr.indexOf(max);
  
  arr[minInd] = max;
  arr[maxInd] = min;
  return arr;
}

* 194. Plus - minus - plus - plus - ... - Count
const catchSignChange = arr => {
  let count = 0;
  for(let i = 0; i < arr.length; i++){
    if(arr[i] >= 0 && arr[i+1] < 0 || arr[i] < 0 && arr[i+1] >=0) count++;
  }
  return count;
}

* 195.Хранит ли аргумент функции значение NaN?
Напишите функцию isValid, которое проверяет, содержит ли аргумент value значение NaN.

Если аргумент является NaN, возвратить строку "Value is not a number".

В противном случае возвратить строку "Value is valid".

Используйте в решении метод Number.isNaN(value)

Примеры:

функция isValid(NaN) должна возвратить "Value is not a number";
функция isValid('abc' * 3) должна возвратить "Value is not a number";
функция isValid(NaN + 1) должна возвратить "Value is not a number";
функция isValid(0/0) должна возвратить "Value is not a number";
функция isValid('abc' + 3) должна возвратить "Value is valid";
функция isValid(25) должна возвратить "Value is valid";
функция isValid(1/0) должна возвратить "Value is valid";
функция isValid('abc') должна возвратить "Value is valid".
Write your solution here
function isValid(value){
  if(Number.isNaN(value)) return 'Value is not a number';
  else return 'Value is valid';
}


