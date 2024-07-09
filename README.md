____________________________![Take (2)](https://github.com/FernandoCMFilho/Take-a-look/assets/54756245/b678187e-8796-418f-8d9b-624733494b5b) ___________________________
#### Esse é meu trabalho final da materia de AP1, onde uma parte foi feita em portugol, e a outra em C
### ![electro 15](https://github.com/FernandoCMFilho/Take-a-look/assets/54756245/0339e8a7-3132-41b9-97df-60de91fb2a38) Cadastro (Portugol)
``` Portugol
Algoritmo "cadastro"
// Disciplina   : [Linguagem e Lógica de Programação]
// Professor   : Antonio Carlos Nicolodi
// Descrição   : Aqui você descreve o que o programa faz! (função)
// Autor(a)    : Nome do(a) aluno(a)
// Data atual  : 23/11/2022
Var
   // Seção de Declarações das variáveis
   ndu,senha,nomeu,email,senhac:Caracter
   opc,i,sexo,idd,info:inteiro
Inicio
   // Seção de Comandos, procedimento, funções, operadores, etc...
   opc<-0
   escreval("--------------------")
   escreval("|   Bem vindo ao   |")
   escreval("|    Take A Look   |")
   escreval("--------------------")
   repita                                 //Loop caso opção não seja 1, 2 ou 3
      escreval("---------------------")
      escreval("| Escolha uma opção |")
      escreval("|     1-Login       |")
      escreval("|     2-Cadastro    |")
      escreval("|     3-Sair        |")
      escreval("---------------------")
      leia (opc)
      se(opc=1) entao
         repita            //Loop para caso nome de usuário ou senha incorretos


            escreval("---------------------")
            escreval("| Nome de usuario:  |")
            escreval("---------------------")
            leia(ndu)
            escreval("---------------------")
            escreval("| Digite sua senha: |")
            escreval("---------------------")
            leia(senha)
            se ((ndu<>nomeu)ou(senha<>senhac)) entao
               escreval("xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx")
               escreval("\Usuario ou senha incorreto(s)/")
               escreval("xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx")
               opc<-0
               repita     //Loop caso a pessoa escolha uma opção inválida
                  escreval("--------------------------------")
                  escreval("|  Escolha uma opção a seguir  |")
                  escreval("|       1-Menu anterior        |")
                  escreval("|       2-Fazer Cadastro       |")
                  escreval("|       3-Sair                 |")
                  escreval("--------------------------------")
                  leia(opc)
               ate ((opc=1)ou(opc=2)ou(opc=3))
            senao
            fimse
         ate ((ndu=nomeu)e(senha=senhac))ou((opc=1)ou(opc=2)ou(opc=3))
      fimse
      se (opc=2) entao
         escreval("--------------------")
         escreval("|  Bem vindo ao    |")
         escreval("|   Cadastro       |")
         escreval("--------------------")
         escreval("Crie um nome de usuario:")
         leia(nomeu)
         escreval("Seu email:")
         leia(email)
         repita
            escreval("Sexo:")
            escreval("1-Masculino, 2-Feminino, 3-Prefiro não dizer")
            leia(sexo)
            se ((sexo<>1)e(sexo<>2)e(sexo<>3)) entao
               escreval("Por favor, digite um valor valido")
            fimse
         ate (sexo=1)ou(sexo=2)ou(sexo=3)
         repita
            escreval("Idade:")
            leia(idd)
            se (idd<=11) entao
               escreval("xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx")
               escreval("|  Você precisa ter 12 anos ou  |")
               escreval("|  mais para usar o Take a Look |")
               escreval("xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx")
            fimse
            se (idd>=129) entao
               escreval("xxxxxxxxxxxxxxxxxxxxxxxxxxxxx")
               escreval("|  Insira uma idade valida  |")
               escreval("xxxxxxxxxxxxxxxxxxxxxxxxxxxxx")
            fimse
         até ((idd>=12)e(idd<130))
         escreval("Crie uma senha:")
         leia(senhac)
         escreval("-----------------------")
         escreval("| * Cadastro          |")
         escreval("|     Realizado       |")
         escreval("|       Com sucesso! *|")
         escreval("-----------------------")
      fimse
      se (opc=3) entao
fimalgoritmo
senao
fimse
se (opc<>1)e(opc<>2)e(opc<>3) entao
   escreval("xxxxxxxxxxxxxxxxxxxxxxxxxxx")
   escreval("| Insira uma opção valida |")
   escreval("xxxxxxxxxxxxxxxxxxxxxxxxxxx")
fimse
ate ((ndu=nomeu)e(senha=senhac)e(ndu<>0))    //     Menu no Code:Blocks (C) //
repita                                       //-----------------------------//
   escreval("--------------------------")    // 1-Ver Perfil                //
   escreval("|      1-Ver perfil      |")    // 2-Meu guarda-roupa          //
   escreval("|      2-Sair            |")    // 3-Voltar ao meno anterior   //
   escreval("--------------------------")    //-----------------------------//
   leia(i)
   escolha (i)
   caso 1
      escreval("Usuario:",nomeu)
      escreval("Email:",email)
      se (sexo=1) entao
         escreval("Sexo:Masculino")
      fimse
      se (sexo=2) entao
         escreval("Sexo:Feminino")
      fimse
      se (sexo=3) entao
         escreval("Sexo:Prefiro Não Dizer")
      fimse
      escreval("Idade:",idd)
      escreval("Deseja mudar alguma informação?")
      escreval("Pressione 1 para Sim")
      escreval("Pressione qualquer tecla para não")
      leia(info)
      se (info=1) entao
         repita
            escreval("Qual informação deseja mudar?")
            escreval("---------------------")
            escreval("|   1-Usuario       |")
            escreval("|   2-Email         |")
            escreval("|   3-Sexo          |")
            escreval("|   4-Idade         |")
            escreval("|   5-Menu Anterior |")
            escreval("---------------------")
            leia(info)
            escolha (info)
            caso 1
               escreval("Digite o novo nome de usuario:")
               leia(nomeu)
            caso 2
               escreval("Digite o novo email:")
               leia(email)
            caso 3
               repita
                  escreval("Digite a nova opção:")
                  escreval("1-Masculino, 2-Feminino, 3-Prefiro não dizer")
                  leia(sexo)
                  se (sexo<>1)e(sexo<>2)e(sexo<>3) entao
                     escreval("xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx")
                     escreval("| Por favor, digite um valor valido |")
                     escreval("xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx")
                  fimse
               ate (sexo=1)ou(sexo=2)ou(sexo=3)
            caso 4
               repita
                  escreval("Digite a nova idade:")
                  leia(idd)
                  se (idd<=11) entao
                     escreval("xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx")
                     escreval("|  Você precisa ter 12 anos ou  |")
                     escreval("|  mais para usar o Take a Look |")
                     escreval("xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx")
                  fimse
                  se (idd>=129) entao
                     escreval("xxxxxxxxxxxxxxxxxxxxxxxxxxxxx")
                     escreval("|  Insira uma idade valida  |")
                     escreval("xxxxxxxxxxxxxxxxxxxxxxxxxxxxx")
                  fimse
               até ((idd>=12)e(idd<130))
            caso 5
            outrocaso
               escreval("xxxxxxxxxxxxxxxxxxxxxxxxxxx")
               escreval("| Insira uma opção valida |")
               escreval("xxxxxxxxxxxxxxxxxxxxxxxxxxx")
            fimescolha
         ate (info=5)
      senao
      fimse
   caso 2
   outrocaso
      escreval("xxxxxxxxxxxxxxxxxxxxxxxxxxx")
      escreval("| Insira uma opção valida |")
      escreval("xxxxxxxxxxxxxxxxxxxxxxxxxxx")
   fimescolha
ate (i=2)
Fimalgoritmo
```

### ![electro 15](https://github.com/FernandoCMFilho/Take-a-look/assets/54756245/e6dcc298-6ab1-4378-94f2-7f79509d7cfb) Parte logica 
``` C
#include <stdio.h>
#include <stdlib.h>
#include <locale.h>

int main ()
{
    int opc,camiseta[6]= {0,0,0,0,0,0},cal[4]= {0,0,0,0},berm[3]= {0,0,0},tenis[3]= {0,0,0}, casoc[2] = {0,0};    //camiseta,calça,bermuda,sapatos,camisa social
    int c=0,cl=0,b=0,t=0,cs=0,aux1,aux2,aux3,aux4,aux5;                                                          //Camiseta,CaLça,Bermuda,sapaTos
    int coresb[8] = {0,0,0,0,0,0,0,0};                                                                          //cores de blusas
    int cortipo[4] = {0,0,0,0};                                                                                //Tipos e cores de calça
    int corberm[4] = {0,0,0,0,0};                                                                             //Cores e tipos de bermuda
    int tipot[3] = {0,0,0};                                                                                  //Tipos de tenis{social, casual e esportivo
    int corsoc[2] = {0,0};
    int opc_2;


    setlocale(LC_ALL, "Portuguese");
    do
    {
        printf("---------------------------------------------\n");
        printf("|==============MENU PRINCIPAL===============|\n");
        printf("|--------- Bem vindo ao Take a Look! -------|\n");
        printf("|--------- Selecione sua opção! ------------|\n");
        printf("|--------- 1-Meu Guarda-Roupa --------------|\n");
        printf("|--------- 2-Take A Look -------------------|\n");
        printf("|--------- 3-Meu perfil --------------------|\n");
        printf("|--------- 4-Contatos para relatar bugs ----|\n");
        printf("|--------- 5-Encerrar o programa -----------|\n");
        printf("---------------------------------------------\n");
        printf("\n\n\n\n");



        scanf("%d",&opc);
        fflush(stdin);

        switch (opc)
        {
        case 1:
            printf("-----------------------------\n");
            printf("| Bem vindo ao guarda roupa |\n");
            printf("-----------------------------\n");

            printf("\n^>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>^\n");
            printf("^  Você tem %d camisetas normais brancas       ^\n",coresb[0]);
            printf("^  Você tem %d camisetas normais pretas        ^\n",coresb[1]);
            printf("^  Você tem %d camisetas normais vermelhas     ^\n",coresb[2]);
            printf("^  Você tem %d camisetas normais estampadas    ^\n",coresb[3]);
            printf("^  Você tem %d Regatas brancas                 ^\n",coresb[4]);
            printf("^  Você tem %d Regatas pretas                  ^\n",coresb[5]);
            printf("^  Você tem %d Regatas vermelhas               ^\n",coresb[6]);
            printf("^  Você tem %d Regatas estampadas              ^\n",coresb[7]);
            printf("^<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<^\n");
            printf("\n\n\n");
            do
            {

                printf("    //////////////////////////////////\n");
                printf("   /Deseja adicionar alguma peça?   /\n");
                printf("  /1-sim                           /\n");
                printf(" /0-não                           /\n");
                printf("//////////////////////////////////\n");
                scanf("%d",&aux1);
                if ((aux1!=1)&&(aux1!=0))
                {
                    printf("xxxxxxxxxxxxxxxxxxxx\n");
                    printf("|  Opção Invalida  |\n");
                    printf("xxxxxxxxxxxxxxxxxxxx\n");
                }

            }
            while((aux1!=1)&&(aux1!=0));

            if ((camiseta[0]==0)&&(camiseta[1]==0)&&(camiseta[2]==0)&&(camiseta[3]==0)&&(camiseta[4]==0)&&(camiseta[5]==0))
            {
                printf("     //////////////////////////////////\n");
                printf("    /Seu Guarda-Roupa de camisetas   /\n");
                printf("   /Está Vazio                      /\n");
                printf("  //////////////////////////////////\n");
            }
            if (aux1==1)
            {
                for(c==0; c<6; c++)
                {


                    printf("-----------------------------------------------------------\n");
                    printf("|         Digite valores para suas roupas (até 6 peças)   |\n");
                    printf("|       Abaixo a lista de codigos para cada tipo de roupa |\n");
                    printf("|      Numero 10---camisetas normais brancas              |\n");
                    printf("|      Numero 20---camisetas normais pretas               |\n");
                    printf("|      Numero 30---camisetas normais vermelhas            |\n");
                    printf("|      Numero 40---camisetas normais estampadas           |\n");
                    printf("|      Numero 50---Regatas brancas                        |\n");
                    printf("|      Numeor 60---Regatas pretas                         |\n");
                    printf("|      Numero 70---Regatas Vermelhas                      |\n");
                    printf("|      Numero 80----Regatas estampadas                    |\n");
                    printf("|      Digite qualquer valor para não adicionar nenhuma   |\n");
                    printf("-----------------------------------------------------------\n");
                    scanf("%d",&camiseta[c]);

                    if (camiseta[c]==10)
                    {
                        coresb[0]++;
                        printf("Camiseta normal branca adicioanda!\n");
                    }
                    if (camiseta[c]==20)
                    {
                        coresb[1]++;
                        printf("Camiseta normal preta adicionada!\n");
                    }
                    if (camiseta[c]==30)
                    {
                        coresb[2]++;
                        printf("Camiseta normal vermelha adicionada!\n");
                    }
                    if (camiseta[c]==40)
                    {
                        coresb[3]++;
                        printf("Camiseta normal estampada adicionada!\n");
                    }
                    if (camiseta[c]==50)
                    {
                        coresb[4]++;
                        printf("Regata branca adicionada!\n");
                    }
                    if (camiseta[c]==60)
                    {
                        coresb[5]++;
                        printf("Regata preta adicionada!\n");
                    }
                    if (camiseta[c]==70)
                    {
                        coresb[6]++;
                        printf("Regata vermelha adicionada!\n");
                    }
                    if (camiseta[c]==80)
                    {
                        coresb[7]++;
                        printf("Regata estampada adicionada!\n");
                    }
                    if ((camiseta[c]!=10) && (camiseta[c]!=20) && (camiseta[c]!=30) && (camiseta[c]!=40) && (camiseta[c]!=50) && (camiseta[c]!=60) && (camiseta[c]!=70) && (camiseta[c]!=80))
                        printf("Nenhuma peça foi adicionada!\n");
                }
                fflush(stdin);
            }
            printf("\n^>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>^\n");
            printf("^  Você tem %d camisetas normais brancas       ^\n",coresb[0]);
            printf("^  Você tem %d camisetas normais pretas        ^\n",coresb[1]);
            printf("^  Você tem %d camisetas normais vermelhas     ^\n",coresb[2]);
            printf("^  Você tem %d camisetas normais estampadas    ^\n",coresb[3]);
            printf("^  Você tem %d Regatas brancas                 ^\n",coresb[4]);
            printf("^  Você tem %d Regatas pretas                  ^\n",coresb[5]);
            printf("^  Você tem %d Regatas vermelhas               ^\n",coresb[6]);
            printf("^  Você tem %d Regatas estampadas              ^\n",coresb[7]);
            printf("^<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<^\n");
            if (aux1==0)
                printf("Indo para proxima opção\n");
            printf("PRoxima opção:\n");
            printf("*CALÇAS*");
            c=0;

            //Codigos para calças
            printf("\n^>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>^\n");
            printf("^ Você tem %d calças jeans             ^\n",cortipo[0]);
            printf("^ Você tem %d calças jeans skinny      ^\n",cortipo[1]);
            printf("^ Você tem %d calças moletom cinza     ^\n",cortipo[2]);
            printf("^ Você tem %d calças moletom pretas    ^\n",cortipo[3]);
            printf("^<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<^\n");
            printf("\n\n\n");
            do
            {
                printf("    //////////////////////////////////\n");
                printf("   /Deseja adicionar alguma peça?   /\n");
                printf("  /1-sim                           /\n");
                printf(" / 0-não                          /\n");
                printf("//////////////////////////////////\n");
                scanf("%d",&aux2);
                if ((aux2!=1)&&(aux2!=0))
                {
                    printf("xxxxxxxxxxxxxxxxxxxx\n");
                    printf("|  Opção Invalida  |\n");
                    printf("xxxxxxxxxxxxxxxxxxxx\n");
                }

            }
            while((aux2!=1)&&(aux2!=0));

            fflush(stdin);
            if ((cal[0]==0)&&(cal[1]==0)&&(cal[2]==0)&&(cal[3]==0))
            {
                printf("     /////////////////////////////////\n");
                printf("    /Seu Guarda-Roupa de calças     /\n");
                printf("   /      Está Vazio               /\n");
                printf("  /////////////////////////////////\n");
                printf("\n\n\n");
            }
            fflush(stdin);
            if (aux2==1)
            {
                for(cl==0; cl<4; cl++)
                {

                    printf("-----------------------------------------------------------\n");
                    printf("|     Digite valores para suas calças (até 4 peças)       |\n");
                    printf("|   Abaixo a lista de codigos para cada tipo de roupa     |\n");
                    printf("|      Numeros de 100---calças jeans                      |\n");
                    printf("|      Numeros de 110---calças jeans skinny               |\n");
                    printf("|      Numeros de 120---calças moletom cinza              |\n");
                    printf("|      Numeros de 130---calças moletom preta              |\n");
                    printf("|      Digite qualquer valor para não adicionar nenhuma   |\n");
                    printf("-----------------------------------------------------------\n");
                    scanf("%d",&cal[cl]);
                    if (cal[cl]==100)
                    {
                        cortipo[0]++;
                        printf("Calça jeans adicionada!\n");
                    }
                    if (cal[cl]==110)
                    {
                        cortipo[1]++;
                        printf("Calça jeans skinny adicionada!\n");
                    }
                    if (cal[cl]==120)
                    {
                        cortipo[2]++;
                        printf("Calça moletom cinza adicionada!\n");
                    }
                    if (cal[cl]==130)
                    {
                        cortipo[3]++;
                        printf("Calça moletom preta adicionada!\n");
                    }
                    if ((cal[cl]!=100) && (cal[cl]!=110) && (cal[cl]!=120) && (cal[cl]!=130))
                        printf("Nenhuma peça foi adicionada!\n");
                }
                fflush(stdin);
                printf("^>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>^\n");
                printf("^ Você tem %d calças jeans             ^\n",cortipo[0]);
                printf("^ Você tem %d calças jeans skinny      ^\n",cortipo[1]);
                printf("^ Você tem %d calças moletom cinza     ^\n",cortipo[2]);
                printf("^ Você tem %d calças moletom pretas    ^\n",cortipo[3]);
                printf("^<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<^\n");
            }


            if (aux2==0)
            {
                printf("Indo para proxima opção\n");
            }
            printf("PRoxima opção:\n");
            printf("BERMUDAS\n");
            cl=0;
            fflush(stdin);

            //Codigos para bermuda


            printf("\n^>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>^\n");
            printf("^ Você tem %d Bermuda jeans             ^ \n",corberm[0]);
            printf("^ Você tem %d Bermuda Tactel preta      ^ \n",corberm[1]);
            printf("^ Você tem %d Bermuda Tactel vermelha   ^ \n",corberm[2]);
            printf("^ Você tem %d Bermuda Tactel estampada  ^ \n",corberm[3]);
            printf("^<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<^\n");
            printf("\n\n\n");
            do
            {
                printf("    ///////////////////////////////////\n");
                printf("   /Deseja adicionar alguma peça?    /\n");
                printf("  /1-sim                            /\n");
                printf(" / 0-não                           /\n");
                printf("///////////////////////////////////\n");
                scanf("%d",&aux3);
                if ((aux3!=1)&&(aux3!=0))
                {
                    printf("xxxxxxxxxxxxxxxxxxxx\n");
                    printf("|  Opção Invalida  |\n");
                    printf("xxxxxxxxxxxxxxxxxxxx\n");
                }

            }
            while((aux3!=1)&&(aux3!=0));

            fflush(stdin);
            if ((berm[0]==0)&&(berm[1]==0)&&(berm[2]==0))
            {
                printf("     ///////////////////////////////////\n");
                printf("    /Seu Guarda-Roupa de bermudas     /\n");
                printf("   /        Está Vazio               /\n");
                printf("///////////////////////////////////\n");
            }
            fflush(stdin);
            if (aux3==1)
            {
                for(b==0; b<3; b++)
                {

                    printf("-----------------------------------------------------------\n");
                    printf("|       Digite valores para suas bermudas (até 3 peças)   |\n");
                    printf("|       Abaixo a lista de codigos para cada tipo de roupa |\n");
                    printf("|      Numeros de 150---Bermuda jeans                     |\n");
                    printf("|      Numeros de 160---Bermuda Tactel preta              |\n");
                    printf("|      Numeros de 170---Bermuda Tactel vermelha           |\n");
                    printf("|      Numeros de 180---Bermuda Tactel estampada          |\n");
                    printf("|      Digite qualquer valor para não adicionar nenhuma   |\n");
                    printf("-----------------------------------------------------------\n");
                    scanf("%d",&berm[b]);
                    if (berm[b]==150)
                    {
                        corberm[0]++;
                        printf("Bermuda Jeans Adicionada!\n");
                    }
                    if (berm[b]==160)
                    {
                        corberm[1]++;
                        printf("Bermuda Tactel preta Adicionada!\n");
                    }
                    if (berm[b]==170)
                    {
                        corberm[2]++;
                        printf("Bermuda Tactel Vermelha Adicionada!\n");
                    }
                    if (berm[b]==180)
                    {
                        corberm[3]++;
                        printf("Bermuda Tactel estampada adicionada!\n");
                    }
                    if ((berm[b]!=150) && (berm[b]!=160) && (berm[b]!=170) && (berm[b]!=180))
                        printf("Nenhuma peça foi adicionada!\n");
                }
                fflush(stdin);
                printf("\n^>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>^\n");
                printf("^ Você tem %d Bermuda jeans             ^ \n",corberm[0]);
                printf("^ Você tem %d Bermuda Tactel preta      ^ \n",corberm[1]);
                printf("^ Você tem %d Bermuda Tactel vermelha   ^ \n",corberm[2]);
                printf("^ Você tem %d Bermuda Tactel estampada  ^ \n",corberm[3]);
                printf("^<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<^\n");
            }
            if (aux3==0)
            {
                printf("Indo Para proxima opção\n");
            }
            printf("Proxima opção:\n");
            printf("SAPATOS\n");
            b=0;
            fflush(stdin);

            //codigo para tenis

            printf("\n^>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>^\n");
            printf("^ Você tem %d Tenis Sociais       ^\n",tipot[0]);
            printf("^ Você tem %d Tenis Casuais       ^\n",tipot[1]);
            printf("^ Você tem %d Tenis Esportivos    ^\n",tipot[2]);
            printf("^<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<^\n");
            printf("\n\n\n");
            do
            {
                printf("    ////////////////////////////////\n");
                printf("   /Deseja adicionar alguma peça? /\n");
                printf("  /1-sim                         /\n");
                printf(" /0-não                         /\n");
                printf("////////////////////////////////\n");
                scanf("%d",&aux4);
                if ((aux4!=1)&&(aux4!=0))
                {
                    printf("xxxxxxxxxxxxxxxxxxxx\n");
                    printf("|  Opção Invalida  |\n");
                    printf("xxxxxxxxxxxxxxxxxxxx\n");
                }

            }
            while((aux4!=1)&&(aux4!=0));

            fflush(stdin);
            if ((tenis[0]==0)&&(tenis[1]==0)&&(tenis[2]==0))
            {
                printf("\n");
                printf("   ////////////////////////////\n");
                printf("  /Seu Guarda-Roupa de Tenis /\n");
                printf(" /      Está Vazio          /\n");
                printf("////////////////////////////\n");
                printf("\n\n");
            }
            fflush(stdin);
            if (aux4==1)
            {
                for(t==0; t<3; t++)
                {

                    printf("-----------------------------------------------------------\n");
                    printf("|       Digite valores para seus sapatos (até 3 itens)    |\n");
                    printf("|       Abaixo a lista de codigos para cada tipo de tenis |\n");
                    printf("|      Numeros de 200---Social                            |\n");
                    printf("|      Numeros de 210---Casual                            |\n");
                    printf("|      Numeros de 220---Esportivo                         |\n");
                    printf("|      Digite qualquer valor para não adicionar nenhum    |\n");
                    printf("-----------------------------------------------------------\n");
                    scanf("%d",&tenis[t]);
                    if (tenis[t]==200)
                    {
                        tipot[0]++;
                        printf("Sapato Social Adicionado\n");
                    }
                    if (tenis[t]==210)
                    {
                        tipot[1]++;
                        printf("Sapato Casual Adicionado\n");
                    }
                    if (tenis[t]==220)
                    {
                        tipot[2]++;
                        printf("Sapato Esportivo Adiconado\n");
                    }
                    if ((tenis[t]!=200) && (tenis[t]!=210) && (tenis[t]!=220))
                        printf("Nenhuma peça foi adicionada!\n");
                }
                fflush(stdin);
                printf("\n^>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>^\n");
                printf("^ Você tem %d Tenis Sociais       ^\n",tipot[0]);
                printf("^ Você tem %d Tenis Casuais       ^\n",tipot[1]);
                printf("^ Você tem %d Tenis Esportivos    ^\n",tipot[2]);
                printf("^<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<^\n");
                printf("\n");
            }
            if (aux4==0)
            {
                printf("Indo para a próxima opção:");
            }
            printf("Próxima opção:");
            printf("*CAMISAS SOCIAIS*");
            t=0;


            //codigo para Camisas sociais

            printf("\n^>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>^\n");
            printf("^ Você tem %d Camisas Sociais pretas     ^\n",corsoc[0]);
            printf("^ Você tem %d Camisas Sociais Brancas    ^\n",corsoc[1]);
            printf("^<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<^\n");
            printf("\n\n\n");
            do
            {
                printf("    ////////////////////////////////\n");
                printf("   /Deseja adicionar alguma peça? /\n");
                printf("  /1-sim                         /\n");
                printf(" /0-não                         /\n");
                printf("////////////////////////////////\n");
                scanf("%d",&aux5);
                if ((aux5!=1)&&(aux5!=0))
                {
                    printf("xxxxxxxxxxxxxxxxxxxx\n");
                    printf("|  Opção Invalida  |\n");
                    printf("xxxxxxxxxxxxxxxxxxxx\n");
                }

            }
            while((aux5!=1)&&(aux5!=0));

            fflush(stdin);
            if ((casoc[0]==0)&&(casoc[1]==0))
            {
                printf("\n");
                printf("   //////////////////////////////\n");
                printf("  /Seu Guarda-Roupa de Camisas /\n");
                printf(" /     Sociais Está Vazio     /\n");
                printf("//////////////////////////////\n");
                printf("\n\n");
            }
            fflush(stdin);
            if (aux5==1)
            {
                for(cs==0; cs<2; cs++)
                {

                    printf("-----------------------------------------------------------\n");
                    printf("|  Digite valores para suas camisas sociais (até 2 peças) |\n");
                    printf("|       Abaixo a lista de codigos para cada cor de roupa  |\n");
                    printf("|      Numeros de 250---Social Branca                     |\n");
                    printf("|      Numeros de 260---Social Preta                      |\n");
                    printf("|      Digite qualquer valor para não adicionar nenhuma   |\n");
                    printf("-----------------------------------------------------------\n");
                    scanf("%d",&casoc[cs]);
                    if (casoc[cs]==250)
                    {
                        corsoc[0]++;
                        printf("Camisa Social Branca Adicionada!\n");
                    }
                    if (casoc[cs]==260)
                    {
                        corsoc[1]++;
                        printf("Camisa Social Preta Adicionada!\n");
                    }
                    if ((casoc[cs]!=250) && (casoc[cs]!=260))
                        printf("Nenhuma peça foi adicionada!\n");
                }
                fflush(stdin);
                printf("\n^>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>^\n");
                printf("^ Você tem %d Camisas Sociais Brancas    ^\n",corsoc[0]);
                printf("^ Você tem %d Camisas Sociais Pretas     ^\n",corsoc[1]);
                printf("^<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<^\n");
                printf("\n");
            }
            if (aux5==0)
            {
                printf("Todas as opções finalizadas\n");
            }
            printf("Retornando para o menu principal\n");
            cs=0;

            break;
        case 2:
            printf("Bem vindo a Combinações de roupas\n");
            printf("Escolha um tipo de look\n");
            printf("1-CASUAL\n\n");
            printf("2-SOCIAL\n\n");
            printf("3-ESPORTIVO\n\n");
            scanf("%d",&opc_2);
            switch (opc_2)
            {
            case 1:
                printf("Look Casual:\n");
                int cas = (rand()%6)+1;
                printf("Opção %d\n",cas);
                if (cas==1)
                {
                    if ((coresb[1]!=0) && (corberm[0]!=0) &&(tipot[1]!=0))
                        printf("Use uma camiseta normal preta, uma bermuda jeans e qualquer tênis casual\n");
                    else
                    {
                        printf("O look consiste em uma camiseta normal preta, uma bermuda jeans e um tênis casual\n");
                        printf("Para usar o look casual 1, está(ão) faltando alguma(as) peças(as)\n");
                    }
                }
                if (cas==2)
                {
                    if ((coresb[2]!=0) && (cortipo[0]!=0) && (tipot[1]!=0))
                        printf("Use uma camiseta normal vermelha, uma calça jeans e qualquer tênis casual\n");
                    else
                    {
                        printf("O look consiste em uma camiseta normal vermelha, uma calça jeans e qualquer tênis casual\n");
                        printf("Para usar o look casual 2, está(ão) faltando alguma(as) peça(as)\n");
                    }
                }
                if (cas==3)
                {
                    if ((coresb[3]!=0) && (corberm[1]!=0) && (tipot[1]!=0))
                        printf("Use uma camiseta normal estampada, uma bermuda tactel preta e qualquer tênis casual\n");
                    else
                    {
                        printf("O look consiste em uma camiseta normal estampada, uma bermuda tactel preta e qualquer tênis casual\n");
                        printf("Para usar o look casual 3, está(ão) faltando alguma(as) peça(as)\n");
                    }
                }
                if (cas==4)
                {
                    if ((coresb[6]!=0) && (corberm[0]!=0) && (tipot[1]!=0))
                        printf("Use uma regata vermelha, uma bermuda jenas e qualquer tênis casual\n");
                    else
                    {
                        printf("O look consiste em uma regata vermelha, uma bermuda jeans e qualquer tênis casual\n");
                        printf("Para usar o look casual 4, está(ão) faltando alguma(as) peça(as)\n");
                    }
                }
                if (cas==5)
                {
                    if ((coresb[5]!=0) && (corberm[0]!=0) && (tipot[1]!=0))
                        printf("Use uma regata preta, uma bermuda jeans e qualquer tênis casual\n");
                    else
                    {
                        printf("O look consiste em uma regata preta, uma bermuda jeans e qualquer tênis casual\n");
                        printf("Para usar o look casual 5, está(ão) faltando alguma(as) peça(as)\n");
                    }
                }
                if (cas==6)
                {
                    if ((coresb[0]!=0) && (cortipo[3]!=0) && (tipot[1]!=0))
                        printf("Use uma camiseta normal branca, uma calça moletom preta e qualquer tênis casual\n");
                    else
                    {
                        printf("O look consiste em uma camiseta normal branca, uma calça moletom preta e qualquer tênis casual\n");
                        printf("Para usar o look casual 6, está(ão) faltando alguma(as) peça(as)\n");
                    }
                }
                break;
            case 2:
                printf("Look social:\n");
                int soc = (rand()%4)+1;
                printf("Opção %d\n", soc);
                if (soc==1)
                {
                    if ((corsoc[0]!=0) && (cortipo[0]!=0) && (tipot[0]!=0))
                        printf("Use uma camisa social branca, uma calça jeans e qualquer tênis social\n");
                    else
                    {
                        printf("O look consiste em uma camisa social branca, uma calça jeans e qualquer tênis social\n");
                        printf("Para usar o look social 1, está(ão) faltando alguma(as) peça(as)\n");
                    }
                }
                if (soc==2)
                {
                    if ((corsoc[1]!=0) && (cortipo[0]!=0) && (tipot[0]!=0))
                        printf("Use uma camisa social preta, uma calça jeans e qualquer tênis social\n");
                    else
                    {
                        printf("O look consiste em uma camisa social preta, uma calça jeans e qualquer tênis social\n");
                        printf("Para usar o look social 2, está(ão) faltando alguma(as) peça(as)\n");
                    }
                }
                if (soc==3)
                {
                    if ((corsoc[0]!=0) && (cortipo[1]!=0) && (tipot[0]!=0))
                        printf("Use uma camisa social branca, uma calça jeans skinny e qualquer tênis social\n");
                    else
                    {
                        printf("O look consiste em uma camisa social branca, uma calça jeans skinny e qualquer tênis social\n");
                        printf("Para usar o look social 3, está(ão) faltando alguma(as) peça(as)\n");
                    }
                }
                if (soc==4)
                {
                    if ((corsoc[1]!=0) && (cortipo[1]!=0) && (tipot[0]!=0))
                        printf("Use uma camisa social preta, uma calça jeans skinny e qualquer tênis social\n");
                    else
                    {
                        printf("O look consiste em uma camisa social preta, uma calça jeans skinny e qualquer tênis social");
                        printf("Para usar o look social 4, está(ão) faltando alguma(as) peça(as)\n");
                    }
                }
                break;
            case 3:
                printf("Look esportivo:\n");
                int esp = (rand()%7)+1;
                printf("Opção %d\n", esp);
                if (esp==1)
                {
                    if ((coresb[5]!=0) && (corberm[1]!=0) && (tipot[2]!=0))
                        printf("Use uma regata preta, uma bermuda tactel preta e qualquer tênis esportivo\n");
                    else
                    {
                        printf("O look consiste em uma regata preta, uma bermuda tactel preta e qualquer tênis esportivo\n");
                        printf("Para usar o look esportivo 1, está(ão) faltando alguma(as) peça(as)\n");
                    }

                }
                if (esp==2)
                {
                    if ((coresb[4]!=0) && (corberm[3]!=0) && (tipot[2]!=0))
                        printf("Use uma regata branca, uma bermuda tactel estampada e qualquer tênis esportivo\n");
                    else
                    {
                        printf("O look consiste em uma regata branca, uma bermuda tactel preta e qualquer tênis esportivo\n");
                        printf("Para usar o look esportivo 2, está(ão) faltando alguma(as) peça(as)\n");
                    }

                }
                if (esp==3)
                {
                    if ((coresb[6]!=0) && (corberm[1]!=0) && (tipot[2]!=0))
                        printf("Use uma regata vermelha, uma bermuda tactel preta e qualquer tênis esportivo\n");
                    else
                    {
                        printf("O look consiste em uma regata vermelha, uma bermuda tactel preta e qualquer tênis esportivo\n");
                        printf("Para usar o look esportivo 3, está(ão) faltando alguma(as) peça(as)\n");
                    }

                }
                if (esp==4)
                {
                    if ((coresb[4]!=0) && (corberm[2]!=0) && (tipot[2]!=0))
                        printf("Use uma regata branca, uma bermuda tactel vermelha e qualquer tênis esportivo\n");
                    else
                    {
                        printf("O look consiste em uma regata branca, uma bermuda tactel vermelha e qualquer tênis esportivo\n");
                        printf("Para usar o look esportivo 4, está(ão) faltando alguma(as) peça(as)\n");
                    }

                }
                if (esp==5)
                {
                    if ((coresb[7]!=0) && (corberm[1]!=0) && (tipot[2]!=0))
                        printf("Use uma regata estampada, uma bermuda tactel preta e qualquer tênis esportivo\n");
                    else
                    {
                        printf("O look consiste em uma regata estampada, uma bermuda tactel preta e qualquer tênis esportivo\n");
                        printf("Para usar o look esportivo 5, está(ão) faltando alguma(as) peça(as)\n");
                    }
                }
                if (esp==6)
                {
                    if ((coresb[4]!=0) && (cortipo[3]!=0) && (tipot[2]!=0))
                        printf("Use uma regata branca, uma calça moletom preta e qualquer tênis esportivo\n");
                    else
                    {
                        printf("O look consiste em uma regata branca, uma calça moletom preta e qualquer tênis esportivo\n");
                        printf("Para usar o look esportivo 6, está(ão) faltando alguma(as) peça(as)\n");
                    }
                }
                if (esp==7)
                {
                    if ((coresb[5]!=0) && (cortipo[2]!=0) && (tipot[2]!=0))
                        printf("Use uma regata preta, uma calça moletom cinza e qualquer tênis esportivo\n");
                    else
                    {
                        printf("O look consiste em uma regata preta, uma calça moletom cinza e qualquer tênis esportivo\n");
                        printf("Para usar o look esportivo 7, está(ão) faltando alguma(as) peça(as)\n");
                    }
                }
                break;
            }


            break;
        case 3:
            printf("Perfil exibido no visualg\n");
            break;
        case 4:
            printf("Esses são os contatos para relatar erros no app\n");
            printf("Fernando Carvalho---fernando.filho@discente.ufj.edu.br\n");
            printf("Roger Moraes---roger.russi@discente.ufj.edu.br\n");
            printf("Thomaz Da Silva---thomaz.silva@discente.ufj.edu.br\n");
            break;
        case 5:
            printf("Encerrando o programa.\n");
            printf("Obrigado por usar nosso app\n");
            printf("Criadores: Fernando Carvalho, Róger Mores, Thomaz da Silva\n");
            printf("Pressione qualquer tecla para sair!\n");
            getch();
            break;
        default:
            printf("xxxxxxxxxxxxxxxxxxxxxxxxxxxx\n");
            printf("| Digite uma opção válida! |\n");
            printf("xxxxxxxxxxxxxxxxxxxxxxxxxxxx\n");
        }

    }
    while (opc!=5);

    return 0;
}
```
