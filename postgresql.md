## References
- [Curso Online Grátis: Conceitos e melhores práticas com bancos de dados PostgreSQL](https://web.digitalinnovation.one/course/conceitos-e-melhores-praticas-com-bancos-de-dados-postgresql/learning/83cbc77b-5abe-4a19-bcba-5ccc0baa502d)
- [PlayList PostgreSQL - UpInside](https://www.youtube.com/playlist?list=PLi_gvjv-JgXpl8w8mzdBH9R00d6RVv2XC)
- [SQL & PostgreSQL for Beginners: Become an SQL Expert - Udemy](https://www.udemy.com/course/sql-and-postgresql-for-beginners/)
- Official Site: https://www.postgresql.org/
- Install Ubuntu APT: https://wiki.postgresql.org/wiki/Apt
- Oficial Documentation: https://www.postgresql.org/docs/manuals/

## PGAdmin
- https://www.pgadmin.org/
- $ pgadmin4 
- http://127.0.0.1:42205/browser/

## PG CLI
- $ psql --help
- $ sudo service postgresql status
- $ sudo service postgresql stop
- $ sudo service postgresql start
- $ sudo service postgresql restart
- $ psql -d database -U  user -W (Connect to a database)
- $ psql -h host -d database -U user -W (If you want to connect to a database that resides on another host)
- $ psql -U user -h host "dbname=db sslmode=require" (In case you want to use SSL mode for the connection)
- $ \c dbname username (SWITCH to a new database)
- $ \l (List available databases)
- $ \dt (List available tables)
- $ \d table_name (Describe table)
- $ \dn (List available schema)
- $ \df (List available functions)
- $ \dv (List available views)
- $ \du (List users and their roles)
- $ \q (QUIT PSQL)
- $ \? (To know all available psql commands)
- $ \h ALTER TABLE (To get help on specific PostgreSQL statement, you use the \h command)

## Comandos básicos
- https://ajuda.locaweb.com.br/wiki/conectar-ao-postgresql/
- $ psql -h HOST -U USUARIODOBANCO -W
   - $ psql -h testewikinova.postgresql.dbaas.com.br -U cliente -W
   - $ psql -h 179.188.16.126 -U cliente -W
<table width="500">
<tbody>
<tr>
<td width="125">\d</td>
<td width="375">Lista as tabelas contidas em sua base</td>
</tr>
<tr>
<td> \d nome da tabela</td>
<td>Descreve todos os atributos da tabela e suas propriedades</td>
</tr>
<tr>
<td>\g</td>
<td>Executa determinada query</td>
</tr>
<tr>
<td>\q</td>
<td>Sai do console psql</td>
</tr>
<tr>
<td>\i</td>
<td>/caminho/pasta/script.sql   Importar um script.sql</td>
</tr>
<tr>
<td>\timing &#8212;</td>
<td>Inicia ou para  o cronômetro para atividades</td>
</tr>
<tr>
<td>\dT+ &#8212;</td>
<td>Lista os tipos de dados do PG com detalhes</td>
</tr>
<tr>
<td>\cd &#8212;</td>
<td>Muda para outro diretório</td>
</tr>
<tr>
<td>\dt</td>
<td>Lista tabelas</td>
</tr>
<tr>
<td>\di</td>
<td>Lista indices</td>
</tr>
<tr>
<td>\ds</td>
<td>Lista sequências</td>
</tr>
<tr>
<td>\dv</td>
<td>Lista views</td>
</tr>
<tr>
<td>\dS</td>
<td>Lista tabelas do sistema</td>
</tr>
<tr>
<td>\dn</td>
<td>Lista esquemas</td>
</tr>
<tr>
<td>\dp</td>
<td>Lista privilégios</td>
</tr>
<tr>
<td>\e</td>
<td>Abre o editor vi com a última consulta</td>
</tr>
<tr>
<td>\o</td>
<td>Inicia ou termina a criação de arquivo. Ex.: \o arquivo.sql</td>
</tr>
<tr>
<td>\?</td>
<td>Ajuda geral dos comandos do psql</td>
</tr>
<tr>
<td>\h *</td>
<td>Exibe ajuda de todos os comandos</td>
</tr>
<tr>
<td>\encoding</td>
<td>Exibe codificação atual</td>
</tr>
</tbody>
</table>

## Conectar a base via pgAdmin
<ul>
<li>Primeiramente, para realizar o acesso ao Postgres via pgAdmin 4, crie uma conexão com o servidor utilizando a opção <strong>Add new server</strong>:</li>
</ul>
<p><img class="alignnone size-full wp-image-10152" src="https://ajuda.locaweb.com.br/files/2018/11/Pg01.jpg" alt="" width="691" height="527" srcset="https://ajuda.locaweb.com.br/files/2018/11/Pg01.jpg 691w, https://ajuda.locaweb.com.br/files/2018/11/Pg01-300x229.jpg 300w, https://ajuda.locaweb.com.br/files/2018/11/Pg01-50x38.jpg 50w, https://ajuda.locaweb.com.br/files/2018/11/Pg01-60x46.jpg 60w, https://ajuda.locaweb.com.br/files/2018/11/Pg01-100x76.jpg 100w" sizes="(max-width: 691px) 100vw, 691px" /></p>
<ul>
<li>Na aba <strong>General</strong>, inclua o host de conexão com o banco de dados:</li>
</ul>
<p style="padding-left: 30px"><img class="alignnone size-full wp-image-10153" src="https://ajuda.locaweb.com.br/files/2018/11/Pg02.jpg" alt="" width="494" height="294" srcset="https://ajuda.locaweb.com.br/files/2018/11/Pg02.jpg 494w, https://ajuda.locaweb.com.br/files/2018/11/Pg02-300x179.jpg 300w, https://ajuda.locaweb.com.br/files/2018/11/Pg02-50x30.jpg 50w, https://ajuda.locaweb.com.br/files/2018/11/Pg02-60x36.jpg 60w, https://ajuda.locaweb.com.br/files/2018/11/Pg02-100x60.jpg 100w" sizes="(max-width: 494px) 100vw, 494px" /></p>
<ul>
<li>Em Connection, insira novamente o host de conexão e em <strong>Maintenance database</strong> digite o nome do banco de dados. Para finalizar, em <strong>User name</strong>, insira o login da base e em <strong>Password</strong> a senha deste usuário:</li>
</ul>
<p style="padding-left: 30px"><img class="alignnone size-full wp-image-10154" src="https://ajuda.locaweb.com.br/files/2018/11/Pg03.jpg" alt="" width="498" height="545" srcset="https://ajuda.locaweb.com.br/files/2018/11/Pg03.jpg 498w, https://ajuda.locaweb.com.br/files/2018/11/Pg03-274x300.jpg 274w, https://ajuda.locaweb.com.br/files/2018/11/Pg03-46x50.jpg 46w, https://ajuda.locaweb.com.br/files/2018/11/Pg03-55x60.jpg 55w, https://ajuda.locaweb.com.br/files/2018/11/Pg03-91x100.jpg 91w" sizes="(max-width: 498px) 100vw, 498px" /></p>
<ul>
<li>Realizado este processo a conexão com o banco de dados terá sido realizada. Serão apresentados vários bancos de dados, porém, esta é uma característica do PostgreSQL onde o acesso será possível somente em sua base, veja:</li>
</ul>
<p><img class="alignnone size-full wp-image-10155" src="https://ajuda.locaweb.com.br/files/2018/11/Pg04.jpg" alt="" width="762" height="344" srcset="https://ajuda.locaweb.com.br/files/2018/11/Pg04.jpg 762w, https://ajuda.locaweb.com.br/files/2018/11/Pg04-300x135.jpg 300w, https://ajuda.locaweb.com.br/files/2018/11/Pg04-50x23.jpg 50w, https://ajuda.locaweb.com.br/files/2018/11/Pg04-60x27.jpg 60w, https://ajuda.locaweb.com.br/files/2018/11/Pg04-100x45.jpg 100w" sizes="(max-width: 762px) 100vw, 762px" /></p>


## Conectando-se ao Postgre usando PDO
```php
 try {
    $db = new PDO("pgsql:host=localhost dbname=nome_do_banco user=jvideos10 password=password");
 } catch (PDOException  $e) {
    print $e-&gt;getMessage();
 }
```
 
## Exemplo PDO
```php
try {
	$pdo = new PDO("pgsql:host=localhost 
	                dbname=dbteste 
			user=postgres 
			password=root");
} catch(PDOException $e){
	print $e->getMessage(); die;
}

$sql = $pdo->prepare("SELECT movie_name 
                      FROM movies 
		      WHERE movie_length > :length 
		      AND movie_lang = :lang");
$sql->bindValue(":length", 90);
$sql->bindValue(":lang", 'English');
$sql->execute();
if($sql->rowCount() > 0){
	var_dump($sql->fetchAll()); die;
}
```

## Fast Reference
```sql
/* 
create the directors table
*/ 
CREATE TABLE directors (
	director_id SERIAL PRIMARY KEY,
	first_name VARCHAR(30),
	last_name VARCHAR(30) NOT NULL,
	date_of_birth DATE, 
	nationality VARCHAR(20)
);

/*
Create the actors table
*/
CREATE TABLE actors (
	actor_id SERIAL PRIMARY KEY,
	first_name VARCHAR(30),
	last_name VARCHAR(30),
	gender CHAR(1),
	date_of_birth DATE 
);

/*
Create the movies table
*/ 
CREATE TABLE movies (
	movie_id SERIAL PRIMARY KEY,
	movie_name VARCHAR(50),
	movie_length INT, 
	movie_lang VARCHAR(20),
	release_date DATE,
	age_certificate VARCHAR(5),
	director_id INT REFERENCES directors (director_id)
);

/*
Create the movie_revenues 
*/ 
CREATE TABLE movie_revenues (
	revenue_id SERIAL PRIMARY KEY,
	movie_id INT REFERENCES movies (movie_id),
	domestic_takings DECIMAL(6,2),
	international_takings DECIMAL(6,2)
);

/*
Create the movies_actors 
*/ 
CREATE TABLE movies_actors (
	movie_id INT REFERENCES movies (movie_id),
	actor_id INT REFERENCES actors (actor_id),
	PRIMARY KEY (movie_id, actor_id)
);


-- 1.Create a new database called owners_pets
-- 2. Create the owners table
CREATE TABLE owners (

	id SERIAL PRIMARY KEY,
	first_name VARCHAR(30),
	last_name VARCHAR(30),
	city VARCHAR(30),
	state CHAR(2)
);
SELECT * FROM owners;

-- 3. Create the pets table (with a foreign key)
CREATE TABLE pets (

	id SERIAL PRIMARY KEY, 
	species VARCHAR(30),
	full_name VARCHAR(30),
	age INT, 
	owner_id INT REFERENCES owners(id)
);
SELECT * FROM pets;

-- 4. Add an email column to the owners table
ALTER TABLE owners
ADD COLUMN email VARCHAR(50) UNIQUE;
SELECT * FROM owners;

-- 5. Change the data type of the last_name column in the owners table to VARCHAR(50).
ALTER TABLE owners
ALTER COLUMN last_name TYPE VARCHAR(50);
SELECT * FROM owners;


-- 1. Insert the data into the owners table
INSERT INTO owners (first_name, last_name, city, state, email)
VALUES ('Samuel','Smith','Boston','MA','samsmith@gmail.com'),
('Emma','Johnson','Seattle','WA','emjohnson@gmail.com'),
('John','Oliver','New York','NY','johnoliver@gmail.com'),
('Olivia','Brown','San Francisco','CA','oliviabrown@gmail.com'),
('Simon','Smith','Dallas','TX','sismith@gmail.com'),
(null,'Maxwell',null,'CA','lordmaxwell@gmail.com');
SELECT * FROM owners;

-- 2. Insert the data into the pets table
INSERT INTO pets (species, full_name, age, owner_id)
VALUES ('Dog','Rex',6,1),
('Rabbit','Fluffy',2,5),('Cat','Tom',8,2),('Mouse','Jerry',2,2),
('Dog','Biggles',4,2),('Tortoise','Squirtle',42,3);
SELECT * FROM pets;

-- 3. Update Fluffy the rabbits age to 3
UPDATE pets
SET age = 3
WHERE full_name = 'Fluffy';
SELECT * FROM pets;

-- 4. Delete Mr Maxwell from the owners table
SELECT * FROM owners;
DELETE FROM owners
WHERE last_name = 'Maxwell';

/* 
Insert data into directors table
*/
INSERT INTO DIRECTORS (first_name, last_name, date_of_birth, nationality) VALUES ('Tomas','Alfredson','1965-04-01','Swedish'),
('Paul','Anderson','1970-06-26','American'),
('Wes','Anderson','1969-05-01','American'),
('Richard','Ayoade','1977-06-12','British'),
('Luc','Besson','1959-03-18','French'),
('James','Cameron','1954-08-16','American'),
('Guillermo','del Toro','1964-10-09','Mexican'),
('Victor','Fleming','1889-02-23','American'),
('Francis','Ford Coppola','1939-04-07','American'),
('Kinji','Fukasaku','1930-07-03','Japanese'),
('Florian ','Henckel von Donnersmarck','1973-05-02','German'),
('Terry','Jones','1942-02-01','British'),
('Stanley','Kubrick','1928-07-26','American'),
('John','Lasseter','1957-01-12','American'),
('Ang','Lee','1954-10-23','Chinese'),
('Bruce','Lee','1940-11-27','Chinese'),
('George','Lucas','1944-05-14','American'),
('Martin','McDonagh','1970-03-26','British'),
('James','McTeigue','1967-12-29','Australian'),
('Fernando','Meirelles','1955-11-09','Brazilian'),
('Hayao ','Miyazaki','1941-01-05','Japanese'),
('Paulo','Morelli','1966-03-10','Brazilian'),
('Chan-wook','Park','1963-08-23','South Korean'),
('Sam','Raimi','1959-10-23','American'),
('Mark','Romanek','1959-09-18','American'),
('Martin','Scorsese','1942-11-17','American'),
('Ridley','Scott','1937-11-30','British'),
('Tony','Scott','1944-06-21','British'),
('Zack','Snyder','1966-03-01','American'),
('Sion','Sono','1961-12-18','Japanese'),
('Steven','Spielberg','1946-12-18','American'),
('Robert','Stevenson','1905-03-31','British'),
('Quentin','Tarantino','1963-03-27','American'),
('Robert','Wise','1914-09-10','American'),
('Kar Wai','Wong','1958-07-17','Chinese'),
('Robert','Zemeckis','1952-05-14','American'),
('Yimou','Zhang','1950-04-02','Chinese');

INSERT INTO actors (first_name, last_name, gender, date_of_birth) VALUES ('Malin','Akerman','F','1978-05-12'),
('Tim','Allen','M','1953-06-13'),
('Julie','Andrews','F','1935-10-01'),
('Ivana','Baquero','F','1994-06-11'),
('Lorraine','Bracco','F','1954-10-02'),
('Alice','Braga','F','1983-04-15'),
('Marlon','Brando','M','1924-04-03'),
('Adrien','Brody','M','1973-04-14'),
('Peter','Carlberg','M','1950-12-08'),
('Gemma','Chan','F','1982-11-29'),
('Chen','Chang','M','1976-10-14'),
('Graham','Chapman','M','1941-01-08'),
('Pei-pei','Cheng','F','1946-12-04'),
('Maggie ','Cheung','F','1964-09-20'),
('Min-sik','Choi','M','1962-05-30'),
('Yun-fat','Chow','M','1955-05-18'),
('John','Cleese','M','1939-10-27'),
('Paddy','Considine','M','1973-09-05'),
('Abbie','Cornish','F','1982-08-07'),
('Brian','Cox','M','1946-06-01'),
('Scatman','Crothers','M','1910-05-23'),
('Russell','Crowe','M','1964-04-07'),
('Tom','Cruise','M','1962-07-03'),
('Darlan','Cunha','M','1988-07-26'),
('Willem','Dafoe','M','1955-07-22'),
('Paul','Dano','M','1984-06-19'),
('Daniel','Day-Lewis','M','1957-04-29'),
('Robert','De Niro','M','1943-08-17'),
(null,'Denden','M','1950-01-23'),
('Leonardo','DiCaprio','M','1974-11-11'),
('Peter','Dinklage','M','1969-06-11'),
('Hiroki','Doi','M','1999-08-10'),
('Kirsten','Dunst','F','1982-04-30'),
('Shelley','Duvall','F','1949-07-07'),
('Ralph','Fiennes','M','1962-12-22'),
('Leandro','Firmino','M','1978-06-23'),
('Carrie','Fisher','F','1956-10-21'),
('Harrison','Ford','M','1942-07-13'),
('Jodie','Foster','F','1962-11-19'),
('James','Franco','M','1978-04-19'),
('Dillon','Freasier','M','1996-03-06'),
('Tatsuya','Fujiwara','M','1982-05-15'),
('Mitsuru','Fukikoshi','M','1965-02-17'),
('Clark','Gable','M','1901-02-01'),
('Mason','Gamble','M','1986-01-16'),
('Xian','Gao','M',null),
('Andrew','Garfield','M','1983-08-20'),
('Judy','Garland','F','1922-06-10'),
('Martina','Gedeck','F','1961-09-14'),
('Jeff','Goldblum','M','1952-10-22'),
('Carla','Gugino','F','1971-08-29'),
('Alec','Guiness','M','1914-04-02'),
('Jackey','Haley','M','1961-07-14'),
('Mark','Hamill','M','1951-09-25'),
('Tom','Hanks','M','1956-07-09'),
('Daryl','Hannah','F','1958-12-03'),
('Woody','Harrelson','M','1961-07-23'),
('Rutger','Hauer','M','1944-01-23'),
('Sally','Hawkins','F','1976-04-27'),
('Kare','Hedebrant','M','1995-06-28'),
('Rumi','Hiiragi','F','1987-08-01'),
('Ian','Holm','M','1931-09-12'),
('Dennis','Hopper','M','1936-05-17'),
('Eric','Idle','M','1943-03-29'),
('Miyu','Irino','M','1988-02-19'),
('Samuel','Jackson','M','1948-12-21'),
('Terry','Jones','M','1942-02-01'),
('Milla','Jovovich','F','1975-12-17'),
('Megumi','Kagurazaka','F','1981-09-28'),
('Takeshi','Kaneshiro','M','1973-10-11'),
('Hei-Jung','Kang','F','1982-01-04'),
('Irfan','Khan','M','1967-01-07'),
('Nicole','Kidman','F','1967-06-20'),
('Val','Kilmer','M','1959-12-31'),
('Takeshi','Kitano','M','1947-01-18'),
('Keira','Knightley','F','1985-03-26'),
('Sebastian','Koch','M','1962-05-31'),
('Asuka','Kurosawa','F','1971-12-22'),
('Andy','Lau','M','1961-09-27'),
('Jude','Law','M','1972-12-29'),
('Lina','Leandersson','F','1995-09-27'),
('Bruce','Lee','M','1940-11-27'),
('Vivien','Leigh','F','1913-11-05'),
('Tony','Leung','M','1962-06-27'),
('Ray','Liotta','M','1954-12-18'),
('Danny','Lloyd','M','1972-10-13'),
('Sihung','Lung','M','1930-01-01'),
('Aki','Maeda','F','1985-07-11'),
('Tobey','Maguire','M','1975-06-27'),
('Francis','McDormand','F','1957-06-23'),
('Malcolm','McDowell','M','1943-06-13'),
('Alfred','Molina','M','1953-05-24'),
('Cathy','Moriarty','F','1960-11-29'),
('Ulrich','Muhe','M','1953-06-20'),
('Carey','Mulligan','F','1985-05-28'),
('Bill','Murray','M','1950-09-21'),
('Mari','Natsuki','F','1952-05-02'),
('Jack','Nicholson','M','1937-04-22'),
('Connie','Nielsen','F','1965-07-03'),
('Ika','Nord','F','1960-04-29'),
('Chuck','Norris','M','1940-03-10'),
('Edward','Norton','M','1969-08-18'),
('Gary','Oldman','M','1958-03-21'),
('Yasmin','Paige','F','1991-06-24'),
('Michael','Palin','M','1943-05-05'),
('Rebecca','Pan','F','1931-12-29'),
('Joe','Pesci','M','1943-02-09'),
('Joaquin','Phoenix','M','1974-10-28'),
('Natilie','Portman','F','1981-06-09'),
('Per','Ragnar','M','1941-05-29'),
('Oliver','Reed','M','1938-02-13'),
('Jean','Reno','M','1948-07-30'),
('Tony','Revolori','M','1996-04-28'),
('Craig','Roberts','M','1991-01-21'),
('Sam','Rockwell','M','1968-11-05'),
('Alexandre','Rodrigues','M','1983-05-21'),
('Saoirse','Ronan','F','1994-04-12'),
('Roy','Scheider','M','1932-11-10'),
('Jason','Schwartzmann','M','1980-06-26'),
('Suraj','Sharma','M','1993-03-21'),
('Martin','Sheen','M','1940-08-03'),
('Douglas','Silva','M','1988-09-27'),
('Dandan','Song','F','1961-08-25'),
('Rafe','Spall','M','1983-03-10'),
('Tilda','Swinton','F','1960-11-05'),
('George','Tokoro','M','1955-01-26'),
('Noah','Taylor','M','1969-09-04'),
('Uma','Thurman','F','1970-04-29'),
('John','Travolta','M','1954-02-18'),
('Chris','Tucker','M','1971-08-31'),
('Dick','Van Dyke','M','1925-12-13'),
('Hugo','Weaving','M','1960-04-04'),
('Olivia','Williams','F','1968-07-26'),
('Mykelti','Williamson','M','1957-03-04'),
('Bruce','Willis','M','1955-03-19'),
('Luke','Wilson','M','1971-09-21'),
('Owen','Wilson','M','1968-11-18'),
('Patrick','Wilson','M','1973-07-03'),
('Kate','Winslet','F','1975-10-05'),
('Faye','Wong','F','1969-08-08'),
('Robin','Wright','F','1966-04-08'),
('Michelle','Yeoh','F','1962-08-06'),
('Ji-tae','Yoo','M','1976-04-13'),
('Jin-seo','Yoon','F','1983-08-05'),
('Sean','Young','F','1959-11-20'),
('Billy','Zane','M','1966-02-24'),
('Ziyi','Zhang','F','1979-02-09');


INSERT INTO movies (movie_name, movie_length, movie_lang, release_date, age_certificate, director_id) VALUES ('A Clockwork Orange','112','English','1972-02-02','18','13'),
('Apocalypse Now','168','English','1979-08-15','15','9'),
('Battle Royale ','111','Japanese','2001-01-04','18','10'),
('Blade Runner ','121','English','1982-06-25','15','27'),
('Chungking Express','113','Chinese','1996-08-03','15','35'),
('City of God','145','Portuguese','2003-01-17','18','20'),
('City of Men','140','Portuguese','2008-02-29','15','22'),
('Cold Fish','108','Japanese','2010-09-12','18','30'),
('Crouching Tiger Hidden Dragon','139','Chinese','2000-07-06','12','15'),
('Eyes Wide Shut','130','English','1999-07-16','18','13'),
('Forrest Gump','119','English','1994-07-06','PG','36'),
('Gladiator','165','English','2000-05-05','15','27'),
('Gone with the Wind','123','English','1939-12-15','PG','8'),
('Goodfellas','148','English','1990-09-19','15','26'),
('Grand Budapest Hotel','117','English','2014-07-03','PG','3'),
('House of Flying Daggers','134','Chinese','2004-03-12','12','37'),
('In the Mood for Love','124','Chinese','2001-02-02','12','35'),
('Jaws','134','English','1975-06-20','12','31'),
('Leon','123','English','1994-11-18','15','5'),
('Let the Right One In','128','Swedish','2008-10-24','15','1'),
('Life of Brian','126','English','1979-08-17','15','12'),
('Life of Pi','129','English','2012-11-21','PG','15'),
('Mary Poppins','87','English','1964-08-29','U','32'),
('Never Let Me Go','117','English','2010-09-15','15','25'),
('Oldboy','130','Korean','2005-03-25','18','23'),
('Pans Labyrinth','98','Spanish','2006-12-29','PG','7'),
('Ponyo','107','Japanese','2009-08-14','U','21'),
('Pulp Fiction','136','English','1994-10-14','15','33'),
('Raging Bull','132','English','1980-11-14','18','26'),
('Rushmore','104','English','1998-11-12','12','3'),
('Spider-Man','118','English','2002-05-03','PG','24'),
('Spider-Man 2','115','English','2004-06-30','PG','24'),
('Spider-Man 3','112','English','2007-05-04','PG','24'),
('Spirited Away','120','Japanese','2001-06-19','U','21'),
('Star Wars: A New Hope','123','English','1977-05-25','PG','17'),
('Star Wars: Empire Strikes Back','150','English','1980-05-21','PG','17'),
('Star Wars: Return of the Jedi','139','English','1983-05-25','PG','17'),
('Submarine','115','English','2011-06-03','15','4'),
('Taxi Driver','117','English','1976-02-7','15','26'),
('The Darjeeling Limited','119','English','2007-09-29','PG','3'),
('The Fifth Element','149','English','1997-05-09','12','5'),
('The Lives of Others','165','German','2007-02-09','15','11'),
('The Shining','126','English','1980-05-23','18','13'),
('The Sound of Music','91','English','1965-03-02','U','34'),
('The Wizard of Oz','120','English','1939-08-25','U','8'),
('There Will Be Blood','168','English','2007-12-26','15','2'),
('Three Billboards Outside Ebbing, Missouri ','134','English','2017-11-10','15','18'),
('Titanic','143','English','1997-12-19','12','6'),
('Top Gun','121','English','1986-05-16','12','28'),
('Toy Story','95','English','1995-11-22','U','14'),
('V for Vendetta','140','English','2006-03-17','12','19'),
('Watchmen','138','English','2009-03-06','12','29'),
('Way of the Dragon ','99','Chinese','1972-06-01','12','16');


INSERT INTO movie_revenues (revenue_id, movie_id, domestic_takings, international_takings) VALUES ('1','45','22.2','1.3'),
('2','13','199.4','201.2'),
('3','23','102.1',null),
('4','44','158.7',null),
('6','1','27.1',null),
('7','53',null,null),
('17','18','260.3','210.9'),
('9','39','28.1',null),
('5','35','461.2','314.2'),
('13','2','83.4',null),
('15','21','19.6',null),
('8','36','290.3','247.8'),
('11','43','44.1',null),
('12','29','23.1',null),
('14','4','33.3',null),
('10','37','309.1','166.2'),
('16','49','180.1','177.3'),
('18','14','46.6',null),
('21','11','330.3','348.1'),
('20','28','107.9','106.2'),
('19','19',null,null),
('23','50','192.1','182.4'),
('22','5',null,null),
('27','41','64.1','200.3'),
('24','48','659.2','1528.1'),
('25','30','16.9',null),
('26','10','55.7','106.3'),
('30','12','188.2','273.4'),
('28','9','128.1','85.1'),
('29','3',null,null),
('32','17','2.9','10.2'),
('31','34','11.1','265.4'),
('33','31','404.1','418.1'),
('37','6','8.2','23.5'),
('35','16','11.1','82.5'),
('36','32','374.1','410.4'),
('34','25','1.1','13.8'),
('38','51','71.2','62.5'),
('40','26','37.8','46.4'),
('48','42','11.3','66.1'),
('39','33','337','554'),
('51','40','11.9','23.2'),
('41','46','39.9','35.8'),
('42','7','0.3','2.2'),
('49','20','2.1','9.1'),
('45','52','107.5','77.5'),
('44','27','15.1','186.7'),
('47','8',null,null),
('46','24','2.4','7.1'),
('43','38','0.5','0.4'),
('50','22','124.9','484.1'),
('52','15','59.3','115.5'),
('53','47','54.5','104.7');



INSERT INTO movies_actors (actor_id, movie_id) VALUES ('1','52'),
('2','50'),
('3','23'),
('4','26'),
('5','14'),
('6','6'),
('7','2'),
('8','15'),
('8','40'),
('9','20'),
('10','38'),
('11','9'),
('12','21'),
('13','9'),
('14','17'),
('15','25'),
('16','9'),
('17','21'),
('18','38'),
('19','47'),
('20','30'),
('21','43'),
('22','12'),
('23','10'),
('23','49'),
('24','7'),
('25','15'),
('25','31'),
('25','32'),
('25','33'),
('26','46'),
('27','46'),
('28','14'),
('28','29'),
('28','39'),
('29','8'),
('30','48'),
('31','47'),
('32','27'),
('33','31'),
('33','32'),
('33','33'),
('34','43'),
('35','15'),
('36','6'),
('37','35'),
('37','36'),
('37','37'),
('38','2'),
('38','4'),
('38','35'),
('38','36'),
('38','37'),
('39','39'),
('40','31'),
('40','32'),
('40','33'),
('41','46'),
('42','3'),
('43','8'),
('44','13'),
('45','30'),
('46','9'),
('47','24'),
('48','45'),
('49','42'),
('50','15'),
('51','52'),
('52','35'),
('53','52'),
('54','35'),
('54','36'),
('54','37'),
('55','11'),
('55','50'),
('56','4'),
('57','47'),
('58','4'),
('59','24'),
('59','38'),
('60','20'),
('61','27'),
('61','34'),
('62','41'),
('63','2'),
('64','21'),
('65','34'),
('66','28'),
('67','21'),
('68','41'),
('69','10'),
('70','5'),
('70','16'),
('71','25'),
('72','22'),
('73','10'),
('74','49'),
('75','3'),
('76','24'),
('77','42'),
('78','8'),
('79','16'),
('80','15'),
('81','20'),
('82','53'),
('83','13'),
('84','5'),
('84','17'),
('85','14'),
('86','43'),
('87','9'),
('88','3'),
('89','31'),
('89','32'),
('89','33'),
('90','47'),
('91','1'),
('92','32'),
('93','29'),
('94','42'),
('95','24'),
('96','15'),
('96','30'),
('97','34'),
('98','43'),
('99','12'),
('100','20'),
('101','53'),
('102','15'),
('103','19'),
('103','41'),
('104','38'),
('105','21'),
('106','17'),
('107','14'),
('107','29'),
('108','12'),
('109','19'),
('109','51'),
('110','20'),
('111','12'),
('112','19'),
('113','15'),
('114','38'),
('115','47'),
('116','6'),
('117','15'),
('118','18'),
('119','15'),
('119','40'),
('120','22'),
('121','2'),
('122','7'),
('123','16'),
('124','22'),
('125','15'),
('126','27'),
('127','38'),
('128','28'),
('129','28'),
('130','41'),
('131','33'),
('132','51'),
('133','15'),
('134','11'),
('135','28'),
('135','41'),
('136','30'),
('137','15'),
('137','40'),
('138','52'),
('139','48'),
('140','5'),
('141','11'),
('142','9'),
('143','25'),
('144','25'),
('145','4'),
('146','48'),
('147','9'),
('147','16');


-- 1. Select the movie_name and release_date of every movie. 
SELECT movie_name, release_date FROM movies;

-- 2. Select the first and last names of all American directors. 
SELECT first_name, last_name FROM directors 
WHERE nationality = 'American';

-- 3. Select all male actors born after the 1st of January 1970. 
SELECT * FROM actors
WHERE gender = 'M'
AND date_of_birth > '1970-01-01';

-- 4. Select the names of all movies which are over 90 minutes long and movie
-- language is English.
SELECT movie_name FROM movies
WHERE movie_length > 90 
AND movie_lang = 'English';



-- 1.Select the movie names and movie language of all movies with a movie language of English, 
-- Spanish or Korean. 
SELECT movie_name, movie_lang FROM movies
WHERE movie_lang IN ('English','Spanish','Korean');

-- Select the first and last names of the actors whose last name begins with M and were born 
-- between 01/01/1940 and 31/12/1969. 
SELECT first_name, last_name FROM actors
WHERE last_name LIKE 'M%'
AND date_of_birth BETWEEN '1940-01-01' AND '1969-12-31';

-- Select the first and last names of the directors with nationality of British, French or 
-- German born between 01/01/1950 and 31/12/1980. 
SELECT first_name, last_name FROM directors
WHERE nationality IN ('British','French','German')
AND date_of_birth BETWEEN '1950-01-01' AND '1980-12-31';


-- 1. Select the American directors ordered from oldest to youngest. 
SELECT * FROM directors
WHERE nationality = 'American'
ORDER BY date_of_birth;

-- 2. Return the distinct nationalities from the directors table. 
SELECT DISTINCT nationality FROM directors;

-- 3. Return the first names, last names and date of births of the 10 youngest female actors.
SELECT first_name, last_name, date_of_birth FROM actors
WHERE gender = 'F'
ORDER BY date_of_birth DESC
LIMIT 10;


-- 1. Return the top 3 movies with the highest international takings. 
SELECT * FROM movie_revenues
WHERE international_takings IS NOT NULL
ORDER BY international_takings DESC
LIMIT 3;

-- 2. Concatenate the first and last names of the directors, separated by a space, 
-- and call this new column full_name. 
SELECT CONCAT(first_name, ' ', last_name) AS full_name FROM directors;

-- 3. Return the actors with missing first_names or missing date_of_births. 
SELECT * FROM actors
WHERE first_name IS NULL 
OR date_of_birth IS NULL;


-- selecting data from a table 

/*

SELECT * FROM tablename; 

SELECT columnname1, columnname2, columnname3 FROM tablename;

*/

SELECT * FROM directors;

SELECT first_name FROM directors;

SELECT first_name, last_name FROM directors;

SELECT first_name, last_name, nationality FROM directors;

-- Retrieving data with a where clause 

/* 

SELECT columnname FROM tablename 
WHERE columnname = 'value';

*/

SELECT * FROM movies
WHERE age_certificate = '15';

SELECT * FROM movies
WHERE age_certificate = '15'
AND movie_lang = 'Chinese';

SELECT * FROM movies
WHERE age_certificate = '15'
OR movie_lang = 'Chinese';

SELECT * FROM movies 
WHERE movie_lang = 'English'
AND age_certificate = '15'
AND director_id = 27;

-- Using logical operators (>, >=, <, <=)

SELECT movie_name, movie_length FROM movies
WHERE movie_length > 120;

SELECT movie_name, movie_length FROM movies
WHERE movie_length >= 120;

SELECT movie_name, movie_length FROM movies
WHERE movie_length < 120;

SELECT movie_name, movie_length FROM movies
WHERE movie_length <= 120;

SELECT * FROM movies
WHERE release_date < '1999-12-31';

SELECT * FROM movies
WHERE movie_lang <= 'English';

-- Using IN and NOT IN 

/* 

SELECT columnname1, columnname2 FROM tablename
WHERE columnname3 IN ('value1','value2');

SELECT columnname1, columnname2 FROM tablename
WHERE columnname3 NOT IN ('value1','value2');

*/

SELECT first_name, last_name FROM actors 
WHERE first_name IN ('Bruce','John');

SELECT first_name, last_name FROM actors 
WHERE first_name IN ('Bruce','John','Peter');

SELECT first_name, last_name FROM actors 
WHERE first_name NOT IN ('Bruce','John','Peter');

SELECT actor_id, first_name, last_name FROM actors 
WHERE actor_id IN (2,3,4,5,6,8);

SELECT actor_id, first_name, last_name FROM actors 
WHERE actor_id NOT IN (2,3,4,5,6,8);

-- Using LIKE with % and _ 

/* 

SELECT columnname FROM table 
WHERE columnname LIKE '%pattern%';

SELECT columnname FROM table 
WHERE columnname LIKE '_pattern_';

*/  

SELECT * FROM actors 
WHERE first_name LIKE 'P%';

SELECT * FROM actors 
WHERE first_name LIKE 'Pe_';

SELECT * FROM actors 
WHERE first_name LIKE '%rl%';

SELECT * FROM actors 
WHERE first_name LIKE '__rl__';

-- selecting data where a column is between 2 values 

/* 

SELECT columnname1, columnname2 FROM tablename 
WHERE columnname3 BETWEEN value1 AND VALUE2;

*/

SELECT * FROM movies;

SELECT movie_name, release_date FROM movies 
WHERE release_date BETWEEN '1995-01-01' AND '1999-12-31';

SELECT movie_name, movie_length FROM movies
WHERE movie_length BETWEEN 90 AND 120;

SELECT movie_name, movie_lang FROM movies 
WHERE movie_lang BETWEEN 'Eo' AND 'Portuguese';

-- Ordering the results returned 

/*

SELECT columnname1, columnname2 FROM tablename 
ORDER BY columnname3;

*/

SELECT * FROM actors;

SELECT first_name, last_name, date_of_birth FROM actors 
ORDER BY first_name;

SELECT actor_id, first_name, last_name, date_of_birth FROM actors 
ORDER BY actor_id DESC;

SELECT actor_id, first_name, last_name, date_of_birth FROM actors 
WHERE gender = 'F'
ORDER BY date_of_birth DESC;

-- Limiting the number of records returned 

/* 

SELECT columnname1, columnname2 FROM tablename
LIMIT N;

SELECT columnname1, columnname2 FROM tablename
LIMIT N OFFSET M;

*/

SELECT * FROM movie_revenues
ORDER BY revenue_id
LIMIT 8 OFFSET 2;

-- Using Fetch 

/* 
SELECT column1 FROM table1 
FETCH FIRST 1 ROW ONLY;
*/ 

SELECT movie_id, movie_name FROM movies 
FETCH FIRST 1 ROW ONLY;

SELECT movie_id, movie_name FROM movies 
FETCH FIRST 10 ROW ONLY;

SELECT movie_id, movie_name FROM movies 
OFFSET 8 ROWS
FETCH FIRST 10 ROW ONLY;

-- Distinct values 

/*

SELECT DISTINCT columnname FROM tablename;

*/

SELECT DISTINCT movie_lang, age_certificate FROM movies 
ORDER BY movie_lang;

SELECT DISTINCT * FROM movies;

-- Dealing with NULL values 

/* 
SELECT * FROM tablename 
WHERE columname IS NULL;

SELECT * FROM tablename 
WHERE columname IS NOT NULL;
*/ 

SELECT * FROM actors
WHERE date_of_birth IS NOT NULL;

SELECT * FROM movie_revenues
WHERE domestic_takings IS NOT NULL
ORDER BY domestic_takings DESC;

SELECT * FROM movie_revenues
WHERE international_takings IS NULL;

-- Setting a column name alias 

/* 

SELECT columname AS new_columnname FROM tablename;

*/ 

SELECT last_name AS surname FROM directors;

SELECT last_name AS surname FROM directors
WHERE last_name LIKE 'A%'
ORDER BY surname;

-- Using concatenate  

/* 
SELECT 'string1' || 'string2' AS new_string;

SELECT CONCAT(column1, column2) AS new_column FROM tablename; 

SELECT CONCAT_WS(' ', column1, column2) AS new_column FROM tablename;
*/ 

SELECT 'concat' || 'together' AS new_string;
SELECT 'concat' || ' ' || 'together' AS new_string;

SELECT CONCAT(first_name, last_name) AS full_name FROM actors;

SELECT CONCAT(first_name,':', last_name) AS full_name FROM actors;

SELECT CONCAT_WS(' ', first_name, last_name, date_of_birth) AS full_name FROM actors;


-- 1. Count the number of actors born after the 1st of January 1970. 
SELECT COUNT(*) FROM actors 
WHERE date_of_birth > '1970-01-01';

-- 2. What was the highest and lowest domestic takings for a movie?
SELECT MAX(domestic_takings) FROM movie_revenues;
SELECT MIN(domestic_takings) FROM movie_revenues;

-- 3. What is the sum total movie length for movies rated 15?
SELECT SUM(movie_length) FROM movies
WHERE age_certificate = '15';

-- 4. How many Japanese directors are in the directors table?
SELECT COUNT(*) FROM directors
WHERE nationality = 'Japanese';

-- 5. What is the average movie length for Chinese movies?
SELECT AVG(movie_length) FROM movies 
WHERE movie_lang = 'Chinese';


-- 1. How many directors are there per nationality? 
SELECT nationality, COUNT(nationality) FROM directors
GROUP BY nationality;

-- 2. What is the sum total movie length for each age certificate and movie language combination? 
SELECT movie_lang, age_certificate, SUM(movie_length) FROM movies 
GROUP BY movie_lang, age_certificate
ORDER BY movie_lang, age_certificate;

-- 3. Return the movie languages which have a sum total movie length of over 500 minutes.
SELECT movie_lang, SUM(movie_length) FROM movies
GROUP BY movie_lang 
HAVING SUM(movie_length) > 500;


-- Aggregate Functions : COUNT 

/* 
SELECT COUNT(columnname) FROM tablename; 
*/ 

SELECT COUNT(*) FROM movie_revenues;

SELECT COUNT(international_takings) FROM movie_revenues;

SELECT COUNT(*) FROM movies
WHERE movie_lang = 'English';

-- Aggregate Functions : SUM 

/* 
SELECT SUM(columnname) FROM tablename; 
*/

SELECT SUM(domestic_takings) FROM movie_revenues;

SELECT SUM(domestic_takings) FROM movie_revenues
WHERE domestic_takings > 100.0;

SELECT SUM(movie_length) FROM movies
WHERE movie_lang = 'Chinese';

-- Aggregate Functions : MIN and MAX 

/* 
SELECT MAX(columnname) FROM tablename;
SELECT MIN(columnname) FROM tablename;
*/

SELECT MAX(movie_length) FROM movies;
SELECT MIN(movie_length) FROM movies;

SELECT MIN(movie_length) FROM movies
WHERE movie_lang = 'Japanese';

SELECT MAX(release_date) FROM movies;
SELECT MIN(release_date) FROM movies;

SELECT MAX(movie_name) FROM movies;
SELECT MIN(movie_name) FROM movies;

-- Aggregate Function : AVG 

/* 
SELECT AVG(columnname) FROM tablename;
*/

SELECT AVG(movie_length) FROM movies;

SELECT AVG(movie_length) FROM movies
WHERE age_certificate = '18';

-- Grouping data 

/* 
SELECT column1, AGGFUN(column2) FROM tablename
GROUP BY column1; 
*/

SELECT COUNT(movie_lang) FROM movies;

SELECT movie_lang, COUNT(movie_lang) FROM movies
GROUP BY movie_lang;

SELECT movie_lang, AVG(movie_length) FROM movies
GROUP BY movie_lang;

SELECT movie_lang, age_certificate, AVG(movie_length) FROM movies
GROUP BY movie_lang, age_certificate;

SELECT movie_lang, age_certificate, AVG(movie_length) FROM movies
WHERE movie_length > 120
GROUP BY movie_lang, age_certificate;

SELECT movie_lang, MIN(movie_length), MAX(movie_length) FROM movies
WHERE age_certificate = '15'
GROUP BY movie_lang;

-- HAVING Clauses 

/*
SELECT column1, AGGFUN(column2) FROM tablename
GROUP BY column1 
HAVING AGGFUN(column3) = value;
*/

SELECT movie_lang, COUNT(movie_lang) FROM movies
GROUP BY movie_lang
HAVING COUNT(movie_lang) > 1;

SELECT movie_lang, COUNT(movie_lang) FROM movies
WHERE movie_length > 120
GROUP BY movie_lang
HAVING COUNT(movie_lang) > 1;

 -- Using Mathematical Operators 
 
 /* 
 
 + - / * % 

 */ 
 
SELECT 5 + 6 AS addition;
SELECT 8 -3 AS subtraction;
SELECT 35 / 3 AS division;
SELECT 4 * 6 AS multiplication;

SELECT 8 % 2 AS modulus;

SELECT * FROM movie_revenues;

SELECT movie_id, (domestic_takings + international_takings) AS total_takings FROM movie_revenues;


-------------------------------- JOINING TABLES ------------------------------------------
-- 1. Select the directors first and last names, the movie names and release dates for all 
-- Chinese, Korean and Japanese movies. 
SELECT d.first_name, d.last_name, mo.movie_name, mo.release_date FROM directors d
JOIN movies mo ON d.director_id = mo.director_id
WHERE mo.movie_lang IN ('Chinese','Japanese','Korean');

-- 2. Select the movie names, release dates and international takings of all English language
-- movies.
SELECT mo.movie_name, mo.release_date, mr.international_takings FROM movies mo 
JOIN movie_revenues mr ON mo.movie_id = mr.movie_id
WHERE mo.movie_lang = 'English';

-- 3. Select the movie names, domestic takings and international takings for all movies 
-- with either missing domestic takings or missing international takings and order the results 
-- by movie name.
SELECT mo.movie_name, mr.international_takings, mr.domestic_takings FROM movies mo
JOIN movie_revenues mr ON mo.movie_id = mr.movie_id 
WHERE mr.domestic_takings IS NULL
OR mr.international_takings IS NULL
ORDER BY mo.movie_name;

-- 1. Use a left join to select the first and last names of all British directors and 
-- the names and age certificates of the movies that they directed.
SELECT d.first_name, d.last_name, mo.movie_name, mo.age_certificate FROM directors d 
LEFT JOIN movies mo ON d.director_id = mo.director_id 
WHERE d.nationality = 'British';

-- 2. Count the number of movies that each director has directed.
SELECT d.first_name, d.last_name, COUNT(mo.movie_id) FROM directors d
LEFT JOIN movies mo ON d.director_id = mo.director_id 
GROUP BY d.first_name, d.last_name;


-- 1. Select the first and last names of all the actors who have starred in movies 
-- directed by Wes Anderson. 
SELECT ac.first_name, ac.last_name FROM actors ac 
JOIN movies_actors ma ON ac.actor_id = ma.actor_id 
JOIN movies mo ON mo.movie_id = ma.movie_id
JOIN directors d ON d.director_id = mo.director_id
WHERE d.first_name = 'Wes'
AND d.last_name = 'Anderson';

-- 2. Which director has the highest total domestic takings.
SELECT d.first_name, d.last_name, SUM(mr.domestic_takings) AS total_dom_takings FROM directors d
JOIN movies mo ON d.director_id = mo.director_id 
JOIN movie_revenues mr ON mo.movie_id = mr.movie_id 
WHERE mr.domestic_takings IS NOT NULL
GROUP BY d.first_name, d.last_name
ORDER BY total_dom_takings DESC
LIMIT 1;


-- 1. Select the first names, last names and dates of birth from directors and actors. 
-- Order the results by the date of birth.
SELECT first_name, last_name, date_of_birth FROM directors 
UNION ALL 
SELECT first_name, last_name, date_of_birth FROM actors 
ORDER BY date_of_birth;

-- 2. Select the first and last names of all directors and actors born in the 1960s. 
-- Order the results by last name. 
SELECT first_name, last_name FROM directors
WHERE date_of_birth BETWEEN '1960-01-01' AND '1969-12-31'
UNION ALL 
SELECT first_name, last_name FROM actors
WHERE date_of_birth BETWEEN '1960-01-01' AND '1969-12-31'
ORDER BY last_name;


-- 1. Intersect the first name, last name and date of birth columns in the directors 
-- and actors tables.
SELECT first_name, last_name, date_of_birth FROM directors
INTERSECT 
SELECT first_name, last_name, date_of_birth FROM actors;

-- 2. Retrieve the first names of male actors unless they have the same first name as any
-- British directors.
SELECT first_name FROM actors 
WHERE gender = 'M'
EXCEPT 
SELECT first_name FROM directors 
WHERE nationality = 'British';


-- INNER JOINS: PART 1 

/* 
SELECT table1.column1, table1.column2, table2.column1 FROM table1 
INNER JOIN table2 ON table1.column3 = table2.column3; 
*/ 

SELECT * FROM directors;
SELECT * FROM movies;

INSERT INTO directors (first_name, last_name, date_of_birth, nationality)
VALUES ('Christopher','Nolan','1970-07-30','British');

SELECT directors.director_id, directors.first_name, directors.last_name, movies.movie_name 
FROM directors
INNER JOIN movies ON directors.director_id = movies.director_id;

SELECT directors.director_id, directors.first_name, directors.last_name, movies.movie_name 
FROM directors
INNER JOIN movies ON directors.director_id = movies.director_id
WHERE movies.movie_lang = 'Japanese'
ORDER BY movies.movie_length;

-- INNER JOINS : PART 2

/* 
SELECT table1.column1, table1.column2, table2.column1 FROM table1 
INNER JOIN table2 ON table1.column3 = table2.column3; 

SELECT t1.column1, t1.column2, t2.column1 FROM table1 t1 
JOIN table2 t2 ON t1.column3 = t2.column3; 
*/ 

SELECT directors.director_id, directors.first_name, directors.last_name, movies.movie_name 
FROM directors
INNER JOIN movies ON directors.director_id = movies.director_id
WHERE movies.movie_lang = 'Japanese'
ORDER BY movies.movie_length;

SELECT d.director_id, d.first_name, d.last_name, mo.movie_name FROM directors d
JOIN movies mo ON d.director_id = mo.director_id
WHERE mo.movie_lang = 'Japanese'
ORDER BY mo.movie_length;

SELECT mo.movie_name, mr.domestic_takings, mr.international_takings FROM movies mo 
JOIN movie_revenues mr ON mo.movie_id = mr.movie_id
ORDER BY mr.domestic_takings;

-- INNER JOINS : PART 3 

-- ONLY WHEN THE JOINING COLUMNS HAVE THE SAME NAME! 

/* 
SELECT t1.column1, t1.column2, t2.column1 FROM table1 t1 
JOIN table2 t2 USING (column3);
*/

SELECT mo.movie_name, mr.domestic_takings FROM movies mo
JOIN movie_revenues mr USING (movie_id)
WHERE mo.age_certificate IN ('12','15','18')
ORDER BY mr.domestic_takings DESC;

-- LEFT JOINS

/* 
SELECT t1.column1, t1.column2, t2.column1 FROM table1 t1 
LEFT JOIN table2 t2 ON t1.column3 = t2.column3; 
*/

SELECT d.director_id, d.first_name, d.last_name, mo.movie_name FROM directors d
LEFT JOIN movies mo ON d.director_id = mo.director_id;

SELECT d.director_id, d.first_name, d.last_name, mo.movie_name FROM movies mo
LEFT JOIN directors d ON d.director_id = mo.director_id;

SELECT d.director_id, d.first_name, d.last_name, mo.movie_name FROM directors d
LEFT JOIN movies mo ON d.director_id = mo.director_id
WHERE d.nationality = 'British';

-- RIGHT JOINS

/* 
SELECT t1.column1, t1.column2, t2.column1 FROM table1 t1 
RIGHT JOIN table2 t2 ON t1.column3 = t2.column3; 
*/

SELECT d.director_id, d.first_name, d.last_name, mo.movie_name FROM movies mo
RIGHT JOIN directors d ON d.director_id = mo.director_id;

SELECT d.director_id, d.first_name, d.last_name, mo.movie_name FROM movies mo
RIGHT JOIN directors d ON d.director_id = mo.director_id
WHERE mo.age_certificate = '18';

-- FULL OUTER JOINS

/* 
SELECT t1.column1, t1.column2, t2.column1 FROM table1 t1 
FULL JOIN table2 t2 ON t1.column3 = t2.column3; 
*/

SELECT d.director_id, d.first_name, d.last_name, mo.movie_name FROM directors d
FULL JOIN movies mo ON d.director_id = mo.director_id;

SELECT d.director_id, d.first_name, d.last_name, mo.movie_name FROM directors d
FULL JOIN movies mo ON d.director_id = mo.director_id
WHERE mo.movie_lang IN ('German','Korean')
ORDER BY d.last_name;

-- Joining More Than Two Tables 

/* 
SELECT t1.column, t2.column, t3.column FROM table1 t1
JOIN table2 t2 ON t1.column = t2.column 
JOIN table3 t3 ON t3.column = t2.column;
*/ 

SELECT d.first_name, d.last_name, mo.movie_name, mr.international_takings, mr.domestic_takings
FROM directors d 
JOIN movies mo ON d.director_id = mo.director_id
JOIN movie_revenues mr ON mr.movie_id = mo.movie_id;

SELECT ac.first_name, ac.last_name, mo.movie_name FROM actors ac 
JOIN movies_actors ma ON ac.actor_id = ma.actor_id
JOIN movies mo ON mo.movie_id = ma.movie_id
WHERE mo.movie_lang = 'English'
ORDER BY mo.movie_name;

SELECT d.first_name, d.last_name, mo.movie_name, ac.first_name, ac.last_name,
mr.domestic_takings, mr.international_takings FROM directors d
JOIN movies mo ON d.director_id = mo.director_id 
JOIN movies_actors ma ON ma.movie_id = mo.movie_id 
JOIN actors ac ON ac.actor_id = ma.actor_id 
JOIN movie_revenues mr ON mr.movie_id = mo.movie_id;

-- Union

/* 
SELECT column1, column2 FROM table1 
UNION 
SELECT column1, column2 FROM table2; 
*/

SELECT first_name, last_name FROM directors 
UNION
SELECT first_name, last_name FROM actors;

SELECT first_name, last_name, date_of_birth FROM directors
WHERE nationality = 'American'
UNION
SELECT first_name, last_name, date_of_birth FROM actors
WHERE gender = 'F'
ORDER BY first_name;

-- Union All 

/* 
SELECT column1, column2 FROM table1 
UNION ALL
SELECT column1, column2 FROM table2; 
*/

SELECT first_name FROM directors 
UNION
SELECT first_name FROM actors
ORDER BY first_name;

SELECT first_name FROM directors 
UNION ALL
SELECT first_name FROM actors
ORDER BY first_name;

-- Intersect 

/* 
SELECT column1 FROM table1 
INTERSECT 
SELECT column1 FROM table2; 
*/ 

SELECT first_name FROM directors 
WHERE nationality = 'American'
INTERSECT 
SELECT first_name FROM actors
ORDER BY first_name;

-- Except

/* 
SELECT column1 FROM table1 
EXCEPT
SELECT column1 FROM table2; 
*/

SELECT first_name FROM directors
WHERE nationality = 'American'
EXCEPT
SELECT first_name FROM actors
ORDER BY first_name;



------------------------- SUBQUERIES ----------------------------------------
-- 1. Select the first and last names of all the actors older than Marlon Brando. 
SELECT first_name, last_name FROM actors 
WHERE date_of_birth < 
(SELECT date_of_birth FROM actors
WHERE first_name = 'Marlon'
AND last_name = 'Brando');

-- 2. Select the movie names of all movies that have domestic takings above 300 million. 
SELECT movie_name FROM movies
WHERE movie_id IN
(SELECT movie_id FROM movie_revenues
WHERE domestic_takings > 300.0);

-- 3. Return the shortest and longest movie length for movies with an above average 
--    domestic takings.
SELECT MIN(movie_length), MAX(movie_length) FROM movies 
WHERE movie_id IN
(SELECT movie_id FROM movie_revenues 
WHERE domestic_takings > 
(SELECT AVG(domestic_takings) FROM movie_revenues));



-- 1. Select the first name, last name and date of birth for the oldest actors of each gender. 
SELECT ac1.first_name, ac1.last_name, ac1.date_of_birth FROM actors ac1
WHERE ac1.date_of_birth = 
(SELECT MIN(ac2.date_of_birth) FROM actors ac2 
WHERE ac2.gender = ac1.gender);

-- 2. Select the movie name, movie length and age certificate for movies with an
-- above average length for their age certificate. 
SELECT mo1.movie_name, mo1.movie_length, mo1.age_certificate FROM movies mo1
WHERE movie_length > 
(SELECT AVG(mo2.movie_length) FROM movies mo2
WHERE mo2.age_certificate = mo1.age_certificate)
ORDER BY mo1.age_certificate;



-- Uncorrelated Subqueries Part 1

SELECT movie_name, movie_length FROM movies 
WHERE movie_length > 
(SELECT AVG(movie_length) FROM movies);

SELECT movie_name, movie_length FROM movies 
WHERE movie_length > 126.13;

SELECT AVG(movie_length) FROM movies;


SELECT first_name, last_name, date_of_birth FROM directors 
WHERE date_of_birth >
(SELECT date_of_birth FROM actors 
WHERE first_name = 'Tom'
AND last_name = 'Cruise');

SELECT date_of_birth FROM actors 
WHERE first_name = 'Tom'
AND last_name = 'Cruise';

-- Uncorrelated Subqueries Part 2 

SELECT movie_name FROM movies 
WHERE movie_id IN
(SELECT movie_id FROM movie_revenues
WHERE international_takings > domestic_takings);

SELECT mo.movie_id, mo.movie_name, d.first_name, d.last_name FROM movies mo 
JOIN directors d ON mo.director_id = d.director_id
WHERE mo.movie_id IN
(SELECT movie_id FROM movie_revenues
WHERE international_takings > domestic_takings);

-- Correlated Subqueries 
SELECT d1.first_name, d1.last_name, d1.date_of_birth 
FROM directors d1
WHERE d1.date_of_birth = 
(SELECT MIN(date_of_birth) FROM directors d2
WHERE d2.nationality = d1.nationality);

SELECT MIN(date_of_birth) FROM directors d2
WHERE d2.nationality = d1.nationality;

SELECT mo1.movie_name, mo1.movie_lang, mo1.movie_length FROM movies mo1
WHERE mo1.movie_length = 
(SELECT MAX(movie_length) FROM movies mo2
WHERE mo2.movie_lang = mo1.movie_lang);



-- 1. Select the directors first and last names and movie names in upper case.
SELECT UPPER(d.first_name), UPPER(d.last_name), UPPER(m.movie_name) FROM directors d
JOIN movies m ON d.director_id = m.director_id;

-- 2. Select the first and last names, in initial capitalisation format, of all the actors
-- who have starred in a Chinese or Korean movie.
SELECT DISTINCT INITCAP(a.first_name), INITCAP(a.last_name) FROM actors a 
JOIN movies_actors ma ON a.actor_id = ma.actor_id 
JOIN movies m ON m.movie_id = ma.movie_id
WHERE m.movie_lang IN ('Chinese','Korean');

-- 3. Retrieve the reversed first and last names of each directors and the first three 
-- characters of their nationality. 
SELECT REVERSE(first_name), REVERSE(last_name), LEFT(nationality, 3) FROM directors;

-- 4. Retrieve the initials of each director and display it in one column named ‘initials’. 
SELECT CONCAT_WS('.',LEFT(first_name, 1),LEFT(last_name, 1)) AS initials, first_name, last_name 
FROM directors;


-- UPPER AND LOWER FUNCTIONS 

/* 
SELECT UPPER('string');

SELECT LOWER('string');

SELECT UPPER(column_name) FROM table_name;

SELECT LOWER(column_name) FROM table_name;
*/ 

SELECT UPPER('stop shouting');

SELECT first_name, UPPER(last_name) AS last_name FROM actors;

SELECT * FROM actors;

SELECT LOWER('StOP SHoutiNG');

SELECT LOWER(movie_name) FROM movies;

SELECT movie_name FROM movies;

-- INITCAP STRING FUNCTION 

/* 
SELECT INITCAP('example string'); 

SELECT INITCAP(column_name) FROM table_name; 
*/ 

SELECT INITCAP('eXamplE sTRING');

SELECT movie_name FROM movies;

SELECT INITCAP(movie_name) FROM movies;

-- LEFT AND RIGHT STRING FUNCTIONS 

/* 
SELECT LEFT('string', int); 

SELECT LEFT(column_name, int) FROM table_name; 

SELECT RIGHT('string', int);

SELECT RIGHT(column_name, int) FROM table_name; 
*/

SELECT LEFT('string', 3);

SELECT LEFT(movie_name, 5) FROM movies;

SELECT RIGHT('example', 2);

SELECT RIGHT(first_name, 2) FROM actors;

SELECT * FROM actors;

-- REVERSE FUNCTION

/* 
SELECT REVERSE('string');

SELECT REVERSE(column_name) FROM table_name;
*/

SELECT REVERSE('reverse');

SELECT movie_name, REVERSE(movie_name) FROM movies;

-- SUBSTRING FUNCTION 

/*
SELECT SUBSTRING('string', from, count);

SELECT SUBSTRING(column_name, from, count) FROM table_name;
*/ 

SELECT SUBSTRING('long string', 5, 3);

SELECT first_name, SUBSTRING(first_name, 3, 4) FROM actors;

-- REPLACE FUNCTION 

/* 
SELECT REPLACE('source_string', 'old_string', 'new_string'); 

SELECT REPLACE(column_name, 'old_string', 'new_string') FROM table_name;

UPDATE table_name 
SET column_name = REPLACE(column_name, 'old_string', 'new_string')
WHERE column_name = 'value';
*/
SELECT REPLACE('a cat plays with another cat', 'cat', 'dog');

SELECT * FROM actors;

SELECT first_name, last_name, REPLACE(gender, 'M', 'Male') FROM actors;

SELECT * FROM directors;

UPDATE directors 
SET nationality = REPLACE(nationality, 'Brit', 'Engl')
WHERE nationality = 'British';

-- SPLIT_PART FUNCTION 

/*
SELECT SPLIT_PART('string', 'delimiter', field_number);

SELECT SPLIT_PART(column_name, 'delimiter', field_number) FROM table_name;
*/
SELECT SPLIT_PART('first_name.last_name@gmail.com', '.', 3);

SELECT movie_name, SPLIT_PART(movie_name, ' ', 1) AS first_word,
SPLIT_PART(movie_name, ' ', 2) AS second_word
FROM movies;

-- Using Casting to apply String Functions to Non String Data Types 

/* 
SELECT column_name::DATATYPE FROM table_name; 
*/ 
SELECT * FROM directors;

SELECT date_of_birth::TEXT FROM directors;

SELECT SPLIT_PART(date_of_birth::TEXT, '-', 1) FROM directors;


```



