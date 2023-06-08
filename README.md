# Steam_Database_Model

This is a model of the gamestore Steam's database, it's not perfect because I had little time making it before the deadline and had to sacrifice anything that wasn't required of the model like a relation that keeps track of the game transfers (gifts) or a table that keeps track of achievement and so on and so forth.

It has 10 tables: user, friend_user, group, group_user, game, game_user, company, game_company, sale and game_sale.

friend_user, group_user, game_user, game_user and game_sale are relations that link two other tables to each other, I couldn't keep every game a user had in the user table because a user can have multiple games and having multiple games would mean there would be more than one row with the same steam_id which would inhibit me from using steam_id as the primary key of the user relation. The same applies to the other tables listed.

For the DML commands in order to generate random data I first tried using Mockaroo but as it didn't provide enough options for randomly generated data (like gamer usernames or fake video game company names) I resorted to using ChatGPT.

I would tell GPT-4 something like this:
    
