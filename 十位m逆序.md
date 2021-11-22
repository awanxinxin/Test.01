#include<stdio.h>
int main()
{
	int m=1;
	scanf_s("%d", &m);
	int a[10], t, i;
	for (i = 0; i < 10; i++)
		scanf_s("%d", &a[i]);	//输入数组的10个元素
	for (i = 0; i < (10-m+1)/2; i++){	//将对称位置的元素对调位置
		t = a[i+m-1]; 
		a[i+m-1] = a[9-i];
		a[9-i] = t;
	}
	for (i = 0; i < 10; i++)
		printf("%d ", a[i]);	//输出逆序后的排列数
	printf("\n");
	return 0;
}