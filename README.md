//                Faculty of Computers and Information
// Course:        CS213 - Programming II  - 2018
// Title:         Assignment II - Task 3
// Purpose:       Odometer to known miles ,efficiency of fuel and no. of gasoline
// Instructor:    Dr. Mohammad El-Ramly
// Authors:      Seif Mostafa Abobakr 20170123
// Date:          1 November 2018
#include <iostream>
using namespace std;


class Odometer{
private:
    double Miles;
    double Efficieny;

public:
 double M;
 Odometer(){Miles =0; Efficieny=0;}///constructor
 void Resetodometer(){ Miles=0;}///reset to odometer
 void SetEfficieny(double E){Efficieny=E;}///setter
 void SetMiles( double M ){Miles+=M; this->M=Miles;} ///setter
 double getgasoline()/// to get no. of gasoline gas
 {
 int x=(this->M/Efficieny);
 return x;
 }


};

int main(){

Odometer trip1;

trip1.SetEfficieny(3);
trip1.SetMiles(2);
trip1.SetMiles(4);
trip1.Resetodometer();
cout<<trip1.getgasoline()<<endl;

}

