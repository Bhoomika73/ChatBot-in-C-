# Task 2 : CHAT BOT

### Task 2B :

##### CHAT BOT...

A chatbot is a very basic program that can be written in any language. A chatbot basically takes a string or a phrase in natural language (like English) and responds to that phrase. The given task is to make a simple chatbot in C++ which when given an English phrase responds to it.



Below is a program to create a simple ***CHATBOT***.

###### Instructions:

* This is a very simple chat bot that can **answer a very limited number of questions**.
* The bot will answer to the question **only if the question is stored in the bot program**.
* The question must be asked in **UPPERCASE**.
* **DO NOT use any CHARACTERS** like "?", "!", ".", etc while asking the questions.

> Example : If u want to ask "What is your name?" You must input "WHAT IS YOUR NAME"

* If you want to leave the conversation **type *"EXIT"***.

```c++
#include <iostream>
#include <process.h>
#include <stdio.h>
#include <conio.h>
#include <stdlib.h>
#include <time.h>
#include <string>

using namespace std;

int main()
{
    string L1[] = {"CUTIEPIE","WHAT IS YOURS","WHAT WOULD U LIKE IT TO BE"};
    string L2[] = {"ONE OF THE 7 DAYS OF THE WEEK","UR FAVORITE DAY","THE MOST BORING DAY","SLEEPY DAY"};
    string L3[] = {"2+2","4","IM NOT UR CALCULATOR","IDK","HOW MUCH DO U WANT IT TO BE"};
    string L4[] = {"BHOOMIKA","OBVIOUSLY NOT U","A RANDOM HUMAN BEING","UR BETTER HALF"};
    string L5[] = {"HURRY UP...ITS TODAY","WHENEVER U R FREE","WHEN INDIA WINS","AFTER U FINISH UR HOMEWORK"};
    string L6[] = {"I CAN IRRITATE","WHAT DO U WANT ME TO DO","I CAN GO INTO THE BLACKHOLE UNHARMED"};
    string L7[] = {"AGE IS JUST A NUMBER","YOUNGER THAN U THINK I AM","SECRET","TAKE A GUESS","FORGOT!!!"};
    string L8[] = {"HELLO!!","WELCOME TO THE CONVERSATION","HOPE U WILL HAVE A GREAT TIME SPEAKING WITH ME"};
    string L0[] = {"I CANNOT UNDERSTAND U","SORRY!!!","U R NOT FOLLOWING INSTRUCTIONS"};
    string L01[]= {"THANK U FOR SPENDING TIME WITH ME","HOPE U ENJOYED SPEAKING WITH ME","THANK U, C U SOON"};

    string user;
    cout<<"Hii....Welcome to the conversation,\n"<<"USER : ";
    while (user != "EXIT")
    {
        int a;
        getline(cin,user);
        srand(time(NULL));

        if (user == "WHAT IS YOUR NAME")
        {
            a = rand()%3;
            cout<<"BOT : "<<(L1[a])<<"\n"<<"USER : ";
        }
        else if (user == "WHICH DAY IS TODAY")
        {
            a = rand()%4;
            cout<<"BOT : "<<(L2[a])<<"\n"<<"USER : ";
        }
        else if (user == "WHAT IS 2+2")
        {
            a = rand()%5;
            cout<<"BOT : "<<(L3[a])<<"\n"<<"USER : ";
        }
        else if (user == "WHO IS YOUR CREATOR")
        {
            a = rand()%4;
            cout<<"BOT : "<<(L4[a])<<"\n"<<"USER : ";
        }
        else if (user == "WHEN IS THE NEXT MATCH OF INDIA")
        {
            a = rand()%4;
            cout<<"BOT : "<<(L5[a])<<"\n"<<"USER : ";
        }
        else if (user == "WHAT MORE CAN YOU DO")
        {
            a = rand()%3;
            cout<<"BOT : "<<(L6[a])<<"\n"<<"USER : ";
        }
        else if (user == "WHAT IS YOUR AGE")
        {
            a = rand()%5;
            cout<<"BOT : "<<(L7[a])<<"\n"<<"USER : ";
        }
        else if (user == "EXIT")
        {
            a = rand()%3;
            cout<<"BOT : "<<L01[a]<<"\n";
            break;
        }
        else if (user == "HELLO")
        {
            a = rand()%3;
            cout<<"BOT : "<<L8[a]<<"\n"<<"USER : ";
        }
        else
        {
            a = rand()%3;
            cout<<"BOT : "<<(L0[a])<<"\n"<<"USER : ";
        }
    }
}
```



Following are the outputs of the *CHAT BOT* program.

> Output1 : 

![a](https://imgur.com/Q4xZHaJ.png)



> Output2 : 

![b](https://imgur.com/wGISUBm.png)



#### Design Approach :

This program was to create a simple **"ChatBot"** which could answer a few questions asked by the user. Only the questions that were stored in the program can be answered. First all the possible answers to the questions are stored in different **lists**. Then the input is taken from the user. Then I have used a **while** loop. This loop terminates when the user inputs **EXIT**. Inside the loop, I have used **if-else if-else** command. This command checks if the input from the user matches with any of the questions that are previously determined. if it matches then using **random** command, any string is taken from the corresponding list and is given as the output. If the input from user is **EXIT**, then using the **Break** command the program comes out of the while loop. If the input from user does not match any of the predefined questions then I have given a separate output for that as well.