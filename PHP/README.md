# PHP Basic

## php?
php는 서버측에서 실행되는 프로그래밍 언어로 HTML을 프로그래밍적으로 생성
해주고, 데이터베이스와 상호작용을 하면서 데이터를 저장하고, 표현한다. 사용자가 >업로드한 파일을 서버에 저장하거나, 사용지가 입력한 데이터를 받아서 데이터베이스>나 파일에 저장하고, 저장된 정보를 불러와서 HTML을 생성해서 웹 브라우저로 전송하>는 등의 일을 한다.

## install php on Mac
https://bitnami.com/stack/mamp/installer

 ## web hosting
- paran web hosting service 
  + http://bizfree.kr
- cloud computing 
  + amazon web service 
  + https://opentutorials.org/course/608/3002
  + https://www.000webhost.com

## configuration 
- PHP가 동작하는 기본적인 작동방법을 변경
- php.ini 를 통해 변경 
- 에러설정 
  + error off 경우: 실서버
  + error on  경우: 개발환경
- service
````php
display_errors = Off
display_startup_errors = Off
error_reporting = E_ALL
log_errors = On
````
- develop
````php
display_errors = On
display_startup_errors = On
error_reporting = -1
log_errors = On
````

## First attempt
- http://localhost:8080/o2_php/helloworld.php
- code의 구조: 모든 코드는 <?php ?>안에 와야 php파일로써 작동함
````php
<?php
   ...
?>
````
## print
`echo "Hello world";` 

## why?

## data types
- check data type
`var_dump(data);`
- string
  + 1234: number
  + "1234": string
  + 문자열들을 합칠때: `echo "hello"."world";`
  + 문자열 안에 따옴표 쓸때: `\"` 

## variable 
- declare a variable 
`$a=1;`
`$first = "coding";`
- 변수를 선언할때 데이터형을 미리 지정할 필요가 없다.

## comment
- one line comment
`#this is my first comment`
- multiple lines 
````php
/*
s
t
a
r
t
/* 
````

## const
- declare 
`define('TITLE', 'PHP Tutorial');
- gettype & settype
  + gettype: 데이터형 검사
  + settype: 데이터타입 변경
````php
<?php
  $a = 100;
  echo gettype($a);
  settype($a, 'double');
  echo '<br />';
  echo gettype($a);
?>
````

## compare
skip

## input/output
````php
<?php
echo $_GET['id'];
?>
````
위와 같이 코드작성 후, 해당 URL뒤에 ?id=qksalwjd93 라고 입력하면브라우저에 qksalwjd93이 출력된다.
- 이것은 php 어플리케이션은 url을 통해서 데이터를 입력 받을 수 있다는 의미. 
  + ?: 주소와 입력 데이터의 구분자
  + $: 값과 값 사이의 구분자
  + =: 이름과 값 사이의 구분자

## Form
- `action= '해당 php파일'`
- method
  + GET: url에 데이터를 첨부해서 전송하는 방식, 정보에 대한 링크로 많이 사용 
  + POST: HTTP 메시지의 본문에 데이터를 포함해서 전송, 아이디나 비밀번호와 같은 데이터를 전송하는 방식->url에 데이터 포함X
 
## condition1
- 조건문을 form 에 활용할 수 있다
   + id 검사하는 경우
````php
<?php
if($_GET['id'] === 'qksalwjd93'){
  echo 'hello mijeong!';
} else {
  echo 'who are you?';
}
?>
````
````html
<!DOCTYPE html>
<html>
  <body>
    <form class="" action="condition1.php" method="get">
      <input type="text" name="id" value="">
      <input type="submit" name="" value="submit">
    </form>
  </body>
</html>
````

  + id & password 검사하는 경우, nested if statement
````php
<?php
if($_POST['id'] === 'qksalwjd93'){
  if($_POST['password'] === '8818') {
    echo 'hello mijeong!';
  } else {
    echo 'wrong password';
  }
} else {
  echo 'wrong id';
}
?>
````
````html
<!DOCTYPE html>
<html>
  <body>
    <form class="" action="condition2.php" method="post">
      id: <input type="text" name="id">
      password: <input type="text" name="password">
      <input type="submit" value="submit">
    </form>

  </body>
</html>
````

## condition2
&& || 
- 논리 연산자를 이용한 id & password check 
````php
<?php
if($_POST['id'] === 'qksalwjd93' && $_POST['password'] === '8818') {
  echo 'hello mijeong!';
} else {
  echo 'wrong';
}
?>
````
````html
<!DOCTYPE html>
<html>
  <body>
    <form class="" action="condition3.php" method="post">
      id: <input type="text" name="id">
      password: <input type="password" name="password">
      <input type="submit" name="" value="submit">
    </form>
  </body>
</html>
````
- another example
````php
<?php
if(
    ($_POST['id'] === 'irene' || $_POST['id'] === 'qksalwjd93' || $_POST['id'] === 'mjban')
    &&
    $_POST['password'] === '8818'
){
    echo 'right';
} else {
    echo 'wrong';
}
?>
````
````html
<!DOCTYPE html>
<html>
  <body>
    <form class="" action="condition4.php" method="post">
      id: <input type="text" name="id">
      password: <input type="password" name="password">
      <input type="submit" name="" value="submit">
    </form>

  </body>
</html>
````

## loop
- while  
````php
while(condition) {
	...
	...
}
````
- for 
````php
for($i = 0; i < 10; i++){
	echo 'hello';
}
````

## function
- 기본 구조
````php
function 함수명([인자 ...]) {
	...
	return 반환값;
}
````
- argument
````php
<?php
function get_argument($arg){
  return $arg;
}

print get_argument(1);
print get_argument(2);

?>
````
- argument's default value 
````php
<?php
function get_arguments($arg1=100){
  return $arg1;
}

echo get_arguments(1); #return 1
echo ', ';
echo get_arguments(); #return 100
?>
````

## Array
- declare
  + `$member = ['mijeong', 'irene', 'mjban'];`
  + `$member = array('mijeong', 'irene', 'mjban');
- call
  + `$member[0]` or `$member[1]`

- array size
````php
<?php
$l = [1, 2, 3, 4, 5];
echo count($l);
?>
```` 
- add element 
  + add one element: `array_push($arr, 'a');`
  + add multiple elements: `$li = array_merge($li, ['f', 'g']);`
  + add elem at the beginning: `array_unshift($li, 'z');`
  + add elem at the specific placd: `array_splice($li, 2, 0, 'B');`
- remove element
  + remove first elem: `array_shift($li);`
  + remove last elem: `array_pop($li);`
- sort array
  + sort `sort($li);`
  + reverse `rsort($li);`

## 연관배열, associative array, hash, dictionary
- `$grades = array('egoing'=>10, 'k8805'=>6, 'sorialgi'=>80);`
````php
<?php
$grades = [];
$grades['egoing'] = 10;
$grades['k8805'] = 6;
$grades['sorialgi'] = 80;
var_dump($grades);
?>
````

## include 
- 다른 php파일을 코드 안으로 불러와서 사용하는 것
- `include 'filename.php'`
- commands
  + include
  + include_once: load once
  + require
  + require_once

## namespace 
