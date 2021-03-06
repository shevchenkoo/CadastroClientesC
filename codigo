#include <stdio.h>
#include <string.h>
#include <stdlib.h>      //Bibliotecas
#include <ctype.h>

struct pedido
{ //Alocação de espaço em memória
    char namePed[200];
    char CPF[200];
    char TS[200];
    char consut1[200];
    char consut2[200];
    char custocons1[200];
    int cod;
    int sac1;
}logP[200];

struct clientes
{
	//variaveis para fazer as funçoes
    char CPF[500];
    char telefone[500];
    char TS[500];
    char nome[500];
    char endereco[500];
    char data[500];
    int vazio,cod;
    int sac1;
    struct pedido clientePed;
   
}log[500];
//Declarei as funções que vão ser usadas na clínica
int verifica_pos(void);
int verifica_cod( int cod );
int opt;
void cadastroP(int cod,int pos);
void list();
void cadastroPedido();
void consultaCod (void);
void excluirCliente (void);
void equipe();
int main(void){ //Aqui começa o main

    int i,Opcao,mec,OpcaoCliente,posicao,retorno;
    int codaux;
    do //Opçoes do Menu - 
    {
    	printf("\n\t\tClinica Med++\n\n\n");
        printf(" 1 | Cadastrar Novo Cliente\n");
        printf(" 2 | Area Cliente\n");
        printf(" 3 | Localizacao\n");
        printf(" 4 | Excluir Cliente\n");
        printf(" 5 | Agendar Consulta\n");
        printf(" 6 | SAC\n");
        printf(" 7 | WhatsApp\n");
        printf(" 8 | Sair\n");
        printf(" Selecione uma opcao por favor: ");
        scanf("%d", &Opcao);
        getchar();
        if (Opcao == 1)
        { //if else para validar a opção selecionada (se repete)
            printf("Voce selecionou a opcao 1 - Cadastrar Novo Cliente\n");
            posicao=verifica_pos();

                if ( posicao != -1 )
                {

                    printf("\nEscolha um numero de 1 a 200 para inicar seu cadastro: \n");
                    scanf("%d",&codaux);fflush(stdin);

                    retorno = verifica_cod( codaux );

                    if ( retorno == 1 )
                        cadastroP( codaux, posicao );
                    else{
                        printf("\nJa Existe um Cadastro nesse Codigo, tente novamente.\n");
                        getchar();
                        system("cls");
                        main();
                    }
                  // 
                }
                else
                    printf("\nO Numero de Cadastros Chegou ao Maximo.\n");

                break;
 
        }
        else if (Opcao == 2)
        {
            system("cls"); //Comando pra limpar a tela.
            do{
            printf("Voce selecionou a opcao 2 - Clientes\n\n");
            printf("1 - Pesquisar cliente por codigo\n");
            printf("2 - Lista de todos os clientes\n");
            printf("3 - Voltar ao menu principal\n");
            printf("Por favor, selecione uma opcao: ");
            scanf("%d", &OpcaoCliente);
            getchar();
                 if(OpcaoCliente == 1){
                    consultaCod();
                }
                else if(OpcaoCliente == 2){
                    list();
                }
                else if(OpcaoCliente == 3){
                    printf("Voce selecionou voltar ao menu principal, pressione ENTER para continuar");
                    getchar();
                    system("cls");
                }
                else
                    printf("Opcao Invalida\n\n");
    }while(OpcaoCliente =!3 || OpcaoCliente > 3 || OpcaoCliente < 0 || OpcaoCliente == 0);
        }
        else if (Opcao == 3)
        {
            printf("Voce selecionou a opcao 3 > Localizacao\n");
            printf("\n\tCole esse Link no seu navegador para achar a melhor rota ate a clinica: \n\n encurtador.com.br/esHW3\n\t");
            scanf("%d", &posicao);
		}
        
        else if (Opcao == 4)
        {
            printf("Voce selecionou a opcao 4 > Excluir Cliente\n");
            excluirCliente();
        }
        else if (Opcao == 5)
        {
            printf("Voce selecionou a opcao 5 > Agendar Consulta\n");
            cadastroPedido();
        }
        else if (Opcao == 6)
        {
        	printf("Voce selecionou a opcao 6 > SAC\n");
        	printf("\n\tDigite sua critica ou elogio ah nossa equipe: \n\n");
            scanf("%d", &mec);
            printf("\nMuito obrigado pela sua opniao.\n");
            
		//	  system("cls");
 			   
        
        }
        else if (Opcao == 7)
        {
            printf("Voce selecionou a opcao 7 > Whatsapp\n");
            printf("\n\n\nNosso telefone eh o 4002-8922\n\n\n\n");
        
        }
        else if (Opcao == 8)
        {
            printf("Voce selecionou a opcao 8 - Sair\n");
        }
        else{
            printf("Opcao invalida, favor pressione enter para voltar ao menu principal");
            getchar();
            system("cls");
        }
        }    while (Opcao != 8 || Opcao < 8);

} // Fim do main
void list(){ // Lista os usuarios cadastrados.
    int i,j;  
    for(i=0;i<200;i++){
        if(log[i].cod!=NULL){
            printf("\nCodigo: %d \nNome: %s\nCPF: %s\nEndereco: %s\nTelefone: %s\n\n", log[i].cod,log[i].nome,log[i].CPF,log[i].endereco,log[i].telefone);
    }
}
    printf("Pressione enter para volta ao menu principal");
    getchar();
    system("cls");

} //Fim do List
void cadastroP(int cod, int pos){ //Cadastro das pessoas
    int i;
    do{
    pos = verifica_pos();
    log[pos].cod = cod;
        printf("\nDigite seu nome: ");
        gets(log[pos].nome);
        printf("\nDigite seu CPF: ");
        gets(log[pos].CPF);
        printf("\nDigite seu Endereco: ");
        gets(log[pos].endereco);
        printf("\nDigite seu Tipo Sanguineo: ");
        gets(log[pos].TS);
        printf("\nDigite seu Telefone: ");
        gets(log[pos].telefone);
        log[pos].vazio = 1;
        //printf("\nDigite enter para efetuar novo cadastro ou qualquer outra tecla para volar ao menu principal");
        //scanf("%d", &opt);
        opt ==1;
        getchar();  
    }while(opt==1);
    system("cls");
    main();

} // Final do castro de pessoas 
int verifica_pos( void ) //verificador da posicão = código do cadastro
{
    int cont = 0;

    while ( cont <= 200 )
    {

        if ( log[cont].vazio == 0 )
            return(cont);

        cont++;

    }

    return(-1);

} // Final do verificador, while if - log, incremento
int verifica_cod( int cod ) //Verificador do código (repetição)
{
    int cont = 0;

    while ( cont <= 200 )
    {
        if ( log[cont].cod == cod )
            return(0);

        cont++;
    }

    return(1);

} 
void cadastroPedido(){ //Cadastro dos pedidos
    system("cls");    
    int i;
    int Option;
    int OpcaoPedido;
    char nomeCad[200];
    printf("\nDigite seu nome como esta no cadastro: ");
    gets(nomeCad);
    for(i=0;i<200;i++){
            if(strcmp(log[i].nome, nomeCad)==0){
                do{
                printf("\nEscolha a Consulta que deseja: ");  // Marcação de Consultas, Provavel mudança de código.
                printf("\n1- Dermatologia");
                printf("\n2- Cardiologia");
                printf("\n3- Dentista\n:");
                scanf("%d", &OpcaoPedido);
                if(OpcaoPedido == 1){
                    strcpy(log[i].clientePed.namePed, "Dematologia");
                    printf("\nVoce escolheu %s, seu agendamento foi adicionado ao seu cadastro.",log[i].clientePed.namePed);
                    printf("\nPressione 1 para continuar pedindo ou 2 para volar ao menu principal: ");
                    scanf("%d", &Option);
                    i++;
                }
                else if(OpcaoPedido == 2){
                    strcpy(log[i].clientePed.namePed, "Cardiologia");
                    printf("\nVoce escolheu %s, seu agendamento foi adicionado ao seu cadastro.", log[i].clientePed.namePed);
                    printf("\nPressione 1 para continuar pedindo ou 2 para volar ao menu principal: ");
                    scanf("%d", &Option);
                    i++;
                   }
                   else if(OpcaoPedido == 3){
                    strcpy(log[i].clientePed.namePed, "Dentista");
                    printf("\nVoce escolheu %s, seu agendamento foi adicionado ao seu cadastro.", log[i].clientePed.namePed);
                    printf("\nPressione 1 para continuar pedindo ou 2 para volar ao menu principal: ");
                    scanf("%d", &Option);
                    i++;
                }
    }while(Option == 1);
    system("cls");

   
}
}
} //
void consultaCod (void) // Mecanismo de busca, pesquisar o cliente pelo código
{
    int cont = 0, cod;

    printf("\nEntre com o codigo\n");
    scanf("%d",&cod);
    fflush(stdin);
    system("cls");

    while ( cont <= 200 )
    {

        if (log[cont].cod==cod)
        {
            if (log[cont].vazio==1)
            {
               
                printf("\nCodigo: %d \nNome: %s\nCPF: %s\nEndereco: %s\nTelefone: %s\n\n", log[cont].cod,log[cont].nome,log[cont].CPF,log[cont].endereco,log[cont].telefone);
               

                system ("pause");

                system("cls");

                break;

            }
        }

        cont++;

        if ( cont > 200 ){
            printf("\nCodigo nao encontrado, pressione enter para volar ao menu principal\n");
            getchar();
            system("cls");
        }

    }
} // Função consultar 
void excluirCliente(void)  // Exclusão do cliente
{
    int cod, cont = 0;
    char resp;
    printf("\nDigite o codigo do registro que deseja excluir: \n");
    scanf("%d", &cod );

    while ( cont <= 200 )
    {

        if ( log[cont].cod == cod )
        {

            if (log[cont].vazio == 1 )
            {
                printf("\nCodigo: %d \nNome: %s\nCPF: %s\nEndereco: %s\nTelefone: %s\n\n", log[cont].cod,log[cont].nome,log[cont].CPF,log[cont].endereco,log[cont].telefone);
                getchar();
                printf("\nDeseja realmente exlucir? s/n: ");
                scanf("%s",&resp);

                if ( ( resp == 'S' ) || ( resp == 's' ) )
                {
                    log[cont].vazio=0;
                    log[cont].cod = NULL;
                    printf("\nO Registro foi excluido.\n");
                    break;
                }
                else
                {
                    if ( ( resp == 'N' ) || ( resp == 'n' ) )
                    {
                        printf("Algo deu errado, o registro continua no sistema.\n");
                        break;
                    }
                }

            }

        }

        cont++;

        if ( cont > 200 )
            printf("\nCodigo nao encontrado\n");

    }

    system("pause");
    system("cls");
}
