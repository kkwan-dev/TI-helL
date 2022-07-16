# DATABASE ISSUE

## CASE 01

### Issue

Tool(DataGrip, ...)을 통해 데이터베이스 덤프 시도 시  정상적으로 데이터베이스 덤프가 되지 않음

### Solution

로컬 환경에 데이터베이스 엔진(MySQL, MariaDB, ...)을 설치하지 않고, 컨테이너만을 활용하여 데이터베이스를 사용하다보니 해당 이슈가 발생하였음.

따라서 다음과 같이 로컬에 데이터베이스 엔진 설치 후 시도하면 정상적으로 데이터베이스 덤프가 되는 것을 확인 할 수 있음.

```sh
brew install mysql@5.7
brew install mysql-client
brew install --cask mysqlworkbench

sudo ln -s /Applications/MySQLWorkbench.app/Contents/MacOS/mysql /usr/local/bin/mysql
sudo ln -s /Applications/MySQLWorkbench.app/Contents/MacOS/mysqldump /usr/local/bin/mysqldump
```
