# CONTADOR DE VITÓRIAS EM GRENAIS

O obejtivo deste programa é exibir qual time ganhou mais grenais a partir da inserção do numero de gols para cada time **por parte do usuário**, todos os dados são ficticios. 

#Funcionamento

* **Declaração de variáveis**

Foram declaradas 7 variáveis iniciais são elas: 

```C
    int gremio=0, inter=0, x=0, y=0, empate=0, jogo=0;
    int vax=1;
```

* **Estrutura do código**

De inicio um ''c printf ''  solicita ao usuário que insira o resultado de um **GreNal**, neste ponto o usuário deve informar o placar do jogo em questão, por exemplo:

''C
        printf("digite os gols do inter e depois do gremio: ");
        scanf("%d %d", &x, &y);
    \\ Exemplo de dado inserido: 3x2
''

Após o sistema utiliza IF e Else para determinar para quem irá a pontuação do jogo.

''C
    if(x > y)
	{
		inter++;	
	}
	else if(y > x)
	{
		gremio++;	
	}
	else if(x == y)
	{
		empate++;
	}
''
Então ele solicita se o usuário deseja inserir um novo resultado utilizando uma estrutura de **Do - While** conforme exemplo: 

''C
	    do
		{
			printf("Novo grenal (1-sim 2-nao)\n");
			scanf("%d", &vax);
		}while(vax != 1 && vax != 2);
		
		if(vax!=1)
			break;
''

**Resultado** 

Após o sistema utiliza outra esturua de **IF - Else** para definir qual time obteve mais vitórias no **clássico GreNal** conforme exemplo: 

''C
    printf("%d grenais\n", jogo);
        printf("Vitorias doInter:%d\nVitorias doGremio:%d\nEmpates:%d\n", inter, gremio, empate);
        
        if(inter > gremio)
        {
            printf("Inter venceu mais\n");
        }
        else if(gremio > inter)
        {
            printf("Gremio venceu mais\n");
        }
        else if(inter == gremio)
        {
            printf("Nao houve vencedor\n");
        }
''