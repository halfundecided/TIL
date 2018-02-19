### 생활코딩 강의

#### MySQL server 접속 
- `mysql -uroot -p`

#### MySQL Schema의 사용
- Database 생성: `CREATE DATABASE opentutorials;`
- Database 삭제: `DROP DATABASE opentutorials;`
- 생성확인: `SHOW DATABASES;` or `SHOW SCHEMAS;`
- Database 사용: `USE opentutorials;`

#### SQL과 테이블 구조 
- SQL? Structured Query Language: MySQL 서버가 알아들을 수 있는 언어
- 행과 열

#### MySQL 테이블의 생성
````mysql
CREATE TABLE topic(
	id INT(11) NOT NULL AUTO_INCREMENT,
	title VARCHAR(100) NOT NULL,
	description TEXT NULL,
	created DATETIME NOT NULL,
	author VARCHAR(15) NULL,
	profile VARCHAR(100) NULL,
	PRIMARY KEY(id)
	);
````

#### CRUD
- Create
- Read
- Update
- Delete

#### SQL의 INSERT
- `DESC topic;`
- `INSERT INTO topic ( ...`
- `SELECT * FROM topic;`
- `SELECT title, description FROM topic;`
- `SELECT egoing FROM author;`
- `SELECT id,title,created,author FROM topic WHERE author='egoing' ORDER BY id DESC`;`

#### SQL의 UPDATE
- `UPDATE topic SET description='Oracle is ..', title='Oracle' WHERE id=2;`
- WHERE문 빠트리지 않기!

#### SQL의 DELETE
- `DELETE FROM topic WHERE id=5;`

#### Relational Database 
- `SELECT * FROM topic LEFT JOIN author ON topic.author_id = author.id;`

#### Internet & database
- mySQL: commands를 통해서 database server을 제어하는 것.
 
