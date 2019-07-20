# Assignment3
Assignment 3 is here 
Refactor Source code:

#include<iostream>
#include<dominion.c>
#include<interface.c>
using namespace std;
int cardEfect(int cardName);
int main()
{
	int numPlayers; //number of players
	int outpostPlayed;
	int outpostTurn;
	int whoseTurn;
	int phase;
	int numActions; /* Starts at 1 each turn */
	int coins; /* Use as you see fit! */
	int numBuys; /* Starts at 1 each turn */
	int playedCardCount;
	int MAX_PLAYERS;
	string kingdomCards[10];
	if (numPlayers > MAX_PLAYERS || numPlayers < 2)
	{
		return -1;
	}
	//check selected kingdom cards are different
	for (i = 0; i < 10; i++)
	{
		for (j = 0; j < 10; j++)
		{
			if (j != i && kingdomCards[j] == kingdomCards[i])
			{
				return -1;
			}
		}
	}
	//set number of Curse cards
	if (numPlayers == 2)
	{
		state->supplyCount[curse] = 10;
	}
	else if (numPlayers == 3)
	{
		state->supplyCount[curse] = 20;
	}
	else
	{
		state->supplyCount[curse] = 30;
	}
	//set number of Victory cards
	if (numPlayers == 2)
	{
		state->supplyCount[estate] = 8;
		state->supplyCount[duchy] = 8;
		state->supplyCount[province] = 8;
	}
	else
	{
		state->supplyCount[estate] = 12;
		state->supplyCount[duchy] = 12;
		state->supplyCount[province] = 12;
	}
	return 0;
}
int cardEfect(int cardName)
{
	string option;
	cin >> option;
	switch (option)
		case baron;
	{
		//draw player hands
		for (i = 0; i < numPlayers; i++)
		{
			//initialize hand size to zero
			state->handCount[i] = 0;
			state->discardCount[i] = 0;
			//draw 5 cards
			// for (j = 0; j < 5; j++) 
			// {
			// drawCard(i, state);
			// } 
		break;
	}
	case minion;
	{
		//draw player hands
		for (i = 0; i < numPlayers; i++)
		{
			//initialize hand size to zero
			state->handCount[i] = 0;
			state->discardCount[i] = 0;
			//draw 5 cards
			// for (j = 0; j < 5; j++) 
			// {
			// drawCard(i, state);
			// } 
		break;
	}
	case ambassador:
	{
		//draw player hands
		for (i = 0; i < numPlayers; i++)
		{
			//initialize hand size to zero
			state->handCount[i] = 0;
			state->discardCount[i] = 0;
			//shuffle player decks
			for (i = 0; i < numPlayers; i++)
			{
				if (shuffle(i, state) < 0)
				{
					return -1;
				}
			}

			//draw 5 cards
			// for (j = 0; j < 5; j++) 
			// {
			// drawCard(i, state);
			// } 
		break;
	}
	case tribute:
	{
		//draw player hands
		for (i = 0; i < numPlayers; i++)
		{
			//initialize hand size to zero
			state->handCount[i] = 0;
			state->discardCount[i] = 0;
			//draw 5 cards
			// for (j = 0; j < 5; j++) 
			// {
			// drawCard(i, state);
			// } 
			//shuffle player decks
			for (i = 0; i < numPlayers; i++)
			{
				if (shuffle(i, state) < 0)
				{
					return -1;
				}
			}

		break;
	}
	case mine:
	{
		//draw player hands
		for (i = 0; i < numPlayers; i++)
		{
			//initialize hand size to zero
			state->handCount[i] = 0;
			state->discardCount[i] = 0;
			//draw 5 cards
			 for (j = 0; j < 5; j++) 
			 {
			 drawCard(i, state);
			 }
			 //shuffle player decks
			 for (i = 0; i < numPlayers; i++)
			 {
				 if (shuffle(i, state) < 0)
				 {
					 return -1;
				 }
			 }

		break;
	}
	{
	default:
		break;
	}
}
