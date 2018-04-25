
Curso Kotlin online gratuito:

* https://www.youtube.com/watch?v=5BSSq921XNo&index=1&list=PLmcyA-BbqsvJnOZoGNHPMF1dCBq0m6Qzg

Site muito bom, com ele é possível aprender e salvar projetos em Kotlin totalmente online, sem depender de uma IDE:

* https://try.kotlinlang.org

"Olá mundo" em Kotlin:

```
fun main(args: Array<String>){

  println ("Olá mundo!");

}
```

A linha abaixo:

```
fun main(args: Array<String>){

  código

} 
```

Equivale ao main do java:

```
public static void main(String[] args) {

  código


}
```


O uso do  semicolon é opcional em kotlin; estou mantendo aqui apenas por uma
questão de hábito.    


Variáveis em Kotlin:

Em Kotlin, temos basicamente o mesmo tipo de variávis que utilizamos em Java 
(int, double, float, etc); porém não é necessário declarar, a menos que se queira.
Se não é declarado uma variável numérica, o Kotlin assume automaticamente 
que é um double. Também há o tipo de variável imutavel, que declaramos como var 
e a mutável, que declaramos como var.
Segue os exemplos abaixo:

```
fun main(args: Array<String>){

    var usuario = "Zé Ruela"; //variavel mutavel
    usuario = "Ruela Zé";
    val PI = 3.14 // variavel imutavel


    println (usuario);  
    println (PI);

    var salario = 100;
    var bonus  = 30 ;

    println ( salario + bonus);

    var total = salario + bonus;

    println ("O salário é $total");

    var numero = 3.54545454545;
    var numero1 = "qualquer coisa";

    var numero2: Double = 34.54;
    var numero3: String = "ET telefone minha casa";

    println(numero);
    println(numero1);
    println(numero2);
    println(numero3);

} 
```


Arrays em Kotlin:


Os arrays em Kotlin são declarados utilizando arrayOf e entre parêntesis
passamos os dados que queremos guardar. Porém diferente do Java, em
Kotlin não é necessário declarar o tipo de array que é criado; podemos 
inclusive misturar os tipos de dados que queremos guardar no mesmo array.
Segue o exemplo abaixo:


```
fun main(args: Array<String>){

    var nomes = arrayOf ("Zé", "Ruela", "Silva");
    var tudoJuntoReunido = arrayOf (30,"Ze",1.36);

    println (nomes[2]);
    println (tudoJuntoReunido[2]);

}
```


Funções em Kotlin:

Funções em Kotlin são declaradas utilizando a palavra reservada fun. Como o
exemplo abaixo mostra, é muito semelhante ao Java, porém podemos imprimir
o conteúdo de uma variável somente colocando o $ antes do nome da variável.
Em Java, teríamos que fechar as aspas e colocar o símbolo de + antes da
variável. Segue o exemplo abaixo:


```
fun exibirMenssagem(nome: String){

     println ("Atenção, alerta de discos voadores, $nome");

}


fun main (args: Array<String>){

     exibirMenssagem("Zé"); // chamando a variável

}
```

Em Java :

```
public static String exibirMenssagem (String nome){

     System.out.println("Atenção, alerta de discos voadores, " + nome);

}

public static void main(String[] args){


     exibirMenssagem("Zé"); // chamando a variável

}
```
Classes de instância em Kotlin

Em Kotlin, podemos criar classes de instância que servirão para referenciar objetos
de forma mais rápida (e mais clara) do que em Java. Vamos criar uma classe chamada "Casa",
onde terão como atributos apenas a variável String "cor" e a variável inteira vagasGaragem.
 Faremos também os métodos "abrirJanela", "abrirPorta ", "abrirCasa"(que abre a porta e a janela)
e por último "detalhesCasa", que retorna a cor a o número de vagas na garagem.

Em Kotlin:

```
class Casa {
    
    
   // Propiedades 
   var cor: String
   var vagasGaragem: Int
    
    
    constructor (cor: String, vagasGaragem: Int ){
        
        this.cor = cor;
        this.vagasGaragem = vagasGaragem;
             
    }
 
 
    init { 
        
       this.cor = cor;
       this.vagasGaragem = vagasGaragem;  
        
    }
      
    //Métodos
    
   fun detalhesCasa(){
       
   	   println("A casa tem a cor $cor, e $vagasGaragem vaga(s) ");	   
        
   }
    
   fun abrirJanela(){
       
       println ("Janela Aberta");
       
   }    
       
   fun abrirPorta(){
       
       println ("Porta Aberta");    
       
   } 
       
    fun abrirCasa(){
       
       this.abrirJanela();
       this.abrirPorta();   
       
   	}    
    
}
```
Como podemos ver, essa sintaxe é muito parecida com o Java. Vejamos um objeto casa chamando alguns métodos desta classe:

```
fun main(args: Array<String>){
    
    
    val casa = Casa("Vermelha", 20);
 
    casa.abrirCasa();
    casa.detalhesCasa();
      
}
```
Existe uma maneira mais simples e rápida de inicializar um construtor em Kotlin. Basta passar os parâmetros direto no nome da classe, como se fosse em Java uma classe de métodos em vez de instância. Vejamos a mesma classe inicializada de uma forma mais direta:

```
class Casa ( var cor: String, var vagasGaragem: Int ){
          
   //Métodos
   
   fun detalhesCasa(){
       
       println("A casa tem a cor $cor, e $vagasGaragem vaga(s) ");	   
        
   }
    
   fun abrirJanela(){
       
       println ("Janela Aberta");
       
   }    
       
   fun abrirPorta(){
       
       println ("Porta Aberta");    
       
   } 
       
    fun abrirCasa(){
       
       this.abrirJanela();
       this.abrirPorta();   
       
   	}    
    
}
```
A inicialização continua a mesma:

```
fun main(args: Array<String>){
    
    val casa = Casa("Vermelha", 20);
 
    casa.abrirCasa();
    casa.detalhesCasa();
       
}
```
Como podemos ver, desta forma é muito mais rápido codar em Kotlin. Mas nada impede de usarmos os dois tipos de construtores
juntos; desta forma teremos um construtor chamado primario para o tipo acima e chamado secundário para o do tipo semelhante ao java:

```

//construtor primario
class Casa ( var cor: String, var vagasGaragem: Int ){
    
  /* 
   // Propiedades 
   var cor: String
   var vagasGaragem: Int


    
    //construtor secundario
    constructor (cor: String, vagasGaragem: Int ){
        
        this.cor = cor;
        this.vagasGaragem = vagasGaragem;
        
    }
  
    init{ 
        
       this.cor = cor;
       this.vagasGaragem = vagasGaragem;
               
    }
    
   */


      
    //Métodos
    //
   fun detalhesCasa(){
       
   	   println("A casa tem a cor $cor, e $vagasGaragem vaga(s) ");	   
        
   }
    
   fun abrirJanela(){
       
       println ("Janela Aberta");
       
   }    
       
   fun abrirPorta(){
       
       println ("Porta Aberta");    
       
   } 
       
    fun abrirCasa(){
       
       this.abrirJanela();
       this.abrirPorta();   
       
   	}    
    
}
```
Aqui o construtor secundário está comentado entre /* e */ , pois tratam-se dos mesmos parãmetros de inicialização





