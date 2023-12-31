![header](https://capsule-render.vercel.app/api?type=rounded&color=timeGradient&text=Minty%20&animation=twinkling&fontSize=40&fontAlignY=50&fontAlign=50&height=180)

## 🖥️Introduction
**개인상점을 간편하게 관리하고 거래할 수 있도록 도와주는 중고거래 플랫폼 웹사이트**입니다.
코로나19로 인한 여파로 소극적이게 변한 외부활동, 보다 더 편리하고 새로운 서비스로 사람들의 관심을 사 중고거래를 다시 활성화시키고자 하는 의도를 담아 개발했습니다.

이 프로젝트는 저의 첫 API 사용 경험이었습니다. API를 활용함으로써, 웹 개발에서 정보의 중요성과 데이터 연결의 복잡성을 체감할 수 있었고, API를 통해 외부 시스템과의 연동이 얼마나 강력한 도구가 될 수 있는지를 체험할 수 있었습니다.

최근에 인기가 많은 React 를 적용하여 각 컴포넌트가 독립적으로 동작하고 재사용 하여 가독성을 향상시키고 중복을 줄여주었습니다.
또한, Vritual DOM 을 이해하고 사용하면서 화면 렌더링 과정의 효율성에 대해 배울 수 있었고, 
React의 생명주기 메서드와 Hook 등의 개념을 이해하고 적용하면서, 동적인 웹 애플리케이션 개발에 대한 깊은 이해를 얻을 수 있었습니다.

이 경험은 저에게 많은 도전과 학습의 기회를 제공했고, 이를 통해 웹 개발에 대한 보다 깊은 이해와 역량을 키울 수 있었습니다.
앞으로도 React프레임워크와 API를 적극 활용하여, 효과적이고 최신 기술 기반의 프로젝트를 구축하겠습니다.

### 주요 기능
사용자 : 중고물품 판매, 급해요 시스템, 시세 조회, 잔고 충전 출금, 포인트 서비스, 이벤트(출석,룰렛), 채팅, 지역채팅, 고객문의, 광고문의
<br>
관리자 : 대시보드, 사용자 관리, 컨텐츠 관리, 마케팅 관리, 수입 관리, 통계, 메인페이지 관리, 고객지원

## 🔨 Technology Stack(s)

* Frontend : HTML5, CSS3, JavaScript, React
* Backend : Java, Python
* Framework : Spring boot
* Database : MySQL
* Version Control : GitHub

## 역할	
총 8명의 팀원으로 구성된 팀에서 풀스택 개발과 기술 멘토 역할 수행


## 담당한 기능

### 회원가입
- 작업 내용 : 정규식으로 유효성 체크 NAVER API와 통신하는 방식으로 본인 확인 문자 메시지 인증 기능을 구현. [SmsService](https://github.com/Minyung2/Minty2/blob/master/src/main/java/com/Reboot/Minty/member/service/SmsService.java)
- 아쉬웠던 점 : DTO로 기본적인 정규식, Null 체크 등의 유효성 체크만 하던 부분이 아쉬움. 
- 해결 방안 : Validator를 상속받아 유효성 체크를 구현할 수 있다는 것을 배웠고 중복 체크, 비밀번호 체크 등 뷰 파일에서 어떤 부분에서 사용자의 입력 값이 틀렸는지 체크하고 제공. [JoinFormValidator](https://github.com/Minyung2/Minty2/blob/master/src/main/java/com/Reboot/Minty/member/service/JoinFormValidator.java)
### 통합 로그인 환경
- 작업 내용 : 사용자 보안을 위해 Spring이 제공하는 Spring Security를 사용. 사용자 경험을 위해 간편로그인 OAuth2를 활용하여 구현. 
- 어려웠던 점 : 통합 로그인의 처리에 어려움을 겪음.
- 해결방안 : 자체 로그인과 OAuth2의 엔트리 포인트가 다르다는 것을 활용하여 엔트리 포인트를 구분하여 로그인 성공 처리. [SecurityConfig](https://github.com/Minyung2/Minty2/blob/master/src/main/java/com/Reboot/Minty/config/SecurityConfig.java)
### 게시판 CRUD 페이징
- 작업 내용 : 중고 거래 게시물을 무한 스크롤로 페이징 구현 및 각종 검색 필터 적용.
- 어려웠던 점 : 기존 카테고리와 제목/내용만 가능했던 검색 필터의 아쉬움.
- 해결방안 : JPA의 비즈니스 로직을 구성하는데 집중할 수 있는 장점을 유지하기 위해 JPQL보단 QueryDSL을 활용하여 동적인 검색 쿼리를 생성. 정렬방법, 최소/최대가격, 판매하는 사용자 명 등 필터를 확장하여 사용자 경험을 향상. [TradeBoardController](https://github.com/Minyung2/Minty2/blob/6a20b3f513788587bce62b9f96f5cf231870fd41/src/main/java/com/Reboot/Minty/tradeBoard/controller/TradeBoardController.java#L116), [TradeBoardCustomRepository](https://github.com/Minyung2/Minty2/blob/master/src/main/java/com/Reboot/Minty/tradeBoard/repository/TradeBoardCustomRepository.java)
### 게시판 CRUD 원하는 거래 범위 지정
- 작업 내용 : 거래게시판 페이지에서 거래 범위 단계별 지정. 인증한 위치 기반으로 범위를 3단계까지 확장.
- 어려웠던 점 : 프로젝트 구현 중 가장 어려웠던 부분으로 카카오 맵 API로 범위 지정 UI를 구현하는데 어려움을 겪음.
- 해결방안 : GeoJson을 활용하여 행정동 이름을 비교하고 Multipolygon 프로퍼티를 활용하여 카카오가 제공하는 Polygon 함수로 구현. [drawPolygon](https://github.com/Minyung2/Minty2/blob/6a20b3f513788587bce62b9f96f5cf231870fd41/src/main/reactview/src/component/boardList.js#L458)
### 게시판 CRUD 글쓰기, 수정
- 작업 내용 : 드래그 앤 드롭으로 이미지 순서 변경, 대표이미지 설정. 파이썬으로 카테고리를 스크래핑 하였고 사용자가 정확하게 선택하는 기능 제공. 
- 어려웠던 점 : 이미지 파일 첨부 시 사용자가 의도한 대로 이미지 순서나 대표 이미지를 설정할 수 없었던 문제.
- 해결방안 : React의 dnd-kit 라이브러리를 활용하여 컴포넌트에 담아 상태 관리. [sortablePhoto](https://github.com/Minyung2/Minty2/blob/master/src/main/reactview/src/component/sortablePhoto.js), [dndContext](https://github.com/Minyung2/Minty2/blob/6a20b3f513788587bce62b9f96f5cf231870fd41/src/main/reactview/src/component/tradeForm.js#L292C37-L292C37)
### 게시판 CRUD  글 상세보기
- 작업 내용 :
1. 부트스트랩 이미지 리스트를 부트스트랩 Carousel로 순차적으로 넘기고 해당 사진은 크게 Modal로 띄워주는 방식.[Carousel](https://github.com/Minyung2/Minty2/blob/6a20b3f513788587bce62b9f96f5cf231870fd41/src/main/reactview/src/component/boardDetail.js#L163)
2. 글쓴이의 개인 상점 정보 및 해당 상품의 링크, 해당 글쓴이의 모든 글로 접근 가능 한 버튼 - 거래 희망 지역. [userItemSellList](https://github.com/Minyung2/Minty2/blob/6a20b3f513788587bce62b9f96f5cf231870fd41/src/main/reactview/src/component/boardDetail.js#L239C58-L239C58)
3. 글쓴이에게 수정 / 삭제 버튼 생성, 이외 사용자인 경우 채팅, 찜하기 버튼 생성. 
### 거래 위치 잡기
- 작업 내용 : Kakao Map API 공식 참조 사이트를 거래 장소 선택 기능을 구현. 사용자가 원하는 지역을 정확하게 선택할 수 있도록 마커의 움직임과 행정 중심지 입력 기능을 제공.
###  기타 해결한 문제점  기여한 부분
- JSON 직렬화 문제 해결
Entity 간의 참조관계로 인해 JSON 으로 변환 과정에서 서로의 엔티티를 순환 참조하면서 발생하는 Json Serializable Error를 경험.
직렬화 문제를 해결하기 위해 DTO(Data Transfer Object)를 도입. 필요한 데이터만 전달하면서 데이터의 통신 안정성을 높이고 성능을 개선.
- 인터셉터 활용
인터셉터를 활용하여 사용자가 인증한 위치 정보가 없으면 입력하도록 유도 [userLocationInterceptor](https://github.com/Minyung2/Minty2/blob/master/src/main/java/com/Reboot/Minty/interceptor/UserLocationInterceptor.java)
- 전반적인 스키마 설계 도움
JPA로 데이터베이스의 구조와 관련하여 효율적인 설계를 제안하고 도움
<br><br>

## 구현 스크린샷
### 거래게시판 페이징
<img src="https://github.com/Minyung2/Minty2/assets/90165157/c05c9cc0-bc59-48c6-a82b-65917a300fd2" width="800" height="400"/>

### 거래게시판 거래 지역 범위 지정
<img src="https://github.com/Minyung2/Minty2/assets/90165157/85e0ecc3-820b-4f26-bc7f-4cad5a25b785" width="800" height="400"/>

### 거래게시판 글 상세보기
<img src="https://github.com/Minyung2/Minty2/assets/90165157/24421a33-376e-4609-b745-63506c5e2814" width="800" height="400"/>

### 거래게시판 글쓰기, 수정
<img src="https://github.com/Minyung2/Minty2/assets/90165157/74d74cb2-5ece-4992-8555-7d9f43c1efc0" width="800" height="400"/>

### 거래 위치 잡기
![image](https://github.com/Minyung2/Minty2/assets/90165157/1c4d834e-5fa3-417e-a10e-93052e3a9aca)

### 회원가입
![image](https://github.com/Minyung2/Minty2/assets/90165157/8fcb7aba-53fe-4046-b4ed-2c7143232813)

### 통합 로그인 환경
![image](https://github.com/Minyung2/Minty2/assets/90165157/10863acb-616b-4f84-a64d-103f491ed754)




<br>
