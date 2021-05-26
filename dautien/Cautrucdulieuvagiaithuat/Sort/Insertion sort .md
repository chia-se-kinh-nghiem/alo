# Thuật toán Insertion sort 

Insertion sort hay nôm na là sắp xếp theo kiểu chèn trực tiếp được  thực hiện đơn giản mô phỏng lại cách xếp bài của những người yêu bộ môn giải trí  "Bài tây" . 

``` 
Input : + Dãy Ar[n] bất kỳ 
		+ số nguyên n
Output: + Dãy Ar[n] đã được sắp xếp
```

Ý tưởng cơ bản của thuật toán như sau :

1. Lấy phần tử đầu tiên của dãy Ar[0] làm dãy đã sắp xếp
2. lấy phần tử đầu của dãy chưa sắp xếp lúc này là  Ar[1] rồi chèn vào vị trí thích hợp trong dãy đã sắp xếp
3. lặp lại bước 2 cho đến khi dãy được sắp xếp hoàn toàn

```c++
#include<iostream>
//#include<fstream>  //doc ghi dia
//#include<algorithm>
//#include<cmath>
//#include<windows.h>
//#include<ctime>
//#include<string>
//#include<bits/stdc++.h>
using namespace std;
void Out(int *a,int n){
	 for(int i=0;i<n;i++){
			 cout<<a[i]<<" ";
	 }
	 cout<<endl;
}
void InsertionSort(int *a,int n){
	for(int i=0;i<n;i++){
		int key=a[i];
		int j=i-1;
		while(j>=0&&a[j]>key){
			a[j+1]=a[j];
			j--;
		}
		a[j+1]=key;
		Out(a,n);
	}
}

int main(){
	int bo;cin>>bo;
	while(bo--){
	int n,k;cin>>n;
		int a[n];
		for(int i=0;i<n;i++){
			cin>>a[i];
		}
		InsertionSort(a,n);
	}

	return 0;
}
```

Độ phức tạp thuật toán :O(n^2)