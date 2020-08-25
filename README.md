# Poker Hands

![](https://a1s.unicdn.net/polopoly_fs/1.696321.1595491081!/image/1470891313.jpg)

## Rules: 

* **Royal Flush**

A straight flush is a hand that contains five cards of sequential rank, all of the same suit, but starting from 10 to Ace, such as A♥ K♥ Q♥ J♥ 10♥ . It ranks first and above four of a kind.

* **Straight Flush**

A straight flush is a hand that contains five cards of sequential rank, all of the same suit, such as Q♥ J♥ 10♥ 9♥ 8♥ . It ranks below five of a kind and above four of a kind

* **Four of a kind**

Four of a kind, also known as quads, is a hand that contains four cards of one rank and one card of another rank, such as 9♣ 9♠ 9♦ 9♥ J♥ . It ranks below a straight flush and above a full house.

* **Full house**

A full house is originally called a full hand, is a hand that contains three cards of one rank and two cards of another rank, such as 3♣ 3♠ 3♦ 6♣ 6♥. It ranks below four of a kind and above a flush.

* **Flush**

A flush is a hand that contains five cards all of the same suit, not all of sequential rank, such as K♣ 10♣ 7♣ 6♣ 4♣. It ranks below a full house and above a straight.

* **Straight**

A straight is a hand that contains five cards of sequential rank, not all of the same suit, such as 7♣ 6♠ 5♠ 4♥ 3♥. It ranks below a flush and above three of a kind

* **Three of a Kind**

Three of a kind, also known as trips or a set, is a hand that contains three cards of one rank and two cards of two other ranks, such as 2♦ 2♠ 2♣ K♠ 6♥. It ranks below a straight and above two pair.


* **Two Pair**

Two pair is a hand that contains two cards of one rank, two cards of another rank and one card of a third rank (the kicker), such as J♥ J♣ 4♣ 4♠ 9♥. It ranks below three of a kind and above one pair.

* **One Pair**

One pair, or simply a pair, is a hand that contains two cards of one rank and three cards of three other ranks (the kickers), such as 4♥ 4♠ K♠ 10♦ 5♠. It ranks below two pair and above high card.

* **High Card**

High card, also known as no pair or simply nothing, is a hand that does not fall into any other category, such as K♥ J♥ 8♣ 7♦ 4♠. It ranks below one pair.


# Program

## TASK 1: USING ZIP, LAMBDA & MAP

    def card_deck( _list: list, suits: list=['spades', 'clubs', 'hearts', 'diamonds']) -> list:
        '''
        This func returns a list of card deck
            Input: 
                _list: list of values
                suits: list of suits
            Returns:
                List of Card Deck
        '''
        all_suits(suits) 
        _suits = [s for i in _list for s in suits ]
        _vals = [v for s in suits for v in _list]
        return list(zip(_suits, _vals))
        
        
 ## TASK 2: WITHOUT USING ZIP, MAP & LAMBDA
 
     def create_deck(vals: list, suits: list) -> list:
        '''
        This function creates a deck of cards without using Zip, Map & Lambda function
            Input:
                List of Values and List of Suits
            Returns:
                list of card deck
        '''
        validate_suits_vals_len(suits, vals)
        card_deck = []
        for i in range(52):
            tup = (vals[i], suits[i])
            card_deck.append(tup)
        validate_card_deck(card_deck)
        return card_deck


## TASK 3: POKER WINNER
      
    def find_the_winner(cardset1: list, cardset2: list)-> str:
        '''
        This Func takes in two set of cards of length 3,4,5 and returns the winning set of cards i.e winner
            Input: 2 List of cards
            Returns: String 
        '''

        validate_same_num_cards(cardset1, cardset2)
        validate_num_cards_range(cardset1, cardset2)
        validate_same_cards(cardset1, cardset2)

        poker1, ph1 = Poker(cardset1).poker_hand()
        poker2, ph2 = Poker(cardset2).poker_hand()

        print(f'poker1: {poker1}, {ph1}')
        print(f'poker2: {poker2}, {ph2}')

        if poker1 > poker2:
            return 'Poker1 Wins!'
        elif poker2 > poker1:
            return 'Poker2 Wins!'
        else:
            return 'Tie b/w Poker1 & Poker2!'
            
            
*Note: Poker() is user-defined class which is in session6.py and poker_hand() is one of its method.

# TEST CASES


## README TEST CASES
test_readme_exists()
test_readme_contents()
test_readme_proper_description()
test_readme_file_for_formatting()

## FILE TEST CASES
test_function_name_had_cap_letter()
test_class_name_had_cap_letter()

## PROGRAM TEST CASES
test_suit_val_len()
test_card_deck()
test_invalid_input()
test_diff_num_cards()
test_out_of_range_cards()
test_diff_cardset()
test_valid_suits()
test_full_house()
test_two_pair()
test_results()
test_royal_flush_result()
test_straight_flush_result()
test_four_of_a_kind_result()
test_full_house_result()
test_flush_result()
test_straight_result()
test_three_of_a_kind_result()
test_two_pair_result()
test_one_pair_result()
test_20()
test_annotations()
test_docstrings()


