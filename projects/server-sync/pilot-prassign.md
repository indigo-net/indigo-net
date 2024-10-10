# Pilot for 'prassign,' a function in ServerSync

_이 프로젝트는 [server-sync]() 프로젝트의 일부인 'Prassign' 기능의 파일럿 버전입니다._

<br/>
<br/>

## 🎯 목적 (Purpose)
- Pov(Proof of Value) 확보
  - 프로젝트의 효익 및 가치를 증명
- Prassign 기능의 시범 작동
- 사용자 피드백 수집 및 분석

<br/>

> **참고) Prassign 이란?**
>
> - indigo-net 팀 내부에서 정의한 용어입니다.
> - 다음 운동 참여 대기자에게 준비를 알리는 기능입니다.
> - Firebase 클라우드 메시징(FCM)을 이용한 푸시 알림으로 구현됩니다.

<br/>
<br/>

## 🧪 증명하고 싶은 가설 (Hypothesis)

### 1. (운영진) 게임 참여 직전, 회원에게 푸시 알림을 통해 준비시키는 것은 동아리 운영에 효과적일 것이다.
  - 인원 통제의 편의성
  - 게임 코드 및 시간 관리의 편의성
  - etc.

### 2. (일반 회원) 다음 게임 대상자임을 모바일을 통해 전달받는 것이 더 만족스러울 것이다.
  - 회원들의 만족도
  - 정보전달의 정확성
  - etc.

<br/>
<br/>

## 🛠️ 기능 (Features)

### 운영진 (Manager)
- 당일 모임의 출석 확인용 QR 이미지를 생성합니다.
- 출석 인원 리스트를 조회합니다. 
- 모든 부원 중 다음 게임 대상자를 선택하고, Prassign 을 실행합니다.
- `휴식` | `게임 중` 상태인 회원의 경우, Prassign 대상으로 선택할 수 없습니다.
- 모임 종료 후, 출석 인원에 대한 모든 정보를 초기화(=삭제) 합니다.

### 일반 회원 (Member)
- 출석 확인을 위한 QR 코드를 인식할 수 있습니다.
- QR 코드 인식 후, 사용자의 이름을 입력하여 출석을 server에 등록합니다.
- 자신의 상태를 `휴식`, `준비`, `게임 중` 중 하나로 선택할 수 있습니다.
- Prassign 대상자(운동 참여 대기자)는 QR 코드를 인식한 기기를 통해 알림을 받아, 운동 참여 준비를 할 수 있습니다.

<br/>

> __참고) 일반 회원이 가질 수 있는 "상태"에 대해..__
>
> - `휴식`: 
>    - 휴식을 취하려는 회원은 다음 게임에 참여시켜선 안됩니다. 
>    - **Prassign 대상이 아닙니다.**
> - `준비`: 
>   - 게임 참여를 의사를 밝힌 상태입니다. 
>   - **Prassign 대상입니다.**
> - `게임 중`: 
>   - 게임에 참여하고 있는 회원에게 알림이 울려선 안됩니다. 
>   - **Prassign 대상이 아닙니다.**

<br/>
<br/>

## 📝 [설문링크 (Survey Link)]()

<br/>
<br/>

## 👥 기여자 (Contributors)

### Backend

|<img src="https://github.com/straipe.png" width="100" height="100" style="border-radius: 50%;" alt="straipe">|
|:--:|
|[신도영](https://github.com/straipe)|

<br/>

### Frontend

|<img src="https://github.com/TransparentDeveloper.png" width="100" height="100" style="border-radius: 50%;" alt="TransparentDeveloper">|
|:--:|
|[이윤신](https://github.com/TransparentDeveloper)|

<br/>
<br/>

## 📁 저장소(Repositories)
- [be-pilot-prassign](https://github.com/indigo-net/be-pilot-prassign): 백엔드팀 코드 저장소
- [fe-pilot-prassign](https://github.com/indigo-net/fe-pilot-prassign): 프론트엔드팀 코드 저장소