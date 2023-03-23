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
 ## Desafio: Animal
 
 ```bash
 // Para ler e escrever dados em Java, aqui na DIO padronizamos da seguinte forma: 
// - new Scanner(System.in): cria um leitor de Entradas, com métodos úteis com prefixo "next";
// - System.out.println:.imprime um texto de Saída (Output) e pulando uma linha.  

import java.io.IOException;
import java.util.Scanner;

public class Main {

	public static void main(String[] args)  throws IOException {
		Scanner sc = new Scanner(System.in);
		
		String AN1,AN2,AN3;
		
		AN1 = sc.nextLine();
		AN2 = sc.nextLine();
		AN3 = sc.nextLine();
		
		if (AN1.equalsIgnoreCase("vertebrado")) {
			if (AN2.equalsIgnoreCase("ave")) {
				if (AN3.equalsIgnoreCase("carnivoro")) {
					System.out.println("aguia");
				} else {
					System.out.println("pomba");
				}
			} else {
				if (AN3.equalsIgnoreCase("onivoro")) {
					System.out.println("homem");
				} else {
					System.out.println("vaca");
				}
			}
		} else {
			if (AN2.equalsIgnoreCase("inseto")) {
				if (AN3.equalsIgnoreCase("hematofago")) {
					System.out.println("pulga");
				} else {
					System.out.println("lagarta");
				}
			} else {
				if (AN3.equalsIgnoreCase("hematofago")) {
					System.out.println("sanguessuga");
				} else {
					System.out.println("minhoca");
				}			
			}
		}
	}
	

	}

 ```
  ## Desafio: Quitanda do Seu Zé
 
 ```bash
// Para ler e escrever dados em Java, aqui na DIO padronizamos da seguinte forma: 
// - new Scanner(System.in): cria um leitor de Entradas, com métodos úteis com prefixo "next";
// - System.out.println:.imprime um texto de Saída (Output) e pulando uma linha.  

import java.util.*;

public class DIO {
    public static void main(String[] args) {
    
        Scanner input = new Scanner(System.in);
       int morangos = input.nextInt();
       int macas = input.nextInt();
       
       
        
  double valorMorangos = (morangos > 5 ? (morangos * 2.2) : (morangos * 2.5));
        double valorMacas = (macas > 5 ? (macas * 1.5) : (macas * 1.8));

        double total = (valorMorangos + valorMacas);

        if ((morangos + macas) > 8 || total > 25) {
            total = (total - (total * 0.1));
        }

        System.out.println(total);
    }
}
```

## Desafio: Triângulo
 
 ```bash
 // Para ler e escrever dados em Java, aqui na DIO padronizamos da seguinte forma: 
// - new Scanner(System.in): cria um leitor de Entradas, com métodos úteis com prefixo "next";
// - System.out.println:.imprime um texto de Saída (Output) e pulando uma linha.  


import java.io.IOException;
import java.util.Scanner;

public class Teste{
	
	public static void main(String[] args) throws IOException {
		Scanner leitor = new Scanner(System.in);
		double A = leitor.nextDouble();
		double B = leitor.nextDouble();
		double C = leitor.nextDouble();
		double maior;
		double soma;
		boolean triangulo;
		
		if ((A < (B + C)) && (B < (A + C)) && (C < (A + B))) {
            System.out.println("Perimetro = " + String.format("%.1f", (A + B + C)));
        } else {
            System.out.println("Area = " + String.format("%.1f", (((A + B) * C) / 2)));
        }
    }
}
```

