# Exercicio-7-em-Java

# Exercicio Replicado do livro Tutorial de Programação em Java e Orientação em Objetos 


//Existem variações sobre o tema que veremos mais tarde: sobrecarga de construtor, “copy
//constructor”, construtor de corpo vazio. O exemplo a seguir é simples, semelhante aos anteriores,
//preste atenção no método com o mesmo nome que a classe, este é o construtor:

//Classe ponto
public class Ponto {
public float x,y;
public Ponto(float ax,float ay) // sempre omita o valor de retorno!
//garante o estado do objeto
{
 this.x = ax; this.y = ay;
}
public void move(float dx,float dy)
{
 this.x += dx; this.y += dy;
}
public void mostra()
{
 System.out.println("(" + this.x + "," + this.y + ")");
}
}
//Classe principal, Arquivo Principal.java
public class Principal {
 public static void main(String args[]) {
 Ponto ap;
 ap = new Ponto((float)0.0, (float)0.0);
 ap.mostra();
 ap.move(1,1);
 ap.mostra();
 ap.x = 100;
 ap.mostra();
 }
}

//COMENTARIOS: 
Note que com a definição do construtor, você é obrigado a passar os argumentos deste no
momento da alocação do objeto. Se você precisa ter a opção de não passar esses valores ou passar
outros, as possíveis soluções serão dadas em “POLIMORFISMO, CLASSES ABSTRATAS”.
(float)0.0 indica que é para ser feita a conversão de 1.0 para ponto flutuante. 1.0 sozinho é
considerado double. (int)1.0 é igual a 1. (int) 2.3 é igual a dois. Esta operação indicada por
(nometipo)tipo_a_ser_convertido é também chamada de “type cast”.
A ocorrência de rotinas de criação de objetos em diversos locais de um programa é muito
comum. Objetos podem ser criados dentro de estruturas condicionais, armazenados em arquivos,
passados como parâmetros, inseridos em estruturas dinâmicas dentro de outros objetos, etc.
