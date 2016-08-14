/*•••••••••••••••••••••••••••••••••••••••••••••••••••••Hangman••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••
______________________________________________________________________________________________________________________________
CLASS DEFINITION :-
-----------------
  >BASE:-
  		Inherits all difficult classes and it helps in reducing the number of objects
  >ENGLISH:-
       ^CLASS TYPE                  CLASS NAME     CLASS OBJECT		INHERITED BY	MEMBER FUNCTIONS
         1.ENGLISH-> EASY            1.ENGEC        1.EE			 <>ENGMOD		 <>ENGEC_1(),ENGEC_2(),ENGEC_3()
         2.ENGLISH-> MODRATE         2.ENGMOD       2.EM			 <>ENGDIFF		 <>ENGMOD_1(),ENGMOD_2(),ENGMOD_3()
         3.ENGLIDH-> DIFFICULT       3.ENGDIFF      3.ED			 <>null			 <>ENGDIFF_1(),ENGDIFF_2(),ENGDIFF_3()
  >HINDI:-
       ^CLASS TYPE                   CLASS NAME     CLASS OBJECT	INHERITED BY	MEMBER FUNCTION
         1.HINDI-> EASY               1.HINEC        1.HE			 <>HINMOD		 <>HINEC_1(),HINEC_2(),HINEC_3()
         2.HINDI-> MODRATE            2.HINMOD       2.HM			 <>HINDIFF		 <>HINMOD_1(),HINMOD_2(),HINMOD_3()
         3.HINDI-> DIFFICULT          3.HINDIFF      3.HD			 <>null			 <>HINDIFF_1(),HINDIFF_2(),HINDIFF_3()
  >TAMIL:-
       ^CLASS TYPE                  CLASS NAME     CLASS OBJECT		INHERITED BY	MEMBER FUNCTION
         1.TAMIL-> EASY              1.TAMEC         1.TE			 <>TAMMOD		 <>TAMEC_1(),TAMEC_2(),TAMEC_3()
         2.TAMIL-> MODRATE           2.TAMMOD        2.TM			 <>TAMDIFF		 <>TAMMOD_1(),TAMMOD_2(),TAMMOD_3()
         3.TAMIL-> DIFFICULT         3.TAMDIFF       3.TD			 <>null			 <>TAMDIFF_1(),TAMDIFF_2(),TAMDIFF_3()
FUNCTION DEFINITION :-
--------------------
    > INT MAIN() ->
		RECIVES ONLY BASIC INFORMATION FOR EDITING THE GAME
	> RETURN_RANDOM_VALUE() ->
		IT WILL RETURN AN INTIGER LESSS THAN 4 SO THAT AN WORD IS RANDOMLY CHOOSED
	> W() ->
		THIS FUNCTION IS USED TO EXECUTE THE MAIN PART OF THE PROGRAM WHICH WILL
		ACCEPT THE VALUES FROM USER ND CHECKS IF THAT VARIABLER IS PRESENT IN
		THE LETTER BY USING "letterfill()"
	> LETTERFILL()->
	    Take a one character guess and the secret word, and fill in the unfinished
   	    guessword. Returns number of characters matched.Also, returns zero if the character
   	    is already guessed.
______________________________________________________________________________________________________________________________*/
#include <iostream>
#include <cstdlib>
#include <ctime>
#include<conio.h>
#include"word.cpp"
#include"random.cpp"
using namespace std;
/* HINDI MOVIES */ 
class HINEC
{
      public:
			 int HINEC_1();
			 int HINEC_2();
			 int HINEC_3();
};
class HINMOD:public HINEC
{
      public:
			 int HINMOD_1();
			 int HINMOD_2();
			 int HINMOD_3();
};
class HINDIFF:public HINMOD
{
      public:
			 int HINDIFF_1();
			 int HINDIFF_2();
			 int HINDIFF_3();
};
/* ENGLISH MOVIES */
class ENGEC
{
      public:
			 int ENGEC_1();
			 int ENGEC_2();
			 int ENGEC_3();
};
class ENGMOD:public ENGEC
{
      public:
			 int ENGMOD_1();
			 int ENGMOD_2();
			 int ENGMOD_3();
};
class ENGDIFF:public ENGMOD
{
      public:
			 int ENGDIFF_1();
			 int ENGDIFF_2();
			 int ENGDIFF_3();
};
/* TAMIL MOVIES */
class TAMEC
{
      public:
			 int TAMEC_1();
			 int TAMEC_2();
			 int TAMEC_3();
};
class TAMMOD:public TAMEC
{
      public:
			 int TAMMOD_1();
			 int TAMMOD_2();
			 int TAMMOD_3();
};
class TAMDIFF:public TAMMOD
{
      public:
			 int TAMDIFF_1();
			 int TAMDIFF_2();
			 int TAMDIFF_3();
};
//class which contains all the objects
class base:public ENGDIFF,public HINDIFF,public TAMDIFF
{}B;
int main()
{
     system("cls");
     int option;
     cout<<"\n\n\n\n\n\n\n\n\n\n\t\t do u want to enter the world of gamming (y/n): \n\t\t\t\t\t";
     char yrn;
     cin>>yrn;
     system("cls");
/* THIS IF STATMENT IS THE BASE IF THE PROGRAM WHICH DECIDES WEATHER THE PROGRAM CAN START OR NOT */

	 do
	 {
	 system("cls");
	 if(tolower(yrn)=='y')
     {
        cout<<"\n\n\n\n\t\t\t    WELCOME TO THE WORLD OF CINEMA GAMMING \n";
        cout<<"\t 1.ENTER THE GAME"<<endl;
        cout<<"\t 2.RULS"<<endl;
        cout<<"\t 3.EXIT GAME"<<endl;
        cout<<"Please enter any option so we may help you: ";
        cin>>option;
        int language,difficulty;
        system("cls");
        switch(option)
        {
/* THIS " CASE 1: " ENTERS WITH A DEFAULT LANGUAGE OF TAMIL AND WITH MODRATE DIFFICULTY */
                      case 1:
                                        char t;
											cout<<"select language:";
                                        	cout<<"\n\t\t 1.Tamil";
                                        	cout<<"\n\t\t 2.English";
                                        	cout<<"\n\t\t 3.Hindi";
                                        	cout<<"\n\t\t 4.Go Back";
                                        	cout<<"\n\t Enter any option:";
                                        	cin>>language;
                                        	switch(language)
                                       		{
                                        	     case 1:
                                             	{
                                                  system("cls");
                                                  cout<<"choose difficulty level:";
                                                  cout<<"\n\t\t 1.Easy";
                                                  cout<<"\n\t\t 2.Modrate";
                                                  cout<<"\n\t\t 3.Difficult";
                                                  int choice1;
                                                  cout<<"\n\t Enter any option:";
                                                  cin>>choice1;
                                                  switch(choice1)
                                                  {
                                                       case 1:B.TAMEC_1();
                                                          break;
                                                       case 2:B.TAMMOD_1();
                                                          break;
                                                       case 3:B.TAMDIFF_1();
                                                          break;
                                                  }
                                                  break;
                                             	}
                                             	case 2:
                                             	{
                                                  system("cls");
                                                  cout<<"choose difficulty level:";
                                                  cout<<"\n\t\t 1.Easy";
                                                  cout<<"\n\t\t 2.Modrate";
                                                  cout<<"\n\t\t 3.Difficult";
                                                  int choice1;
                                                  cout<<"\n\t Enter any option:";
                                                  cin>>choice1;
                                                  switch(choice1)
                                                  {
                                                       case 1:B.ENGEC_1();
                                                          break;
                                                       case 2:B.ENGMOD_1();
                                                          break;
                                                       case 3:B.ENGDIFF_1();
                                                          break;
                                                  }
                                                  break;
                                             	}
                                             	case 3:
                                             	{
                                                  system("cls");
                                                  cout<<"choose difficulty level:";
                                                  cout<<"\n\t\t 1.Easy";
                                                  cout<<"\n\t\t 2.Modrate";
                                                  cout<<"\n\t\t 3.Difficult";
                                                  int choice1;
                                                  cout<<"\n\t Enter any option:";
                                                  cin>>choice1;
                                                  switch(choice1)
                                                  {
                                                       case 1:B.HINEC_1();
                                                          break;
                                                       case 2:B.HINMOD_1();
                                                          break;
                                                       case 3:B.HINDIFF_1();
                                                          break;
                                                  }
                                                  break;
                                             	}
                                        	}
                      break;
/* THIS " CASE 2: "  USED TO DISPLAY RULES*/
                      case 2:
                      		system("cls");
                      		cout<<"Hangman (game)"<<endl<<"Hangman is a paper and pencil guessing game for two or more players."<<endl<<" One player thinks of a word, phrase or sentence and the other tries to guess it by suggesting letters or numbers, within a certain number of guesses."<<endl<<"Overview"<<endl<<"The word to guess is represented by a row of dashes, representing each letter of the word."<<endl<<" In most variants, proper nouns, such as names, places, and brands, are not allowed."<<endl<<" If the guessing player suggests a letter which occurs in the word, the other player writes it in all its correct positions."<<endl<<" If the suggested letter or number does not occur in the word, the other player draws one element of a hanged man stick figure as a tally mark."<<endl<<"The player guessing the word may, at any time, attempt to guess the whole word."<<endl<<" If the word is correct, the game is over and the guesser wins."<<endl<<" Otherwise, the other player may choose to penalize the guesser by adding an element to the diagram."<<endl<<" On the other hand, if the other player makes enough incorrect guesses to allow his opponent to complete the diagram, the game is also over, this time with the guesser losing."<<endl<<" However, the guesser can also win by guessing all the letters or numbers that appears in the word, thereby completing the word, before the diagram is completed."<<endl<<"Variants"<<endl<<"As the name of the game suggests, the diagram is designed to look like a hanging man."<<endl<<" Although debates have arisen about the questionable taste of this picture,"<<endl<<"[1] it is still in use today."<<endl<<" A common alternative for teachers is to draw an apple tree with ten apples, erasing or crossing out the apples as the guesses are used up."<<endl<<"The exact nature of the diagram differs; some players draw the gallows before play and draw parts of the man's body (traditionally the head, then the torso, then the arms and legs one by one)."<<endl<<" Some players begin with no diagram at all,"<<endl<<" and drawing the individual elements of the gallows as part of the game, effectively giving the guessing players more chances."<<endl<<" The amount of detail on the man can also vary, affecting the number of chances."<<endl<<" Some players include a face on the head, either all at once or one feature at a time."<<endl<<"Some modifications to game play (house rules) to increase the difficulty level are sometimes implemented, such as limiting guesses on high-frequency consonants and vowels."<<endl<<" Another alternative is to give the definition of the word; this can be used to facilitate the learning of a foreign language.";
                      		cout<<endl<<"Example game"<<endl<<"The following example game illustrates a player trying to guess the word hangman using a strategy based solely on letter frequency."<<endl<<"Word:	_ _ _ _ _ _ _"<<endl<<"Guess:	E"<<endl<<"Misses:	"<<endl<<"Word:	_ _ _ _ _ _ _"<<endl<<"Guess:	T"<<endl<<"Misses:	e"<<endl<<"Word:	_ _ _ _ _ _ _"<<endl<<"Guess:	A"<<endl<<"Misses:	e,t"<<endl<<"Word:	_ A _ _ _ A _"<<endl<<"Guess:	N"<<endl<<"Misses:	e,t"<<endl<<"Word:	_ A N _ _ A N"<<endl<<"Guess:	H"<<"Misses:	e,t"<<endl<<"Word:	H A N _ _ A N"<<endl<<"Guesser loses - the answer was HANGMAN.";
                            getch();
                           break;
/* THIS " CASE 3: "THIS " CASE 5: " ENTERS AN EXIT PAGE WHERE THE USER GETS IRRITATED BECAUSE OF TOO MANY QUESTIONS ASKED AND WILL PLAY THE GAME */
                      case 3:
                           system("cls");
                                        cout<<"\n\n\n\n\t\t\t R Ew Sure OF EXTING :( (y/n)";
                                        cin>>yrn;
                                        if(tolower(yrn)=='y')
                                           cout<<"\t\t\t\tBBBBB YYYYY EEEEE";
                                        break;
                }
     }
 	 }while(option>0 && option<3);
     return 0;
}
int HINDIFF::HINDIFF_1()
             {
                   system("cls");
                   string words[] =
                   {
                           "HINDI311",
                           "HINDI312",
                           "HINDI313"
                   };
//choose and copy a word from array of words randomly
                   int n=return_random_value();;
                   int j=w(words[n]);
				   if (j==1)
                   {
					 cout << endl << "GO to NEXT RoUNd ;) " ;
                     getch();
                     B.HINDIFF_2();
                   }
                   return 0;
             }
