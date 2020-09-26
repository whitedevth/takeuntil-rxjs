### ตัวอย่างการใช้งาน takeWhile ใน rxjs [Learn RxJS](https://www.learnrxjs.io/learn-rxjs/operators/filtering/take)
 
 #### ปล่อยค่าตามจำนวนที่ระบุ

```
import { of } from 'rxjs';
import { take } from 'rxjs/operators';

const source = of('A', 'B', 'C', 'D', 'E');
const example = source.pipe(take(3));

// ผลลัพธ์
// A
// B
// C
example.subscribe(console.log);
```
