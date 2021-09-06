# 定义一个person的class
using System;
using System.Collections.Generic;
using System.Text;

namespace ConsoleApp1
{
    class Person
    {
        private int age; //私有化age；
        public string name;
        public gender gender;

        public int Age  
        {
            get { return age; }  //get:取值
            set // { age = value; } //set:赋值
            {
                if(value > 100 || value < 0) //对返回的赋值进行判断；
                {
                    age = 18;
                    //Console.WriteLine("您是老妖精？");
                }
                else
                {
                    age = value;
                }
            }
        }   
    }
}
------------------------------------------------------------------------
using System;

namespace ConsoleApp1
{
    public enum gender
    {
        男,
        女
    }

    class Program
    {
        static void Main(string[] args)
        {
            Person p1 = new Person(); //类的使用方法
            p1.name = "rick";
            p1.Age = 101;
            p1.gender = gender.男;
            Console.WriteLine(p1.name + p1.Age + p1.gender);
            //Console.ReadKey();


            //Apple a1 = new Apple();
            a1.color = Color.Red;
            a1.Shape = "圆形";
            a1.Weight = 200;
            Console.WriteLine(a1.Weight + a1.Shape + a1.color);
            Console.ReadKey();
            
                
        }
    }
}