int HINDIFF::HINDIFF_2()
             {
                   system("cls");
                   string words[] =
                   {
                           "HINDI321",
                           "HINDI322",
                           "HINDI323"
                   };
//choose and copy a word from array of words randomly
                   int n=return_random_value();;
                   int j=w(words[n]);
				   if (j==1)
                   {
					 cout << endl << "GO to NEXT RoUNd ;) " ;
                     getch();
                     B.HINDIFF_3();
                   }
                   return 0;
             }
int HINDIFF::HINDIFF_3()
             {
                   system("cls");
                   string words[] =
                   {
                           "HINDI331",
                           "HINDI332",
                           "HINDI333"
                   };
//choose and copy a word from array of words randomly
                   int n=return_random_value();;
                   int j=w(words[n]);
				   if (j==1)
                   {
					 cout << endl << "YOU HAVE SUCCESSFULLY COMPLETED THE HINDI DIFF ROUND :D " ;
                     getch();
                   }
                   return 0;
             }
int HINMOD::HINMOD_1()
             {
                   system("cls");
                   string words[] =
                   {
                           "HINDI211",
                           "HINDI212",
                           "HINDI213"
                   };
//choose and copy a word from array of words randomly
                   int n=return_random_value();
                   int j=w(words[n]);
				   if (j==1)
                   {
					 cout << endl << "GO to NEXT RoUNd ;) " ;
                     getch();
                     B.HINMOD_2();
                   }
                   return 0;
             }
