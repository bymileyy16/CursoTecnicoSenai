# CursoTecnicoSenai
### Nessa Etapa, fizemos algumas atividades envolvendo codigos de progamação na linguagem C# ;)

## **Vogais**
using System;
					
public class Program
{
	public static void Main()
	{
		Console.Write("Digite uma letra: ");
		string input = Console.ReadLine();
		int i;
		
		if(int.TryParse(input, out i) || input.Length > 1){
			Console.Write("Digite uma letra!");
		}else{
			char lett = input[0];
			
			if(lett == 'a' || lett == 'e' || lett == 'i' || lett == 'o' || lett == 'u'){
				Console.Write($"A letra {lett} é uma vogal!");
			}else{
				Console.Write($"A letra {lett} é uma consoante!");
			}
		}
	}
}

## **Valor de Imposto**
using System;
					
public class Program
{
	public static void Main()
	{
		Console.Write("informar o imposto de renda:" );
		if (decimal.TryParse(Console.ReadLine(), out decimal salarioBruto))
		{
			decimal imposto;
			if ( salarioBruto <= 3000)
			{
				imposto = salarioBruto * 0.10m;
				Console.WriteLine("O valor do imposto de 10% a ser pago é: " + imposto);
			}
			else
			{
				if ( salarioBruto <= 6000)
				{
					imposto = salarioBruto * 0.15m;
					Console.WriteLine("O valor do imposto de 15% a ser pago é: " + imposto);
				}
				else
				{
					imposto = salarioBruto * 0.20m;
					Console.WriteLine("O valor do imposto de 20% a ser pago é: " + imposto);
				}
			}
		}
		else 
		{
			Console.WriteLine("ERRO: Você nao informou um valor valido");
		}
## **Tabuada**
using System;
					
public class Program
{
	public static void Main()
	{
		Console.Write("Informe um número: ");
		if (int.TryParse(Console.ReadLine(), out int n))
		{
			Console.Write("Escolha a operação a ser utilizada (+  -  *  /): ");
				string operador = Console.ReadLine();
				for (int i = 1; i <=10; i++)
			{
				switch(operador)
				{
					case"+":
						double resultado = n + i;
						Console.WriteLine(n + "+" + i + "=" + resultado);
						break;
					case"-":
						resultado = n - i;
						Console.WriteLine(n + "-" + i + "=" + resultado);
						break;
					case"*":
						resultado = n * i;
						Console.WriteLine(n + "*" + i + "=" + resultado);
						break;
					case"/":
						resultado = n / i;
						Console.WriteLine(n + "/" + i + "=" + resultado);
						break;
					default:
						Console.WriteLine("Operação Inválida");
						break;
				}
			}
		}
		else
		{
			Console.WriteLine("Número Inválido");
		}
	}
}

## **Sorteio de Numeros**
using System;

public class HelloWorld
{
    public static void Main(string[] args)
    {
        int j = 0;
        for(j = 0; j < 6; j++)
        {
            Random na = new Random();
            int vi = na.Next(10, 99);
            Console.WriteLine("Os numero sorteados são: "+ vi);
        }
    }
}

## **Separador de Frases**
using System;

public class Program
{
	public static void Main(string[] args)
	{
		Console.Write("Insira a palavra ou frase que deseja: ");
		string palavra = Console.ReadLine();
		{
			foreach (char letra in palavra)
			{
				Console.WriteLine(letra);
			}
		}
	}
}

## **Bolão**
using System;

public class HelloWorld
{
	public static void Main(string[] args)
	{
		bool repetir = false;
		Console.Write("Quantos jogos vc deseja fazer? ");
		int jogadas = int.Parse(Console.ReadLine());
		do
		{
			Console.Write("Quantas dezenas vc deseja fazer? ");
			int dezenas = int.Parse(Console.ReadLine());
		    if (dezenas <= 15)
		    {
			if (dezenas >= 6)
			{
				repetir = false;
				for (int n = 1; n <= jogadas; n++)
				{
					Console.WriteLine($"\nJogo {n}:");
					for (int contador = 1; contador <= dezenas; contador++)
					{
						Random na = new Random();
						int valores = na.Next(01, 60);
						if (contador == dezenas)
						{
							Console.Write(valores.ToString("00"));
						}
						else
						{
							Console.Write(valores.ToString("00")+"-");
						}
					}
				}
			}
			else
			{
				repetir = true;
				Console.WriteLine("Ops! minimo de dezenas e 6! digite novamente o numero de dezenas ;) ");
			}
		    }
		    else
		    {
		    		repetir = true;
				Console.WriteLine("Ops! o maximo e 15 dezenas digite novamente o numero de dezenas ;) ");
		    }
		}
		while (repetir == true);
	}
}

## **Nota dos alunos**
using System;
					
public class program
{
	public static void Main()
	{

		Console.WriteLine("informar nota 1 ");
		double nota1 = Convert.ToDouble(Console.ReadLine());

		Console.WriteLine("informar nota 2" );
		double nota2 = Convert.ToDouble(Console.ReadLine());
		
		Console.WriteLine("Informar nota 3 ");
		double nota3 = Convert.ToDouble(Console.ReadLine());

		Console.WriteLine("informar nota 4 ");
		double nota4 = Convert.ToDouble(Console.ReadLine());
		
		double media =( nota1 + nota2 + nota3 + nota4) / 4;
		Console.WriteLine("Media = " + media);

		// Verifica se o número e par ou impar
		if (nota1 % 2 == 0)
		{
			Console.WriteLine ( $"o numero {nota1} é par." );
		}
			Console.WriteLine ( $"O numero {nota1} é impar.");
		}
		
	}

## **Idade dos alunos**
using System;
					
public class Program
{
	public static void Main()
	{
		Console.WriteLine("informe a idade do usuário");
		
		if (int.TryParse(Console.ReadLine(), out int idade))
		{
			if(idade > 0 && idade <= 12 )
			{
				Console.WriteLine("criança");
			}
				if(idade > 13 && idade  <=17 )
			{
				Console.WriteLine("adolescente");
			}
				if(idade > 18 && idade  <=64 )
			{
				Console.WriteLine("adulto");
			}
				if(idade > 65 )
			{
				Console.WriteLine("idoso");
			}
		}
		else
		{
			Console.WriteLine("ERRO ");
		}
			
	}
}

## **Roleta**
using System;

public class HelloWorld
{
    public static void Main(string[] args)
    {
       int ct = 0;
       int t = 0;
        Random na = new Random();
		int ns = na.Next(1, 100);
		do
		{ 
			Console.Write("Tente adivinhar um número de 1 a 100: ");
		    t = Convert.ToInt32(Console.ReadLine());
		    ct++;
		    
		    switch (t.CompareTo(ns))
		    {
		        case<0:
		            Console.WriteLine("Muito Baixo. Tente novamente");
		            break;
		        case>0:
		            Console.WriteLine("Muito Alto. Tente novamente");
		            break;
		        case 0:
		            Console.WriteLine($"Parabéns, você acertou em {ct} tentativas");
		            break;
		    }
		}
		while(t != ns);
    }
}

## ** Distancia **
// Online C# Editor for free
// Write, Edit and Run your C# code using C# Online Compiler

using System;

public class HelloWorld
{
    public static void Main(string[] args)
    {
        Console.WriteLine ("Informe a distancia em metros" );
        if (int.TryParse(Console.ReadLine(), out int metro))
        {
            Console.Write("Escolha a unidade de conversão (km, cm, mi): ");
            string unidadeMedida = Console.ReadLine();
            int resultado = 0;
            switch (unidadeMedida)
            {
                case "cm" :
                    resultado = metro * 100;
                    Console.WriteLine($"Essa distancia em centimentros é igual a {resultado}");
                    break;
                case "km" :
                    resultado = metro / 1000;
                    Console.WriteLine($"Essa distancia em kilometros é igual a {resultado}");
            break;
            
            case "mi":
                resultado = metro / 1609;
                Console.WriteLine($"Essa distancia em milhas é igual a {resultado}");
             break;
        default:
            Console.WriteLine("Escreva uma unidade de medida valida!");
            break;
            }
        }
        else
        {
        Console.WriteLine("Escreva um numero valido!");
        }
    }

 ## ** Conversão de Moedas**
 // Online C# Editor for free
// Write, Edit and Run your C# code using C# Online Compiler

using System;

public class HelloWorld
{
    public static void Main(string[] args)
    {
        Console.WriteLine ("Informe a distancia em metros" );
        if (int.TryParse(Console.ReadLine(), out int metro))
        {
            Console.Write("Escolha a unidade de conversão (km, cm, mi): ");
            string unidadeMedida = Console.ReadLine();
            int resultado = 0;
            switch (unidadeMedida)
            {
                case "cm" :
                    resultado = metro * 100;
                    Console.WriteLine($"Essa distancia em centimentros é igual a {resultado}");
                    break;
                case "km" :
                    resultado = metro / 1000;
                    Console.WriteLine($"Essa distancia em kilometros é igual a {resultado}");
            break;
            
            case "mi":
                resultado = metro / 1609;
                Console.WriteLine($"Essa distancia em milhas é igual a {resultado}");
             break;
        default:
            Console.WriteLine("Escreva uma unidade de medida valida!");
            break;
            }
        }
        else
        {
        Console.WriteLine("Escreva um numero valido!");
        }
    }

## ** Adivinhação de Numeros**
// Online C# Editor for free
// Write, Edit and Run your C# code using C# Online Compiler

using System;

public class Program
{
	public static void Main()
	{
    	int t = 0;
    	bool r = false;
		    Random na = new Random();
	    	int vi = na.Next(1,100);
	    	Console.WriteLine(vi);
	    	do
	    	{
				Console.Write("Adivinhe um numero de 1 a 100: ");
				int n = int.Parse(Console.ReadLine());
				if (n == vi)
				{
					t++;
					Console.WriteLine("Parabéns! Você Acertou! Com apenas "+ t + " tentativas!");
					r = true;
				}
		    	else
		    	{
					if (n > vi)
					{
					    t++;
			        	Console.WriteLine("Muito alto! :(, Tente um número menor. ");
						r = false;
					}
			    	else
					{
				        t++;
				    	Console.WriteLine("Muito baixo! :(, Tente um número maior. ");
						r = false;
					}
			}
		}
	    	while (r == false);
	}
}