using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace OddEvenPosition
{
    class OddEvenPosition
    {
        static void Main(string[] args)
        {
            int n = int.Parse(Console.ReadLine());

            double oddMin = int.MaxValue;
            double oddMax = int.MinValue;
            double oddSum = 0;
            double evenMin = int.MaxValue;
            double evenMax = int.MinValue;
            double evenSum = 0;

            if (n == 0)
            {
                Console.WriteLine($"OddSum = {n}, Oddmin = No, OddMax = No, EvenSum = {n}, EvenMin = No, EvenMax = No");
            }
            else if (n == 1)
            {
                double m = double.Parse(Console.ReadLine());
                Console.WriteLine($"OddSum = {m}, Oddmin = {m}, OddMax = {m}, EvenSum = 0, EvenMin = No, EvenMax = No");
            }
            else
            {

                for (int i = 1; i <= n; i++)
                {
                    double m = double.Parse(Console.ReadLine());

                    int level = i % 2;


                    if (level != 0)
                    {
                        oddSum += m;

                        if (oddMin > m)
                        {
                            oddMin = m;
                        }
                        if (oddMax < m)
                        {
                            oddMax = m;
                        }
                    }
                    else if (level == 0)
                    {
                        evenSum += m;

                        if (evenMin > m)
                        {
                            evenMin = m;
                        }
                        if (evenMax < m)
                        {
                            evenMax = m;
                        }
                    }
                }
                Console.WriteLine($"OddSum = {oddSum}, Oddmin = {oddMin}, OddMax = {oddMax}, EvenSum = {evenSum}, EvenMin = {evenMin}, EvenMax = {evenMax}");
            }
        }
    }
}
