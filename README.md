# ES5-JS
잘 몰랐던 ES5 문법정리


# use strict ( 엄격 모드 )

"use strict" defines that the JavaScript code should be executed in "strict mode".

With strict mode you can, for example, not use undeclared variables.

# Array forEach() 

forEach() 를 이용하여 배열 엘레먼트를 순환한다.

``` javascript

let myFunction = (value) => {
  console.log(value)
}

let numbers = [45, 4, 9, 16, 25];
numbers.forEach(myFunction);

```
# Array map()

map 을 이용하여 배열 엘레먼트를 순환한다. 콜백함수가 적용된 새 요소를 반환한다. 
``` javascript 

const myArrary = [0,1,2,3,4,5];

let arr2 = myArrary.map((num,index,item) => {
  console.log(num,index,item)
});


```

# Array filter()

배열 엘레멘트에서 필요한 조건에 따라 필터링을 해줄수있다. , 조건물을 만족한 요소를 반환한다는 점이다. 

``` javascript 

let users = [
  { id: 85, name: 'William', age: 34, group: 'editor' },
  { id: 97, name: 'Oliver', age: 28, group: 'admin' }
];

/**
* filter() 를 이용한 filtering 
**/
let res = users.filter(result => result.name.includes('W'));
console.log('filering data =>' , res);
/**
* for loop 를 이용한 filtering 
**/
for(let i = 0 ; i < users.length ; i++){
  if(users[i].name === 'William'){
    console.log(users[i].id);
  }
}

```
``` javascript 
// filter api 를 이용하여 2보다 큰수를 return 하는 logic
let num = [1,2,3,4,5,6,7,8,9,10];
let result = num.filter(result => result >2);

```
