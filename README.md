# Exercicos-05-10
/*Tendo como dados de entrada o nome, a altura e o sexo (M ou F) de uma pessoa, calcule e mostre seu peso ideal, utilizando as seguintes fórmulas:
- para sexo masculino: peso ideal = (72.7 * altura) - 58
- para sexo feminino: peso ideal = (62.1 * altura) - 44.7*/

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Peso_Ideal
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Informe o nome:");
            string nome = Console.ReadLine();

            Console.WriteLine("Informe a altura:");
            Double altura = double.Parse(Console.ReadLine());

            Console.WriteLine("Informe M para sexo feminino e H para sexo masculino :");
            char sexo = char.Parse(Console.ReadLine());

            if (sexo == 'M')
            {
                double pesoidealfem = 62.1 * altura - 44.7;
                Console.WriteLine("O seu peso ideal " + nome + " é " + pesoidealfem);

            }
            else if (sexo == 'H')
            {
                double pesoidealmas = 72.7 * altura - 58;
                Console.WriteLine("O seu peso ideal " + nome + " é " + pesoidealmas);
            }
            else
            {
                Console.WriteLine("Você informou uma letra invalida");

            }



            Console.ReadKey();
        }
    }
}



/*Ler o salário fixo e o valor das vendas efetuadas pelo vendedor de uma empresa. 
Sabendose que ele recebe uma comissão de 3% sobre o total das vendas até R$1.500,00 mais 5%
sobre o que ultrapassar este valor, calcular e escrever o seu salário total.*/


using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;


namespace Salario_Total
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Informe o salário do vendedor:");
            Double salario = double.Parse(Console.ReadLine());

            Console.WriteLine("Informe o valor de vendas efetuadas pelo vendedor:");
            Double vendas = double.Parse(Console.ReadLine());

            if (vendas <= 1.500)
            {
                Console.WriteLine("O salário total é " + (vendas + (vendas * 3 / 100)));
            }
            else if (vendas > 1.500)
            {
                Console.WriteLine("O salário total é " + (vendas + (vendas * 5 / 100)));
            }
            else
            {
                Console.WriteLine("Você informou um valor inválido");
            }
            Console.ReadKey();
        }
    }
}

/*Ler 3 valores (considere que não serão informados valores iguais)e escrever o maior deles.*/


using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Maior_Valor
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Informe 3 valores diferentes: ");

            Console.WriteLine("Informe o primeiro valor: ");
            int primeiro = int.Parse(Console.ReadLine());

           
           Console.WriteLine("Informe o segundo valor : ");
           int segundo = int.Parse(Console.ReadLine());

            while (segundo == primeiro)
            {
                Console.WriteLine("Informe um valor diferente: ");
                int segundo1 = int.Parse(Console.ReadLine());
               segundo = segundo1;
            }

            Console.WriteLine("Informe o terceiro valor : ");
            int terceiro = int.Parse(Console.ReadLine());

            while ((terceiro == primeiro)||(terceiro == segundo))
            {
                Console.WriteLine("Informe um valor diferente: ");
                int terceiro1 = int.Parse(Console.ReadLine());
                terceiro = terceiro1;
            }

            if ((segundo > primeiro)&&(segundo > terceiro))
            {
                Console.WriteLine("O maior valor é " + segundo);
            }
            else if ((terceiro > primeiro) && (terceiro > segundo))
            {

                Console.WriteLine("O maior valor é " + terceiro);
            }
            else
            {
                Console.WriteLine("O maior valor é " + primeiro);
            }

            

            //Aguarda uma tecla a ser precionada
            Console.ReadKey();
        }
    }
}

/*Ler 3 valores (A, B e C) representando as medidas dos lados de um triângulo e escrever se
formam ou não um triângulo. OBS: para formar um triângulo, o valor de cada lado deve ser
menor que a soma dos outros 2 lados.*/

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;


namespace Lados__triangulos
{
    class Program
    {
        static void Main(string[] args)
        {
           

            Console.WriteLine("Informe tamanho do lado (A)do Triângulo: ");
            int A = int.Parse(Console.ReadLine());

            Console.WriteLine("Informe tamanho do lado (B)do Triângulo: ");
            int B = int.Parse(Console.ReadLine());

            Console.WriteLine("Informe tamanho do lado (C)do Triângulo: ");
            int C = int.Parse(Console.ReadLine());

            if (A == B && B == C && C == A)
            {
                Console.WriteLine(" triângulo Equilatero\n");
            }
            else if (A == B || B == C || C == A)
            {
                Console.WriteLine(" triângulo Isósceles\n");
            }
            else if (A != B && B != C && C != A)
            {
                Console.WriteLine(" triângulo Escaleno\n");
            }
            else
                Console.WriteLine("Valores invalidos para formar um triangulo\n");

            Console.ReadKey();
        }
    }
}


###################################################################################

/*Faça um algoritmo para ler o código e o preço de 15 produtos, calcular e escrever:

- o maior preço lido
- a média aritmética dos preços dos produtos*/

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Maior_preço
{
    class Program
    {
        static void Main(string[] args)
        {

            int preco;
            int soma = 0;
            float media , maior = 0;

            Console.WriteLine("Informe o preço de 15 produtos:");
           
            for (int i = 0; i < 15; i++) 
            {
                Console.WriteLine("Informe o preço:");
                preco = int.Parse(Console.ReadLine());
               

                if (preco > maior)
                {
                    maior = preco ;
                }

                soma = soma + preco;
            }
            
            media = soma/ 15;

            Console.WriteLine("soma de preço = " + soma);
            Console.WriteLine("Média de preço = " + media );
            Console.WriteLine("Maior preço = " + maior);



            Console.ReadKey();
        }
    }
}

###################################################################################

/*A prefeitura de uma cidade deseja fazer uma pesquisa entre seus habitantes. Faça um
algoritmos para coletar dados sobre o salário e número de filhos de 4 habitantes e após as
leituras, escrever:

a) Média de salário da população
b) Média do número de filhos
c) Maior salário dos habitantes
d) Percentual de pessoas com salário menor que R$ 150,00*/

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Media_salario
{
    class Program
    {
        static void Main(string[] args)
        {
            double soma = 0;
            double soma1 = 0;
            double maior = 0;
            int salario = 0;
            double totalperc = 0;
            Console.WriteLine("informe o salario e o numero de filhos de 4 Habitaantes:");

            for (int i = 0; i < 4; i++)
            {
                Console.WriteLine("Informe o salario:");
               salario = int.Parse(Console.ReadLine());

                Console.WriteLine("Informe  o numero de filhos:");
                int filhos = int.Parse(Console.ReadLine());

                if (salario > maior)
                {
                    maior = salario;
                }
                else if (salario < 150)
                {
                    double percentual = i;
                    totalperc = percentual / 100;

                }
                else
                {
                    Console.WriteLine();
                }

                soma = soma + salario;
                soma1 = soma1 + filhos;
            }

            double media1 = soma / 4;
            double media2 = soma1 / 4;

            Console.WriteLine("A media do salario da populacao é : " + media1);
            Console.WriteLine("A media do numero dos filhos é : " + media2);
            Console.WriteLine("O maior salario dos habitantes é : " + maior);
            Console.WriteLine("A percentagem das pessoas com salarios menor que 150 é: " + totalperc);

            Console.ReadKey();
        }
    }
}

