## 【C++ 基礎語法 - 上】SCIST S3 演算法 week 1

> https://hackmd.io/@sa072686/cp/%2F%40sa072686%2FHyypNHG_r

線上題目單
> https://docs.google.com/spreadsheets/d/1-HJroVmfbpFI_fXoHtF2zITC08w7DOUUdCmPm4fzh4w/edit#gid=0

![image](https://user-images.githubusercontent.com/96654161/193434257-2d1dbc73-e448-41ae-9aab-76c919b7ef84.png)

解題網站
> https://open.kattis.com/problems/hello

> https://toj.tfcis.org/oj/info/

> Kattis：https://open.kattis.com/
> Uva：https://onlinejudge.org/
> TOJ：https://toj.tfcis.org/oj/
> AtCoder：https://atcoder.jp/
> Codeforces：https://codeforces.com/

> 把問題算對，最短時間完成

初始程式:
```cpp
#include <iostream> 
using namespace std;//cout是在它底下

//integer
int main()//程式進入點 (主) 小括號是函數
{ //哪開始哪結束
	//std::cout << "HI\n"; //如果前面沒有using namespace std;這行，就要加
	//將這段文字用 << 傳達給 cout後，cout 便會將這段文字輸出到畫面上
	cout << "HI\n";//輸出 \n是換行
	return 0;//結束程式 0是給執行的工具看
	
}
```
![image](https://user-images.githubusercontent.com/96654161/193435456-b9c7a69a-c7de-476c-b2da-150b4b828403.png)

需要compile轉換才能讓電腦讀懂你寫的程式

也可以寫成這樣

![image](https://user-images.githubusercontent.com/96654161/193435838-8b85c5df-05a7-4473-b909-7fdcfe5fc7d8.png)

程式內有問題，到return才會被發現

利用換行讓文字更一目了然，可以在文字中間或是後面加上換行
```cpp
#include <iostream>
using namespace std;

int main()
{
	cout << "HI\n meow\n";//輸出
	cout << "HAHA";
	cout << "HAHA\n" << "abc\n"; //可串多個就可輸出很多文字
	
	return 0;
	
}

```
![image](https://user-images.githubusercontent.com/96654161/193436295-26241663-e2f5-4037-873c-fbc9880aef6d.png)

### 題目一

**Input**
There is no input for this problem.

**Output**
Output should contain one line, containing the string “Hello World!”.

![image](https://user-images.githubusercontent.com/96654161/193436426-7b090c1e-a835-4d04-93ba-b33dd07f0c34.png)

#### 輸入

```
#include <iostream>
using namespace std;

int main()
{
	int a,b; //儲存整數類型變數
	cin >> a >> b; //輸入
    cout << "Hello World!\n";//輸出
    cout << "a=" << a <<"\n";
    cout << "b=" << b << "\n";
	return 0;
	
}
```

### 題目二
– 輸入 –

輸入兩個整數 a 和 b 代表要複述的整數。

– 輸出 –

以「Do you want to say $a$ and $b$ ??」的格式複述，並將文中「$a$」替換為輸入的整數 a，「$b$」替換為輸入的整數 b。

– 輸入限制 –

• |a|, |b| ≤ 1000

```cpp
#include <iostream>
using namespace std;

int main()
{
	int a,b; //儲存整數類型變數
	cin >> a >> b; //輸入
        cout << "Do you want to say "<< a <<" and "<< b <<" ??\n";
	return 0;
	
}

```
![image](https://user-images.githubusercontent.com/96654161/193437078-9b256860-d4e5-4a57-aa04-7b99153dd739.png)

![image](https://user-images.githubusercontent.com/96654161/193437054-1aba9279-92de-4a51-b517-c443fedea9e2.png)

### 題目三
– 輸入 –

輸入兩個正整數 a 和 b，數字用來代表你或你朋友。先出現的數字表示是上次優先的。

– 輸出 –

輸出下次的優先順序。先輸出的數字表示較優先。

– 輸入限制 –

• a, b ≤ 1000
• a ̸= b


```cpp
#include <iostream>
using namespace std;

int main()
{
	int a; //儲存整數類型變數
	int b;
	int c;
	
	cin >> a >> b; //輸入
	
	c = a;
        a = b;
	b = c;
	
        cout << a <<" " << b << endl;
	return 0;
	
}
```
![image](https://user-images.githubusercontent.com/96654161/193437418-5828d3bb-893b-4c9d-8731-5122e5513dee.png)
![image](https://user-images.githubusercontent.com/96654161/193437426-0fb011c3-a02e-4aac-951b-1b5656844df4.png)
