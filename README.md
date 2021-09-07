using System;
using System.Collections.Generic;
using System.Text;

namespace FatherTest
{
    class Animal
    {
        private int leg;
        public int Leg
        {
            get { return leg; }
            set { leg = value;}
        }

        public void Eat()
        {
            Console.WriteLine("i am fantong");
        }

        public void Sleep()
        {
            Console.WriteLine("i am zhu");
        }
        public void cry()
        {
            Console.WriteLine("i am very chao");
        }
    }
}
--------------------------------------------------------------
using System;
using System.Collections.Generic;
using System.Text;

namespace FatherTest
{
    class CatType:Animal   //继承父类animal
    {
        public void YSNL()
        {
            Console.WriteLine("i can see things at night");
        }
    }
}
--------------------------------------------------------------
using System;
using System.Collections.Generic;
using System.Text;

namespace FatherTest
{
    class Tiger:CatType //继承父类
    {
        public void Wang()
        {
            Console.WriteLine("i have a 'wong' in my face");
        }
    }
}
-------------------------------------------------------------------
using System;
using System.Collections.Generic;
using System.Text;

namespace FatherTest
{
    class Cat:CatType
    {
        public void ZLS()
        {
            Console.WriteLine("i can catch mouse");
        }
    }
}
---------------------------------------------------------------------
using System;
using System.Collections.Generic;
using System.Text;

namespace FatherTest
{
    class BirdType:Animal
    {
        public void Fly()
        {
            Console.WriteLine("i can fly");
        }
    }
}
--------------------------------------------------------
using System;
using System.Collections.Generic;
using System.Text;

namespace FatherTest
{
    class Bird:BirdType
    {
        public void Small()
        {
            Console.WriteLine("i am small");
        }
    }
}
--------------------------------------------------------------------------------
using System;
using System.Collections.Generic;
using System.Text;

namespace FatherTest
{
    class Eagle:BirdType
    {
        public void Cruel()
        {
            Console.WriteLine("i do eat bird~");
        }
    }
}
------------------------------------------------------------------------------------
using System;

namespace FatherTest
{
    class Program
    {
        static void Main(string[] args)
        {
            Cat c = new Cat();
            c.Leg= 4;
            c.Sleep();
            c.YSNL();
            c.cry();
            c.Eat();
            //Console.WriteLine(c.Leg);


        }
    }
}

