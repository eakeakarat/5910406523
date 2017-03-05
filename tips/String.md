# String #
> ในภาษา c การดำเนินการกับ String นั้นทำได้ ค่อนข้างยาก
> โดยในถาษา c จะสามารถเก็บ String ในรูปของ char ที่เป็นarray
> char string[] = "Hello, World";
> นอกจากนี้ยังมีตัวช่วยในการดำเนินการกับ String
### <String.h> ###

* strlen() = เนับความยาวของStr

> n = strlen("Hello");
> n = 5

* strcmp() = เทียบค่าของStr จาก Ascii

>if( strcmp(str1, str2) > 0 )                   
>	printf("\n%s is greater than %s (ASCIIcode)", str1, str2);
>else  if( strcmp(str1,str2) == 0 )
>	printf("\n%s is equal to %s (ASCII  code)", str1, str2);
>else
>	printf("\n%s is less than %s  (ASCII  code)", str1, str2); 

* strcpy() = คัดลอกStr
> char str1[] = "Hello";
> strcpy(str2,str1);
> str2 = "Hello"

* strcat() = เชื่อมStr
>  char str1[] = "Hello,";
>  char str2[] = "World";
>  strcat(str1, str2) = "Hello, World"