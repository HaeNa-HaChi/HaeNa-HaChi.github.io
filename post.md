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


# 2020.12.22
## 다시 한 번 관련 업무를 정리해 볼려고 한다.

일단 최근에 사용한 Lucene, Apple 공증관련 지식부터 쌓아보도록 하자 

* Apache Lucene
* Apple Mac OS Application or pkg file 인증서 및 공증


# 2020.12.23
## Lucene

Java Lucene / Lucene.net 같은 버전의 API를 참고한다.
EX) Lucene.net 4.8.0 = The API is similar to Java Lucene 4.8.0, which you may also find helpful to review.

Lucene 경우, 원본 문서에서 1. 텍스트 추출 2. 텍스트 분석 3. 색인

* Default Stop Words set : 불용어(검색엔진이 검색을 수행하는 과정에서 또는 데이터베이스로 색인 하는 과정에서 무시해 버리는 문자열)
* 불용어의 예시로는 한글은 조사, 접속사, 어미 등이 있으며, 영어에는 a, an, in, on 등이 있음.
1	a	16	no	31	was  46	또는
2	an	17	not	32	will
3	and	18	of	33	with
4	are	19	on	34	이
5	as	20	or	35	그
6	at	21	such	36	저
7	be	22	that	37	것
8	but	23	the	38	목
9	by	24	their	39	등
10	for	25	then	40	들
11	if	26	there	41	및
12	in	27	these	42	에서
13	into	28	they	43	그리고
14	is	29	this	44	그래서
15	it	30	to	45	또
-- 약 46개 존재

* String Field vs. Text Field
String Field와 TextField는 tokenize를 여부에 따라 사용 결정
String Field : A field that is indexed but not tokenized: the entire String value is indexed as a single token.
Text Field : A field that is indexed and tokenized, without term vectors.
EX) 보통 String Field는 id, category 등에서 사용

* 한글 분석기 중에 Lucene에서 제공하는 CJKAnalyzer도 있으나, 해당 분석기는 2글자씩 끊어서 다수의 인덱스를 추가하기에 다른 분석기보다 인덱스의 크기가 크다.







