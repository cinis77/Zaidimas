using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Zaidimas
{
    class Program
    {
        static void Main(string[] args)
        {
            string up = "up";
            string Up = "Up";
            string down = "down";
            string Down = "Down";
            string Winner = "Winner";
            string winner = "winner";
            int max = 1000;
            int min = 1;
            int guessing = 500;
            string status = null;
            Console.WriteLine("Sugalvokite skaičių nuo 1 iki 1000 ir paspauskite enter");
            Console.ReadLine();
            while(true)
            {
                Console.WriteLine("Ar jusu skaicius yra: " + guessing);
                Console.WriteLine("Jei taip iveskite {0}, jei skaicius yra didesnis iveskite {1}, jei yra mazesnis iveskite {2}", Winner, Up, Down);
                status = Console.ReadLine();
                if(status == up || status == Up)
                {
                    min = guessing;
                    guessing = (min + max) / 2;
                }
                else if (status == down || status == Down)
                {
                    max = guessing;
                    guessing = (min + max) / 2;
                }
                else if (status == winner || status == Winner)
                {
                    break;
                }
            }
            Console.WriteLine("Atspejau !!!!");
            Console.ReadKey();
        }
    }
}
