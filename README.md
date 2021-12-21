//Определить кратчайшее расстояние от заданной точки до границы заданной фигуры, считая, что точка находится вне фигуры.
#include <iostream>
#include <math.h>
using namespace std;

int main() {
double x, y;
float rast , rast1 , rast2;
setlocale (LC_ALL, "rus");
cin>>x>>y;
if (y>0)
{
   rast1=6-x;
   rast2=6-y;
   if (rast1>rast2)
   {
      cout<<rast1;
   }
   else 
   {
      cout<<rast2;
   }
}
else 
   if (x*x+y*y<36)
   {
      rast=6--sqrt(x*x+y*y);
      cout<<rast;
   }
   else 
      if ((y>12) && (fabs(x)<12))
      {
         rast=fabs(y)-12;      
         cout<<rast;
      }
      else 
          if  ((fabs(x)>12) && (y<12))
          {
             rast=fabs(x)-12;         
             cout<<rast;
          }
          else 
              if  (x*x+y*y>144)
              {
                 rast=sqrt(x*x+y*y)-12;              
                 cout<<rast;
              }
              else 
                  if (fabs(x)>12 && fabs(y)>12)
                  {
                     rast=sqrt((fabs(x)-12)*(fabs(x)-12)+(fabs(y)-12)*(fabs(x)-12));
                     cout<<rast;
                  }
                  else 
                  {
                     cout<<"Точка принадлежит заштрихованной фигуре";
                  }   
 return 0;
 }            
