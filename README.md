

```csharp
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Bem-vindo ao Jogo de Adivinhação!");
        
        // Gera um número aleatório entre 1 e 100
        Random random = new Random();
        int numeroParaAdivinhar = random.Next(1, 101);

        int tentativas = 0;
        int palpite = 0;

        while (palpite != numeroParaAdivinhar)
        {
            Console.Write("Digite seu palpite: ");

            // Certifique-se de que a entrada é um número inteiro
            while (!int.TryParse(Console.ReadLine(), out palpite))
            {
                Console.WriteLine("Por favor, insira um número válido.");
                Console.Write("Digite seu palpite: ");
            }

            tentativas++;

            if (palpite < numeroParaAdivinhar)
            {
                Console.WriteLine("Tente um número maior.");
            }
            else if (palpite > numeroParaAdivinhar)
            {
                Console.WriteLine("Tente um número menor.");
            }
            else
            {
                Console.WriteLine($"Parabéns! Você acertou em {tentativas} tentativas.");
            }
        }
    }
}
```

