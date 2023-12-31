# 1. About team IIIIEE
- 개발기간: 2023.07.14 ~ 2023.07.28
- [FrontEnd](https://github.com/wecode-bootcamp-korea/47-2nd-IIIIEE-frontend.git) : 양회진 / 최진이
- [BackEnd](https://github.com/wecode-bootcamp-korea/47-2nd-IIIIEE-backend.git) : 김상원 / 신동현 / 정성남 / 최리나
- FrontEnd의 기술 스택 : javascript, react, html, css, styled-compoenets
- 협업 툴 : git & github, slack, trello, notion, VScode
  
## 1-1. airbnb PET 분석

### Products
- 최근 코로나 이후, 여행객의 수요가 증가하면서 숙박업 시장의 눈부신 성장 : 2020년 대비 147.1% 상승 (2022) / 84억 달러
- 공유 경제 서비스 : Host / Guest 에 거리낌 없는 공유 경제 서비스, 고객과 host 중개/연결해주는 시스템
- 원하는 날짜 / 장소 필터링 후 예약 기능 : 장소와 시간에 구애받지 않으며, 소비자의 자유로운 선택이 가능
- 현장 체험 시스템 : 숙소를 단순 머무는 공간에 한정 짓지 않으며, 호스트가 주최한 다양한 체험을 추가하여 소비자의 선택 폭 확장.

### End_User
- 고객 : 여행지만의 독특한 점을 생생하게 느낄 수 있도록 현지인의 숙소를 이용할 수 있고 독특한 체험이 가능
- host : 인간관계의 다양화 또는 pipe money (부수익 창출 가능)
- Tech : front end 가 사용할 기술스택

## 1-2. 그럼 IIIIEE는 어떤 프로젝트를 하고 싶은가?

### Products
- 누구나 주최자 (host) / 고객 (Joiner)가 될 수 있다는 것
- 원하는 맛집을 호스트가 주최하고, 게스트가 참여하며 서로 만남을 가짐과 동시에 맛있는 음식을 먹으며 대화를 하며 친목 도모
- 맛집 탐방을 취미로 즐기는 사람들을 연결해주는 커뮤니티
- 해당 커뮤니티와 자사 서비스를 사용하는 파트너 식당의 중개 역할
- 수익 창출은 방 수수료 및 파트너사를 통하여 진행.
- 방을 만들고 예약 할 때 수수료를 받고 예약금은 파트너 식당으로
- 예약금은 식당을 위한 노쇼 방지로 활용 됨.

### End_User
- 홀로 맛집을 가고 싶지 않으며, 사람들과 함께 가고 싶어하는 사람들
- 다양한 인맥을 넓히고자 모임을 원하는 사람들.
- 고객을 끌어들이고 싶은 식당

### 구현하고 싶은 사항
- 소셜 네트워크 로그인 : 서비스의 접근성 증가
- 강남언니의 ui를 가져와 모바일 웹으로 구현 : 서비스의 접근성 증가 및 광고를 통해 추가 수익 창출 가능
- 필터링 : 유저가 원하는 장소, 시간, 연령대, 성별 선택해 원하는 모임에 접근 가능
- 유저가 직접 모임을 등록 : 원하는 조건의 모임 생성 가능
- 식당 위치 표시 : 카카오 맵 API를 활용
- 리뷰 서비스 : 호스트의 리뷰 작성 및 악플 필터링
- 결제 서비스 : 카카오 페이 API를 활용
- 메신저 알림 기능  : 스케쥴러 활용
 
## 1-3. 참고자료

- [IIIIEE의 ERD 구성](https://dbdiagram.io/d/64b3a9ce02bd1c4a5e2508b7)
- [IIIIEE의 Trello](https://trello.com/b/HrqeM69z/iiiiee)
- [IIIIEE의 맛나는 만남 사이트 시현영상](https://www.youtube.com/watch?v=rx7zdgdbR0s)
- [관련 회고록](https://coding-haebojago.tistory.com/47)

# 2. 내가 맡은 역할

#### 메인페이지
- 레이아웃
- useParams 이용해 모임 제목 누르면 모임의 상세페이지로 이동
- 슬라이드 라이브러리 사용해서 슬라이드 이미지 구현
- useParams 이용해 맛집의 모임 등록 페이지로 이동
- 상태관리를 이용해 맛집 사진 누르면 각 맛집의 대한 모임목록 토글로 뜨게 하기

![iiiee 메인페이지](https://github.com/hjyang369/IIIIEE-frontend/assets/125977702/d00d4116-38b6-4995-a825-392f2a7cc1c7)


#### 모임페이지
- 레이아웃
- 모임 정보 및 호스트 정보, 후기 정보 get 요청
- 신청 인원 넘어가면 신청하기 버튼 비활성화
- 호스트 정보 및 리뷰 컴포넌트 분리
- 후기 등록 버튼 클릭 시 post 요청
- custom hook 제작해 후기평점을 별점 모양으로 이미지화
- 모임의 정보를 가지고 호스트와 밥을 먹은 사람만 리뷰를 작성할 수 있도록 구현
- 신청하기 버튼 클릭 시 post 요청과 성공 시 신청목록으로 이동

![iiiee 모임 정보 (1)](https://github.com/hjyang369/IIIIEE-frontend/assets/125977702/2c4d11e4-98c2-4428-9777-b6b14d7bcda1)
![iiiee 별점후기 (1)-min (1) (1)](https://github.com/hjyang369/IIIIEE-frontend/assets/125977702/de86f981-f696-49af-9d3a-32d49d439f29)


#### 모임 등록 페이지
- 레이아웃
- 모임 등록 post 요청 후 response로 받아온 roomId 값과 유저가 업로드한 사진을 formdata로 post 재요청
- 캘린더 라이브러리 사용
- 유저가 동적으로 바꾸는 값들을 state로 관리
- 유저가 직접 작성할 수 있는 태그 추가 및 삭제 가능하도록 구현

![iiiee 모임등록 (1)](https://github.com/hjyang369/IIIIEE-frontend/assets/125977702/2fa6a9a2-d5a3-4a34-b568-e84e13a9379f)
![폼데이터로 이미지 전송](https://github.com/hjyang369/IIIIEE-frontend/assets/125977702/185fdf96-38de-4992-9189-5677382e5f0a)


#### 모임 목록 페이지
- 레이아웃
- 유저가 만든 모임에 신청한 게스트 유저를 수락, 거절할 수 있는 버튼 구현 ->추가구현위해 미리 ui만 구현
- 예약하기 버튼 클릭 시 카카오페이 결제 api 연결
- useParams 이용해 모임 제목 누르면 상세페이지로 이동
- 결제 성공 시 예약하기 버튼이 사라지고 예약완료 텍스트 보여줌
- 모임의 대한 정보를 통해 신청인원이 모두 찼을 때 예약하기 버튼 활성화
- 유저가 만든 모임 모두 가져오는 get 요청

![iiiee 결제 api 사용](https://github.com/hjyang369/IIIIEE-frontend/assets/125977702/31fe214e-b338-4b9f-b5dc-61aa25d19643)


#### 404페이지 및 frame 페이지
- 레이아웃 및 라우터 구성
- 광고란에 동영상 넣을 수 있도록 구현

![iiiee 404](https://github.com/hjyang369/IIIIEE-frontend/assets/125977702/a139f2ed-eaf7-4255-a498-7af18432a096)


# 3. 추가 구현하고 싶은 내용
- 추가구현이었던 후기 삭제, 신청한 유저를 호스트가 수락/거절하는 기능, 알림기능
- 페이지네이션
- 현재 시간을 기준으로 과거는 예약을 못 하는 기능

# 4. Reference
이 프로젝트는 에어비엔비 및 강남언니 사이트를 참조하여 학습목적으로 만들었습니다.

실무수준의 프로젝트 이지만 학습용으로 만들었기 때문에 이 코드를 활용하여 이득을 취하거나 무단 배포할 경우 법적으로 문제가 될 수 있습니다.

이 프로젝트에서 사용하고 있는 사진 대부분은 위코드에서 구매한 것으로, 해당 프로젝트 외부인이 사용할 수 없습니다.
