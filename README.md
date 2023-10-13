#include<iostream>
#include<ctime>
#include<cmath>
using namespace std;

int sum_of_points,points  =  0;

int main(){
    int xi,yi,i = 0;

    srand(time(NULL));

    while (i<5) {
        i++;
        cout << "Set the coordinates of the shot " <<i<< endl;
        cout << "Xi = ";
        cin >> xi;
        cout << "  Yi = ";
        cin >> yi;
        xi += rand() % 10 - 5;
        yi += rand() % 10 - 5;
        cout <<endl<<"Shot "<<i<<" = ("<<xi<<","<<yi<<")"<<endl;
        points = 5 - (int)sqrt(pow(xi,2)+pow(yi,2));
        if (((points>>31)&1) == 0){
            sum_of_points += points;
        };
    }

 if (sum_of_points >= 10) cout <<"You Win!";
     else cout<<"You loser!";

    return 0;
}

