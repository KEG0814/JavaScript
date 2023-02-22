프로미스(Promise)
=============================

### Promise

`기본 구문'
> resolve : 성공 , reject : 실패 시 실행되는 함수.
> callback 함수 : 어떤 일이 완료되고 실행되는 함수.

```
const pt = new Promise((resolve,reject)=>{
    //code
});
```

* * *

### new Promise 생성자가 반환하는 객체
{
    state : pending(대기)
    result : undefined
}

>'resolve(value)' 가 호출되면 
{
    state : fulfilled(이행됨)
    result : value
}
**Example code**
```
const pr = new Promise((resolve,reject)=>{
    setTimeout(()=>{
        resolve('OK');
    },3000);
});
```

>'reject(error)' 가 호출되면 
{
    state : rejected(거부됨)
    result : error
}
**Example code**
```
const pr = new Promise((resolve,reject)=>{
    setTimeout(()=>{
        reject(new Error("error..."));
    },3000);
});
```

* * *
### pr.then을 이용한 resolve & reject 처리

```
const pr = new Promise((resolve,reject)=>{
    setTimeout(()=>{
        resolve('value:OK');
        //reject(new Error('error...'));
    },3000);
});

pr.then(
    (result)=>{
        console.log(result);
    }
).catch(
    (err)=>{
        console.log(err);
    }
).finally(
    function(){
        console.log('--끝--');
    }
);
```




**Example(중글자)**
```
여기에는 코드가 삽입되면 된다.
실전 코드 및 예제 등...
```

//아래는 구분선 추가
* * *