# JavaScript & Vue.js 실습

해당 실습은 [Inflearn 실습 UI 개발로 배워보는 순수 javascript 와 VuesJS 개발](https://www.inflearn.com/course/%EC%88%9C%EC%88%98js-vuejs-%EA%B0%9C%EB%B0%9C-%EA%B0%95%EC%A2%8C/)의 김정환 강사님의 [Github 레파지토리](https://github.com/jeonghwan-kim/lecture-vue/tree/master/1-vanilla)의 소스를 클론하여 사용합니다.

## 패턴 설명

### MVC 패턴(Vanilla JS)

- Model, View, Controller의 약자
- Model: 백엔드 API를 통한 데이터 관리(전달, 저장)
- View: Model 데이터를 기반으로한 화면 구성(HTML, CSS, JS) 및 사용자 입력 데이터 처리
- Controller: Model과 View를 연결하는 역할을 수행. 모델 데이터를 View에 전달 및 View로부터 사용자 입력 데이터를 받아 모델에게 전달

### MVVM 패턴(Vue.js)

- Model, View, ViewModel의 약자
- Model과 View는 MVC의 MV와 같다.
- VM(ViewModel)은 Model과 View 사이에 위치함
- VM(ViewModel)은 Model로 부터 View에 적합한 데이터로 가공하여 가져오므로 ViewModel이 변결될 때마다 연관된 화면의 데이터가 변경되어 갱신됨
- 하나의 View에는 하나의 VM(ViewModel)이 1:1로 매칭됨

<br>

## 실습 프로젝트 요구분석


### 검색폼 구현

- 검색 상품명 입력 폼을 위치시키고 검색어가 없는 경우엔 x 버튼을 노출시키지 않음
- 검색어를 입력하면 x 버튼이 노출됨
- 엔터를 입력하면 검색 결과가 보임(컨트롤러에게 위임)
- x 버튼을 클릭하거나, 검색어를 삭제하면 검색 결과를 삭제

### 검색 결과 구현

- 검색 결과가 검색폼 아래 위치 및 결과 노출
- x 버튼을 클릭하면 검색 폼이 초가화되며 검색 결과가 사라짐

### 탭 구현

- 추천 검색어, 최근 검색어 탭이 검색 폼 아래에 위치
- 기본적으로 추천 검색어 탭을 선택
- 각 탭을 클릭하면 탭 아래 내용이 변경됨

### 추천 검색어 구현

- 번호와 추천 검색어 목록이 탭 아래 위치
- 목록에서 검색어를 클릭하면 선택된 검색어로 검색 결과 화면으로 이동
- 검색 폼에 선택된 추천 검색어 설정

### 최근 검색어 구현

- 최근 검색어, 목록이 탭 아래에 위치
- 목록에서 검색어를 클릭하면 선택된 검색어로 검색 결과 화면으로 이동
- 검색 일자 및 버튼 목록 노출
- 목록에서 x 버튼을 클릭하면 선택된 검색어가 최근 검색어 목록에서 삭제
- 검색 마다 최근 검색어 목록에 해당 검색어 추가
