# String #
> ในภาษา c การดำเนินการกับ String นั้นทำได้ ค่อนข้างยาก<br/>
> โดยในถาษา c จะสามารถเก็บ String ในรูปของ char ที่เป็นarray<br/>
> char string[] = "Hello, World";<br/>
> นอกจากนี้ยังมีตัวช่วยในการดำเนินการกับ String<br/>
### <String.h> ###

* strlen() = เนับความยาวของStr<br/>

> n = strlen("Hello");<br/>
> n = 5<br/>

* strcmp() = เทียบค่าของStr จาก Ascii

>if( strcmp(str1, str2) > 0 )<br/>
>	printf("\n%s is greater than %s (ASCIIcode)", str1, str2);<br/>
>else  if( strcmp(str1,str2) == 0 )<br/>
>	printf("\n%s is equal to %s (ASCII  code)", str1, str2);<br/>
>else<br/>
>	printf("\n%s is less than %s  (ASCII  code)", str1, str2);<br/> 

* strcpy() = คัดลอกStr
> char str1[] = "Hello";<br/>
> strcpy(str2,str1);<br/>
> str2 = "Hello"<br/>

* strcat() = เชื่อมStr
>  char str1[] = "Hello,";<br/>
>  char str2[] = "World";<br/>
>  strcat(str1, str2) = "Hello, World"<br/>