int HINMOD::HINMOD_2()
             {
                   system("cls");
                   string words[] =
                   {
                           "HINDI221",
                           "HINDI222",
                           "HINDI223"
                   };
//choose and copy a word from array of words randomly
                   int n=return_random_value();
                   int j=w(words[n]);
				   if (j==1)
                   {
					 cout << endl << "GO to NEXT RoUNd ;) " ;
                     getch();
                     B.HINMOD_3();
                   }
                   return 0;
             }
int HINMOD::HINMOD_3()
             {
                   system("cls");
                   string words[] =
                   {
                           "HINDI231",
                           "HINDI232",
                           "HINDI233"
                   };
//choose and copy a word from array of words randomly
                   int n=return_random_value();
                   int j=w(words[n]);
				   if (j==1)
                   {
					 cout << endl << "YOU HAVE SUCCESSFULLY COMPLETED THE HINDI MOD ROUND  \n YOU CAN GO TO HINDI DIFFICULT ROUND :D " ;
                     getch();
                     B.HINDIFF_1();
                   }
                   return 0;
             }
int HINEC::HINEC_1()
             {
                   system("cls");
                   string words[] =
                   {
                           "HINDI111",
                           "HINDI112",
                           "HINDI113"
                   };
//choose and copy a word from array of words randomly
                   int n=return_random_value();
                   int j=w(words[n]);
				   if (j==1)
                   {
					 cout << endl << "GO to NEXT RoUNd ;) " ;
                     getch();
                     B.HINEC_2();
                   }
                   return 0;
             }
