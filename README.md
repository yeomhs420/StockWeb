# StockWeb

<실행 영상>
###
https://youtu.be/LStiBWvVnc4

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


## 프로젝트 내용
< 개요 >
- Blueprint
- Main page
- Check page
- Statistics page
- Domain 발급

### Blueprint

![image](https://user-images.githubusercontent.com/69899248/212120783-2b87bd90-c033-41db-b952-db8f2e3a0350.png)

MVC구조에서 C에 해당하는 Controller은 사용자가 요청한 URL를 확인해서, 해당 요청을 담당하는 메소드로 매핑시켜주는 역할을 한다. 그리고 이 메소드에서는 요청에 대한 처리(DB 등)가 이루어지고, 최종적으로 사용자에게 결과 페이지를 보여주기 위해 View로 이동시키게 된다.

그런데, 이 Controller처리를 한 파일에서 모두 수행한다면 소스코드가 매우 길어져서 유지보수는 상당히 어려워지게 된다. 그래서 Flask에 Blueprint를 도입하게 되었다.

Blueprint는 상위 경로와 하위 경로를 각각의 파일로 계층적으로 관리하기 위한 Flask의 기능이다.
