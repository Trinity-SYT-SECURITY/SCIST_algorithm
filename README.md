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

```cpp
#include <iostream>
using namespace std;
int main(){
	int a,b;
	cin >> a >> b;
	//comparison operator
	// >
	// <
	// >=
	// <=
	// == 等於
	// != 不等於
	//0 or not 0
	if (a == b)
	{
		cout << "equal!!!\n";
		
	}
	else
	{
		cout << "nooooo.......\n";
	}
	cout << "a: " << a << " b:" << b << "\n";
	
	return 0;
	
}
```
![image](https://user-images.githubusercontent.com/96654161/193443627-c5a88567-fc56-42e0-8fa6-7acd504cd8af.png)

```cpp
#include <iostream>
using namespace std;
int main(){
	int a,b;
	bool alive;
	cin >> a >> b;
	alive = (a>b);
	cout << "cond:" << alive << "\n";
	cout << "true:" << true <<"\n";
	cout << "false:" << false <<"\n";
	
	if (alive)
	{
		cout << "TRUE!!!\n";
		
	}
	else
	{
		cout << "false.......\n";
	}
	
	return 0;
	
}
```
![image](https://user-images.githubusercontent.com/96654161/193443822-365f8ab2-653e-4206-bf35-04785d254509.png)

```cpp
#include <iostream>
using namespace std;
int main(){
	int a,b;
	bool alive;
	cin >> a >> b;
	//logical operator
	//and &&
	// or ||
	// not !
	//if (a <= b <= a+b)
	
	if (b >= a && b <= a+a)
	{
		cout << "TRUE!!!\n";
		
	}
	else
	{
		cout << "false.......\n";
	}
	alive = (a>b);
	if (!alive)
	{
		cout<<"NOMEOW...\n";
	}
	else
	{
		cout<<"OKKK\n";
		
	}
	return 0;
	
}
```
![image](https://user-images.githubusercontent.com/96654161/193444109-1743c6c9-9b05-4b73-9801-5685477edc5e.png)

```cpp
#include <iostream>
using namespace std;
int main(){
	int a,b,c, fit;
	cin >> a >> b >> c ;
	fit = 0;
	if (a > 10)
	{
		fit +=1;
	}
	if (b > 10)
	{
		fit +=1;
	}
	if (c > 10)
	{
		fit ++;
	}
	
	cout << "cout: "<<fit <<"\n";
	return 0;
	
	
}
```
![image](https://user-images.githubusercontent.com/96654161/193444356-a477b295-340f-476d-a0f3-77847b419b10.png)

閏年

```cpp
#include <iostream>
using namespace std;
int main(){
	int year;
	bool leap;
	
	cin >> year;
	if (year % 4 ==0)
	{
		if (year % 100 == 0)
		{
			if (year %400 == 0)
			{
				//cout << "yes\n";
				leap = true;
			}
			else
			{
				//cout << "no\n";
				leap = false;
				
			}
		}
		else
		{
			//cout << "yes\n";
			leap = true;
		}
		
	}
	else
	{
		 //cout << "not\n";
		 leap = false;
	}
	//把結果保留，最後處理
	if (leap)
	{
		cout << "leap!\n";
	}
	else
	{
		cout << "not leap\n";
	}
	
	return 0;
	
	
}
```
![image](https://user-images.githubusercontent.com/96654161/193444649-a93add38-b595-4aff-8b39-832706295936.png)



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

### 第三節 作業一(必做)
– 輸入 –

輸入為一個整數 n 代表某天的人數變動，以正數代表加入，負數代表退出。

– 輸出 –

輸出 |n|。

– 輸入限制 –

• 0 ≤ |n| ≤ 2, 147, 483, 647

![image](https://user-images.githubusercontent.com/96654161/193445395-12bc44ff-51ad-4d47-814d-89dcbe21f6f1.png)

```cpp
#include <iostream>
#include <stdio.h>
#include <math.h>

using namespace std;
int main(){
	
	int i;
	
	cin >> i;
	
	cout << abs(i)<<"\n";
	
	return 0;
	
	
}
```
![image](https://user-images.githubusercontent.com/96654161/193446153-2f658b28-fd3a-4ae7-be81-2970fe6ba57e.png)
![image](https://user-images.githubusercontent.com/96654161/193446159-46016fc9-05f1-42fe-9c0b-71a60c3eee9b.png)

### 第三節 作業二(必做)

– 輸入 –

輸入為兩個正整數 p、q，其中 p 代表賽亞人自身戰鬥力，q 代表對手的戰鬥力。

– 輸出 –

輸出「true」代表探測器故障了，輸出「false」則代表沒故障。

– 輸入限制 –

• 1 ≤ p, q ≤ 999, 999

```cpp
#include <iostream>
#include <stdio.h>
#include <math.h>

using namespace std;
int main(){
	
	int p,q;
	cin >> p >> q;
	
	if (q>p)
	{
		cout << "true"<< "\n";
	}
	else
	{
		cout << "false"<< "\n";
	}
	
	return 0;
	
	
}
```
![image](https://user-images.githubusercontent.com/96654161/193446474-eb5dcdfa-a190-4f06-a432-81a487caaf5c.png)

### 第三節 作業三(必做)

– 輸入 –

輸入三個整數 a、b、n，其中 a 為範圍下限，b 為範圍上限，n 為想詢問的目標數值。

– 輸出 –

如果落在守備範圍內，輸出「yes」；如果不是，輸出「no」。落在邊界上也算守備範圍內。

– 輸入限制 –

• 1 ≤ a ≤ b ≤ 2, 147, 483, 647

• 1 ≤ n ≤ 2, 147, 483, 647

通常會有個上限和下限，而掉在範圍內的，就說是落在守備範圍內。例如要求智商介於 50 到 120 之間，那麼 70 落在守備範圍內，而 130 不是。
給予上限、下限和目標數值，請判斷是否落在守備範圍內。

```cpp
#include <iostream>
#include <stdio.h>
#include <math.h>

using namespace std;
int main(){
	
	int a,b,n;
	cin >> a >> b >> n;
	
	if (a<=n && b>=n) //不可寫成a<=n<=b
//在大多數語言，a<=n<=b 會被視為 (a<=n)<=b 
//python倒是可以這樣寫(a<=n<=b)，不過在後台也是自動轉回(a<=n && b>=n)
	{
		cout << "yes"<<"\n";
	}
	else
	{
		cout << "no"<<"\n";
	}
	
	return 0;
	
	
}
```
![image](https://user-images.githubusercontent.com/96654161/193447701-66abffd0-54db-43c2-b2f1-3ae04bac853e.png)


### 第三節 作業四(必做)

– 輸入 –

輸入為一個正整數 s 代表分數。

– 輸出 –

輸出 s 所代表的階級。

– 輸入限制 –

• 0 ≤ s ≤ 100

```cpp
#include <iostream>
#include <stdio.h>
#include <math.h>

using namespace std;
int main(){
	
	int S;
	cin >> S;
	
	if (S==100)
	{
		cout << "S"<<endl;
	}
	else
	if (S>=90)
	{
		cout << "A"<<endl;
	}
	else
	if (S>=80)
	{
		cout << "B"<<endl;
	}
	else 
	if (S>=70)
	{
		cout << "C"<<endl;
	}
	else 
	if (S>=60)
	{
		cout << "D"<<endl;
	}
	else 
	{
		cout << "F"<<endl;
	}
		
	return 0;
	
}
```
![image](https://user-images.githubusercontent.com/96654161/193457705-413e93e2-151d-484d-80d0-f018acaee190.png)

### 第三節 作業五(必做)


– 輸入 –

輸入為四個相異整數 X0、X1、X2、X3，其中 X0、X1 依序為敵艦的左端點與右端點座標，

X2、X3 依序為島風所發射的魚雷左端點與右端點座標。

– 輸出 –

若能夠命中，輸出「yes」；否則輸出「no」。

– 輸入限制 –

+ −109 ≤ X0 < X1 ≤ 109
+ −109 ≤ X2 < X3 ≤ 109
+ X0、X1、X2、X3 兩兩皆不相等。

將敵艦看成一維數線上的一條線段，發射的魚雷投影到該數線上也會形成一條線段，若兩條線段重疊的面積大於 0 則判定此次魚雷命中。

```cpp
#include <iostream>
#include <stdio.h>
#include <math.h>

using namespace std;
int main(){
	//X0、X1 依序為敵艦的左端點與右端點座標
	//X2、X3 依序為島風所發射的魚雷左端點與右端點座標
	int X0,X1,X2,X3;
	cin >> X0>>X1>>X2>>X3;
	if ((X0 <=X2 && X2<=X1) || (X0<=X3 && X3<=X1) || (X2 <=X0 && X1 <= X3))
	{
		cout << "yes"<<endl;
	}
	else
	{
		cout << "no"<<endl;
	}
		
	return 0;
	
}
```
![image](https://user-images.githubusercontent.com/96654161/193458973-e21d567c-5544-472c-8673-574d083b7618.png)


### 第三節 作業六(必做)

數學中的一個常見問題是確定給定點位於哪個像限。有四個像限，編號從至 ，如下圖所示：

![image](https://user-images.githubusercontent.com/96654161/193459872-dac2a8c4-888f-4b7f-b27d-e6fc30920675.png)

![image](https://user-images.githubusercontent.com/96654161/193459891-b471d465-ff3d-4d39-8b67-bd0d3c107b17.png)

```cpp
#include <iostream>
#include <stdio.h>
#include <math.h>

using namespace std;
int main(){
	
	float x,y;
	cin >> x>>y;
	
	if (x>0 && y>0)
	{
		cout << "1"<<endl;
	}
	else
	if (x<0 && y>0)
	{
		cout << "2"<<endl;
	}
	else
	if (x<0 && y<0)
	{
		cout << "3"<<endl;
	}
	else
	if (x>0 && y<0)
	{
		cout << "4"<<endl;
	}
	
	
	return 0;
	
}
```
![image](https://user-images.githubusercontent.com/96654161/193461067-5c2e66d4-095d-4d34-a062-e7f7b076ca7a.png)

### 第三節 作業七(必做)

– 輸入 –

輸入為一個正整數 n 代表要判斷的數字。

– 輸出 –

輸出是否為他要的數字。如果是，輸出「GREAT!!」；如果不是，輸出「OAQ」。

– 輸入限制 –

+ 1 ≤ n ≤ 2, 147, 483, 647

![image](https://user-images.githubusercontent.com/96654161/193464652-5bb0572c-7e3c-44f2-bb9b-f9256b3d9fce.png)

> 7777 就是數字完全相同的四位數，但 8787 就不是。而 666 不是四位數，因此也不是。

```cpp
#include <iostream>
#include <stdio.h>
#include <math.h>

using namespace std;
int main(){
	
	int n,unit1,ten2,hundred3,thousand;
	cin >> n;
	
	unit1 = n / 1 % 10; //取個位數
	ten2 = n / 10 % 10;
	hundred3 = n / 100 % 10;
	thousand = n / 1000% 10;
	
	if (n % 10000 == n)
	{
		if (unit1 == ten2 && ten2 == hundred3 && hundred3 == thousand && thousand == unit1)
		{
			cout << "GREAT!!" <<endl;
		}
		else
		{
			cout << "OAQ" <<endl;
		}
	}
	else
	{
		cout << "OAQ" <<endl;
	}
		

	return 0;
	
}
```

![image](https://user-images.githubusercontent.com/96654161/193464602-c2eea224-bed3-468c-9dad-f570e7b30e55.png)

### 第三節 作業八(必做)

![image](https://user-images.githubusercontent.com/96654161/193467496-bdababdd-b636-44e3-b15b-598f8e55d0ed.png)

求長方形第四個未知座標

![image](https://user-images.githubusercontent.com/96654161/193467782-49b001e0-6226-4fcc-a80a-e0ab949f4086.png)

```cpp
#include <iostream>
using namespace std;

int main(){
    int a,b,c,d,e,f;
    while(cin >> a >> b){
        cin >> c >> d;
        cin >> e >> f;
        
        if (a == c){
            if (f == b) cout << e << " " << d << endl;
            else cout << e << " " << b << endl;
            
        }
        else{
            if (b == d) cout << a << " " << f << endl;
            else cout << a << " " << d << endl;
            
        }
    }
    
    
}
```

![image](https://user-images.githubusercontent.com/96654161/193467475-92d69ada-03ed-456e-b5f0-7af9a56931e4.png)
