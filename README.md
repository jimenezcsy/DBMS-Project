# DBMS-Project
# Google Doc Version: https://docs.google.com/document/d/1TG00R3ZInnQFA39LqRclsuUaBFJcjHqL48-ROokQV9Q/edit?usp=sharing
# Slide Presentation: https://docs.google.com/presentation/d/1YjIciIclYQxZ-mWiltSH8ZOLUdgvcUnecAs3v5vB5Tg/edit?usp=sharing

# Implemented Search Queries
Goal: Make a RPG database with Account, Player Character, Location, NPC, & Item entities. 

How much damage all items do - SELECT DISTINCT ITEM.i_damage from ITEM GROUP BY (ITEM.i_name); in doc

Search relationship to a NPC - SELECT RELATIONSHIP.enemy, RELATIONSHIP.supplier, RELATIONSHIP.enemy FROM RELATIONSHIP, NPC where RELATIONSHIP.npcid = NPC.id GROUP BY (NPC.name); in doc

Search an item according to their location - SELECT DISTINCT ITEM.i_name FROM ITEM, LOCATION where ITEM.locationname = LOCATION.lname GROUP BY (LOCATION.lname);
In doc

Return list of accounts and their player character - SELECT PCHAR.p_a_name, charname FROM PCHAR, ACCOUNT where PCHAR.p_a_name = ACCOUNT.acct_name;
In doc

Search Plants in each location - SELECT DISTINCT LOCATION.plant FROM LOCATION GROUP BY (LOCATION.lname); finished

 Player characters who are level 5 or higher - SELECT PCHAR.charname FROM PCHAR where PCHAR.level > 5;

 Accounts with ‘e’ in their email address - SELECT ACCOUNT.acct_name FROM ACCOUNT where ACCOUNT.email LIKE “%e%”;

 Enemy NPCS and their attack points - SELECT NPC.name, NPC.attack_pnts FROM NPC, RELATIONSHIP where RELATIONSHIP.npcid = NPC.id GROUP BY (RELATIONSHIP.enemy);

AVG of all player character EXP - SELECT AVG(PCHAR.EXP) FROM PCHAR;

 Sum of all player character max damage- SELECT SUM(PCHAR.MAXDAMAGE) from PCHAR;
