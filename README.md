# BÁO CÁO HỌC HÀM
### KHAI BÁO HÀM  
Thông thường hàm thực hiện việc tính toán trên các tham số và cho lại giá trị kết quả, hoặc chỉ thực hiện một chức năng nào đó mà không cần trả lại kết quả. Kiểu giá trị trả về này được gọi là kiểu của hàm.
Hàm thường được khai báo ở đầu chương trình. Cách để khai báo một hàm như sau:  
```<kiểu của hàm><tên hàm>(danh sách tham số);```  
Trong đó:  
- Kiểu của hàm: Là kiểu dữ liệu mà hàm trả về. Nếu không có giá trị trả về thì kiểu của hàm là void.   
- Tên hàm: Là tên của hàm, do người lập trình đặt. Tên hàm không được chứa ký tự đặt biệt, không được bắt đầu bằng số.  
- Danh sách tham số: là danh sách các tham số dùng như các biến cục bộ. Nếu có nhiều tham số, thì chúng sẽ được phân tách theo các dấu phẩy.  
Vd: `int test(int a,int b);`  

### ĐỊNH NGHĨA HÀM
 
Cấu trúc một hàm bất kỳ được bố trí cũng giống như hàm main(). Cụ thể:  
``` c
<kiểu hàm><tên hàm>(danh sách tham số);
{  
dãy lệnh của hàm;
return(biểu thức trả về);
}
```  
Vd:  
```C
int sum(int a,int b)
{
return(a+b);
}
```  
### SỬ DỤNG HÀM  
Một hàm khi định nghĩa thì chúng vẫn chưa được thực thi trừ khi ta có một lời gọi đến hàm đó.  
Cú pháp gọi hàm: `<Tên hàm>([Danh sách các tham số])`  
VD:  
```c
include<stdio.h>
int n,a[100];
void input();
void output();
void BubbleSort();
void input()
{
    int i;
    for(i=0;i<n;i++)
        scanf("%d",&a[i]);
}
void output()
{
    int i;
    for(i=0;i<n;i++)
        printf("%d\t",a[i]);
}

void BubbleSort()
{
    int i,j,temp;
    for(i=0;i<n;i++)
        for(j=n-1;j>i;j--)
            if(a[j]<a[j-1])
            {
                temp=a[j];
                a[j]=a[j-1];
                a[j-1]=temp;
            }
}
main()
{

    printf("Nhap n:");
    scanf("%d",&n);
    input();
    BubbleSort();
    printf("Sau khi sap xep\n");
    output();

}
```
