# Poker-Hand-Sorter

A poker hand consists of a combination of five playing cards, ranked in the following ascending order:

| Rank  | Combination     | Description                                                   |
|-------|-----------------|---------------------------------------------------------------|
| 1     | High card       | Highest value card                                            |
| 2     | Pair            | Two cards of same value                                       |
| 3     | Two pairs       | Two different pairs                                           |
| 4     | Three of a kind | Three cards of the same value                                 |
| 5     | Straight        | All five cards in consecutive value order                     |
| 5     | Flush           | All five cards having the same suit                           |
| 7     | Full house      | Three of a kind and a Pair                                    |
| 8     | Four of a kind  | Four cards of the same value                                  |
| 9     | Straight flush  | All five cards in consecutive value order, with the same suit |
| 10    | Royal Flush     | Ten, Jack, Queen, King and Ace in the same suit               |

The cards are valued in the order: 2, 3, 4, 5, 6, 7, 8, 9, 10, Jack, Queen, King, Ace*

* For this exercise, Ace is considered high only. (i.e. cannot be used as a low card below 2 in a
straight).

Suits are: Diamonds (D), Hearts (H), Spades (S), Clubs (C)

## File despcriptions

**poker-hands.txt**

It is a test file containing 500 entries (games) between 2 players. Example:

9C 9D 8D 7C 3C 2S KD TH 9H 8H

Each line is read via STDIN and it will consist of 10 cards. Each card is represented by 2 characters - the value
and the suit. The first 5 cards in the line have been dealt to Player 1 (9C to 3C), the last 5 cards in the line
belong to Player 2 (2S to 8H).

**final_card_game.py**

This file is very well documented for the ease of understanding my code. In a nutshell the file does the following:

It first reads the data line by line from 'poker-hands.txt' via STDIN. It then splits it into two lists of hands one for player 1 and the other for player2.
It than compares the rank of each player's poker hand. The player with the higher rank wins the game. However, if the rank happens to be the same: for example, if both players have a pair of Jacks, then highest cards in each hand are compared; if the highest cards tie then the next highest cards are compared, and so on.

## Instructions

Download/Clone this repository onto your local machine. In your command line type the following:

**$ cat poker-hands.txt | python final_card_game.py**

Since 'shebang' line is also included in the 'final_card_game.py' therefore you can also type the following to see my results

**$ chmod +x final_card_game.py**

**$ cat poker-hands.txt | ./final_card_game.py**

## Expected Output

The output will be a dictionary summarising the number of games won by Player 1 and Player2.

{'Player1': 263, 'Player2': 237}


