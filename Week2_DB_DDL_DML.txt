/* Create movie_ratings database */
CREATE DATABASE movie_ratings;

/* Use movie_ratings database */
USE movie_ratings;

/* Drop all movie_ratings database tables */
DROP TABLE movie_ratings.movie_info;
DROP TABLE movie_ratings.genre_info;
DROP TABLE movie_ratings.director_info;
DROP TABLE movie_ratings.actor_info;
DROP TABLE movie_ratings.movie_actor_map;
DROP TABLE movie_ratings.movie_genre_map;


/* Create movie_ratings.movie_info table */
CREATE TABLE movie_info
(
	ID INT(5) NOT NULL,
	TITLE VARCHAR(100),
	DIRECTOR_ID VARCHAR(10),
	RELEASE_DATE DATE,
	MINUTES INT(3),
	RATINGS INT(2),
	GROSS_INCOME DECIMAL(13, 2),
	PRIMARY KEY (ID)
)

/* Create movie_ratings.genre_info table */
CREATE TABLE genre_info
(
        ID INT(5) NOT NULL,
        NAME VARCHAR(100),
	PRIMARY KEY (ID)
)

/* Create movie_ratings.director_info table */
CREATE TABLE director_info
(
        ID INT(5) NOT NULL,
        NAME VARCHAR(100),
	PRIMARY KEY (ID)
)

/* Create movie_ratings.actor_info table */
CREATE TABLE actor_info
(
        ID INT(5) NOT NULL,
        NAME VARCHAR(100),
	PRIMARY KEY (ID)
)

/* Create movie_ratings.movie_cast_map table */
CREATE TABLE movie_actor_mp
(
        MOVIE_ID INT(5) NOT NULL,
        ACTOR_ID INT(5) NOT NULL
)

/* Create movie_ratings.movie_genre_map table */
CREATE TABLE movie_genre_map
(
        MOVIE_ID INT(5) NOT NULL,
        GENRE_ID INT(5) NOT NULL
)


/* Populate movie_ratings.movie_info table */
INSERT INTO movie_ratings.movie_info VALUES (1,	'War Dogs', 1, STR_TO_DATE('08/09/2016', '%m/%d/%Y'), 114, 3, 39.80);
INSERT INTO movie_ratings.movie_info VALUES (2,	'The Light Between Oceans', 2, STR_TO_DATE('09/02/16', '%m/%d/%Y'), 133, 5, 7.61);
INSERT INTO movie_ratings.movie_info VALUES (3,	'Hell or High Water (II)', 3, STR_TO_DATE('08/02/16', '%m/%d/%Y'), 102, 4, 19.82);
INSERT INTO movie_ratings.movie_info VALUES (4,	'Sully', 4, STR_TO_DATE('09/09/16', '%m/%d/%Y'), 96, 5, 35.51);
INSERT INTO movie_ratings.movie_info VALUES (5,	'The Legend of Tarzan',	5, STR_TO_DATE('06/30/16', '%m/%d/%Y'), 110, 3, 125.90);
INSERT INTO movie_ratings.movie_info VALUES (6,	'Don\'t Breathe', 6, STR_TO_DATE('08/25/16', '%m/%d/%Y'), 88, 2, 66.83);
INSERT INTO movie_ratings.movie_info VALUES (7,	'Mechanic Resurrection', 7, STR_TO_DATE('08/26/16', '%m/%d/%Y'), 98, 2, 16.95);
INSERT INTO movie_ratings.movie_info VALUES (8,	'Jason Bourne',	8, STR_TO_DATE('07/29/16', '%m/%d/%Y'), 123, 3, 156.98);
INSERT INTO movie_ratings.movie_info VALUES (9,	'Now You See Me 2', 9, STR_TO_DATE('06/10/16', '%m/%d/%Y'), 129, 4, 65.03);
INSERT INTO movie_ratings.movie_info VALUES (10, 'Morgan', 10, STR_TO_DATE('09/02/16', '%m/%d/%Y'), 92, 1, 0.00);
INSERT INTO movie_ratings.movie_info VALUES (11, 'Suicide Squad', 11, STR_TO_DATE('08/05/16', '%m/%d/%Y'), 123, 4, 307.41);
INSERT INTO movie_ratings.movie_info VALUES (12, 'Star Trek Beyond', 12, STR_TO_DATE('07/22/16', '%m/%d/%Y'), 122, 5, 150.89);
INSERT INTO movie_ratings.movie_info VALUES (13, 'Ghostbusters', 13, STR_TO_DATE('07/11/16', '%m/%d/%Y'), 116, 3, 124.96);
INSERT INTO movie_ratings.movie_info VALUES (14, 'Hands of Stone', 14, STR_TO_DATE('08/26/16', '%m/%d/%Y'), 111, 4, 1.75);
INSERT INTO movie_ratings.movie_info VALUES (15, 'Greater', 15, STR_TO_DATE('08/26/16', '%m/%d/%Y'), 130, 5, 0.63);


