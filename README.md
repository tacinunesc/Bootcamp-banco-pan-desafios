# Bootcamp-banco-pan-desafios

## Desafio: Fábrica de Carros

```bash
- Para ler e escrever dados em Java, aqui na DIO padronizamos da seguinte forma: 
- new Scanner(System.in): cria um leitor de Entradas, com métodos úteis com prefixo "next";
- System.out.println:.imprime um texto de Saída (Output) e pulando uma linha.  

import java.util.*;

public class Main {
    public static void main(String[] args) {
  Scanner scan = new Scanner(System.in);
      int custoFabrica = scan.nextInt();
	    int porcentagemDistribuidor = scan.nextInt();
	    int PercentualImpostos = scan.nextInt();

            int custoConsumidor;
     
            int Distribuidor;
            int ValorImpostos;
 
        // TODO: Implemente uma condição que calcule a porcentagem do distribuidor e dos impostos:
 
        Distribuidor = (custoFabrica * porcentagemDistribuidor) / 100;
        ValorImpostos = (custoFabrica * PercentualImpostos) / 100;
        int total = Distribuidor + ValorImpostos + custoFabrica;
 
        System.out.println(total);
    }
}
 ```
 
 ## Desafio: Imprimindo Positivos e Média
 
 ```bash
 // Para ler e escrever dados em Java, aqui na DIO padronizamos da seguinte forma: 
// - new Scanner(System.in): cria um leitor de Entradas, com métodos úteis com prefixo "next";
// - System.out.println:.imprime um texto de Saída (Output) e pulando uma linha.  

import java.io.IOException;
import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;

public class DIO {
	
  public static void main(String[] args) throws IOException {
     Scanner leitor = new Scanner(System.in);
     int cont = 0;
     double media = 0;

     List<Float> listaDeValores = new ArrayList<>();

     //TODO: Implemente as condições adequadas para obter a quantidade 
    //de valores positivos e a média dos valores positivos:
    
    for (int i = 0; i < 6; i++){
        listaDeValores.add(leitor.nextFloat());
    }

    for (float valor: listaDeValores){
        if(valor > 0){
            cont ++;
            media += valor;
        }
    }

        media = media/cont;
        System.out.println(cont + " valores positivos");
        System.out.println(String.format("%.1f", media));
    }
}
```

## Desafio: Soma de H com N Termos

```bash
// Para ler e escrever dados em Java, aqui na DIO padronizamos da seguinte forma: 
// - new Scanner(System.in): cria um leitor de Entradas, com métodos úteis com prefixo "next";
// - System.out.println:.imprime um texto de Saída (Output) e pulando uma linha.  

import java.util.Scanner;

import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
         double h = 0;
     Scanner sc = new Scanner(System.in);
     double n = sc.nextDouble();


     for (double i = 1; i <= n; i++) {
     //TODO: Calcule o valor de H de forma que resulte na soma dos termos:
        h +=  1/i;  
      }
     //TODO: Imprima a soma dos termos, considerando um resultado com duas casas decimais:
     System.out.println(String.format("%.0f", h));   
    }
}
 
 ```
 
 ## Desafio: Dragão
 
 ```bash
 
 // Para ler e escrever dados em Java, aqui na DIO padronizamos da seguinte forma: 
// - new Scanner(System.in): cria um leitor de Entradas, com métodos úteis com prefixo "next";
// - System.out.println:.imprime um texto de Saída (Output) e pulando uma linha.  

import java.util.*;
import java.util.Scanner;

public class DesafioDragao{ 
    
   public static void main(String[] args){
            int casos, poderDeLuta;
    
            Scanner ler = new Scanner(System.in);
    
            casos = ler.nextInt();
    
            for(int i = 0; i < casos; i++){
                poderDeLuta = ler.nextInt();

                //TODO: Implemente a condição adequada para a impressão dos textos conforme o solicitado no desafio:
    
                if(poderDeLuta <= 8000){
                    System.out.println("Inseto!");
                } else {
                    System.out.println("Mais de 8000!");
                }
            }
    }
}
 
 ```
 
 ## Desafio: Fibonacci Fácil
 
 ```bash
 
 // Para ler e escrever dados em Java, aqui na DIO padronizamos da seguinte forma: 
// - new Scanner(System.in): cria um leitor de Entradas, com métodos úteis com prefixo "next";
// - System.out.println:.imprime um texto de Saída (Output) e pulando uma linha.  

import java.io.IOException;
import java.util.Scanner;

import java.io.IOException;
import java.util.Scanner;

public class DesafioFibonacciFacil {

    public static void main(String[] args) throws IOException {
        Scanner leitor = new Scanner(System.in);
        int N = leitor.nextInt();
        int proximo, anterior = 0, atual = 1;
        for (int i = 1; i <= N; i++) {
          if (i == N) System.out.println(anterior);
       
     //TODO: Implemente a condição ideal para que possamos obter os valores solicitados:
        	else System.out.print(anterior + " ");
        	proximo = anterior + atual;
        	anterior = atual; 
        	atual =  proximo; 
        }
    }
	
}
 
```
