#include<stdio.h>
int MaxDivisor(int a, int b);       //最大公约数
int MinMultiple(int a, int b);      //最小公倍数

int main(void)
{
    int a, b, maxdivisor, minmultiple;
    scanf ("%d %d", &a, &b);

    if (b>a)                        //把大的给a，小的给b
    {
        maxdivisor = MaxDivisor(b, a);
        minmultiple = MinMultiple(a, b);
    }
    else
    {
        maxdivisor = MaxDivisor(a, b);
        minmultiple = MinMultiple(a, b);
    }

    printf ("maxdivisor = %d, minmultiple = %d\n", maxdivisor, minmultiple);

    return 0;
}

int MaxDivisor(int a, int b)        //辗转相除法
{
    int temp;
    do
    {
        temp = a % b;               //取余
        a = b;                      //将被除数给a
        b = temp;                   //将取余得到的数给b
    }while (temp != 0);             //当取余==0时，最后的赋给a的b是最大公约数

    return a;
}

int MinMultiple(int a, int b)
{
    int result;
    result = a * b / MaxDivisor(a, b);      //两数的乘积大小==最大公约数*最小公倍数

    return result;
}

/*2020.09.09__Gubo*/
