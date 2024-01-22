# betting_game.py

import random

def simulate_round():
    # Simulate the outcome of a round
    outcome = random.choice(["Red", "Green"])
    return outcome

def determine_winners(participant_bets, actual_outcome):
    # Determine the winners based on participant bets and actual outcome
    winners = [participant for participant, bet in participant_bets.items() if bet == actual_outcome]
    return winners

# Example usage
if __name__ == "__main__":
    # Simulate a round
    actual_outcome = simulate_round()

    # Participants and their bets (you can replace this with GitHub usernames and comments)
    participant_bets = {
        "Participant1": "Red",
        "Participant2": "Green",
        "Participant3": "Green",
        # Add more participants and their bets as needed
    }

    # Determine winners
    winners = determine_winners(participant_bets, actual_outcome)

    # Display results
    print(f"Actual Outcome: {actual_outcome}")
    print("Winners:")
    for winner in winners:
        print(f"- {winner}")
