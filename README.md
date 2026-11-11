# 🎁 Kakaolink Sender (카카오톡 낚시 메시지 발송기)

오픈소스 레퍼런스인 **`Sharlottes/KakaoNacksee`**와 **`enaenen/kakaoprank`**의 핵심 로직과 UI를 100% 그대로 반영한 카카오톡 낚시 메시지 발송 프로젝트입니다.

---

## 💡 레퍼런스 프로젝트 위치
사용자의 요청에 따라 GitHub 원본 저장소 2개가 본 프로젝트 폴더와 나란히 클론되어 있습니다:
- [`/KakaoNacksee`](file:///Users/jangseongjin/Library/CloudStorage/MYBOX-aaa03172/KakaoNacksee): Next.js/TypeScript 기반 선착순 선물 게임 발송기 원본
- [`/kakaoprank`](file:///Users/jangseongjin/Library/CloudStorage/MYBOX-aaa03172/kakaoprank): React 기반 카카오페이 송금/봉투/기프티콘 발송기 원본

---

## 🚀 왜 이 방식은 절대 티가 안 날까요?

1. **단순 웹 링크(URL)가 아닙니다**:
   - URL 링크를 보내면 카카오톡에 웹사이트 주소와 브라우저 카드가 떠서 친구들이 금방 눈치챕니다.
2. **카카오톡 공식 SDK(`Kakao.Share.sendDefault`) 연동**:
   - 이 도구는 카카오 공식 JavaScript SDK를 통해 카카오톡 앱을 직접 호출합니다.
   - 친구의 카카오톡 채팅방에 **카카오톡 네이티브 말풍선 카드(Feed 템플릿)** 형태로 직접 꽂힙니다.
   - 공식 카카오 배너 이미지, 공식 폰트 레이아웃, `[지금 달려가기]`, `[받기]` 버튼이 그대로 렌더링되므로 단톡방에 올리면 100% 속아 넘어갑니다.

---

## ✨ 지원하는 4가지 낚시 모드 (레퍼런스 원본 구현)

1. **선착순 선물 게임 (KakaoNacksee 원본)**:
   - 카카오톡 공식 선착순 선물 타이틀 배너(`giftTitle.png`)
   - 문구: `선착순 선물 게임을 시작합니다! 기회는 단 {10분간}, 선착순 {2}명에게!`
   - 버튼: `지금 달려가기`
2. **카카오페이 송금 (kakaoprank 원본)**:
   - 카카오페이 송금 말풍선 이미지(`transfer.png`)
   - 문구: `{50,000} 원을 받으세요.`
   - 버튼: `받기`
3. **스타벅스 기프티콘 (kakaoprank 원본)**:
   - 스타벅스 아메리카노 기프티콘 이미지
   - 문구: `{김철수}님이 선물과 메시지를 보냈습니다.`
   - 버튼: `선물함으로 가기`
4. **카카오페이 축하/용돈 봉투 (kakaoprank 원본)**:
   - 용돈 봉투, 정산 봉투, 감사 봉투, 축하 봉투, 부자되세요 봉투 등
   - 문구: `봉투가 도착했어요.`
   - 버튼: `받기`

---

## 📱 사용 방법

1. 브라우저에서 [`index.html`](file:///Users/jangseongjin/Library/CloudStorage/MYBOX-aaa03172/kakao-gift-prank/index.html) 열기.
2. 상단 탭에서 원하는 낚시 모드 선택.
3. 실시간으로 카카오톡 채팅방 미리보기가 바뀌는 것을 확인.
4. **[💬 카카오톡으로 저지르기]** 버튼 클릭!
   - 모바일: 카카오톡 앱이 자동으로 열리며 친구/단톡방 선택 화면이 나타납니다.
   - PC: 카카오톡 로그인 팝업이 나타납니다.
5. 친구가 카카오톡에서 버튼을 누르면 [`trolled.html`](file:///Users/jangseongjin/Library/CloudStorage/MYBOX-aaa03172/kakao-gift-prank/trolled.html)("하하 낚시지롱!") 페이지로 이동합니다.
