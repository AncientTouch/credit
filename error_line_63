#include <stdio.h>

int main(void)
{
    long long num;
    int count = 0;
    int fn1 = 0;
    int fn2 = 0;
    
    printf("Enter Credit Card Number: ");
    scanf("%llu", &num);
    
    while ( num != 0 )
    {
        num /= 10;
        ++count;
    }
    for ( int i = 0; i < count/2; i++ )
    {
        for ( int m = 100; m < (10^count); m = m*100 )
        {
            int mod1 = num % m;
            for( int n = 10; n < m; n = n*100 )
            {
                int mul = (mod1 / n)*2;
                if ( (mul % 10) == mul )
                fn1 =  fn1 + mul;
                else
                {
                int f = mul / 10;
                int b = mul % 10;
                fn1 = fn1 + b + f;
                }
            }
        }
        for ( int p = 10; p < (10^count); p = p*100 )
        {
            int mod2 = num % p;
            fn2 = fn2 + mod2;
        }
    }
    int final = fn1 + fn2;
    
    if ( final % 10 != 0 )
    {
        printf("INVALID\n");
    }
        else if( count < 13 || count == 14 || count > 16 )
        {
        printf("INVALID\n");
        }
        else if( count == 15 )
        {
        printf("AMEX\n");
        }
        else if( count == 13 )
        {
        printf("VISA\n");
        }
        else if( count == 16 )
        {
            if( (unsigned long long) num / (1000000000000000)  == 5 )
            {
            printf("MASTERCARD\n");
            }
            else
            {
            printf("VISA\n");
            }        
        }
}    
