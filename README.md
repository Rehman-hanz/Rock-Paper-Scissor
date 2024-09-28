# Rock-Paper-Scissor
python simple game


	import random

    def get_user_choice():
	
		"""
	    Get the user's choice and ensure it's valid.
	    """
	 
		user_choice = input("Enter a choice (rock, paper, scissors): ").lower()
	    
		while user_choice not in ["rock", "paper", "scissors"]:
	    
			user_choice = input("Invalid choice. Please enter rock, paper, or scissors: ").lower()
	    
		return user_choice

	def get_computer_choice():
		    
			"""
		    Randomly select a choice for the computer.
		    """
		    
			choices = ["rock", "paper", "scissors"]
		    
			return random.choice(choices)
	
		def determine_winner(user_choice, computer_choice):
	    
		"""
	    Determine the winner based on the classic rules:
	    - Rock crushes Scissors
	    - Scissors cuts Paper
	    - Paper covers Rock
	    """
	    
		if user_choice == computer_choice:
	    
			return "tie"
	    
		elif (user_choice == "rock" and computer_choice == "scissors") or \
	    
			 (user_choice == "paper" and computer_choice == "rock") or \
	         
			 (user_choice == "scissors" and computer_choice == "paper"):
	        
			return "user"
	    else:
	    
			return "computer"

	def play_game():
	    
		"""
	    Play three rounds of Rock, Paper, Scissors and keep track of the score.
	    """
	    
		user_score = 0
	    
		computer_score = 0
	    
		rounds = 3
	
	    for _ in range(rounds):
	    
			user_choice = get_user_choice()
	        
			computer_choice = get_computer_choice()
	        
			print(f"\nYou chose {user_choice}, computer chose {computer_choice}.")
	        
			
	  		winner = determine_winner(user_choice, computer_choice)
	        
			if winner == "user":
	        
				print("You win this round!")
	            
				user_score += 1
	        
			elif winner == "computer":
	        
				print("Computer wins this round!")
	            
				computer_score += 1
	        
			else:
	        
				print("This round is a tie!")
	
	        print(f"Score: You {user_score} - {computer_score} Computer\n")
	
	    	if user_score > computer_score:
	    
			print("Congratulations! You won the game!")
	    
		elif computer_score > user_score:
	    
			print("Computer wins the game! Better luck next time.")
	    
		else:
	    
			print("The game is a tie!")
	if __name__ == "__main__":
	
 		play_game()


















 
