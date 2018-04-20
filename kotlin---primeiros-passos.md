
Curso Kotlin online gratuito:

* https://www.youtube.com/watch?v=5BSSq921XNo&index=1&list=PLmcyA-BbqsvJnOZoGNHPMF1dCBq0m6Qzg

Site muito bom, com ele é possível aprender e salvar projetos em Kotlin

totalmente online, sem depender de uma IDE

* https://try.kotlinlang.org

"Olá mundo" em Kotlin:


fun main(args: Array<String>){

  println ("Olá mundo!");

}

A linha abaixo:


fun main(args: Array<String>){


} 


Equivale ao main do java:

public static void main(String[] args) {

}



O uso do  semicolon é opcional em kotlin; estou mantendo aqui apenas por uma
questão de hábito.    


Variáveis em Kotlin:

Em Kotlin, temos basicamente o mesmo tipo de variávis que utilizamos em Java 
(int, double, float, etc); porém não é necessário declarar, a menos que se queira.
Se não é declarado uma variável numérica, o Kotlin assume automaticamente 
que é um double. Também há o tipo de variável imutavel, que declaramos como var 
e a mutável, que declaramos como var.
Segue os exemplos abaixo:


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


Arrays em Kotlin:


Os arrays em Kotlin são declarados utilizando arrayOf e entre parêntesis
passamos os dados que queremos guardar. Porém diferente do Java, em
Kotlin não é necessário declarar o tipo de array que é criado; podemos 
inclusive misturar os tipos de dados que queremos guardar no mesmo array.
Segue o exemplo abaixo:



fun main(args: Array<String>){

    var nomes = arrayOf ("Zé", "Ruela", "Silva");
    var tudoJuntoReunido = arrayOf (30,"Ze",1.36);

    println (nomes[2]);
    println (tudoJuntoReunido[2]);

}

Funções em Kotlin:

Funções em Kotlin são declaradas utilizando a palavra reservada fun. Como o
exemplo abaixo mostra, é muito semelhante ao Java, porém podemos imprimir
o conteúdo de uma variável somente colocando o $ antes do nome da variável.
Em Java, teríamos que fechar as aspas e colocar o símbolo de + antes da
variável. Segue o exemplo abaixo:



fun exibirMenssagem(nome: String){

println ("Atenção, alerta de discos voadores, $nome");

//em Java ficaria:

//System.out.println ("Atenção, alerta de discos voadores," + nome);

}


fun main (args: Array<String>){

    exibirMenssagem("Zé"); // chamando a variável


}