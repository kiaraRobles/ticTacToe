#include <windows.h>
#include <iostream>
using namespace std;

// Initialize a two dimensional array	 
char square[2][10] = { {'0', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' '},  // Row 0 as the visible squares 
                       {'0', '1', '2', '3', '4', '5', '6', '7', '8', '9'}}; // Row 1 for the saved off inputs necessary to compute the win 

void universe();
int check();
int main(){

	int  input = 1, turn = 1, progress = -1;
	char tic, play, p1, p2;

/*===========================================================================/
                                Game Intro
============================================================================*/
	
	cout << "Welcome to the two-player two-dimentional" << endl;					
	cout << "Tic-Tac-Toe Universe";
    	Sleep(300);
    	cout << "!";
    	Sleep(200);
    	cout << "!";
    	Sleep(100);
    	cout << "!" << endl << endl;
    	Sleep(500);
	
	// Prompt player with the choice to play
	cout << "Do you want to play?(y/n): ";	
	cin  >> play;
	
	if (play == 'y' || play == 'Y'){
	
		system("cls");
	
		cout << "The board looks like this:" << endl << endl;
		Sleep(300);
		cout << "     |     |     " << endl;
		cout << "  " << square[1][1] << "  |  " << square[1][2] << "  |  " << square[1][3] << endl;
		cout << "_____|_____|_____" << endl;
		cout << "     |     |     " << endl;
		cout << "  " << square[1][4] << "  |  " << square[1][5] << "  |  " << square[1][6] << endl;
		cout << "_____|_____|_____" << endl;
		cout << "     |     |     " << endl;
		cout << "  " << square[1][7] << "  |  " << square[1][8] << "  |  " << square[1][9] << endl;
		cout << "     |     |     " << endl << endl;
		Sleep(300);
		cout << "Each player will enter a number 1-9 to place their piece on the board." << endl;
		cout << "Make sence? Press 'y' to play.";
		cin  >> play;
		
		if (play == 'y' || play == 'Y'){

/*===========================================================================/
                           Game Status Fuction
============================================================================*/
	    	  	  	  
					do{
						universe();
			
						// Establish turn
						if (turn % 2)   											  
  							turn = 1;
					
					
						if(turn == 1){	// Assign 'X' and 'O' values to each player
  						tic = 'X';
				
						cout << "Player " << turn << ", enter a number(1-9): ";	// Prompt player one to make a move
			    		cin  >> p1;
				
						switch (p1){	 	 	 	 	 	 	 	 	 	 				
							case '1': (square[0][1] = tic) && (square[1][1] = tic); break;
							case '2': (square[0][2] = tic) && (square[1][2] = tic); break;
							case '3': (square[0][3] = tic) && (square[1][3] = tic); break;
							case '4': (square[0][4] = tic) && (square[1][4] = tic); break;
							case '5': (square[0][5] = tic) && (square[1][5] = tic); break;
							case '6': (square[0][6] = tic) && (square[1][6] = tic); break;
							case '7': (square[0][7] = tic) && (square[1][7] = tic);	break;
							case '8': (square[0][8] = tic) && (square[1][8] = tic); break;
							case '9': (square[0][9] = tic) && (square[1][9] = tic); break;
							default: cout << "Invalid choice. Please try again.";
								turn = 2;
								Sleep(2000);
 							}	 	 
						}
					else if(turn == 2){
  						tic = 'O';
								
						cout << "Player " << turn << ", enter a number(1-9): ";	// Prompt player two to make a move			
			  	  		cin  >> p2;
				
						switch (p2){	 	 	 	 	 	 	 	 	 	 	 	 		
							case '1': (square[0][1] = tic) && (square[1][1] = tic); break;
							case '2': (square[0][2] = tic) && (square[1][2] = tic); break;
							case '3': (square[0][3] = tic) && (square[1][3] = tic); break;
							case '4': (square[0][4] = tic) && (square[1][4] = tic); break;
							case '5': (square[0][5] = tic) && (square[1][5] = tic); break;
							case '6': (square[0][6] = tic) && (square[1][6] = tic); break;
							case '7': (square[0][7] = tic) && (square[1][7] = tic);	break;
							case '8': (square[0][8] = tic) && (square[1][8] = tic); break;
							case '9': (square[0][9] = tic) && (square[1][9] = tic); break;
							default: cout << "Invalid choice. Please try again.";
								turn = 1;
								Sleep(2000);
 						}	 	 	 	 
					}
					else if (turn > 2){
						turn = 1;
					}
						progress = check();
						turn++;
					}while(progress == -1 && (play == 'y' || play == 'Y'));
		   
		universe();
	
		if(progress == 1){
			// Anounces winner
			cout << "Player " << --turn << " wins!" << endl;	
		}
		else{
			// Declares a tie
			cout << "Tie Game" << endl; 
		}
	}
	}
	// Out of game output
	else{	
		cout << "Okay. Bye, Felicia." << endl; 
	}
	
	return 0;
	}
	
/*===========================================================================/
                           Current Board Fuction
============================================================================*/

void universe(){

	system("cls");
	cout << "The Tic-Tac-Toe Universe" << endl << endl;

	cout << "     |     |     " << endl;
	cout << "  " << square[0][1] << "  |  " << square[0][2] << "  |  " << square[0][3] << endl;

	cout << "_____|_____|_____" << endl;
	cout << "     |     |     " << endl;

	cout << "  " << square[0][4] << "  |  " << square[0][5] << "  |  " << square[0][6] << endl;

	cout << "_____|_____|_____" << endl;
	cout << "     |     |     " << endl;

	cout << "  " << square[0][7] << "  |  " << square[0][8] << "  |  " << square[0][9] << endl;

	cout << "     |     |     " << endl << endl;
}

/*===========================================================================/
                           Game Status Fuction
============================================================================*/
// -1 = in progress
//  0 = game over with tie
//  1 = game over with winner

int check(){

	if (square[1][1] == square[1][2] && square[1][2] == square[1][3])
		return 1;
	else if (square[1][4] == square[1][5] && square[1][5] == square[1][6])
		return 1;
	else if (square[1][7] == square[1][8] && square[1][8] == square[1][9])
		return 1;
	else if (square[1][1] == square[1][4] && square[1][4] == square[1][7])
		return 1;
	else if (square[1][2] == square[1][5] && square[1][5] == square[1][8])
		return 1;
	else if (square[1][3] == square[1][6] && square[1][6] == square[1][9])
		return 1;
	else if (square[1][1] == square[1][5] && square[1][5] == square[1][9])
		return 1;
	else if (square[1][3] == square[1][5] && square[1][5] == square[1][7])
		return 1;
	else if (square[1][1] != '1' && square[1][2] != '2' && square[1][3] != '3' 
             && square[1][4] != '4' && square[1][5] != '5' && square[1][6] != '6' 
             && square[1][7] != '7' && square[1][8] != '8' && square[1][9] != '9')
		return 0;
	else
		return -1;
}