int HINEC::HINEC_2()
             {
                   system("cls");
                   string words[] =
                   {
                           "HINDI121",
                           "HINDI122",
                           "HINDI123"
                   };
//choose and copy a word from array of words randomly
                   int n=return_random_value();
                   int j=w(words[n]);
				   if (j==1)
                   {
					 cout << endl << "GO to NEXT RoUNd ;) " ;
                     getch();
                     B.HINEC_3();
                   }
                   return 0;
             }
int HINEC::HINEC_3()
             {
                   system("cls");
                   string words[] =
                   {
                           "HINDI131",
                           "HINDI132",
                           "HINDI133"
                   };
//choose and copy a word from array of words randomly
                   int n=return_random_value();
                   int j=w(words[n]);
				   if (j==1)
                   {
					 cout << endl << "YOU HAVE SUCCESSFULLY COMPLETED THE HINDI EC ROUND  \n YOU CAN GO TO HINDI MOD ROUND :D " ;
                     getch();
                     B.HINMOD_1();
                   }
                   return 0;
			}
int ENGDIFF::ENGDIFF_1()
             {
                   system("cls");
                   string words[] =
                   {
                           "ENGLISH311",
                           "ENGLISH312",
                           "ENGLISH313"
                   };
//choose and copy a word from array of words randomly
                   int n=return_random_value();
                   int j=w(words[n]);
				   if (j==1)
                   {
					 cout << endl << "GO to NEXT RoUNd ;) " ;
                     getch();
                     B.ENGDIFF_2();
                   }
                   return 0;
             }
