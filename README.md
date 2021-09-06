# hello-world
using System;
using System.Collections.Generic;
using System.Text;

namespace Class
{
    public enum gender
    {
        男,
        女
    }
    class Person 
    {
        private string name;
        private string address;
        private int age;
        private gender gender ;
        public Person()
        {

        }
        public Person(string name,string address,int age,gender gender)//初始化对象；
        {
            this.name = name;
            this.address = address;
            this.age = age;
            this.gender = gender;
        }

        public string Name
        {
            get { return name; }   //取值
            set { name = value; }  //赋值
        }
        public string Address
        {
            get { return address; }
            set { address = value; }
        }
        public int Age
        {
            get { return age; }
        set { 
                if(value<0||value>100)   //对年龄进行判断
                {
                    Console.WriteLine("年龄不对哦！");
                }
            else
                { 
                    age = value;
                }
            }
            
            
        }
        public gender Gender   //定义性别
        {
            get { return gender; }
            set { gender = value; }
        }
        public void Eat()
        {
            Console.WriteLine("我一天吃三顿饭");
        }
        public void Sleep()
        {
            Console.WriteLine("我一天睡八小时");
        }
        public void Work()
        {
            Console.WriteLine("我一天工作八小时");
        }
    }
}
---------------------------------------------------------------------------------------------
using System;

namespace Class
{
    class Program
    {
        static void Main(string[] args)
        {
            Person p1 = new Person();  //仅存10分钟就被淘汰的落后方法
            p1.Address = "浙江绍兴小越镇";
            p1.Age = 18;
            p1.Gender = gender.男;
            p1.Name = "Rick";
            p1.Eat();
            p1.Sleep();
            p1.Work();
            Console.WriteLine("p1名字是{0}，性别是{1}，地址是{2}，年龄是{3}", p1.Name, p1.Gender, p1.Address, p1.Age);

            Person p2 = new Person("Rick", "浙江", 20, gender.男);//先进方法，建议使用

            Console.WriteLine("p2名字是{0}，性别是{1}，地址是{2}，年龄是{3}", p2.Name, p2.Gender, p2.Address, p2.Age);




            Console.ReadKey();

        }
    }
}
