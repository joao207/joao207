- 👋 Hi, I’m @joao 207 (João Miguel) Estou cursando Técnico em Desenvolvimento de Sistemas.
- 👀 I’m interested in  uma forma de  obter conhcimento e em busca de um estágio na área.
- 🌱 I’m currently learning  Banco de dados. Tenho conhecimento em C e C++.
- 💞️ I’m looking to collaborate no possível, dentro das minhas competências.
-📫 How to reach me  miguelrodriguesbh@gmail.com














Atividade feita no curso de Desenvolvimento de Sistemas.

#include <stdio.h>
#include <stdlib.h>
#include <locale.h>

main()
{
	float n1, n2;
	char opcao;
	
	setlocale(LC_ALL,"Portuguese");
	do {
		printf("\n\t\t\t\t\tMENU DE OPÇÕES\n");
		printf("\t\t+ . Adição\n");
		printf("\t\t- . Subtração\n");
		printf("\t\t* . Multiplicação\n");
		printf("\t\t/ . Divisão\n");
		printf("\t\t0 . Sair\n");
		printf("\t\t\t	Escolha uma opção -> ");
		fflush(stdin);
		scanf("%c", &opcao);
		if (opcao == '+' || opcao == '-' || opcao == '*' || opcao == '/'){ 
			printf("\n\t\t\tInforme o 1o operando: ");
			scanf("%f", &n1);
			printf("\n\t\t\tInforme o 2o operando: ");
			scanf("%f", &n2);
		}
		switch(opcao){
			case '+': 
				printf("\n\t\t\tAdição: %.2f\n", n1 + n2);
				break;
			case '-':
				printf("\n\t\t\tSubtração: %.2f\n", n1 - n2);
				break;
			case '*':
				printf("\n\t\t\tMultiplicação: %.2f\n", n1 * n2);
				break;
			case '/':
				if (n2 != 0)
					printf("\n\t\t\tDivisão: %.2f\n", n1 / n2);
				else printf("\n\t\t\tErro: divisão por zero\n");
				break;
			case '0': 
				printf("\n\t\t\tFinalizando...\n");
				break;
			default: printf("\n\t\t\tOpção inválida\n");
		}			 
	}while (opcao != '0');
}