/* Populate movie_ratings.genre_info table */
INSERT INTO movie_ratings.genre_info VALUES (1, 'Action');
INSERT INTO movie_ratings.genre_info VALUES (2, 'Adventure');
INSERT INTO movie_ratings.genre_info VALUES (3, 'Animation');
INSERT INTO movie_ratings.genre_info VALUES (4, 'Biography');
INSERT INTO movie_ratings.genre_info VALUES (5, 'Comedy');
INSERT INTO movie_ratings.genre_info VALUES (6, 'Crime');
INSERT INTO movie_ratings.genre_info VALUES (7, 'Drama');
INSERT INTO movie_ratings.genre_info VALUES (8, 'Family');
INSERT INTO movie_ratings.genre_info VALUES (9, 'Fantasy');
INSERT INTO movie_ratings.genre_info VALUES (10, 'Film-Noir');
INSERT INTO movie_ratings.genre_info VALUES (11, 'History');
INSERT INTO movie_ratings.genre_info VALUES (12, 'Horror');
INSERT INTO movie_ratings.genre_info VALUES (13, 'Music');
INSERT INTO movie_ratings.genre_info VALUES (14, 'Musical');
INSERT INTO movie_ratings.genre_info VALUES (15, 'Mystery');
INSERT INTO movie_ratings.genre_info VALUES (16, 'Romance');
INSERT INTO movie_ratings.genre_info VALUES (17, 'Sci-Fi');
INSERT INTO movie_ratings.genre_info VALUES (18, 'Sport');
INSERT INTO movie_ratings.genre_info VALUES (19, 'Thriller');
INSERT INTO movie_ratings.genre_info VALUES (20, 'War');
INSERT INTO movie_ratings.genre_info VALUES (21, 'Western');


/* Populate movie_ratings.director_info table */
INSERT INTO movie_ratings.director_info VALUES (1, 'Todd Phillips');
INSERT INTO movie_ratings.director_info VALUES (2, 'Derek Cianfrance');
INSERT INTO movie_ratings.director_info VALUES (3, 'David Mackenzie');
INSERT INTO movie_ratings.director_info VALUES (4, 'Clint Eastwood');
INSERT INTO movie_ratings.director_info VALUES (5, 'David Yates');
INSERT INTO movie_ratings.director_info VALUES (6, 'Fede Alvarez');
INSERT INTO movie_ratings.director_info VALUES (7, 'Dennis Gansel');
INSERT INTO movie_ratings.director_info VALUES (8, 'Paul Greengrass');
INSERT INTO movie_ratings.director_info VALUES (9, 'Jon M. Chu');
INSERT INTO movie_ratings.director_info VALUES (10, 'Luke Scott');
INSERT INTO movie_ratings.director_info VALUES (11, 'David Ayer');
INSERT INTO movie_ratings.director_info VALUES (12, 'Justin Lin');
INSERT INTO movie_ratings.director_info VALUES (13, 'Paul Feig');
INSERT INTO movie_ratings.director_info VALUES (14, 'Jonathan Jakubowicz');
INSERT INTO movie_ratings.director_info VALUES (15, 'David Hunt');

