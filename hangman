//hangman

#include <iostream>
#include<cstdlib>
#include<string>
#include <ctime>
using namespace std;

void draw(int guessWrong);

int main()
{
    cout<<"Hangman"<<endl;
    
    const string words[] = {"apple","orange","pineapple","mango"};
    
    int size = sizeof(words) / sizeof(words[0]);
    
    srand(time(0));
    
    string word =words[rand() % size];
    
    //underscores(_) with space
    string hiddenWord;
    for(int i = 0;i < word.length(); i++)
    {
        hiddenWord += "_";
    }
       
    
    char guess;
    bool guessCorrectly;
    int guessWrong = 0;
    const int maxGuesswrong = 6;
    
    while (hiddenWord != word && guessWrong < maxGuesswrong)
    {
       //underscores(_) with space
       cout<<"word hidden:"<<endl;
       for(char c :hiddenWord)
       {
           cout<<c<<" ";
       }
       cout<<"\n"<<endl;
       
       cout<<"\nwrong guess left: "<<(maxGuesswrong - guessWrong)<<endl;
       cout<<"\nguess the letter"<<endl;
       cin>>guess;
       
       //convert to lowercase
       guess = tolower(guess);
       
       guessCorrectly = false;
       for(int i = 0;i < word.length(); i++)
       {
           if(word[i] == guess)
           {
               hiddenWord[i] = guess;
               guessCorrectly = true;
           }
       }
       
       if(!guessCorrectly)
       {
           guessWrong++;
           cout<<"you guessed "<<guess<<" that's not in the word.you lose a life."<<endl;
       }
       
       draw(guessWrong);
       
    }
    
    //check win or lose
       if(hiddenWord == word)
       {
          cout<<"congratulations. you win"<<endl; 
       }
       else
       {
           cout<<"you lose"<<endl;
           cout<<"the correct word is "<<word<<endl;
       }
    
    return 0;
}

void draw(int guessWrong)
{
  if(guessWrong ==0)
       {
            cout<<" +-----+"<<endl;
            cout<<" |     |"<<endl;
            cout<<"       |"<<endl;
            cout<<"       |"<<endl;
            cout<<"       |"<<endl;
            cout<<"       |"<<endl;
            cout<<"=========="<<endl;
       }
       else if(guessWrong ==1)
       {
            cout<<" +-----+"<<endl;
            cout<<" |     |"<<endl;
            cout<<" O     |"<<endl;
            cout<<"       |"<<endl;
            cout<<"       |"<<endl;
            cout<<"       |"<<endl;
            cout<<"=========="<<endl;
       }
       else if(guessWrong ==2)
       {
            cout<<" +-----+"<<endl;
            cout<<" |     |"<<endl;
            cout<<" O     |"<<endl;
            cout<<" |     |"<<endl;
            cout<<"       |"<<endl;
            cout<<"       |"<<endl;
            cout<<"=========="<<endl;
       }
       else if(guessWrong ==3)
       {
            cout<<" +-----+"<<endl;
            cout<<" |     |"<<endl;
            cout<<" O     |"<<endl;
            cout<<"/|     |"<<endl;
            cout<<"       |"<<endl;
            cout<<"       |"<<endl;
            cout<<"=========="<<endl;
       }
       else if(guessWrong ==4)
       {
            cout<<" +-----+"<<endl;
            cout<<" |     |"<<endl;
            cout<<" O     |"<<endl;
            cout<<"/|)    |"<<endl;
            cout<<"       |"<<endl;
            cout<<"       |"<<endl;
            cout<<"=========="<<endl;
       }
       else if(guessWrong ==5)
       {
            cout<<" +-----+"<<endl;
            cout<<" |     |"<<endl;
            cout<<" O     |"<<endl;
            cout<<"/|)    |"<<endl;
            cout<<"/      |"<<endl;
            cout<<"       |"<<endl;
            cout<<"=========="<<endl;
       }
       else if(guessWrong ==6)
       {
            cout<<" +-----+"<<endl;
            cout<<" |     |"<<endl;
            cout<<" O     |"<<endl;
            cout<<"/|)    |"<<endl;
            cout<<"/ )    |"<<endl;
            cout<<"       |"<<endl;
            cout<<"=========="<<endl;
       }
      
}
