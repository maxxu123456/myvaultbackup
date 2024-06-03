## Binary Search

```java
 public static int bs(int a[],int key){
        int start = 0 , end=a.length-1;
        while(start<=end){
            int mid = (start+end)/2;

            if(key==a[mid]){
                return mid;
            }

            if(key<a[mid]){
                end = mid-1;
            }
              else {
                start = mid+1;
              }
        } 
          return -1;
    }
```


