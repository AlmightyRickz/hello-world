# hero karel
using System;
using System.Collections.Generic;
using System.Text;

namespace FinalTest
{
    class Karel:Hero
    {
        public Karel() { }
        public Karel(string m_heroName, string m_heroInfo, int m_attack, int m_defense, string m_nickName)
            :base(m_heroName, m_heroInfo, m_attack, m_defense, m_nickName)
        {
            
        }
        public void XuYiMiao()
        {
            Console.WriteLine("发动了续一秒");
        }
    }
}
----------------------------------------------------------------
hero rick
using System;
using System.Collections.Generic;
using System.Text;

namespace FinalTest
{
    class Rick:Hero
    {
        public Rick() { }
        public Rick(string m_heroName, string m_heroInfo, int m_attack, int m_defense, string m_nickName)
            :base( m_heroName, m_heroInfo, m_attack,m_defense,m_nickName)
        {
          
        }
        public void ManWangChongZhuang()
        {
            Console.WriteLine("发动了蛮王冲撞");
        }

    }
}
--------------------------------------------------------------------
hero 父类
using System;
using System.Collections.Generic;
using System.Text;

namespace FinalTest
{
    class Hero
    {
        private string heroName;
        private string heroInfo;
        private int attack;
        private int defense;
        private string nickName;
        public Hero() { }
        public Hero(string m_heroName, string m_heroInfo, int m_attack, int m_defense, string m_nickName)
        {
            this.heroName = m_heroName;
            this.heroInfo = m_heroInfo;
            this.attack = m_attack;
            this.defense = m_defense;
            this.nickName = m_nickName;

        }
        public void Hello()
        {
            Console.WriteLine("我的名字是：{0},是一个{1},攻击力为：{2},防御力为{3},人送外号{4}", this.heroName, this.heroInfo, this.attack, this.defense, this.nickName);
        }
        public string HeroName
        {
            get { return heroName; }
            set { heroName = value;}
        }
        public string HeroInfo
        {
            get { return heroInfo; }
            set { heroInfo = value;}
        }
        public int Attack
        {
            get { return attack; }
            set { attack = value;}
        }
        public int Defense
        {
            get { return defense; }
            set { defense = value;}
        }
        public string NickName
        {
            get { return nickName; }
            set { nickName = value;}
        }

    }
}
---------------------------------------------------------------
using System;

namespace FinalTest
{
    class Program
    {
        static void Main(string[] args)
        {
            Rick Rick = new Rick("Rick", "宇宙级帅哥", 999, 999, "帅哥恺");
            Karel Karel = new Karel("Karel", "膜法师", 1, 1, "膜法迪");

            Rick.Hello();
            Rick.ManWangChongZhuang();
            Karel.Hello();
            Karel.XuYiMiao();

            Console.ReadKey();
        }
    }
}
