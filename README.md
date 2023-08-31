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

**페이징 검색 필터 개선**

- 사용자가 편리하게 페이징된 결과를 검색하고 필터링할 수 있는 기능을 구현했습니다.
- 기존의 제목과 내용 검색만 가능한 기능을 6개의 필터로 확장하여 사용자 경험을 향상시켰습니다.
- 이를 위해 QueryDSL을 활용하여 동적인 검색 쿼리를 생성하였습니다.

**통합 로그인 환경**

- 시스템 내에서 다양한 로그인 방식을 지원하기 위해 Spring Security를 사용하여 자체 로그인 및 OAuth2를 통한 통합 로그인 시스템을 구축하였습니다.
- 사용자가 편리하게 원하는 로그인 방식으로 접속하고 이용할 수 있도록 하였습니다.

**JSON 직렬화 문제 해결**

- Entity 간의 관계로 인해 발생하는 JSON 직렬화 문제를 해결하기 위해 DTO(Data Transfer Object)를 도입하였습니다.
- DTO를 활용하여 필요한 데이터만 전달하면서 데이터의 통신 안정성을 높이고 성능을 개선하였습니다.

**글쓰기시 이미지의 순서 변경**

- 사용자가 글을 작성할 때 대표 사진 및 기타 이미지의 순서를 변경하고 저장할 수 있는 기능을 개발하였습니다.
- React의 dnd-kit 라이브러리를 활용하여 드래그 앤 드롭 기능을 구현하였으며, 변경된 순서를 서버에 반영하여 데이터의 일관성을 유지하도록 처리했습니다.

**Kakao Map API 활용**

- Kakao Map API를 통해 거래 장소 선택 기능을 구현하였습니다. 사용자가 원하는 지역을 정확하게 선택할 수 있도록 마커의 움직임과 행정 중심지 입력 기능을 제공했습니다.
- 또한 거래 게시판에서 거래 범위 확대 및 축소 기능을 구현하여 사용자가 원하는 범위 내에서 다양한 거래를 찾을 수 있도록 지원하였습니다.

**웹 크롤링**

- 상품 카테고리 정보를 동적으로 크롤링하여 구현하는 과정에서 Python의 BeautifulSoup과 Selenium을 활용하여 사이트의 카테고리 정보를 수집하고 활용하였습니다.
- 이를 통해 사용자가 원하는 상품 카테고리를 정확하게 선택할 수 있는 기능을 제공하였습니다.

**NAVER SENS API 활용하여 본인 확인 문자 메시지 인증 및 정규식으로 유효성 체크**

- NAVER SENS API를 활용하여 본인 확인 문자 메시지 인증 기능을 구현하였고, 입력값의 유효성을 검사하기 위해 정규식을 사용하였습니다.
- 이를 통해 사용자의 입력값을 신뢰성 있게 처리하고 보안을 강화하였습니다.

**전반적인 스키마 설계 도움**

- 팀원들에게 전반적인 스키마 설계 도움을 주어 JPA로 데이터베이스의 구조와 관련하여 효율적인 설계 방법을 제안하고 도움을 주었습니다.

위 프로젝트를 통해 저는 다양한 기술과 도구를 활용하여 웹 애플리케이션을 구축하고 사용자의 편의성과 경험을 개선하는 역할을 수행하였습니다. 이러한 경험을 통해 문제 해결 능력과 협업 능력을 향상시키며 더 나은 서비스 개발에 기여했습니다.


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
