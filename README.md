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