## Desafio: Conta Espaços e Vogais
 
 ```bash
// Para ler e escrever dados em Java, aqui na DIO padronizamos da seguinte forma: 
// - new Scanner(System.in): cria um leitor de Entradas, com métodos úteis com prefixo "next";
// - System.out.println:.imprime um texto de Saída (Output) e pulando uma linha.  

import java.util.Arrays;
import java.util.Scanner;

/**
 *
 * @author Jhansen Barreto
 */
public class Desafio4 {

    /**
     * DESAFIO - Conta Espaços e Vogais:
     *
     * Jorginho é professor do primário de uma determinada escola. Ele tem
     * 100000 alunos e precisa criar um programa que verifica quantos espaços em
     * branco e quantas vogais existem em uma determinada string de entrada que
     * os alunos entregaram na avaliação final. Ajude-o a realizar essa tarefa
     * antes que o tempo para entrega-la no fim do semestre acabe!
     *
     * ENTRADA:
     *
     * A entrada será uma frase no formato de string.
     *
     * SAÍDA:
     *
     * A saída deverá retornar quantos espaços em branco e quantas vogais
     * existem na determinada string, conforme exemplo abaixo:
     *
     * “Amo a DIO” -> Espacos em branco: 2 Vogais: 5
     * “Esse desafio foi facil” -> Espacos em branco: 3 Vogais: 10
     *
     * @param args
     */
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String str = sc.nextLine();

        String[] strSplit = str.split(" ");
        Character[] arrVogais = {'a', 'e', 'i', 'o', 'u'};
        var vogais = Arrays.asList(arrVogais);

        int espacosEmBranco = strSplit.length - 1, quantVogais = 0;

        for (String item : strSplit) {
            var letras = item.toCharArray();
            for (char x : letras) {
                if (vogais.contains(Character.toLowerCase(x))) {
                    quantVogais++;
                }
            }
        }

        System.out.println("Espacos em branco: " + espacosEmBranco + " Vogais: " + quantVogais);
    }
}
```

## Desafio: Taxa de Imposto de Renda
 
 ```bash
 // Para ler e escrever dados em Java, aqui na DIO padronizamos da seguinte forma: 
// - new Scanner(System.in): cria um leitor de Entradas, com métodos úteis com prefixo "next";
// - System.out.println:.imprime um texto de Saída (Output) e pulando uma linha.  

import java.io.IOException;
import java.util.Scanner;

public class Desafio5 {

    /**
     * DESAFIO - Taxa de Imposto de Renda:
     *
     * Há um país denominado Lolipad, todos os habitantes ficam felizes em pagar
     * seus impostos, pois sabem que nele não existem políticos corruptos e os
     * recursos arrecadados são utilizados em benefício da população, sem
     * qualquer desvio. A moeda deste país é o Loli, cujo símbolo é o R$.
     *
     * Você terá o desafio de ler um valor com duas casas decimais, equivalente
     * ao salário de uma pessoa de Loli. Em seguida, calcule e mostre o valor
     * que esta pessoa deve pagar de Imposto de Renda, segundo a tabela abaixo.
     *
     * https://resources.urionlinejudge.com.br/gallery/images/problems/UOJ_1051_pt.png
     *
     * Lembre que, se o salário for R$ 3002.00, a taxa que incide é de 8% apenas
     * sobre R$ 1000.00, pois a faixa de salário que fica de R$ 0.00 até R$
     * 2000.00 é isenta de Imposto de Renda. No exemplo fornecido (abaixo), a
     * taxa é de 8% sobre R$ 1000.00 + 18% sobre R$ 2.00, o que resulta em R$
     * 80.36 no total. O valor deve ser impresso com duas casas decimais.
     *
     * ENTRADA:
     *
     * A entrada contém apenas um valor de ponto flutuante, com duas casas
     * decimais.
     *
     * SAÍDA:
     *
     * Imprima o texto "R$" seguido de um espaço e do valor total devido de
     * Imposto de Renda, com duas casas após o ponto. Se o valor de entrada for
     * menor ou igual a 2000, deverá ser impressa a mensagem "Isento".
     *
     * @param args
     */
    public static void main(String[] args) {
        Scanner leitor = new Scanner(System.in);
        double renda = leitor.nextDouble();

        double imposto = 0.0;
        double diferenca;

        if (renda > 4500) {
            imposto = ((1000 * 0.08) + (1500 * 0.18));
            diferenca = (renda - 4500);
            imposto += (diferenca * 0.28);

        } else if (renda > 3000) {
            imposto = (1000 * 0.08);
            diferenca = (renda - 3000);
            imposto += (diferenca * 0.18);

        } else if (renda > 2000) {
            diferenca = (renda - 2000);
            imposto = (diferenca * 0.08);
        }

        System.out.println((imposto == 0.0 ? "Isento" : "R$ " + String.format("%.2f", imposto)));
    }
}
```

