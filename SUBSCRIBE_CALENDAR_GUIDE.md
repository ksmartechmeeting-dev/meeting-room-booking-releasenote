# 회의실 예약 구독하기 가이드 문서

회의실 예약 프로그램 1.3.0v(2025.08.26)부터 구독하기 기능이 추가되었습니다. 구독하기 기능은 [iCalendar](https://icalendar.org/RFC-Specifications/iCalendar-RFC-5545/) 표준을 통해 지원되고 있습니다. iCal 주소를 사용하면 본인이 사용하시는 주 캘린더(네이버 캘린더, MacOS 캘린더, 구글 캘린더 등)에서도 회의실 예약 내역을 확인하실 수 있어서 서비스의 사용성이 향상되는 효과가 있습니다.

> **iCalendar**      
> 캘린더 데이터 교환을 위해 제안된 인터넷 표준으로, 1998년 IETF(인터넷 기술 표준화 기구)에 의해 최초 정의되었고 RFC 5545에서 최신으로 업데이트되었습니다. 이 표준은 ".ics" 확장자를 가진 파일의 구조와 내용을 정의하며, 구글 캘린더, 마이크로소프트 아웃룩 등 다양한 캘린더 프로그램에서 사용되어 서로 다른 캘린더 간에 일정을 공유하고 상호 운용성을 높이는 데 기여합니다.

-----

## iCal 주소 복사하기 
사용법은 간단합니다. 현재 회의실 예약 시스템 DB의 예약 테이블은 Google Calendar API를 통해 INSERT, UPDATE, DELETE 이벤트가 개발자의 Google 계정으로 동기화되고 있습니다. 그리고 Google Calendar에서는 공개 iCal 주소를 통해 캘린더 내역을 구독할 수 있는 기능을 제공합니다. 따라서 아래의 공개 iCal 주소를 복사합니다.


```jsx
//iCal 형식의 공개주소
https://calendar.google.com/calendar/ical/b434a54e0e2fd9a9660d1a9f3a7421d6d8110037cb4f9b72a6e058ae3ab34b8b%40group.calendar.google.com/public/basic.ics
```
단, 회의실 예약 데이터의 전체 동기화가 아닌 8월 25일 이후에 생성되는 예약 내역만 확인하실 수 있고, 새로운 예약 생성, 삭제, 수정은 여전히 회의실 예약 서비스에서만 가능합니다.

-----

## GOOGLE 캘린더

### 구독하기

구글 캘린더는 워낙 범용성이 넓어서 어디든 사용이 가능합니다. 특히 Windows를 사용하시는 분들께서는 Windows 기본 캘린더에서 iCal 형식을 아직 지원하지 않고 있기 때문에 사용하시면 좋겠습니다.

<img src="https://github.com/user-attachments/assets/2fd18a35-c7cb-4ad6-8d34-bfea35097605" alt="" width="80%">

캘린더 좌측 슬라이드바 - 다른 캘린더 오른쪽에서 + 버튼 - URL로 추가를 눌러줍니다.

<img src="https://github.com/user-attachments/assets/7b09afee-761e-4418-ad85-80c29426410e" alt="" width="80%">

공유된 iCal 형식의 주소를 입력하고 캘린더 추가 버튼을 눌러줍니다. 끝입니다.

<img src="https://github.com/user-attachments/assets/3640bf97-f87a-4576-a123-e5cd94f068c7" alt="" width="80%">

### 구독취소

추가한 캘린더에서 아래와 같이 X 버튼을 눌러줍니다.

<img src="https://github.com/user-attachments/assets/c6a15300-ce49-4f31-8b5a-7fe68debc8fd" alt="" width="80%">

아래에서 캘린더 삭제 버튼을 눌러줍니다.

<img src="https://github.com/user-attachments/assets/25440c8d-b49f-4f62-b162-f9e72e7ca715" alt="" width="80%">

-----

## APPLE 캘린더

### 구독하기

MacOS 사용자께서는 기본 캘린더에서 iCal 형식이 지원됩니다. 캘린더 앱을 열고 파일 - 새로운 캘린더 구독… 을 클릭합니다.

<img src="https://github.com/user-attachments/assets/a50622da-cc25-4a32-a589-d2e80d9e461c" alt="" width="80%">

공개된 iCal 주소를 입력합니다.

<img src="https://github.com/user-attachments/assets/0ed3eb8e-195e-4115-b20f-8e76934fd20f" alt="" width="80%">

아래에서 캘린더 이름과 알림 여부, 저장할 위치, 새로 고침 간격 등을 수정할 수 있습니다.

<img src="https://github.com/user-attachments/assets/daa124c6-d0e3-4858-8dac-5ff8295b90be" alt="" width="80%">

완료되면 구독 캘린더의 내역이 보이게 됩니다.

<img src="https://github.com/user-attachments/assets/504bb238-0130-4ada-ac84-6f8fb2e0c4a6" alt="" width="80%">

### 구독취소

취소도 매우 간단합니다. 구독한 캘린더 우클릭 - 구독 취소를 클릭합니다.

<img src="https://github.com/user-attachments/assets/ca822388-4598-42d7-a7f5-9dcbda67c5f1" alt="" width="80%">

구독 취소를 입력해줍니다. 끝입니다.

<img src="https://github.com/user-attachments/assets/3dd5650f-b426-486d-901e-a36bed75c177" alt="" width="80%">

-----

## NAVER 캘린더

### 구독하기

네이버 캘린더 화면으로 이동합니다. 좌측 사이드바 아래쪽의 구독 캘린더 - 오른쪽 + 버튼 - URL로 구독하기를 클릭합니다.

<img src="https://github.com/user-attachments/assets/e895fe72-d566-45b5-8359-c7a7fe10f66a" alt="" width="80%">


공개된 iCal 형식의 주소를 입력하고, 캘린더명과 색상을 변경할 수 있습니다. 저장을 클릭합니다.

<img src="https://github.com/user-attachments/assets/47bf73c2-f177-4599-8512-ec857b25d72d" alt="" width="80%">


아래와 같이 구독 캘린더의 내역이 보이게 됩니다.

<img src="https://github.com/user-attachments/assets/136b91a7-2710-41f5-80f4-d0a7cbc421a8" alt="" width="80%">


### 구독취소

구독 취소는 같은 메뉴에서 우측 톱니바퀴 모양 - 캘린더 설정을 클릭합니다.

<img src="https://github.com/user-attachments/assets/9a655f86-5b5b-4939-bc72-80d975c695a3" alt="" width="80%">


그러면 메인화면에 캘린더 목록이 나오는데요. 구독한 캘린더에가서 구독해지라고 적혀있는 부분을 클릭합니다.

<img src="https://github.com/user-attachments/assets/527ed744-e27b-44a2-b5ad-326bf0c7dc5b" alt="" width="80%">

그러면 중앙 상단에 아래와 같은 팝업이 뜨고 확인을 클릭하면 끝입니다.

<img src="https://github.com/user-attachments/assets/1f07284f-16d1-4a66-b906-74c2c226a293" alt="" width="80%">
