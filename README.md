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


#include <stdio.h>
#include <stdlib.h>

//Somar o intervalo entre A e B 
//e guardar em uma variavel alocada dinamicamente dentro da funcao
//devolver o endereço dessa variavel alocada
int* somaIntervalo(int A, int B){
    
    int* sum = (int*) malloc(sizeof(int));
    *sum = 0;
    for(int i = A;i <= B; i++){
        *sum += i;
    }
    return sum;
}

int main()
{
    int a = 1,b = 10;
    

    int* end = somaIntervalo(a,b);

    printf("%d\n", *end);
    
    return 0;
}
