
readonly 는 변하지 않는 값을 지정해 준다.   

```
let arr : readonly number[] = [1,2,3,4,5];
arr.push(2) // 에러가 난다. readonly 없애주는 순간 에러도 사라짐.
```

turple은 배열의 길이와 타입을 정해준다.   

```
let arr = [number,string,boolean];   
arr[0] = 1 // 정상
arr[1] = 2 // 에러 
arr[3]은 존재할 수도 없음
```

타입 any 는 사용하지 않는게 좋다.

```
let test1 : any = true;
let test2 : any[] = [1,2,3];
```

test1 + test2 가 가능하기 때문이다.
