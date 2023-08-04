# ROCK-PAPER-SCISSORS
ROCK.PAPER.SCISSORS. THE AGE OLD GAME OF CHANCE YOU PLAY WITH FRIENDS. TODAY YOU WILL BE PLAYING AGAINST A VIRTUAL OPPONENT. 




<h1>FLOWCHART AND UI</h1>
Below shows a visual outline of the pathway to complete the game and the choices made along the way. 
<img src="https://imgur.com/zODgsFQ.png"/>

<br />

<h2>RAW CODE</h2>

    #include <iostream> 
    #include <cstdlib> 
    #include <ctime> 
    const int ROCK = 1;
    const int PAPER = 2;
    const int SCISSORS = 3;

    using namespace std; 

    int main()
    {  
     srand((unsigned int)time(NULL));                    
     int player_choice = 0;
    int ai_choice = 0;
    bool tie = false; 
    char play_again;

    do 
    {
           cout << "Choose an option" << endl;
     cout << "1 = Rock" << endl;
     cout << "2 = Paper"<< endl;
     cout << "3 = Scissors" << endl;
     cout << " Selection: "; 
      cin >> player_choice;

      cout << endl; 
      ai_choice = (rand() % 3) + 1;

      if (ai_choice == ROCK)
      {
        cout << " AI chose ROCK." << endl;
      }
      else if (ai_choice == PAPER)
      {
        cout << "AI chose PAPER." << endl;
      }
      else if (ai_choice == SCISSORS)
      {
        cout << "AI chose SCISSORS." << endl;
      }

      tie = false; 
      // Display section 
      if (player_choice == ai_choice)
      {
    tie = true;
        cout << " Tie Game!! Play Again." << endl;
      }
      else if (player_choice == ROCK && ai_choice == SCISSORS)
      {
        cout << "ROCK beats SCISSORS. You Win!" << endl;
      }
      else if (player_choice == ROCK && ai_choice == PAPER)
      {
        cout << "PAPER beats ROCK. You lose!" << endl;
      }
      else if (player_choice == PAPER && ai_choice == ROCK)
      {
        cout << "PAPER beats ROCK. You Win!" << endl;
      }
      else if (player_choice == PAPER && ai_choice == SCISSORS)
      {
        cout << "SCISSORS beats PAPER. You Lose!" << endl;
      }
      else if (player_choice == SCISSORS && ai_choice == PAPER)
      {
        cout << "SCISSORS beats PAPER. You Win!" << endl;
      }
      else if (player_choice == SCISSORS && ai_choice == ROCK)
      {
        cout << "ROCK beats SCISSORS. You Lose!" << endl;
      }

      cout << endl;
      if (!tie)
      {
        cout << "Wanna play again? (Y/N): ";
        cin >> play_again;
        if (play_again == 'Y' || play_again == 'y')
        { 
        tie = true;
        }
      }
      
    } while (tie);
  
  
    return 0;   
    }

PASTE THIS CODE INTO YOUR C++ COMPILER OF CHOICE AND GIVE THE GAME A TRY. 



<h2> OUTPUT VISUAL</h2>
<img src="https://imgur.com/M4SALf1.png"/>


