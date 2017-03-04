# Math Code #
> รวมฟังก์ชั่นหรือส่วนของโค้ดในการคำนวณทางคณิตศาสตร์ที่ใช้บ่อย

### การยกกำลังตัวเลขจำนวนเต็ม (integers) ###
  - FUNCTION CODE :
    ~~~~
    #include <stdio.h>
    
    int pow(int n)
    {
        return n*n;
    }
    ~~~~
  
    **หมายเหตุ : ไม่ควรใช้ฟังก์ชั่น pow ใน library math.h เพราะเนื่องจาก pow ถูกสร้างมาเพื่อยกกำลังเลขทศนิยม การนำมาใช้กับจำนวนเต็มจะทำให้ค่าผิดเพี้ยนได้**
    
### การหารากที่สองของตัวเลข ###
  - ใช้ฟังก์ชั่น sqrt จาก library math.h
  
  - Example :
    ~~~~
    #include <stdio.h>
    #include <math.h>
    
    int main()
    {
        printf("sqrt of 4 is %.2f", sqrt(4.0));
        return 0;
    }
    ~~~~
    
    **หมายเหตุ : sqrt ใช้ถอดรากของข้อมูลที่เป็น float หรือ double เท่านั้น**
    
### การเช็คว่าเป็นจำนวนเฉพาะหรือไม่ ###
  - FUNCTION CODE :
    ~~~~
    #include <stdio.h>
    
    int check_prime(int n)
    {
        int count = 0, i;

        for (i = 1 ; i <= n ; i++){
            if (n%i == 0)
                count++;
        }

        if (count == 2)
            return 1;
        else
            return 0;
    }
    ~~~~
    
### การหา ห.ร.ม. (GCD)
  - FUNCTION CODE :
    ~~~~
    #include <stdio.h>
    
    int gcd (int max, int min)
    {
      int mod;

      mod = max%min;
      while (mod != 0){
        max = min;
        min = mod;
        mod = max%min;
      }

      return min;
    }
    ~~~~
    
  **อาจประกาศ type ของ parameter ให้เป็น unsigned int ก็ได้ แล้วแต่ความเหมาะสม**
  
### การหา ค.ร.น. (LCM)
  - FUNCTION CODE :
    ~~~~
    #include <stdio.h>
    
    int gcd (int max, int min)
    {
        int mod, gcd;

        mod = max%min;
        while (mod != 0){
            max = min;
            min = mod;
            mod = max%min;
        }

        return min;
    }
    
    int lcm (int max, int min)
    {
        return max / gcd(max, min) * min;
    }
    ~~~~
    
  **อาจประกาศ type ของ parameter ให้เป็น unsigned int ก็ได้ แล้วแต่ความเหมาะสม**
  
## การหาลำดับ Fibonacci ###
  - FUNCTION CODE :
    ~~~~
    #include <stdio.h>
    #include <math.h>
    
    int fibo(int n)
    {
        return ( pow(1+sqrt(5),n) - pow(1-sqrt(5),n) ) / (pow(2,n) * sqrt(5)) ;
    }
    ~~~~