/* Populate movie_ratings.actor_info table */
INSERT INTO movie_ratings.actor_info VALUES (1, 'Aaron Eckhart');
INSERT INTO movie_ratings.actor_info VALUES (2, 'Alexander Skarsgård');
INSERT INTO movie_ratings.actor_info VALUES (3, 'Alicia Vikander');
INSERT INTO movie_ratings.actor_info VALUES (4,	'Anya Taylor-Joy');
INSERT INTO movie_ratings.actor_info VALUES (5,	'Ben Foster');
INSERT INTO movie_ratings.actor_info VALUES (6,	'Chris Pine');
INSERT INTO movie_ratings.actor_info VALUES (7,	'Christian Stevens');
INSERT INTO movie_ratings.actor_info VALUES (8,	'Christoph Waltz');
INSERT INTO movie_ratings.actor_info VALUES (9,	'Christopher Severio');
INSERT INTO movie_ratings.actor_info VALUES (10,'Dale Dickey');
INSERT INTO movie_ratings.actor_info VALUES (11, 'Daniel Zovatto');
INSERT INTO movie_ratings.actor_info VALUES (12, 'Dave Franco');
INSERT INTO movie_ratings.actor_info VALUES (13, 'Dylan Minnette');
INSERT INTO movie_ratings.actor_info VALUES (14, 'Edgar Ramírez');
INSERT INTO movie_ratings.actor_info VALUES (15, 'Florence Clery');
INSERT INTO movie_ratings.actor_info VALUES (16, 'Gregg Weiner');
INSERT INTO movie_ratings.actor_info VALUES (17, 'Jane Levy');
INSERT INTO movie_ratings.actor_info VALUES (18, 'Jared Leto');
INSERT INTO movie_ratings.actor_info VALUES (19, 'Jason Statham');
INSERT INTO movie_ratings.actor_info VALUES (20, 'Jesse Eisenberg');
INSERT INTO movie_ratings.actor_info VALUES (21, 'Jessica Alba');
INSERT INTO movie_ratings.actor_info VALUES (22, 'Jonah Hill');
INSERT INTO movie_ratings.actor_info VALUES (23, 'Karl Urban');
INSERT INTO movie_ratings.actor_info VALUES (24, 'Kate Mara');
INSERT INTO movie_ratings.actor_info VALUES (25, 'Kate McKinnon');
INSERT INTO movie_ratings.actor_info VALUES (26, 'Kristen Wiig');
INSERT INTO movie_ratings.actor_info VALUES (27, 'Laura Linney');
INSERT INTO movie_ratings.actor_info VALUES (28, 'Leslie Easterbrook');
INSERT INTO movie_ratings.actor_info VALUES (29, 'Leslie Jones');
INSERT INTO movie_ratings.actor_info VALUES (30, 'Margot Robbie');
INSERT INTO movie_ratings.actor_info VALUES (31, 'Mark Ruffalo');
INSERT INTO movie_ratings.actor_info VALUES (32, 'Matt Damon');
INSERT INTO movie_ratings.actor_info VALUES (33, 'Melissa McCarthy');
INSERT INTO movie_ratings.actor_info VALUES (34, 'Michael Fassbender');
INSERT INTO movie_ratings.actor_info VALUES (35, 'Michael Parks');
INSERT INTO movie_ratings.actor_info VALUES (36, 'Michael Yare');
INSERT INTO movie_ratings.actor_info VALUES (37, 'Michelle Yeoh');
INSERT INTO movie_ratings.actor_info VALUES (38, 'Miles Teller');
INSERT INTO movie_ratings.actor_info VALUES (39, 'Neal McDonough');
INSERT INTO movie_ratings.actor_info VALUES (40, 'Rachel Weisz');
INSERT INTO movie_ratings.actor_info VALUES (41, 'Robert De Niro');
INSERT INTO movie_ratings.actor_info VALUES (42, 'Rory J. Saper');
INSERT INTO movie_ratings.actor_info VALUES (43, 'Rose Leslie');
INSERT INTO movie_ratings.actor_info VALUES (44, 'Rubén Blades');
INSERT INTO movie_ratings.actor_info VALUES (45, 'Stephen Lang');
INSERT INTO movie_ratings.actor_info VALUES (46, 'Steve Lantz');
INSERT INTO movie_ratings.actor_info VALUES (47, 'Tom Hanks');
INSERT INTO movie_ratings.actor_info VALUES (48, 'Tommy Lee Jones');
INSERT INTO movie_ratings.actor_info VALUES (49, 'Usher Raymond');
INSERT INTO movie_ratings.actor_info VALUES (50, 'Valerie Mahaffey');
INSERT INTO movie_ratings.actor_info VALUES (51, 'Vincent Cassel');
INSERT INTO movie_ratings.actor_info VALUES (52, 'Viola Davis');
INSERT INTO movie_ratings.actor_info VALUES (53, 'Will Smith');
INSERT INTO movie_ratings.actor_info VALUES (54, 'William Sterchi');
INSERT INTO movie_ratings.actor_info VALUES (55, 'Woody Harrelson');
INSERT INTO movie_ratings.actor_info VALUES (56, 'Zachary Quinto');
INSERT INTO movie_ratings.actor_info VALUES (57, 'Zoe Saldana');

