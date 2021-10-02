#include <iostream>
#include <ctime>
#include <string.h>
#include <windows.h>
#include <cstdlib>
using namespace std;
double money;
float multiplier;
bool GameOver;
int multipliercost=1;
inline void wait_on_enter()
{
    string dummy;
    getline(cin, dummy);
}
void setup()
{
   cout<<"You decide to get rich! [Press ENTER to continue]"<<endl;
   wait_on_enter();
   cout<<"You're only starting, with a dollar you found on the ground..."<<endl;
   wait_on_enter();
   cout<<"Rome wasn't built in a day!"<<endl;
   wait_on_enter();
   money=1;
   multiplier=1;
   GameOver=false;
   cout<<"Let's do this!"<<endl;
   wait_on_enter();  //only piece of code that is stolen off the internet, lmao [also only comment] [PS. the function is also from the internet
   system("CLS");

}

void Game()
{   int aux=money+10+multipliercost*(multipliercost/2);
    while(money<aux)
    {
    cout<<"Current money: "<<money<<"$"<<endl;
    cout<<"Multiplier: "<<multiplier<<"x"<<endl;
    Sleep(500);
    cout<<endl<<endl;
    system("CLS");
    money=money+1*multiplier;
    }


}
void ZwischenSpiel()
{

    string UpgradeResponse;
    cout<<"Do you want to buy a multiplier upgrade? [Yes/yes/Y/y] or exit the game? [Exit,exit,out]";
    cin>>UpgradeResponse;
    if (UpgradeResponse=="Yes"||UpgradeResponse=="yes"||UpgradeResponse=="y"||UpgradeResponse=="Y")
    {money=money-multipliercost;
    multiplier++;
    multipliercost=multipliercost+money/2;
    }
    else if(UpgradeResponse=="Exit"||UpgradeResponse=="exit"||UpgradeResponse=="out")
        GameOver=true;
    else cout<<"You chose not to get a better multiplier..."<<endl;
    system("CLS");

}

int main()
{
    setup();
    while (GameOver!=true)
    {
        Game();
        ZwischenSpiel();
    }
    cout<<"The game has finished, you made a total of :"<<money<<"$ ,congratulations!";
    return 0;
}
