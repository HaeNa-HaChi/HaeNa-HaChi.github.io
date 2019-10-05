# 2019.10.05
## 오랜만에 개발환경 설치!

개발 노트북 업그레이드를 위해 노트북 구입으로 인해 기존의 사용했던 개발환경이 다 날아갔다.ㅠㅠ  
그러므로 하나하나 다시 셋팅해야하는데....  
일단!  

* JAVA JDK 1.8
* SPRING 3.9.8
* MAVEN, MYBATIS 등 SPRING관련 
* Tomcat 9 version (사용하는 프로젝트 servlet 4.0)

설치 후, 기존 프로젝트 IMPORT!  

p.s.1
기존 프로젝트 import 시, spring 버전 확인!  
pom.xml 오류 가능성 높아짐. -> maven (.m2폴더 삭제 후, update)   
/ 해당 파일의 버전이 https://mvnrepository.com 있는지 확인!  
  
  
p.s.2
ms-sql jdbc 6.1 이후로 부터 maven 연동 가능!!  
json simple도 가능..  
항상 검색 안하고 외부 jar 썼다가... 시간 엄청 지체함ㅠ
