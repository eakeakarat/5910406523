# How to generate a random data from Array #
> by [inorinchan](https://github.com/inorinchan)

## Random data from Array ##
ในภาษา Python เราสามารถ สุ่มข้อมูลจาก Array ได้ง่ายๆ<br/>
โดยการใช้ คำสั่งดังนี้<br/>
### Random ใน Python ###
```c
import random
x = [1,2,3,4]
print(random.choic(x))
//คำสั่ง choice คือการสุ่มจากใน list ที่มี
```
* ในภาษา C มี function ที่ชื่อว่า `random()` <br/>
ที่สามารถสุ่มข้อมูลได้เหมือนกับ random ใน Python <br/>
โดยการ include <stdlib.h> เพื่อใช้งาน <br/>
### Random ใน C ###
```c
#include <stdio.h>
#include <stdlib.h>
int main() {
    int array[4] = {1,2,3,4};
    int x;
    x = rand();
    printf("%d",array[x%3]);
}
```
```
* Tips ค่า x จะ Random มาจากค่าที่สุ่มขึ้นมาดังนั้นเราจึงต้องรู้ว่าจำนวนช่องของ Array มีเท่าไร
เพราะต้องใช้ในการ mod กับ x การ mod จะได้เลขที่นำไป mod ตั้งแต่ 0 - n-1 
เช่น mod ด้วย 9 จะได้ 0-8 เป็นต้น
```
### ข้อเสีย และ วิธีแก้ไข ###
ใน function random ของ C นั้น จะ random เป็นแพทเทิลเดิม <br/>
ทำให้เราได้ตัวเลขชุดเดิมๆ แต่มีวิธีการเปลยี่นแพทเทิลการ random คือ <br/>
function `srand()` แต่ถึงแม้เว่าเราจะเพิ่มแพทเทิลการสุ่มเข้าไป <br/>
การสุ่มของ random() ก็ยังคงมีแพทเทิลจำกัดอยู่ดี เราสามารถแก้โดยการใช้<br/>
function `time()` เข้ามาช่วย โดย function จะเพิ่มเวลาที่เดิมไปเรื่อยๆ <br>
ทำให้แพทเทิลการสุ่มเปลี่ยนได้เรื่อยๆ สามารถใช้ function time() ได้โดยการ <br/>
`include <time.h>` 
*โดยโปรแกรมที่ได้จะออกมาเป็นดังนี้<br/>
```c
#include <stdio.h>
#include <stdlib.h>
#include <time.h>
int main() {
    int array[4] = {1,2,3,4};
    int x;
    srand(time(NULL));
    x = rand();
    printf("%d",array[x%3]);
}
```
* Function การสุ่มของ random() และ srand() สามารถนำไปประยุกต์ใช้ได้หลายอย่าง <br/>
เช่น การทอยลูกเต๋า การสุ่มไพ่ การสุ่มตัวเลข ฯลฯ โดยขึ้นอยู่กับโปรแกรมของ Programmer แต่ละคน <br/> 






