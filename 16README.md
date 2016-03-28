# GUIA2
GUIA2IAI
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace MR13087GUIA2EJ16
{
    class Program
    {
        static void Main(string[] args)
        {
            //Declaracion de Constantes
            const float bonibasica = 001f;
            const float bon = 7.00f;
            const int primProd = 500;
            //Declaracion de Variables
            string obrero;
            double total;
            int envases;
            //Identificación del Programa
            Console.WriteLine("MR13087 Cálculo de bonificacion de un obrero en fábrica de envases plasticos\n Autor: Marroquín Rivera, Javier Ernesto GL: 36");
            //Entrada de datos
            Console.WriteLine("Nombre del Obrero:");
            obrero = Console.ReadLine();
            Console.WriteLine("Total de envases producidos:");
            envases = int.Parse(Console.ReadLine());
            //Proceso de datos
            if (envases <= primProd)
            {
                total = envases * (bon/primProd);
            }
            else
                total = (primProd*(bon/primProd)) + ((envases-primProd)*bonibasica);
            //Salida de Datos
            Console.WriteLine("Obrero: {0} ", obrero);
            Console.WriteLine("Total bonificacion: $ {0:0.00}", total);
            Console.ReadKey();
            
        }
    }
}

