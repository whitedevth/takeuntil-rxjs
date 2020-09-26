### ตัวอย่างการใช้งาน takeUntil ใน rxjs [Learn RxJS](https://www.learnrxjs.io/learn-rxjs/operators/filtering/takeuntil)
 
 #### ปล่อยค่าออกมาจนกว่า timer จะปล่อยค่าออกมา

```
import { interval, timer } from 'rxjs';
import { takeUntil } from 'rxjs/operators';

//ปล่อยค่าทุกๆ 1 วินาที
const source = interval(1000);
//หลังจาก 5 วินาที, จะปล่อยค่าออกมา
const timer$ = timer(5000);
//เมื่อ timer ปล่อยค่าออกมาหลังจาก 5 วินาที, จะหยุดปล่อยค่า
const example = source.pipe(takeUntil(timer$));
//output: 0,1,2,3
const subscribe = example.subscribe(val => console.log(val));
```