/* Populate movie_ratings.movie_actor_map table */
INSERT INTO movie_ratings.movie_actor_map VALUE (1, 22);
INSERT INTO movie_ratings.movie_actor_map VALUE (1, 38);
INSERT INTO movie_ratings.movie_actor_map VALUE (1, 46);
INSERT INTO movie_ratings.movie_actor_map VALUE (1, 16);
INSERT INTO movie_ratings.movie_actor_map VALUE (2, 34);
INSERT INTO movie_ratings.movie_actor_map VALUE (2, 3);
INSERT INTO movie_ratings.movie_actor_map VALUE (2, 40);
INSERT INTO movie_ratings.movie_actor_map VALUE (2, 15);
INSERT INTO movie_ratings.movie_actor_map VALUE (3, 10);
INSERT INTO movie_ratings.movie_actor_map VALUE (3, 5);
INSERT INTO movie_ratings.movie_actor_map VALUE (3, 6);
INSERT INTO movie_ratings.movie_actor_map VALUE (3, 54);
INSERT INTO movie_ratings.movie_actor_map VALUE (4, 47);
INSERT INTO movie_ratings.movie_actor_map VALUE (4, 1);
INSERT INTO movie_ratings.movie_actor_map VALUE (4, 27);
INSERT INTO movie_ratings.movie_actor_map VALUE (4, 50);
INSERT INTO movie_ratings.movie_actor_map VALUE (5, 2);
INSERT INTO movie_ratings.movie_actor_map VALUE (5, 42);
INSERT INTO movie_ratings.movie_actor_map VALUE (5, 7);
INSERT INTO movie_ratings.movie_actor_map VALUE (5, 8);
INSERT INTO movie_ratings.movie_actor_map VALUE (6, 45);
INSERT INTO movie_ratings.movie_actor_map VALUE (6, 17);
INSERT INTO movie_ratings.movie_actor_map VALUE (6, 13);
INSERT INTO movie_ratings.movie_actor_map VALUE (6, 11);
INSERT INTO movie_ratings.movie_actor_map VALUE (7, 19);
INSERT INTO movie_ratings.movie_actor_map VALUE (7, 21);
INSERT INTO movie_ratings.movie_actor_map VALUE (7, 48);
INSERT INTO movie_ratings.movie_actor_map VALUE (7, 37);
INSERT INTO movie_ratings.movie_actor_map VALUE (8, 32);
INSERT INTO movie_ratings.movie_actor_map VALUE (8, 48);
INSERT INTO movie_ratings.movie_actor_map VALUE (8, 3);
INSERT INTO movie_ratings.movie_actor_map VALUE (8, 51);
INSERT INTO movie_ratings.movie_actor_map VALUE (9, 20);
INSERT INTO movie_ratings.movie_actor_map VALUE (9, 31);
INSERT INTO movie_ratings.movie_actor_map VALUE (9, 55);
INSERT INTO movie_ratings.movie_actor_map VALUE (9, 12);
INSERT INTO movie_ratings.movie_actor_map VALUE (10, 24);
INSERT INTO movie_ratings.movie_actor_map VALUE (10, 4);
INSERT INTO movie_ratings.movie_actor_map VALUE (10, 43);
INSERT INTO movie_ratings.movie_actor_map VALUE (10, 36);
INSERT INTO movie_ratings.movie_actor_map VALUE (11, 53);
INSERT INTO movie_ratings.movie_actor_map VALUE (11, 18);
INSERT INTO movie_ratings.movie_actor_map VALUE (11, 30);
INSERT INTO movie_ratings.movie_actor_map VALUE (11, 52);
INSERT INTO movie_ratings.movie_actor_map VALUE (12, 6);
INSERT INTO movie_ratings.movie_actor_map VALUE (12, 56);
INSERT INTO movie_ratings.movie_actor_map VALUE (12, 23);
INSERT INTO movie_ratings.movie_actor_map VALUE (12, 57);
INSERT INTO movie_ratings.movie_actor_map VALUE (13, 33);
INSERT INTO movie_ratings.movie_actor_map VALUE (13, 26);
INSERT INTO movie_ratings.movie_actor_map VALUE (13, 25);
INSERT INTO movie_ratings.movie_actor_map VALUE (13, 29);
INSERT INTO movie_ratings.movie_actor_map VALUE (14, 14);
INSERT INTO movie_ratings.movie_actor_map VALUE (14, 49);
INSERT INTO movie_ratings.movie_actor_map VALUE (14, 41);
INSERT INTO movie_ratings.movie_actor_map VALUE (14, 44);
INSERT INTO movie_ratings.movie_actor_map VALUE (15, 9);
INSERT INTO movie_ratings.movie_actor_map VALUE (15, 39);
INSERT INTO movie_ratings.movie_actor_map VALUE (15, 28);
INSERT INTO movie_ratings.movie_actor_map VALUE (15, 35);



