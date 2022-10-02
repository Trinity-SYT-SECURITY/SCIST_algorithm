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

## 輸出範例:
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

### 第一節 作業一 (必做)

**Input**
There is no input for this problem.

**Output**
Output should contain one line, containing the string “Hello World!”.

![image](https://user-images.githubusercontent.com/96654161/193436426-7b090c1e-a835-4d04-93ba-b33dd07f0c34.png)

## 輸入範例

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

>定義變數後都要注意有沒有初始化過

### 第一節 作業二 (延伸)
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

### 第一節 作業三 (必做)
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

### 第二節 作業一(必做)
– 輸入 –

輸入兩個正整數 m 和 p，代表你手上擁有 m 元，以及遊戲賣價 p 元。

– 輸出 –

輸出你買完會剩下多少錢。

如果不夠，以負數表示你會負債多少錢。

– 輸入限制 –

• 1 ≤ m, p ≤ 100, 000

```cpp
#include <iostream>
using namespace std;

int main()
{
	int m; //儲存整數類型變數
	int p;
	int price;
	cin >> m >> p;
	price = m - p;
        cout <<price<< endl;
	return 0;
	
}
```
![image](https://user-images.githubusercontent.com/96654161/193437601-cb007354-cbd5-4365-ab37-08c32252d5ad.png)
![image](https://user-images.githubusercontent.com/96654161/193437604-6f2f527e-ca2b-41ea-8803-7e90dc4e12a2.png)

## 運算
有加減乘除順序

```cpp
#include <iostream>
#include <math.h>

using namespace std;

int main()
{
 int a,b,c;
 cin >> a >> b>>c;
 c = b;
 b = 1000;
 
cout <<" b + 1 = "<< b+1 << "\n";
cout <<" b - 1 = "<< b-1 << "\n";
cout <<" b * 1 = "<< b*1 << "\n";
cout <<" b / 1 = "<< b/1 << "\n";
cout <<" b % 1 = "<< b%1 << "\n";

cout << "b...:" << b*100/50<< "\n";//b...:2000
cout << "b...:" << b/100*50<< "\n";//b...:500
//要注意運算優先度

cout << "b...:" << b+10*5<< "\n";//b...:1050
cout << "b...:" << (b+10)*5<< "\n";//b...:5050
//要改變運算優先度，一定要用小括號

a = b += 5;
cout << "b += 5" << a << "\n";
return 0;
	
}
```

![image](https://user-images.githubusercontent.com/96654161/193440793-40fb7710-d92f-43a7-8c55-b122517d3a28.png)

[C++數值大小限制](https://learn.microsoft.com/zh-tw/cpp/cpp/data-type-ranges?view=msvc-170)

超過位元的話可以使用 **long long** 宣告變數，此可以儲存更大數值範圍

![image](https://user-images.githubusercontent.com/96654161/193441120-b6e3ba0a-ce01-41cd-9937-2bc53b80ade3.png)

```cpp
#include <iostream>
using namespace std;
int main(){
int numnum = 299792458 * 10000000000;
long long num1 = 299792458 * 10000000000;
long long num = 299792458LL * 10000000000LL;//LL = long long

 cout << numnum << "\n"<< num1 << "\n"<< num;

}   
```

![image](https://user-images.githubusercontent.com/96654161/193441773-97eaa4fa-54bc-4822-976c-4dae453f5f8e.png)


### 第二節 作業二(必做)

**Jack-O'-Lantern Juxtaposition**

Every year, Pumpkin Pete comes up with a couple of different Jack-O’-Lantern ideas for his annual Halloween special. He stacks them up on haystacks for everyone to enjoy and take pictures with. To make sure that there’s a wide variety of displays, he wants to make sure many possible Jack-O’-Lanterns designs are available. He has come up with many eye, nose, and mouth designs and would like to know how many unique designs are possible. He needs your help to set up the displays before the special kicks off!

**Input**

The input consists of one line which contains three integers. The first,**N**, indicates the number of eye designs. The second,**T**, indicates the number of nose designs. The third, **M** indicates the number of mouth designs. All three values are in the range [1,500].

**Output**

Output a single line containing the number of different possible Jack-O’-Lantern designs.

![image](https://user-images.githubusercontent.com/96654161/193438082-af0c63fe-3071-40f8-ac46-b165a23154ce.png)

```cpp
#include <iostream>
using namespace std;

int main()
{
	int N; //儲存整數類型變數
	int T;
	int M;
	int ALL;
	cin >> N >> T >> M;
	ALL = N*T*M;
	
    cout <<ALL<< endl;
	return 0;
	
}
```
![image](https://user-images.githubusercontent.com/96654161/193438096-2b54dbf6-2c2e-4ef6-8fd5-0a26d36d8ce3.png)

![image](https://user-images.githubusercontent.com/96654161/193438000-069e753d-a2a3-4931-a8ba-e19a06dff356.png)

### 第二節 作業三(必做)

– 輸入 –

輸入為一個非負整數 x 代表流入的魔力量。

– 輸出 –

輸出 x
2 的個位數。

– 輸入限制 –
• 0 ≤ x ≤ 16, 384

```cpp
#include <iostream>
#include <math.h>

using namespace std;

int main()
{
	int X; //儲存整數類型變數
	cin >> X;
	int ALL = pow(X,2);
	
	int take = ALL % 10;
	
    cout <<take<< endl;
	return 0;
	
}

```

![image](https://user-images.githubusercontent.com/96654161/193438576-04b8553f-5101-4b18-b21f-fde75f1ea063.png)

![image](https://user-images.githubusercontent.com/96654161/193438544-434c8142-1ba0-4ebc-b3f4-0a110866cb88.png)

### 第二節 作業四(必做)

**Speed of Light**

地球和太陽之間的平均距離約為 149597870700 公尺。

應用在天文學上，日常通用的單位實在小得可憐。為了避免天文學家算那種長得死人的數字或是因為老花眼看錯各種科學記號上十的次方，有些天才就想到了使用光的行進來測量距離：如同大家所知，一光年(Lightyear, LY)被定義為光在一年之內前進的距離。

地球和太陽之間的平均距離約為 0.00001522070015221 光年。

噢。

顯然需要更多單位才能應付不同的尺度。因此，天文學家引入了光秒(Light-second)，光分(light-minute)，光時(light-hour)...等等。

地球和太陽之間的平均距離約為8.3 光分。 舒服多了。

但這時由出現了一個問題：這些各式各樣單位，換算成我們熟悉的單位又是多長?

請寫一個程式來幫助可憐的天文學家。


輸入說明
本題沒有輸入。

輸出說明
依序將以下六種種單位

	光秒	Light-second(LS)
	光分	Light-minute(LM)
	光時	Light-hour(LH)
	光日	Light-day(LD)
	光週	Light-week(LW)
	光年	Light-year(LY)

換算成公尺，以下列格式輸出：

1 [unit] is [number] metres.

範例輸入
本題沒有輸入。


範例輸出
1 Light-second(LS) is 299792458 metres.
1 Light-minute(LM) is XXXXXXXXX metres.
1 Light-hour(LH) is XXXXXXXXX metres.
1 Light-day(LD) is XXXXXXXXX metres.
1 Light-week(LW) is XXXXXXXXX metres.
1 Light-year(LY) is XXXXXXXXX metres.


提示：
光速 c = 299792458 m/s
一年有365天，一周有7天，一天有24小時，一小時有60分鐘，一分鐘有60秒。

```cpp
#include <iostream>
using namespace std;
int main(){
    unsigned long long num = 299792458;
    
    cout << "1 Light-second(LS) is " << num << " metres."<< endl;
    num *=60;
    cout << "1 Light-minute(LM) is "  << num << " metres."<< endl;
    num *= 60;
    cout << "1 Light-hour(LH) is "  << num << " metres."<< endl;
    num*= 24;
    
    unsigned long long day = num;
    cout << "1 Light-day(LD) is "  << day << " metres."<< endl;
    cout << "1 Light-week(LW) is "  << day*7 << " metres."<< endl;        
    cout << "1 Light-year(LY) is "  << day*365 << " metres."<< endl;    

}   
```
![image](https://user-images.githubusercontent.com/96654161/193441170-2c3cc0ef-94cc-452a-8f33-cb1524603981.png)


## 條件式



```cpp
#include <iostream>
using namespace std;
int main(){
 int a,b;
 cin >> a >> b;
 
 //兩件事情擇一發生
 
 // 可能都發生，或是都不發生
 if (a-b <= 0)
 {
 	cout << "meow..\n";
 	a-=b;
 }
 //else不可單獨出現
 else //or  if (a-b > 0)
 {
 	
 	cout << "noflag..\n";
 }
 
 return 0;
 
}   
```

![image](https://user-images.githubusercontent.com/96654161/193442428-087514b3-456b-40fc-9d10-57ab832badc3.png)

```cpp
#include <iostream>
using namespace std;
int main(){
 int a;
 cin >> a ;
//level >= 100 ->S
//level >= 80 ->A
//level >= 50 ->B
//level < 50 ->C

 if (a >= 100)
 {
 	cout << "S\n";
 }
 else // 要先滿足上個條件式，才會繼續往下
 {
 	if (a >= 80)
 	{
 		cout <<"A\n";
 	}
 	else
 	{
 		if(a>=50)
 		{
 			cout<<"B\n";
 		}
 		else
 		{
 			cout <<"C\n";
 		}
 	}
 }
}   
```
![image](https://user-images.githubusercontent.com/96654161/193442948-cc4635c1-573c-4f1d-bbfa-6d2cc137a6b9.png)
