using System;
class HelloWorld {
   static int number, guess=0;
   static string np2, np1;
  static void Main() {
     
     
    
    Console.WriteLine(" ");
    Console.WriteLine(" -----GUESS IT,TO WIN IT-----");
    ShowMyInitials(); 
    Console.WriteLine(" ----------------------------");
    Console.WriteLine("GAME 1\n    1st Guesser = Player 2\n ");
    Console.WriteLine(" ----------------------------");
    PlayGame1();
    Console.WriteLine("\n\n ----------------------------");
    Console.WriteLine("\n GAME 2\n    2nd Guesser = Player 1\n ");
    Console.WriteLine(" ----------------------------");
    PlayGame2();
    Console.WriteLine("\n\n ----------------------------");
    Console.WriteLine("\n GAME 3\n    3rd Guesser = Player 2\n ");
    Console.WriteLine(" ----------------------------");
    PlayGame3Final();
   
  }
  
  static void ShowMyInitials(){
    int n =7;
    
  for (int i=1; i<=n; i++){
           for (int j=1; j<=n; j++){
           if (i==1 || i==n ||j==1){
          Console.Write(" x");
        }
        else{
          Console.Write("  ");
        }}
    Console.Write("  ");
        for(int j=1; j<=n; j++){
            if(j==1 || (( i==1 || i==n || i==n/2+1) && j<=n-1)){
                Console.Write("x ");
            }
            else if(i!=1 && i!=n && j==n){
                Console.Write("x ");
            }
            else{
                 Console.Write("  ");
            }}
             Console.Write("\n");
}}
   static void PlayGame1(){
       
      int guessCount =0;
      int guessLimit=3;
      bool outofGuesses =false;
      bool playAgain = true;
      string response; 
      
        Console.Write("Enter Player 1's Name: ");
        np1=Console.ReadLine();
        Console.Write("Enter the number you want to be guess: ");
        number=Convert.ToInt32(Console.ReadLine());
        Console.WriteLine("\n\nDone! Now, it's time for Player 2 to guess it!\nLets start the game!\n");
     
        Console.Write("Enter Player 2's Name: ");
        np2=Console.ReadLine();
       
       
       while(playAgain)
        {       
            guess = 0;
            response = "";
        {
      while (guess != number && !outofGuesses)
                {
                if(guessCount<guessLimit)
                   {
                   Console.Write(np2+", type your guess number: ");
                   guess=Convert.ToInt32(Console.ReadLine());
                    
                    if (guess > number)
                    {
                        Console.WriteLine("Incorrect! "+guess+" is to high!");
                    }
                    else if (guess < number)
                    {
                        Console.WriteLine("Incorrect! "+guess+" is to low!");
                    }
                    guessCount++;
                    }
                else
                    {
                    outofGuesses =true;
                   }
                   }
                   }
                   if(outofGuesses)
                   {
                    Console.WriteLine("\n ANSWER: " + number);
                   Console.Write("\nSORRY, YOU LOSE THE GAME!\n Player1-1          Player2-0");
                   
                   }
                   else{Console.Write("\nCONGRATS, YOU WIN THE GAME!\nPlayer1-0          Player2-1");}
                
                  Console.WriteLine("\n\nLet's move on to the next round. type 'YES' to continue.");
                  response = Console.ReadLine();
                  response = response.ToUpper();

                  if (response == "YES")
                  {
                    playAgain = false;
                  }
                  else
                  {
                    playAgain = true;
                  }
                  }

                
   }
   static void PlayGame2(){
       
      int guessCount =0;
      int guessLimit=3;
      bool outofGuesses =false;
      bool playAgain = true;
      string response; 
      
        
        Console.Write("Enter the number you want to be guess,"+np2+": ");
        number=Convert.ToInt32(Console.ReadLine());
        Console.WriteLine("\n\nDone! Now, it's time for Player 1 to guess it!\nLets start the game!\n");
     
        
       
       while(playAgain)
        {       guess = 0;

                response = "";
                {
      while (guess != number && !outofGuesses)
                {
                    if(guessCount<guessLimit)
                    {
                         Console.Write(np1+", type your guess number: ");
                         guess=Convert.ToInt32(Console.ReadLine());
                    
                     if (guess > number)
                    {
                        Console.WriteLine("Incorrect! "+guess+" is to high!");
                    }
                    else if (guess < number)
                    {
                        Console.WriteLine("Incorrect! "+guess+" is to low!");
                    }
                    guessCount++;
                    }
                   else{
                       outofGuesses =true;
                   }
}
                }
                if(outofGuesses)
                {
                Console.WriteLine("\n ANSWER: " + number);
                 Console.Write("\nSORRY, YOU LOSE THE GAME!\n Player1-0          Player2-2");
                 
                }
                else{Console.Write("\nCONGRATS, YOU WIN THE GAME!\nPlayer1-1          Player2-1");}
                

                Console.WriteLine("\n\nLet's get on to the final round. Type 'YES' to continue.");
                response = Console.ReadLine();
                response = response.ToUpper();

                if (response == "YES")
                {
                    playAgain = false;
                }
                else
                {
                    playAgain = true;
                }}}  
   static void PlayGame3Final(){
       
      int guessCount =0;
      int guessLimit=3;
      bool outofGuesses =false;
      bool playAgain = true;
      string response; 
      
        
        Console.Write("Enter the number you want to be guess,"+np1+": ");
        number=Convert.ToInt32(Console.ReadLine());
        Console.WriteLine("\n\nDone! Now, it's time for Player 1 to guess it!\nLets start the game!\n");
     
        
       
       while(playAgain)
        {       guess = 0;

            response = "";
                {
      while (guess != number && !outofGuesses)
                {
                    if(guessCount<guessLimit)
                    {
                         Console.Write(np2+", type your guess number: ");
                         guess=Convert.ToInt32(Console.ReadLine());
                    
                     if (guess > number)
                    {
                        Console.WriteLine("Incorrect! "+guess+" is to high!");
                    }
                    else if (guess < number)
                    {
                        Console.WriteLine("Incorrect! "+guess+" is to low!");
                    }
                    guessCount++;
                    }
                   else{
                       outofGuesses =true;
                   }
}
                }
                if(outofGuesses)
                {
                 Console.WriteLine("\n ANSWER: " + number);
                 Console.Write("\nSORRY, YOU LOSE!\n Player1- 2        Player2- 1");
                 Console.WriteLine("\n\n CONGRATULATIONS PLAYER 1, YOU WIN THE GUESSING GAME!" );
                }
                else{Console.Write("\nCONGRATS, YOU WIN!\n Player1- 0          Player2- 3");
                    Console.WriteLine("\n\n CONGRATULATIONS PLAYER 2, YOU WIN THE GUESSING GAME!" );
                }
                Console.Write("Just type 'NO' to exit the Game, Thanks For Playing!: ");
                response = Console.ReadLine();
                response = response.ToUpper();

                if (response == "Y")
                {
                    playAgain = true;
                }
                else
                {
                    playAgain = false;
                }
            }
                }}    

    
