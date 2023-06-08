# Steam_Database_Model

This is a model of the gamestore Steam's database, it's not perfect because I had little time making it before the deadline and had to sacrifice anything that wasn't required of the model like a relation that keeps track of the game transfers (gifts) or a table that keeps track of achievement and so on and so forth.

It has 10 tables: user, friend_user, group, group_user, game, game_user, company, game_company, sale and game_sale.

friend_user, group_user, game_user, game_user and game_sale are relations that link two other tables to each other, I couldn't keep every game a user had in the user table because a user can have multiple games and having multiple games would mean there would be more than one row with the same steam_id which would inhibit me from using steam_id as the primary key of the user relation. The same applies to the other tables listed.

For the DML commands in order to generate random data I first tried using Mockaroo but as it didn't provide enough options for randomly generated data (like gamer usernames or fake video game company names) I resorted to using ChatGPT.

I would tell GPT-4 something like this:
            Give me 20 INSERT commands for this database table: user(steam_id, username, birth_date, reg_date)
            steam_id should be a randomly generated string with a maximum length of 32 characters that's unique to each row.
            username should be a name that sounds like a gamer's username.
            birth_date should be a date in yyyy/mm/dd format.
            reg_date should be a adte that's after the day Steam (the online video game store) was founded.
            
A it would give me 20 INSERT commands. After inputing the data in two tables that are supposed to be connected to each other (like user and game) I would write the INSERT commands of the third table connecting them to each other (like game_user) mostly by hand because the data in this table can't be randomly generated and has to come from already existing data from other tables so I would tell GPT-4 to give me 20 INSERT commands just like before but I would tell it to pick certain fields out of a list. For example I would give it the list of all the steam_ids in the user table and tell it to pick the steam_id in the game_user table from that list.
