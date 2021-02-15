# Lab-20.50-
#include <iostream>
using namespace std;
void conversion (double& inches, int& foot) {
  cout << "Input how many inches you would like to convert to meters" << endl;
  cin >> inches;
  cout << "Input how many feet you would like to convert to meters" << endl;
  cin >> foot;
}
double calculations ( double inches, int foot ){ 
  double meter = 0.3048 * (foot + inches/ 12); 
  return meter;
}
void results (double inches, int foot, double meter) { 
 cout << "Inches : " << inches << endl;
 cout << "Feet : " << foot << endl;
 cout << "Meters : " << meter << endl;
}
void input (int& meter) {
cout << "Please input how many meters you would like to convert" << endl;
cin >> meter;
}
double calculations2 ( int& meter, double& foot){
  double dfoot = meter /0.3048; 
  foot = int (dfoot);
  double inches = (dfoot - foot)* 12;
  return inches;
}
void results2 (double inches, double foot, int meter) { 
 cout << "Inches : " << inches << endl;
 cout << "Feet : " << foot << endl;
 cout << "Meters : " << meter << endl;
}
int main() {
  int answer; 
 cout << "If you would like to convert from feet and inches to meters enter 1 or from meters to feet and inches enter 2" << endl;
 cin >> answer;
 if (answer == 1) {
   double inches;
  int foot;
  double meter;
  conversion (inches, foot);
  meter = calculations (inches, foot);
  results (inches, foot, meter);
 }
 else if (answer == 2) {
   double inches;
  double foot;
  int meter;
  input (meter);
  inches = calculations2 (meter, foot);
  results2 (inches, foot, meter);

 }
}
