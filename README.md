# StockWeb

<실행 영상>
###
https://youtu.be/LStiBWvVnc4

###

## 프로젝트 이름 : 주식 웹어플리케이션 구현
- 기술 스택 : Python Flask Framework, Crawling(BeautifulSoup, pandas), Bootstrap, matplotlib
- 진행 인원 및 작업 기간 : 2인, 2021.4.10 ~ 2021.5.18
- 본인 담당 작업 : 백엔드 20%(Blueprint, Refactoring), 프론트엔드 100%
- 사용 프로그램 : Visual Studio Code
- 버전 관리 툴 : Git

### 상세기능
 - 사용자가 종목 검색을 하면 주가 정보, 기업 정보, 재무제표를 확인할 수 있다. 
 - 검색 키워드의 공백, 대/소문자가 일치하지 않아도 검색 가능하다. 예) 삼  성전 자, S-OiL
 - 재무제표와 상위 업종/테마 메뉴에서는 pyplot그래프가 추가되어, 데이터를 시각적으로 확인할 수 있다.
 - 데이터를 가져오는 동안 로딩중임을 알리는 Spinner을 웹사이트에 표시했다.

###

## 프로젝트 내용
< 개요 >
- Blueprint
- Main page
- Check page
- Statistics page
- Domain 발급

###

### 1.Blueprint

![image](https://user-images.githubusercontent.com/69899248/212120783-2b87bd90-c033-41db-b952-db8f2e3a0350.png)

MVC구조에서 C에 해당하는 Controller은 사용자가 요청한 URL를 확인해서, 해당 요청을 담당하는 메소드로 매핑시켜주는 역할을 한다. 그리고 이 메소드에서는 요청에 대한 처리(DB 등)가 이루어지고, 최종적으로 사용자에게 결과 페이지를 보여주기 위해 View로 이동시키게 된다.

그런데, 이 Controller처리를 한 파일에서 모두 수행한다면 소스코드가 매우 길어져서 유지보수는 상당히 어려워지게 된다. 그래서 Flask에 Blueprint를 도입하게 되었다.

Blueprint는 상위 경로와 하위 경로를 각각의 파일로 계층적으로 관리하기 위한 Flask의 기능이다.

### 

### 2. Main page

[이미지1]
![image](https://user-images.githubusercontent.com/69899248/212121342-00d89b64-6f78-4b35-b129-07aba30dd72a.png)

[이미지2]

carousel : 슬라이드쇼 기능 (interval=2.5초)

![image](https://user-images.githubusercontent.com/69899248/212121415-698fb559-1085-4db4-a5c9-4177cded0a11.png)

### 3. Check page

[이미지1]
![image](https://user-images.githubusercontent.com/69899248/212121561-06e0255d-9f1b-4ba3-91f1-048b05206166.png)
[이미지2]
![image](https://user-images.githubusercontent.com/69899248/212121635-bb2fe188-9347-4080-9dad-d58764324748.png)

### 4. statistics page

1) 지수 차트

![image](https://user-images.githubusercontent.com/69899248/212121721-4650bdd8-fc7c-460b-96f7-87a609680588.png)

2) 상위 업종/테마

![image](https://user-images.githubusercontent.com/69899248/212121830-bf345a14-019d-4a1f-8917-2a5ea49f6a56.png)

3) 시가 총액 상위

![image](https://user-images.githubusercontent.com/69899248/212121885-9b66b93c-b853-4c07-9a59-60433c5d923a.png)

4) 거래량 상위

![image](https://user-images.githubusercontent.com/69899248/212121925-eb37b472-efbb-4459-a750-05e9266c0dd5.png)

5) 상한가/하한가 종목

![image](https://user-images.githubusercontent.com/69899248/212121970-3d35bdc1-3ee6-4963-a2d8-14a5e78e7550.png)

6) 관리/정지 종목

![image](https://user-images.githubusercontent.com/69899248/212122035-04ac6f6e-c126-4bd1-a00e-834274d22e1a.png)

###

### 5. Domain 발급

![image](https://user-images.githubusercontent.com/69899248/212122104-7af1eadc-db36-4732-afa0-cb5bd5a73632.png)




