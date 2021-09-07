using System;
using System.Collections.Generic;
using System.Text;

namespace ConsoleApp2
{
    class Human
    {
        public virtual void Run()
        {
            Console.WriteLine("RUN!");
        }
    }
}
-------------------------------------
using System;
using System.Collections.Generic;
using System.Text;

namespace ConsoleApp2
{
    class HSS:Human
    {
        public override void Run()
        {
            base.Run();
            Console.WriteLine("种族天赋跑得快");  //默认调用父类中的run 可以//划掉但没必要
        }
    }
}
---------------------------------------
using System;
using System.Collections.Generic;
using System.Text;

namespace ConsoleApp2
{
    class Vietnamese:Human
    {
        public override void Run()
        {
            base.Run();  //默认调用父类中的run 可以//划掉但没必要
            Console.WriteLine("RUN不了啊RUN不了");
        }
    }
}
---------------------------------------------------
using System;

namespace ConsoleApp2
{
    class Program
    {
        static void Main(string[] args)
        {
            HSS H = new HSS();
            H.Run();
            Vietnamese V = new Vietnamese();
            V.Run();
            Console.ReadKey();
                       
                
         }
    }
}
