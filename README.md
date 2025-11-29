# C--1
a simple game
##主要内容
1.随机生成数字，你来猜
2.我会根据你的猜测，给一个反馈
#include<stdio.h>
#include<stdlib.h>
#include<time.h>
int main()
{
	int target,guess;
	 srand(time(NULL));
	 target=rand() %100+1;
	 printf("我已经想好一个1-100之间的数了：\n");
	 printf("你只管猜，我会告诉你大了或小了：\n");
	 do
	 {
	 	printf("请输入你要猜的数字："); 
	 	scanf("%d",&guess);
	 	if(guess>target||guess<target)
	 	 {
		  	if(guess>target)
		  	printf("大了!\n");
			  else 
			  printf("小了!\n");}
	 	else
		 printf("恭喜你猜对了!\n"); 	
	 }while(guess!=target); 
	 return 0;
}
