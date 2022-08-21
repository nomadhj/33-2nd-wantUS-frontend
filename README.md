# 33기 2차 프로젝트 - wantUs 프론트 엔드

## 개요 

- 내용 : wanted 웹페이지 클론코딩 프로젝트
- 기간 : 2022.06.07 ~ 06.17
- 인원 : 총 6명 (프론트엔드: 4명, 백엔드: 2명)
- 구현 기능
  - Nav, Footer, 메인페이지
  - 소셜 로그인 페이지
  - 마이페이지 / 이력서페이지 / 좋아요페이지
  - 채용 공고 리스트 / 채용 상세 페이지
  - 검색바 / 검색 결과

## 사용한 stack & tool (front-end 공통)
- HTML5, CSS3(styled component), JavaScript, React
- github, slack, trello

## 기능 구현 영상 링크
- https://www.youtube.com/watch?v=SqFNWewFKKk

## 담당 구현 기능

### 채용공고리스트, 검색바/검색결과페이지


![infinite scroll](https://user-images.githubusercontent.com/101119985/174231973-78152b27-9222-4f5f-89b0-f6d7a3bf8e13.gif)

- 채용공고리스트
  - 페이지네이션 기능을 활용, 무한 스크롤 페이지 구현
  - interSection Observser API를 활용한 성능 최적화
    - 스크롤에 이벤트를 부여하는 방식에서 interSection Observer API 활용하는 방식으로 변경
    - 데이터의 마지막 요소를 관찰대상으로 지정하고 해당 관찰 대상이 80% 이상 관측 될 때 새로운 데이터를 불러오도록 구현
  - Query Parameter를 활용한 다중 필터 기능
    - 채용직무, 회사위치, 경력, 기술스택, 날짜/인기 순 총 5개 
  - 서버로부터 데이터 로딩 중 로딩 되는 데이터 수 만큼 skeleton UI를 띄워주도하여 유저 친화적인 구성을 할 수 있도록 노력함
  - 검색 결과 페이지에서 좋아요 버튼 클릭 시 해당 내용 서버로 전달 (데이터 좋아요 페이지 연동)
  - 각 아이템 클릭 시 채용상세페이지로 이동 
![search](https://user-images.githubusercontent.com/101119985/174230995-46e5ddf6-25a6-420d-9932-f1d881c75244.gif)

- 검색바/검색결과페이지
  - 검색 모달 창 및 검색 결과 페이지 구현
  - useLocation을 활용, 검색 모달창에 입력한 내용을 백엔드 엔드포인트로 전달하여 검색 결과를 불러옴
  - 검색 결과 페이지에서 좋아요 버튼 클릭 시 해당 내용 서버로 전달 (데이터 좋아요 페이지 연동)
  - useParams 활용, 각 아이템 클릭 시 채용상세페이지로 이동 
