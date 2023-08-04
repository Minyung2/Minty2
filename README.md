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
* Database : My SQL
* Version Control : Git, GitHub

### 담당한 기능

### **Backend**

- 회원가입 / 스프링 시큐리티, OAuth2 ****간편 로그인
- 거래게시판 Querydsl로 동적인 검색 필터 적용
- 거래게시판 글쓰기
- 거래게시판 상세보기
- 거래게시판 지도 거래 장소 확대 및 축소 기능
- 카카오 지도 API로 위치 인증, 거래 장소 잡기 기능
- 네이버 SENS API로 회원가입 시 본인인증 기능

### **Frontend**

- 리액트 : 거래게시판 리스트, 상세보기, 글쓰기 UI
- 타임리프 : 회원가입, 로그인

- ### 기능 구현 중 어려웠던 상황과 극복 과정

1. **페이징 로직의 변화** - 최초 페이징 구현은 1~10 처럼 페이징 버튼으로 구현 하였었는데 강사님과의 피드백 과정에서 이미 수업 과정에서 동일 페이징을 구현해 봤으니 **무한 스크롤**로 구현해보는 것을 도전해 보라고 하셔서 기존의 페이징 수정
**해결 과정** - 리액트 InfiniteScroll 라이브러리를 사용하여 fetchData로 필요 시 리스트를 더 불러오는 방식으로 해결

2. **검색 필터의 부재** -  요구사항에 거래 게시판 리스트의 검색 필터는 생각하지 못했기에 무한 스크롤로 변경 하면서 이 부분도 피드백을 받아 구현하기 시작했습니다. 상세보기로 이동 후 다시 **이전의 필터대로 검색 결과를 유지하기 위해 수정하는 과정이 힘들었습니다.
**해결 과정** - 기존 코드는  url은 그대로 유지하는 코드라 이전의 상태를 유지하기 힘들었으나 리액트 라우터 돔을 이용하여 state 변경 시 url 파라미터를 변경하여 url 기록을 남기는 방식으로 구현하였습니다.

3. **행정동 기준으로 거래 게시판에서 원하는 지역 범위 확장 과정** - 이것은 **제가 기존의 요구사항을 생각하지 못하고** 프로젝트 후반부에 수정한 과정으로 시간 압박을 받았고 **가장 막막했던 부분입니다.
**해결 과정** - **Geojson으로 해결** 하였으며 유저의 위치 인증의 주소명 기반으로 해당하는 행정동 code 번호와 일치하는 중심 위치로 확장하여 해당하는 반경 내의 행정동을 포함하여 검색하게 하는 기능으로 구현하였습니다.

4. **스프링 시큐리티와 OAuth2 의 동시 구현** - 프로젝트 **초창기**의 구현 과정으로 팀원들이 로그인과 회원 가입부터 구현 하면 편할 것 같다고 얘기하여 프로젝트의 시발점이었습니다. 
간편 로그인을 구현하되 거래사이트의 특성 상 필요한 개인정보가 필요하다고 생각하여 간편 로그인의 email 정보가 없으면 자체 DB에서 가입을 받는 로직으로 구현하였습니다. 이 과정에서 자체 로그인을 시큐리티 기준으로 자체 가입으로 유도하는 과정이 힘들었습니다.
**해결 과정** - 우선 간편 로그인시 자체 DB에 해당하는 이메일이 없으면 권한을 ‘REGISTER_USER’라고 부여 하여 회원 가입으로 리다이렉트 하는 방식으로 구현하였고 이 과정에서 간편 로그인은 **스프링 시큐리티가 간편 로그인 과정에서 바로 세션을 부여**하는 것을 검색 과정에서 알게 되어 가입 페이지 유도시 **세션을 invaildate** 하는 방식으로 구현 하엿습니다.

5. **글 수정 시 기존의 이미지 파일 유지 방식** - 글 작성시에는 MultipartFile 로 구글 스토리지에 저장하는 방식으로 구현하였으나 **글 수정시에는 변경 되지 않은 파일에 한해서 컨트롤러에 MultipartFile 객체로 들어오지 않기에** 수정이 안되던 문제가 있었습니다. 
**해결과정 -** **DB에 저장된 파일명을 기준으로 비교**하여 변경되지 않은 파일은 DB에 유지하고 변경된 파일은 삭제 후 추가된 파일은 MultiPartFile로 구글 스토리지에 저장하고 DB에도 저장하는 방식으로 구현하였습니다.
 
