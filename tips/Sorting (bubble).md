# Sorting Algorithm (Bubble Sort) #

  - Ascending order
  
    ~~~~
    #include <stdio.h>
    
    void ascending_arr (int arr[], int size)
    {
        int temp, i, j;

        for (i = 0 ; i < size ; i++){
            for (j = i+1 ; j < size ; j++){
                if (arr[i] > arr[j]){
                    temp = arr[i];
                    arr[i] = arr[j];
                    arr[j] = temp;
                }
            }
        }
    }
    ~~~~
    
  - Descending order
  
    ~~~~
    #include <stdio.h>
    
    void descending_arr (int arr[], int size)
    {
        int temp, i, j;

        for (i = 0 ; i < size ; i++){
            for (j = i+1 ; j < size ; j++){
                if (arr[i] < arr[j]){
                    temp = arr[i];
                    arr[i] = arr[j];
                    arr[j] = temp;
                }
            }
        }
    }
    ~~~~
