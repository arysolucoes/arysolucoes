[![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=arysolucoes)](https://github.com/arysolucoes/github-readme-stats)
```c
#include <stdio.h>

void selection(int vec[], int len) {
    for (int i = 0; i<len; i++) {
        int idx = i;
        int smallest = vec[i];
        for (int j = i+1; j<len; j++) {
            if (vec[j] < smallest) {
                smallest = vec[j];
                idx = j;
            }
        }
        int tmp = vec[i];
        vec[i] = smallest;
        vec[idx] = tmp;
    }
}

int main() {
    int arr[] = {5,4,1,3,63,62,20,3664};
    int len = sizeof(arr) / sizeof(arr[0]);
    selection(arr,len);
    for (int i = 0;i<len;i++) printf("%d ", arr[i]);

    return 0;
}
```

```c
#include <stdio.h>
#include <stdint.h>

// TAIL RECURSION
uint32_t factTR(uint32_t n, uint32_t a) {
    if (n <= 1) return a;
    else return factTR(n-1, n * a);
}

uint32_t factT(uint32_t n) {
    return factTR(n,1);
}

// nomal recursion
uint32_t fact(uint32_t n) {
    if (n <= 1) return 1;
    else return n* fact(n-1);
}


int main() {
    uint32_t number = 10;
    printf("the factorial of %d is %d\n",number,fact(number));
    printf("the factorial of %d is %d\n",number,factT(number));

    return 0;
}
```
