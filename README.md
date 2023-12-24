Отчет по компьютерному практикуму № 12


    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;

    namespace ConsoleApp12
    {
    internal class Program
    {
        static void Main(string[] args)
        {
            //1. Вычислить значение функции для целых аргументов двумя способами (1-й способ: полный условный оператор; 2-й способ: тернарная операция):
            /*Console.Write("Введите число x - ");
            
            int x = int.Parse(Console.ReadLine());
            double y = 0;
            if (x>0)
            {
                y = Math.Pow(Math.Sin(x),2);
            }
            else
            {
                y = 1 - 2*Math.Sin(Math.Pow(x,2));
            }
            int x = int.Parse(Console.ReadLine());
            double y = 0;
            y = (x > 0) ? y = Math.Pow(Math.Sin(x), 2) : y = 1 - 2 * Math.Sin(Math.Pow(x, 2)); ;
            Console.WriteLine(y);*/
            /*
            
            // 2.Используя двузначное случайное число, вывести на экран информацию о четности или нечетности этого числа с использованием тернарной операции.
            Random number = new Random();
            int twonumber = number.Next(10, 99);
            string st = (twonumber % 2 == 0) ? "четное число" : "не четное число";
            Console.WriteLine(twonumber);
            Console.WriteLine(st);*/
            //3. Даны три целых положительных числа. Если все они четные, каждое число увеличить на 1; если хотя бы одно из них четное, уменьшить на 1; если четных чисел нет, каждое число увеличить в 2 раза.
            /*
            Console.WriteLine("Введите 3 положительных числа");
            int x = int.Parse(Console.ReadLine());
            int y = int.Parse(Console.ReadLine());
            int z = int.Parse(Console.ReadLine());
            if (x <= 0 | y <= 0 | z <=0 )
            {
                Console.WriteLine("Есть число или числа равные нулю или меньше нуля");
                Console.ReadLine();
                return;
            }
            if (x % 2 == 0 & y % 2 == 0 & z % 2 == 0)
            {
                Console.WriteLine("Все четные");
                x++;
                y++;
                z++;
            }
            else if (x % 2 == 0 | y % 2 == 0 | z % 2 == 0)
            {
                Console.WriteLine("Хотя бы одно из них четное");
                x--;
                y--;
                z--;
            }
            else if (x % 2 != 0 & y % 2 != 0 & z % 2 != 0)
            {
                Console.WriteLine("Четных чисел нет");
                x *= 2;
                y *= 2;
                z *= 2;
            }
            Console.WriteLine($"{x}\n{y}\n{y}");*/
            //4. По введенному номеру месяца выводится название поры года (зима, весна, лето, осень) и сообщение: сессия, каникулы, 1 семестр, 2 семестр
            Console.Write("Введите номер месяца - ");
            byte seasons = byte.Parse(Console.ReadLine());
            switch (seasons)
            {
                case 1: Console.WriteLine("Время года Зима\nУ вас сессия"); break;

                case 12:
                case 2: Console.WriteLine("Время года Зима\nУ вас второй семестр"); break;

                case 3:
                case 4:
                case 5: Console.WriteLine("Время года Весна\nУ вас второй семестр"); break;

                case 6: Console.WriteLine("Время года Лето\nУ вас сессия"); break;
                case 7:
                case 8: Console.WriteLine("Время года Лето"); break;

                case 9:
                case 10:
                case 11: Console.WriteLine("Время года Осень\nУ вас первый семестр"); ; break;


            }
            Console.ReadKey();
        }
    }
}
