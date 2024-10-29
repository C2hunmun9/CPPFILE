# CPPFILE
/*create a program that generates a random number and asks the user to guess
 it. provide feedback on whether the guess is too high or low until the user
 guesses the correct number.*/
 #include<iostream>
 #include<cstdlib>
 #include<ctime>
 using namespace std;
 int main()
 {        
          int inputuser;
          char moves;
          srand(time(0));
          int random=rand()%100+20;

          cout<<"------------NUMBER GUESSING GAME-----------"<<endl;
          
          do{
                    cout<<"enter number in between range 1 to 100:      ";
                    cin>>inputuser;
                    cout<<endl;
                    if(inputuser>random){
                    cout<<"your guess is too high"<<endl;
                    }
                    else if(inputuser<random){
                    cout<<"your guess is too low"<<endl;
                    }
                    else
                    {
                    cout<<"your guess is correct"<<endl;
                    break;
                    }
                    cout<<"would you like to try again Y/N :     ";
                    cin>>moves;
                    cout<<endl;
                   }
          while(moves!='N');        
          cout<<"game end"<<endl;
          return 0;
}

	
