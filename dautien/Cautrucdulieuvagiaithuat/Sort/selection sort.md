## Selection sort

Là thuật toán đơn giản khi đề cập đến vấn đề sắp xếp . Chia dãy cẫn sắp xếp thành 2 phần .Phần đầu gồm các phần tử đã được sắp xếp .Phần 2 gồm các phần tử chưa được sắp xếp . Ban đầu dãy số chưa được sắp xếp  nên số phần tử phần đầu là 0.  Thuật toán tìm số nhỏ nhất trong dãy chưa sắp xếp  ,đỏi chỗ của nó với phần tử đầu của dãy chưa sắp xếp. Mỗi lần như vậy sẽ tăng số phần tử của dãy đầu thêm 1,và giảm 1 phần tử của dãy 2 đi .

 Ví dụ :

```
Dãy số A={30,45,1,3,60,7,21,16}
Bước 1:dãy chưa sắp xếp bắt đầu từ A[0]
 +tìm phần tử nhỏ nhất của dãy chưa sắp xếp A[0....7] được A[2]=0 là min 
 +đổi chỗ A[2] với A[0]
 +ta được dãy mới : A [1,45,30,3,60,7,21,16]
 
Bước 2:dãy chưa sắp xếp bắt đầu từ A[1]
 +tìm phần tử nhỏ nhất của dãy chưa sắp xếp A[1....7] được A[3]=3 là min 
 +đổi chỗ A[3] với A[1]
 +ta được dãy mới : A [1,3,30,45,60,7,21,16]
 
Bước 1:dãy chưa sắp xếp bắt đầu từ A[2]

 +tìm phần tử nhỏ nhất của dãy chưa sắp xếp A[2....7] được A[5]=7 là min 
 +đổi chỗ A[5] với A[2]
 +ta được dãy mới :A [1,3,7,45,60,30,21,16]
 
Bước 3:dãy chưa sắp xếp bắt đầu từ A[3]
 +tìm phần tử nhỏ nhất của dãy chưa sắp xếp A[3....7] được A[7]=16 là min 
 +đổi chỗ A[7] với A[3]
 +ta được dãy mới : A [1,3,7,16,60,30,21,45]
 
Bước 4:dãy chưa sắp xếp bắt đầu từ A[4]
 +tìm phần tử nhỏ nhất của dãy chưa sắp xếp A[4....7] được A[6]=21 là min 
 +đổi chỗ A[6] với A[4]
 +ta được dãy mới :  A [1,3,7,16,21,30,60,45]
 
Bước 5:dãy chưa sắp xếp bắt đầu từ A[5]
 +tìm phần tử nhỏ nhất của dãy chưa sắp xếp A[5....7] được A[5]=30 là min 
 +đổi chỗ A[5] với A[5] hay giữ nguyên 
 +ta được dãy mới :  A [1,3,7,16,21,30,60,45]
 
Bước 6:dãy chưa sắp xếp bắt đầu từ A[6]
 +tìm phần tử nhỏ nhất của dãy chưa sắp xếp A[6....7] được A[7]=45 là min 
 +đổi chỗ A[7] với A[6]
 +ta được dãy mới :  A [1,3,7,16,21,30,45,60]
 
Bước 7:dãy chưa sắp xếp bắt đầu từ A[7]
 +tìm phần tử nhỏ nhất của dãy chưa sắp xếp A[7] được A[7]=60 là min 
 +ta được dãy mới : A [1,3,7,16,21,30,45,60]
 

```

code trên nền c++ như sau :

```c++
#include<iostream>

using namespace std;
void Out(int *a,int n){
	for(int i=0;i<n;i++){
		cout<<a[i]<<" ";
	}
	cout<<endl;
}
void SellectipnSort(int *a,int n){
	 	for(int i=0;i<n;i++){
			int minIndex=i;
			for(int j=i+1;j<n;++j){  //duyệt tìm min trong dãy chưa sắp xếp 
				if(a[minIndex]>a[j]) minIndex=j;
			}
			swap(a[minIndex],a[i]); //đổi chỗ min vs đầu dãy chưa sắp xếp
			Out(a,n);
		}
}

int main(){
	int bo;cin>>bo;
	while(bo--){
		int n,dem=0;cin>>n;
		int a[n];
		for(int i=0;i<n;++i){
			cin>>a[i];
		}
		SellectipnSort(a,n);	
	
	}

	return 0;
}

```

Độ  phức tạp của thuật toán :O(n^2)