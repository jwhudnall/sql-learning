# SQL 101
These are my collection of notes and lessons as I learn SQL. At first, key concepts I want to remember will populate the README.MD directly. Eventually, this repo will be reorganized.

## Day 1 Findings and Observations
Following along with the book **Head First SQL**, I came to the point of needing to download mysql to interact with the lessons. The following are the key takeaways after installing mySQL:

### Telling the Terminal where to Look
Once downloaded, I learned everything is located at `/usr/local/<name-of-version>/bin`. In order to run mysql commands, you have to make sure that the terminal looks for the MySql command there. 

1. Create/Edit .bash_profile in home directory via `touch .bash_profile`.
2. Add the following to the new file:
`# mysql path

export PATH=${PATH}:/usr/local/<installation-location>/bin`

Where `<installation-location>` was the name of my directory.

3. `source ~/.bash_profile` to refresh.
4. Try to login to the server (that was already running) via `mysql -u root -p`, which prompted me for the password. Success!

## Database 101
* `CREATE DATABASE database_name` - Create a new database.
* `USE database_name` - Defines the database to be used

`CREATE TABLE my_contacts
(
last_name VARCHAR(30),
first_name VARCHAR(20),
email VARCHAR(50),
birthday DATE,
profession VARCHAR(50),
location VARCHAR(50),
status VARCHAR(20),
interests VARCHAR(100),
seeking VARCHAR(100)
);`
