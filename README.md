#include <stdio.h>
#include <stdlib.h>

 /**********
 Aluno: Henrique Claranhan
 Aluno: Aaron Levi
 Turma: 228(A)
 Data:20/09
 */

int contaLetras(char vetor[]){

int z, aux;
char tam_palavra;

for(z=0;z<vetor[z];z++) 
 aux=z;
 tam_palavra=aux;
	
	return tam_palavra;
}

 int main(void){

 char dica[20];
 char tamanho_palavra;
 char palavra[20];
 char letra[20];
 char traco[20]="-";
 int vida=6;
 int c;
 int y, auxiliar;
 int acertos=0;


 printf("\n\nxxxxxxxxxxxxxxxxxxxxxxxx JOGO DA FORCA xxxxxxxxxxxxxxxxxxxxxxxx\n");

 printf("\n\n|Digite a palavra:\n");
 scanf("%[^\n]s", palavra);
 system("cls");
 printf("\n\n|Escreva a dica:\n");
 scanf("%s", dica);
 system("cls");



 for(y=0;y<palavra[y];y++)
 auxiliar=contaLetras(&palavra[y]);
 traco[y]='-';

 while(vida>0)
 {
 c=0;

 printf("\n>A palavra tem %i letras \n", auxiliar);
 printf(">Dica: %s \n", dica);

 if (vida==6){
 printf("\n O\n/|\\ \n/ \\\n");}

 printf("\n\n %s \n",traco);

 printf("\nDigite uma letra: ");

 scanf("%s", letra); 
 system("cls");


 for(y=0;y<palavra[y];y++)
 {

 //if (letra[y]==palavra[y]){acertos=tamanho_palavra;}

 if (y>1){
 if (letra[y]==palavra[y]){
 acertos=tamanho_palavra;}
 }

 if(letra[0]==palavra[y])
 {
 traco[y]=palavra[y];
 acertos++;
 c++;}}

 if(c==0) {vida--;

 if (vida==5){
 printf("\n O\n/|\\ \n/\n");
 }

 if (vida==4){
 printf("\n O\n/|\\ \n");
 }

 if (vida==3){
 printf("\n O\n/|\n");
 }

 if (vida==2){
 printf("\n O\n |\n");
 }

 if (vida==1){
 printf("\n O\n");
 }

 if(vida==0) {
 printf("\n\nSuas chances acabaram!");
 printf("\nApalavra era: %s",palavra);
 break;}

 else
 printf("\nVocê errou!\nA palavra não tem a letra (%s)\n", letra);}

 else{
 if(acertos==tamanho_palavra) {
 printf("\n\nPARABÉNS! VOCE GANHOU!!!"); 
 printf("\n A palavra é: %s",palavra);
 break;}

 else {
 printf("\nVoce acertou uma letra!\n");
 }}}

 return 0; }
