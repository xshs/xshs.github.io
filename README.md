小怂在github的第一篇博客！！！

第十三届蓝桥杯省赛 GCD
！[image](https://github.com/xshs/xshs.github.io/blob/main/images/7.png)

问gcd（a+k，b+k）的最大公约数，不难想到最大公约数为abs（a-b）

举例：a=10，b=17

这俩数同时增加k可以获得最大公约数为7；

10+4,17+4；即14和21的最大公约数，满足7；并且无论怎么凑都无法获得大于7的公约数

所以这题就很简单了，先判断可以获得的最大公约数，然后再寻找最小的k满足条件即



    import java.util.Scanner;
 
    public class GCD {

    public static void main(String[] args) {
		
        Scanner sc=new Scanner(System.in);
				
        long a=sc.nextLong();
				
        long b=sc.nextLong();
				
        long max=Math.abs(a-b);
				
        if (a%max==0){
				
            System.out.print(max);
						
        }else {
				
            System.out.print(max-(a%max));
						
        }
				
    }
