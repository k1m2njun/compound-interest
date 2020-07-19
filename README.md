#include <stdio.h>
#include <cs50.h>
#include <math.h>

float interest = 0.012; //연이율 1.2%

int main(void)
{
    int principal = get_int("\n예금하실 금액을 입력해주세요.\n");
    int year = get_int("몇 년 만기로 설정하실건가요?\n");

    printf("%i년 만기 시 받으실 원리금은 %0.f원입니다\n", year, principal*(1-pow(interest, year+1))/(1-interest)); //입력한 연수에 따른 '등비수열의 합'으로 복리계산
