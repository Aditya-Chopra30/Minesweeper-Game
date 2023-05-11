import java.io.*;
import java.util.*;
class minesweeper
{
public static void main(String vt[])
{
Scanner sc=new Scanner(System.in);
int score=0;
int nf=0;//no. of flags used
int tl=0;//tiles left
System.out.println("Enter size of 2d array (rows and columns)");
int rows=sc.nextInt();
int col=sc.nextInt();
System.out.println("Enter no. of bombs");
int bomb=sc.nextInt();
String minesweeper[][]=new String[rows][col];
int a[][]=new int[rows][col];
int y=0,x=0,i=0,j=0;//loop variable
Random mrd=new Random();
for(x=0;x<bomb;x++)
{
i=mrd.nextInt(1)*i;
j=mrd.nextInt(1)*j;
a[i][j]=10;
if((i-1)>=0 && (j-1)>=0)
a[i-1][j-1]++;
if(i!=0)
a[i-1][j]++;
if(i!=0 && (j+1)<col)
a[i-1][j+1]++;
if((j-1)>=0)
a[i][j-1]++;
if((j-1)>=0)
a[i][j]++;
if((j+1)<col)
a[i][j+1]++;
if((i+1)<rows && (j-1)>=0)
a[i+1][j-1]++;
if((i+1)<rows)
a[i+1][j]++;
if((i+1)<rows && (j+1)<col)
a[i+1][j+1]++;
}
for(i=0;i<rows;i++)
{
 for(j=0;j<col;j++)
 minesweeper[i][j]="|_|";          
}
ab:while(true)
{
 for(i=0;i<rows;i++)
  {
   for(j=0;j<col;j++)
   System.out.print(minesweeper[i][j]);
   System.out.println();
  }
 System.out.println("Enter no. 1-Play 2-Flag 3-Doubt");
 int choice=sc.nextInt();
 System.out.println("Enter coordinate of row");
 x=sc.nextInt();
 System.out.println("Enter coordinate of column");
 y=sc.nextInt();
  switch(choice)
 {
  case 1:
  if(a[x][y]>=10)//encountering a bomb
  {
   if(minesweeper[x][y]=="|@|")
   score=score-10;
   break ab;
  }
  else
  minesweeper[x][y]="|"+a[x][y]+"|";
  break;
  case 2:
  minesweeper[x][y]="|@|";
  nf++;
  break;
  case 3:
  if(minesweeper[x][y]=="|@|")
  nf--;
  minesweeper[x][y]="|?|";
  break;
  default:
  System.out.println("Wrong choice");
  break;
 }
for(i=0;i<rows;i++)
{
 for(j=0;j<col;j++)
 {
  if(minesweeper[i][j]=="|@|")
  tl++;
 }
}
if(tl==bomb)
break ab;
}
 for(i=0;i<rows;i++)
  {
   for(j=0;j<col;j++)
   System.out.print(minesweeper[i][j]);
   System.out.println();
  }
   for(i=0;i<rows;i++)
   {
    for(j=0;j<col;j++)
    {
     if(minesweeper[i][j]=="|@|" && a[i][j]>=10)
     score=score+10;
    }
   }
if(nf>bomb)
score=score-((nf-bomb)*10);
System.out.println("Score is "+score);
}
}














