#	Task 2: CHAT BOT

##### Table of Contents:

* [Task 2: CHAT BOT](#Task 2: CHAT BOT)
  * [What is the difference between C and C++](#What is the difference between C and C++)
    * [C Programming Language](#C Programming Language)
    * [C++ Programming Language](#C++ Programming Language)
    * [Differences between C and C++](#Differences between C and C++)
  * [What is this operator (`::`) in C++? What is it's use?](#What is this operator (`::`) in C++? What is it's use?)
  * [Are C++ strings mutable or immutable?](#Are C++ strings mutable or immutable?)
  * [What are namespaces in C++ and what is their use?](#What are namespaces in C++ and what is their use?)
  * [Write a program in C++ to print the following pattern:](#Write a program in C++ to print the following pattern:)
  * [Why do you think C++ is the right choice to begin programming?](#Why do you think C++ is the right choice to begin programming?)





## Task 2A:

#### What is the difference between C and C++

##### C Programming Language

​		C programming language is a middle-level programming language, developed by Dennis Ritchie. This language is widely used for system programming in implementing operating systems and embedded system applications. 

##### C++ Programming Language

C++ programming language was developed by Bjarne Stroustrup. This programming language contains the features of C programming language and certain other features as well. It encapsulates high and low-level
programming language features. It was designed for resource-constrained software and large systems, with  high performance, efficiency and flexibility of use.

##### Differences between C and C++

| No.  |                              C                               |                             C++                              |
| :--: | :----------------------------------------------------------: | :----------------------------------------------------------: |
|  1.  |       C does not support object oriented programming.        |  C++ is basically an object oriented programming language.   |
|  2.  |              C cannot run all the codes of C++.              |                C++ can run all the codes of C                |
|  3.  |                   C contains 32 keywords.                    |                  C++ contains 52 keywords.                   |
|  4.  |               C is a function-driven language.               |              C++ is an object-driven language.               |
|  5.  |       Namespace features are not present inside the C.       |      Namespace is used in C++ to avoid name collisions.      |
|  6.  |               C supports built-in data types.                |    C++ supports both built-in & user-defined data types.     |
|  7.  |         Reference variables are not supported by C.          |          Reference variables are supported by C++.           |
|  8.  |            C mainly focuses on method or process.            |           C++ mainly focuses on objects and data.            |
|  9.  |            C does not support exception handling.            |               C++ supports Exception handling.               |
| 10.  |  scanf and printf functions are used for input/output in C.  |      Cin>> and cout<< are used for input/output in C++.      |
| 11.  |           C follows Top-Down programming approach.           |         C++ follows bottom-up programming approach.          |
| 12.  |           The file extension of a C program is .c            |          The file extension of C++ program is .cpp           |
| 13.  |    C is not compatible with other programming languages.     | C++ is compatible with other generic programming languages.  |
| 14.  | In this, the variable should be defined at the beginning of the program. | This allows you to declare variables anywhere in the function. |
| 15.  |     It allows multiple declaration of global variables.      | It does not allow multiple declaration of global variables.  |
| 16.  |        It supports primitive and built-in data types.        |          It supports string and boolean data types.          |

***

#### What is this operator (`::`) in C++? What is it's use?

​	The ***scope resolution operator*** [`::`] is used to qualify hidden names so that the user can still use them. A very common example is that they are used as `std::` in front of `cout` and `cin` functions. This basically means that inside the `iostream` standard library in C++, the developers have made a *namespace*  called `std` and put the functions like `cin`, `cout`, `string`, etc into the *namespace*. The main function of the scope resolution operator **::** is that it is used to identify the  identifiers used in different scope so that the functions don’t get extracted from other files and thus they would not get complicated.

Some examples of the use of *scope resolution*:

> class-name :: identifier
>
> namespace :: identifier

```c++
#include <iostream>

int main()
{
    std::cout<<"HIII";
    return 0;
}
```



***

#### Are C++ strings mutable or immutable?

```c++
#include <iostream>

int main()
 {
    std::string a = "grape";
    a[0] = 'd';
    std::cout<<a;
    return 0;
}
```

The output of the program is ***"drape"***.

​	This is a simple program in C++ which shows that the string in C++ are mutable. Initially the string was "grape" and after the program executed the string now is "drape".Thus we see that the strings in c++ are mutable. 

But string literals are not mutable. Any collection of characters in double quotes is a string literal. This string is stored in a read-only part of memory. Since we can't write to this memory, these strings are immutable. But any string in std::string form are mutable. Thus we see that the strings in C++ are mutable unless they are not declared as `std::string const` or they are not string literals.

Example for immutability of *string literal*:

```c++
#include <iostream>

int main()
 {
    const std::string a = "grape";
    a[0] = 'd';
    std::cout<<a;
    return 0;
}
```

This program shows an error since here *"grape"* is a string literal and not a string. 

***

#### What are namespaces in C++ and what is their use?

A namespace is a declarative region that provides a scope to the identifiers (the names of types, functions, variables, etc) inside it. Namespaces are used to organize code into logical groups and to prevent name collisions that can occur especially when the code base includes multiple libraries. Identifiers outside the namespace can access the members by using the fully qualified name for each identifier, for example using `std::string` or a using Directive for all the identifiers in the namespace `using namespace std;`. Code in header files should always use the fully qualified namespace name.

Example:

***

#### Write a program in C++ to print the following pattern:

```c++
    *
   ***
  *****
 *******
*********
```

The required code to print the following pattern:

```c++
#include <iostream>

int main()
{
    int height;
    std::cout<<"Enter the size of the pyramid required : ";
    std::cin>>height;
    int space;
    for (int i=1;i<=height;i++)
    {
        for (space = i; space <height; space++)
        {
            std::cout<<" ";
        }
        {
            for (int j = 1; j<=(2*i-1);j=j+1)
                std::cout<<"*";
            std::cout<<std::endl;
        }
    }
    return 0;
}
```

The output of the program is as follows:

![a](https://imgur.com/4w5bJEd.png)



***

#### Why do you think C++ is the right choice to begin programming?

C++ has complex syntax, lots of rules and it is an old language. It may not be the right choice to begin for programming because it is tougher than other programming languages. Programming languages like *python*, *Ruby* has much simpler syntax and not many rules to be followed while programming. But since C++ has the complex syntax and many rules, it will be easier to learn other programing languages. Since we have learnt a harder programming language, we can easily learn the programming languages that are much more simpler than C++.

***

***

***

