# Swiss Tournament System
This project is a tournament system based on the Swiss Pairing method. The Swiss Pairing method pairs players in each round that are equally (same number of wins) or nearly equal (closest number of wins) to each other. Each player in the each match is assigned the following points:

  - 3 points for a win
  - 1 point for a draw
  - 0 points for a loss

In the event that there are an odd number of players a bye will be assigned to one of the players in the round. A bye counts as a win and 3 points are awarded.

## Requirements
- Python 2.7
- PostgreSQL

## Contents
- tournament.sql - contains the table, view and function definitions
- tournament.py - contains definitions for the functions required by the Swiss pairing system
- tournament_test.py - contains a series of tests to check if the tournament.py functions are working correctly
- play_tournament.py - allows a dummy tournament to be run which selects the winners of each match at random

## Instructions
In order to use this project the database and tables will need to be setup, which can be done by running the tournament.sql file to create the database and tables. Once the database has been setup the play_tournament.py or tournament_test.py can be run.

### Creating the Database
To create the database, tables, views and functions use the following command:

        psql -f tournament.sql

###Running tournament_test.py
To run the tournament_test.py script run the following command:

        python tournament_test.py

### Running play_tournament.py
To see a simulated / dummy tournament run the following command:
        
        python play_tournament.py

Notes:
 
- players can be added or removed by editing the play_tournament.py script