### Introduction

- CGI: Common Gateway Interface 
  + 서버와 응용프로그램 사이에 데이터를 주고받기 위한 표준화된 방법

- Python installing
  + `brew upgrade python`

- Apache & Python CGI 연동방법
  1. config - httpd file
  2. `LoadModule cgid_module modules/mod_cgid.so` 활성화
  3. Inside of <Directory> tag, add 
```
    <Files *.py>
      Options ExecCGI
      AddHandler cgi-script .py
    </Files>
```
  4. `type python3` 실행 후 경로를 .py 파일 안에 가장 첫 라인에 #!와 함께 추가
  5. `sudo chmod a+x filename.py`로 add permission 

- 웹서버 실행 Root 변경 원할 시 
  + config - httpd.config
  + DocumentRoot 변경
