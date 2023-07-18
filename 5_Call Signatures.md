
함수에 마우스를 올렸을 때 보게되는것.

```
type Add = (a: number, b: number) => number;
```

## Overloading
여러개의 call signature를 갖고있는 함수를 말한다.

예시 Nextjs

```
Router.push({
	path : ‘/home’,
	state : 1
})
```

```
.push(‘/home’);
```

### 이렇게 push가 두 가지의 형식으로 사용될 수 있을 때 
```
  type Config = {
    path: string;
    state: object;
  };

  type Push = {
    (path: string): void;
    (obj: Config): void;
  };

  const push: Push = config => {
    if (typeof config === 'string') console.log(config);
    else console.log(config.path);
  };
```

### 받는 인자의 개수가 다른 call signature 를 갖고 있는 함수의 경우
```
  type Add = {
    (a:number, b:number) : number
    (a:number, b:number, c:number) : number
  }

  const adding:Add=(a,b,c?:number)=>{
    return a+b
  }
```
