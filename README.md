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
