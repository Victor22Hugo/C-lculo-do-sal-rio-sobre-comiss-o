#include<stdio.h>// Input e Ouput
#include<windows.h>// Implementa a função Sleep()
int main(){

	float comissao=0.09, sal=200;
	int i, vendedor, V[9]={0,0,0,0,0,0,0,0,0};

	printf("BEM VINDO(A) A NOSSA CALCULADORA DE SALARIOS!\n");
	Sleep(1500);// Faz uma pausa no programa de 1,5 segudos
	do{
        printf("Quantos vendedores a empresa tem? ");
        scanf("%d",&vendedor);
        Sleep(1000);// Faz uma pausa no programa de 1 segudo
	}while(!(vendedor>=0));
	if(vendedor>=10)
        printf("Eita, quantos vendedores!\n");

	float venda[vendedor];
	int cont[vendedor];

	for(i=0;i<vendedor;i++){// Início do for
		printf("\nDigite o total de vendas do vendedor %d: ", i+1);
		scanf("%f",&venda[i]);
	}//Fim do for
	for(i=0;i<vendedor;i++)
		venda[i]=(venda[i]*comissao)+sal;
    for(i=0;i<vendedor;i++){// Início do for
        if ((venda[i]>=200)&&(venda[i]<=299))
            V[0]++;
        else if(venda[i]>=300 && venda[i]<=399)
            V[1]++;
        else if(venda[i]>=400 && venda[i]<=499)
            V[2]++;
        else if(venda[i]>=500 && venda[i]<=599)
            V[3]++;
        else if(venda[i]>=600 && venda[i]<=699)
            V[4]++;
        else if(venda[i]>=700 && venda[i]<=799)
            V[5]++;
        else if(venda[i]>=800 && venda[i]<=899)
            V[6]++;
        else if(venda[i]>=900 && venda[i]<=999)
            V[7]++;
        else if(venda[i]>=1000)
            V[8]++;
    }// Fim do for

	printf("Placar:\n\n200 - 299: %d\n300 - 399: %d\n",V[0], V[1]);
    printf("400 - 499: %d\n500 - 599: %d\n",V[2], V[3]);
    printf("600 - 699: %d\n700 - 799: %d\n",V[4], V[5]);
    printf("800 - 899: %d\n900 - 999: %d\n",V[6], V[7]);
    printf("Acima de 1000: %d\n", V[8]);
    Sleep(4000);// Faz uma pausa no programa de 4 segundos
    system("cls");
    printf("OBRIGADO(A) E VOLTE SEMPRE!\n");
		return 0;
	}
