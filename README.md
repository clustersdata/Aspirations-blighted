# Aspirations-blighted

Aspirations blighted

Problem Description

话说MCA山上各路豪杰均出山抗敌，去年曾在江湖威名显赫的，江湖人称<万军中取上将首级舍我其谁>的甘露也不甘示弱，“天将降大任于斯人也，必先劳其筋骨，饿其体肤，空乏其身”他说。可惜，由于去年取上将首级时不慎右手右关节第七次骨折，养伤达一年之久，空有一腔抱负却壮志难酬，如今天下危亡，习武之人又怎能袖手旁观，于是他决定出山协助威士忌共抗辽贼，这时他的对头枫冰叶子出现，两人都是水属性，但由于十年前的一场恩怨（这是后话）势成水火。


枫冰叶子要求甘露回答一个问题，否则不让他离开，可惜甘露绞尽脑汁未果，希望你来帮他解决，助他完成大业。


问题是这样的：给你一个小数x，让你算出小数点后第n位是什么，(1 <= n <= 6)

Input

首先输入一个t,表示有t组数据，跟着t行：

每行输入一个小数（输入数据保证一定是a.b的形式,为了简单化问题，没有循环小数的情况）

然后跟一个n,表示小数点后第几位

Output

输出一个数表示小数点后第n位的数

Sample Input

3 1.234 1 2.345 2 3.456 3

Sample Output

2 4 6


代码：

#include<stdio.h>

#include<string.h>

char x[99];

int main()

{

	int i,n,t,len,ans;
  
	scanf("%d",&t);
  
	while(t--&&scanf("%s %d",x,&n))
  
	{
  
		len = strlen(x);
    
		for(i=0; i<len; i++)
    
			if(x[i]=='.') break;
      
		if(len-i-1<n) ans = 0;
    
		else ans = x[i+n]-'0';
    
		printf("%d\n",ans);
    
	}
  
}
