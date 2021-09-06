#2d_array in maze
//二维数组实现迷宫，或其他图案。
using System;

namespace maze
{
    class Program
    {
        static void Main(string[] args)
        {
            int[,] maze = new int[,]   //二位数组的定义方法int[,] 2darray=new int[,]{{1,1,1,},{2,2,2},{...}}
            {   
                {1,1,1,1,1,1,1,1,1,1,1},
                {1,1,0,0,1,1,1,0,0,1,1},
                {1,0,1,1,0,1,0,1,1,0,1},
                {1,0,1,1,1,0,1,1,1,0,1},
                {1,0,1,1,1,1,1,1,1,0,1},
                {1,1,0,1,1,1,1,1,0,1,1},
                {1,1,1,0,1,1,1,0,1,1,1},
                {1,1,1,1,0,1,0,1,1,1,1},
                {1,1,1,1,1,0,1,1,1,1,1}
            };
              //遍历二维数组的方法
            for(int i=0; i < maze.GetLength(0); i++)  //获取行轴的长度
            {
                for(int j=0;j < maze.GetLength(1);j++) //获取竖轴的长度
                {
                    if(maze[i, j] == 1)   //判断数组中的值是否为1
                    {
                        Console.Write("■");
                    }
                    if(maze[i,j] == 0)  //判断数组中的值是否为0
                    {
                        Console.Write("◆");
                    }
                    
                }
                Console.WriteLine(); //换行

            }
            Console.ReadKey();
        }
    }
}