int ENGDIFF::ENGDIFF_2()
             {
                   system("cls");
                   string words[] =
                   {
                           "ENGLISH321",
                           "ENGLISH322",
                           "ENGLISH323"
                   };
//choose and copy a word from array of words randomly
                   int n=return_random_value();
                   int j=w(words[n]);
				   if (j==1)
                   {
					 cout << endl << "GO to NEXT RoUNd ;) " ;
                     getch();
                     B.ENGDIFF_3();
                   }
                   return 0;
             }
int ENGDIFF::ENGDIFF_3()
             {
                   system("cls");
                   string words[] =
                   {
                           "ENGLISH331",
                           "ENGLISH332",
                           "ENGLISH333"
                   };
//choose and copy a word from array of words randomly
                   int n=return_random_value();
                   int j=w(words[n]);
				   if (j==1)
                   {
					 cout << endl << "YOU HAVE SUCCESSFULLY COMPLETED THE ENGLISH DIFF ROUND :D " ;
                     getch();
                   }
                   return 0;
             }
int ENGMOD::ENGMOD_1()
             {
                   system("cls");
                   string words[] =
                   {
                           "ENGLISH211",
                           "ENGLISH212",
                           "ENGLISH213"
                   };
//choose and copy a word from array of words randomly
                   int n=return_random_value();
                   int j=w(words[n]);
				   if (j==1)
                   {
					 cout << endl << "GO to NEXT RoUNd ;) " ;
                     getch();
                     B.ENGMOD_2();
                   }
                   return 0;
             }
int ENGMOD::ENGMOD_2()
             {
                   system("cls");
                   string words[] =
                   {
                           "ENGLISH221",
                           "ENGLISH222",
                           "ENGLISH223"
                   };
//choose and copy a word from array of words randomly
                   int n=return_random_value();;
                   int j=w(words[n]);
				   if (j==1)
                   {
					 cout << endl << "GO to NEXT RoUNd ;) " ;
                     getch();
                     B.ENGMOD_3();
                   }
                   return 0;
             }
int ENGMOD::ENGMOD_3()
             {
                   system("cls");
                   string words[] =
                   {
                           "ENGLISH231",
                           "ENGLISH232",
                           "ENGLISH233"
                   };
//choose and copy a word from array of words randomly
                   int n=return_random_value();;
                   int j=w(words[n]);
				   if (j==1)
                   {
					 cout << endl << "YOU HAVE SUCCESSFULLY COMPLETED THE ENGLISH MOD ROUND  \n YOU CAN GO TO ENGLISH DIFFICULT ROUND :D " ;
                     getch();
                     B.ENGDIFF_1();
                   }
                   return 0;
             }
int ENGEC::ENGEC_1()
             {
                   system("cls");
                   string words[] =
                   {
                           "ENGLISH111",
                           "ENGLISH112",
                           "ENGLISH113"
                   };
//choose and copy a word from array of words randomly
                   int n=return_random_value();;
                   int j=w(words[n]);
				   if (j==1)
                   {
					 cout << endl << "GO to NEXT RoUNd ;) " ;
                     getch();
                     B.ENGEC_2();
                   }
                   return 0;
             }
int ENGEC::ENGEC_2()
             {
                   system("cls");
                   string words[] =
                   {
                           "ENGLISH121",
                           "ENGLISH122",
                           "ENGLISH123"
                   };
//choose and copy a word from array of words randomly
                   int n=return_random_value();
                   int j=w(words[n]);
				   if (j==1)
                   {
					 cout << endl << "GO to NEXT RoUNd ;) " ;
                     getch();
                     B.ENGEC_3();
                   }
                   return 0;
             }
int ENGEC::ENGEC_3()
             {
                   system("cls");
                   string words[] =
                   {
                           "ENGLISH131",
                           "ENGLISH132",
                           "ENGLISH133"
                   };
//choose and copy a word from array of words randomly
                   int n=return_random_value();;
                   int j=w(words[n]);
				   if (j==1)
                   {
					 cout << endl << "YOU HAVE SUCCESSFULLY COMPLETED THE ENGLISH EC ROUND  \n YOU CAN GO TO ENGLISH MOD ROUND :D " ;
                     getch();
                     B.ENGMOD_1();
                   }
                   return 0;
             }
int TAMDIFF::TAMDIFF_1()
             {
                   system("cls");
                   string words[] =
                   {
                           "TAMIL311",
                           "TAMIL312",
                           "TAMIL313"
                   };
//choose and copy a word from array of words randomly
                   int n=return_random_value();
                   int j=w(words[n]);
				   if (j==1)
                   {
					 cout << endl << "GO to NEXT RoUNd ;) " ;
                     getch();
                     B.TAMDIFF_2();
                   }
                   return 0;
             }
