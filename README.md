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
  if (typeof num !== 'number' || num < 0){
    return 'Not valid';
  }
  const arr = +(num.toString().split('').reverse().join(''));
  return arr === num;
}

```