/* Populate movie_ratings.movie_genre_map table */
INSERT INTO movie_ratings.movie_genre_map VALUES (1, 5);
INSERT INTO movie_ratings.movie_genre_map VALUES (1, 6);
INSERT INTO movie_ratings.movie_genre_map VALUES (1, 7);
INSERT INTO movie_ratings.movie_genre_map VALUES (2, 7);
INSERT INTO movie_ratings.movie_genre_map VALUES (2, 16);
INSERT INTO movie_ratings.movie_genre_map VALUES (3, 6);
INSERT INTO movie_ratings.movie_genre_map VALUES (3, 7);
INSERT INTO movie_ratings.movie_genre_map VALUES (4, 4);
INSERT INTO movie_ratings.movie_genre_map VALUES (4, 7);
INSERT INTO movie_ratings.movie_genre_map VALUES (5, 1);
INSERT INTO movie_ratings.movie_genre_map VALUES (5, 2);
INSERT INTO movie_ratings.movie_genre_map VALUES (5, 7);
INSERT INTO movie_ratings.movie_genre_map VALUES (6, 12);
INSERT INTO movie_ratings.movie_genre_map VALUES (6, 19);
INSERT INTO movie_ratings.movie_genre_map VALUES (7, 1);
INSERT INTO movie_ratings.movie_genre_map VALUES (7, 6);
INSERT INTO movie_ratings.movie_genre_map VALUES (7, 19);
INSERT INTO movie_ratings.movie_genre_map VALUES (8, 1);
INSERT INTO movie_ratings.movie_genre_map VALUES (8, 19);
INSERT INTO movie_ratings.movie_genre_map VALUES (9, 1);
INSERT INTO movie_ratings.movie_genre_map VALUES (9, 2);
INSERT INTO movie_ratings.movie_genre_map VALUES (9, 5);
INSERT INTO movie_ratings.movie_genre_map VALUES (10, 12);
INSERT INTO movie_ratings.movie_genre_map VALUES (10, 12);
INSERT INTO movie_ratings.movie_genre_map VALUES (10, 17);
INSERT INTO movie_ratings.movie_genre_map VALUES (11, 1);
INSERT INTO movie_ratings.movie_genre_map VALUES (11, 2);
INSERT INTO movie_ratings.movie_genre_map VALUES (11, 6);
INSERT INTO movie_ratings.movie_genre_map VALUES (12, 1);
INSERT INTO movie_ratings.movie_genre_map VALUES (12, 2);
INSERT INTO movie_ratings.movie_genre_map VALUES (12, 17
INSERT INTO movie_ratings.movie_genre_map VALUES (13, 1);
INSERT INTO movie_ratings.movie_genre_map VALUES (13, 5);
INSERT INTO movie_ratings.movie_genre_map VALUES (13, 9);
INSERT INTO movie_ratings.movie_genre_map VALUES (14, 1);
INSERT INTO movie_ratings.movie_genre_map VALUES (14, 4);
INSERT INTO movie_ratings.movie_genre_map VALUES (14, 7);
INSERT INTO movie_ratings.movie_genre_map VALUES (15, 4);
INSERT INTO movie_ratings.movie_genre_map VALUES (15, 8);
INSERT INTO movie_ratings.movie_genre_map VALUES (15, 18);


SELECT * FROM movie_ratings.movie_info;
SELECT * FROM movie_ratings.genre_info;
SELECT * FROM movie_ratings.director_info;
SELECT * FROM movie_ratings.actor_info;
SELECT * FROM movie_ratings.movie_actor_map;
SELECT * FROM movie_ratings.movie_genre_map;
