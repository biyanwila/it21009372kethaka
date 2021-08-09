#include <iostream>
#include "shapeArea.h"
#include <iomanip>
using namespace std;

struct Circle
{
  float radius;

};

struct Rectangle
{
  float length;
  float width;

};

struct Square
{
  float length;

};

int main() 
{
  float circleA;
  float sqrA;
  float bigRecA;
  float smlRecA;
  float GreenArea;

  Circle c1;
  Rectangle big, small;
  Square s1;

  c1.radius = 5;
  s1.length = 4;
  big.length = 28;
  big.width = 15;
  small.length = 7;
  small.width = 3;
  
  circleA = areaCircle(c1.radius);
  sqrA = areaSquare(s1.length);
  bigRecA = areaRectangle( big.length, big.width);
  smlRecA = areaRectangle( small.length, small.width);

  GreenArea = bigRecA - (circleA + smlRecA +  sqrA );

  cout<<"Area of the green path : "<<fixed<<showpoint<<setprecision(2)<<GreenArea<<endl;

}