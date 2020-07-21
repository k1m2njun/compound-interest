#include <stdio.h>
#include <cs50.h>
#include <math.h>

int main(void)
{
    //사용자 원금 입력
    int principal = get_int("\n예금하실 금액을 입력해주세요.\n");
    
    //예금 기간 입력
    int year = get_int("몇 년 만기로 설정하실건가요?\n");
    
    //연복리 계산식
    float compound_interest = principal * pow(1 + 0.012, year);
    
    //입력한 원금과 기간에 따른 복리식 계산
    printf("%i년 만기 시 받으실 원리금은 %.0f원입니다\n", year, compound_interest);
}