int TAMDIFF::TAMDIFF_2()
             {
                   system("cls");
                   string words[] =
                   {
                           "TAMIL321",
                           "TAMIL322",
                           "TAMIL323"
                   };
//choose and copy a word from array of words randomly
                   int n=return_random_value();
                   int j=w(words[n]);
				   if (j==1)
                   {
					 cout << endl << "GO to NEXT RoUNd ;) " ;
                     getch();
                     B.TAMDIFF_3();
                   }
                   return 0;
             }
int TAMDIFF::TAMDIFF_3()
             {
                   system("cls");
                   string words[] =
                   {
                           "TAMILI331",
                           "TAMIL332",
                           "TAMIL333"
                   };
//choose and copy a word from array of words randomly
                   int n=return_random_value();
                   int j=w(words[n]);
				   if (j==1)
                   {
					 cout << endl << "YOU HAVE SUCCESSFULLY COMPLETED THE TAMIL DIFF ROUND :D " ;
                     getch();
                   }
                   return 0;
             }
int TAMMOD::TAMMOD_1()
             {
                   system("cls");
                   string words[] =
                   {
                           "TAMIL211",
                           "TAMIL212",
                           "TAMIL213"
                   };
//choose and copy a word from array of words randomly
                   int n=return_random_value();
                   int j=w(words[n]);
				   if (j==1)
                   {
					 cout << endl << "GO to NEXT RoUNd ;) " ;
                     getch();
                     B.TAMMOD_2();
                   }
                   return 0;
             }
int TAMMOD::TAMMOD_2()
             {
                   system("cls");
                   string words[] =
                   {
                           "TAMIL221",
                           "TAMIL222",
                           "TAMIL223"
                   };
//choose and copy a word from array of words randomly
                   int n=return_random_value();
                   int j=w(words[n]);
				   if (j==1)
                   {
					 cout << endl << "GO to NEXT RoUNd ;) " ;
                     getch();
                     B.TAMMOD_3();
                   }
                   return 0;
             }
int TAMMOD::TAMMOD_3()
             {
                   system("cls");
                   string words[] =
                   {
                           "TAMIL231",
                           "TAMIL232",
                           "TAMIL233"
                   };
//choose and copy a word from array of words randomly
                   int n=return_random_value();
                   int j=w(words[n]);
				   if (j==1)
                   {
					 cout << endl << "YOU HAVE SUCCESSFULLY COMPLETED THE TAMIL MOD ROUND  \n YOU CAN GO TO HINDI TAMIL ROUND :D " ;
                     getch();
                     B.TAMDIFF_1();
                   }
                   return 0;
             }
int TAMEC::TAMEC_1()
             {
                   system("cls");
                   string words[] =
                   {
                           "TAMIL111",
                           "TAMIL112",
                           "TAMIL113"
                   };
//choose and copy a word from array of words randomly
                   int n=return_random_value();
                   int j=w(words[n]);
				   if (j==1)
                   {
					 cout << endl << "GO to NEXT RoUNd ;) " ;
                     getch();
                     B.TAMEC_2();
                   }
                   return 0;
             }
int TAMEC::TAMEC_2()
             {
                   system("cls");
                   string words[] =
                   {
                           "TAMIL121",
                           "TAMIL122",
                           "TAMIL123"
                   };
//choose and copy a word from array of words randomly
                   int n=return_random_value();
                   int j=w(words[n]);
				   if (j==1)
                   {
					 cout << endl << "GO to NEXT RoUNd ;) " ;
                     getch();
                     B.TAMEC_3();
                   }
                   return 0;
             }
int TAMEC::TAMEC_3()
             {
                   system("cls");
                   string words[] =
                   {
                           "TAMIL131",
                           "TAMIL132",
                           "TAMIL133"
                   };
//choose and copy a word from array of words randomly
                   int n=return_random_value();
                   int j=w(words[n]);
				   if (j==1)
                   {
					 cout << endl << "YOU HAVE SUCCESSFULLY COMPLETED THE TAMIL EC ROUND  \n YOU CAN GO TO TAMIL MOD ROUND :D " ;
                     getch();
                     B.TAMMOD_1();
                   }
                   return 0;
         }
