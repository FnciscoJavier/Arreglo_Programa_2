// Francisco Javier baltazar de los santos_20887045_4_E.
// José Octavio Hernández Arcos_20887043_4_E//




using System;
using System.Threading;
namespace Menoramayor
{
   class Program
    {
       private static int i;

      public static void Main(string[] args)
        {

         int mydelay = 2000;
            {

                //Creamos un vector (Array) de enteros con una longitud de 5 elementos
                double[] numeros = new double[5];

                //Solicitamos al usuario los 5 valores (desordenados)
                for (int i = 0; i < 5; i++)
                {
                    Console.WriteLine("Ingrese un valor:");

                    numeros[i] = double.Parse(Console.ReadLine());

                }

                //Ordenamos la lista e imprimimos los valores.
                Array.Sort(numeros);

                Console.WriteLine("\nLos números ordenados de menor a mayor son:");

                for (int i = 0; i < 5; i++)
                {
                    Console.WriteLine(numeros[i]);
                    Thread.Sleep(mydelay);
                }
                if (numeros[i] > 1900)
                {
                    Console.WriteLine("E l equivale la numeros {0} es A", numeros[i]);
                }
                else if (numeros[i] > 1600 && numeros[i] < 1800)
                {
                    Console.WriteLine("E l equivale la nota {0} es B", numeros[i]);


                }
                else if (numeros[i] > 500 && numeros[i] < 1700)
                {
                    Console.WriteLine("E l equivale la nota {0} es C", numeros[i]);

                }
                else
                {
                    Console.WriteLine("E l equivale la nota {0} es F", numeros[i]);
                }

                Array.Reverse(numeros);
                Console.WriteLine("\nLos números ordenados de mayor a menor son:");

                for (int i = 0; i < 5; i++)
                {
                    Console.WriteLine(numeros[i]);
                    Thread.Sleep(mydelay);
                }
                Console.WriteLine("\nLos datos han sido guardados");
                using (StreamWriter writer = new StreamWriter("ArchivoFrancis.txt", false))
                {

                    for (int i = 0; i < numeros.Length; i++)
                    {
                        writer.WriteLine(numeros[i].ToString());
                    }
                }

                //Para mantener la consola abierta
               
                Array.Sort(numeros);
                Console.WriteLine("el numero mas bajo fue {0}", numeros[0]);
                Array.Reverse(numeros);
                Console.WriteLine("el numero mas alto fue {0}", numeros[0]);
                Console.ReadKey();
            }
        }
    }
}
