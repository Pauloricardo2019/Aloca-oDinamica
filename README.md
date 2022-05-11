# Aloca-oDinamica
Exemplo de alocação dinamica

/******************************************************************************

                            Online C Compiler.
                Code, Compile, Run and Debug C program online.
Write your code in this editor and press "Run" button to compile and execute it.

*******************************************************************************/

#include <stdio.h>
#include <stdlib.h>

//Armazenar o resultado da soma em total
void soma(int A, int B, int C, int*total){
    *total = A+B+C;
}

int main()
{
    int* sum=NULL;
    int* A = malloc(sizeof(int));
    int* B = malloc(sizeof(int));
    int* C = malloc(sizeof(int));
    *A = 5;
    *B = 5;
    *C = 5;
    sum = malloc(sizeof(int));
    
    soma(*A,*B,*C,sum);
    
    printf("%d\n", *sum); 
    
    return 0;
}
