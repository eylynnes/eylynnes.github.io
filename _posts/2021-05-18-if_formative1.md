---
layout: single
title: "C언어 수행평가 정리"

toc: true
toc_sticky: true
toc-label: "페이지 주요 목차"

categories: "형성평가"
--- 

### 01. 사주보기 
![saju](/assets/images/사주 보기.jpg) 
~~~c 
#include <stdio.h> 
int main(void) 
{ int year,month,day,result; 
  
printf("당신의 사주를 봐드립니다.\n"); 
printf("연도 월 일을 차례대로 입력하세요 : "); 
scanf("%d %d %d",&year, &month, &day); 
result=(year-month+day)%10; 
if(result==0) 
 printf("당신의 사주는 대박입니다.\n");
else 
 printf("당신의 사주는 그럭저럭입니다.\n"); 
return 0; 
}

~~~ 

### 02. 3개의 터널 통과
![tunnul](/assets/images/3개의 터널 통과.jpg) 
~~~c 
#include <stdio.h> 
int main(void) 
{ int tunnul_1, tunnul_2, tunnul_3; 
 printf("세 터널의 높이를 차례대로 입력하세요 : "); 
 scanf("%d,%d,%d",&tunnul_1,&tunnul_2,&tunnul_3); 
 if(tunnul_1<=170) 
 printf("충돌 %d", tunnul_1); 
 else if(tunnul_2<=170) 
 printf("충돌 %d", tunnul_2); 
 else if(tunnul_3<=170) 
 printf("충돌 %d", tunnul_3); 
 else 
 printf("무사 통과"); 
 return 0; 
}
~~~ 

### 03. 이 달은 며칠까지 있을까? 
![callenderl](/assets/images/달이 며칠까지 있을까.jpg) 
~~~c 
#include <stdio.h> 
int main(void) 
{ int year, month; 
  
 printf("연도와 월을 입력하세요 : "); 
 scanf("%d%d", &year, &month); 
 printf("%d년 %d월의 마지막날은 ", year, month); 
  
 if(month==1||month==3||month==5||month==7||month==8||month==10||month==12)  printf("31일"); 
 else if(month==4||month==6||month==9||month==11) 
 printf("30일"); 
 else 
 { 
 if((year%4==0 && year%100!=0) || year%400==0) 
 printf("29일");
  else 
 printf("28일"); 
 } 
 printf("입니다.\n"); 
 return 0; 
}
~~~ 

### 04. 성적 계산
![grade](/assets/images/grade.PNG) 
~~~c
#include <stdio.h>
 
int main(void) {
float a, b, c;
int d, e, f;
float score;
printf("***과목별 점수 계산 프로그램***\n");
printf("중간고사 반영비율/받은 점수를 입력하세요 : ");
scanf("%f%d", &a, &d);
printf("기말고사 반영비율/받은 점수를 입력하세요 : ");
scanf("%f%d", &b, &e);
printf("중간고사 반영비율/받은 점수를 입력하세요 : ");
scanf("%f%d", &c, &f);
score = a*d+b*e+c*f;
printf("점수는 %.1f입니다.\n", score);
 
return 0;
}
~~~

### 05. 30분 전
![before](/assets/images/clock.PNG) 
~~~c
#include <stdio.h>
int main(void) {
int hour, min;
printf("시간과 분을 입력하세요 : ");
scanf("%d, %d", &hour, &min);
printf("입력한 시간의 30분 전 시간은 : ");
if(min>=30)
printf("%d시 %d분\n", hour, min-30);
else{
 if(hour==0)
 printf("%d시 %d분\n", 23, min+30);
 else
 printf("%d시 %d분\n", hour-1, min+30);
}
 return 0;
}
~~~

### 06. 도어락
![doorlock](/assets/images/door.PNG) 
~~~c
#include <stdio.h> 
int main(void) {
int select;
char dic='c', ic;
int dpw=24680, pw;
double dfig=1.22345678, fig;
 
printf("장치 선택 : ");
scanf("%d", &select);
 
if(select==1){
 printf("IC카드: ");
 scanf(" %char", &ic);}
else if(select==2){
  printf("비밀번호 : ");
  scanf("%d", &pw);}
else{
  printf("지문 : ");
  scanf("%lf", &fig);
}
if(dic==ic || dpw==pw || dfig==fig)
 printf("문 열림~");
else
printf("디리릭!디리릭!");}
 return 0; 
}
~~~ 


### 07. 가위바위보
![scissorpaper](/assets/images/rock.PNG) 
~~~c
#include <stdio.h> 
int main(){
 
char com, user;
com='s';
 
printf("r/s/p : ");
scanf("%c", &user);
 
if(com==user)
printf("비겼다.");
else if(com=='r' && user=='s')||(com=='s' && user=='p')||(com=='p' && user=='r')
printf("졌다.")
else
printf("이겼다.")}
 return 0; 
}
~~~ 

