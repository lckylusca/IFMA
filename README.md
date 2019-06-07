#include <stdio.h>
#include <stdlib.h>
#include <locale.h>

typedef struct{
    char nome[100];
    int idade;
    char cpf[13];
    char sexo[30];
}ficha_insc;

int main(){
    int i, j, n;

    setlocale(LC_ALL, "Portuguese");

        printf("\nESSE PROGRAMA TEM COMO FUNÇÃO CRIAR UMA FICHA DE INSCRIÇÃO\n\n");
        printf("Quantas pessoas desejas cadatrar? ");
        scanf("%d",&j);

        ficha_insc ficha;

        for(i=0;i<j;i++){
            printf("Digite a ficha de inscrição da pessoa %d:",i+1);

            printf("\n\nDigite o nome: ");
            fflush(stdin);
            fgets(ficha.nome, 100, stdin);

            printf("Digite a idade: ");
            scanf("%d",&ficha.idade);

            printf("Digite a CPF: ");
            fflush(stdin);
            fgets(ficha.cpf, 100, stdin);

            printf("Digite o sexo: ");
            fflush(stdin);
            fgets(ficha.sexo, 100, stdin);

            if(i=j){
                printf("\n...finalizando a ficha...\n");
            }
                else{
                        printf("\n...proxima pessoa...\n");
                    }

                system("pause");
            system("cls");

        }

    for(i=0;i<j;i++){
        printf("\n\nA ficha da pessoa %d", i+1);
        printf("\nNome: %sIdade: %d \nCPF: %sSexo: %s\n\n", ficha.nome, ficha.idade, ficha.cpf, ficha.sexo);
    }

      system("pause");

    return 0;
}
