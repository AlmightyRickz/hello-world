# hello-world
using System;
using System.Collections.Generic;
using System.Text;

namespace ConsoleApp3
{
    abstract class Abstract //必须在class前面加abstract
    {
        public abstract void Hello();//public后面需要加上abstract
    }
}
------------------------------------------------------------------
using System;
using System.Collections.Generic;
using System.Text;

namespace ConsoleApp3
{
       class Son:Abstract //不能忘记继承父类
    {
        public override void Hello()
        {
            Console.WriteLine("123");
        }
    }
}
--------------------------------------
using System;

namespace ConsoleApp3
{
    class Program
    {
        static void Main(string[] args)
        {
            Son S1 = new Son();
            S1.Hello();
            Console.ReadKey();
        }
    }
}
