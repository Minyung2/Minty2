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

## 담당한 기능

- **통합 로그인 환경**
    - Spring Security로 자체로그인과 OAuth2를 Success Handler로 구분하여 통합 로그인 구현
- **Thymeleaf 와 다르게 동작하는 React Csrf 문제**
    - React에서 Backend에 csrf token 값을 요청하여 App.js에서 필요한 컴포넌트에 할당하여 문제 해결
- **페이징 검색 필터 개선**
    - QueryDSL을 활용하여 기존 제목, 내용만 가능했던 1개 필터에서 6개로 개선
- **ManyToOne 직렬화 문제 해결**
    - 기존에 Entity와 바로 접근하면서 발생한 Json Serializable 에러를 DTO로 해결
    - DTO로 스키마의 필요한 속성만 가지고 오는 것의 안정성 학습
- **글쓰기시 이미지의 순서 변경**
    - React의 dnd-kit 라이브러리를 활용하여 대표 사진, 이미지 순서를 바꾸고 최종 Post 요청시 Backend에 반영
- **거래게시판 거래 범위 확대 및 축소 기능**
    - GeoJson과 React의 turf 라이브러리로 인증된 동네의 범위 내에서 1~3단계까지 가능하도록 구현
- **Kakao Map API 활용 거래 장소 잡기 기능**
    - 공식 참조 사이트를 통해 각종 마커 및 마커의 움직임 , 마커에 따른 행정 중심지입력 등 다양하게 활용하여 구현
- **NAVER SENS 본인 확인 문자 메시지 인증 및 정규식으로 유효성 체크**



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
