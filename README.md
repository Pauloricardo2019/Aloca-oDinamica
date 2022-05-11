# AlocacaoDinamica
Exemplo de alocação dinamica

include <stdio.h>
include <stdlib.h>

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
