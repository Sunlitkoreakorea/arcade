# 🎮 미니게임 오락실

설치 없이 브라우저에서 바로 하는 3D 미니게임 모음 메뉴예요. 목록에서 게임을 하나 고르면 설명과 조작법이 나오고, **▶ 플레이**를 누르면 이 페이지 안에서 바로 게임이 열려요. 위쪽 **◀ 메뉴**로 돌아올 수 있어요.

**▶ 바로 가기: https://sunlitkoreakorea.github.io/arcade/**

## 들어 있는 게임

| 게임 | 설명 | 조작 |
|---|---|---|
| 🎳 [기숙사 볼링](https://sunlitkoreakorea.github.io/dorm-bowling/) | 10프레임 3D 볼링, 1~4명 | 마우스·터치·키보드·웹캠 손동작 |
| 🎯 [기숙사 다트](https://sunlitkoreakorea.github.io/dorm-darts/) | 301·501·크리켓·카운트업, 1~4명 | 마우스·터치·키보드 |
| 🎾 [손 테니스](https://sunlitkoreakorea.github.io/hand-tennis/) | 웹캠으로 치는 Wii 스타일 테니스, vs CPU | 웹캠 손동작·터치패드·키보드·마우스 |

## 쓰는 법

- 마우스로 고르거나 `↑` `↓`(또는 `←` `→`)로 고르고 `Enter`로 시작해요.
- 게임 화면에서는 `새 탭에서 열기`, `전체 화면` 버튼을 쓸 수 있어요.
- 주소 끝에 `#play/hand-tennis`처럼 붙이면 해당 게임이 바로 열려요. 브라우저 뒤로 가기도 메뉴로 돌아가요.
- 웹캠을 쓰는 게임은 프레임에 카메라 권한(`allow="camera"`)을 넘겨 줘요. 카메라가 안 열리면 `새 탭에서 열기`로 열어 보세요.

## 게임 추가하기

`index.html` 안의 `GAMES` 배열에 객체 하나를 넣으면 메뉴에 생겨요.

```js
{
  id: 'my-game', emoji: '🏓', name: '게임 이름', sub: '한 줄 소개 · 인원',
  tagline: '목록 아래 큰 글씨', blurb: '설명 두세 문장',
  inputs: ['🖱️ 마우스', '⌨️ 키보드'], players: '1~2명',
  how: ['조작법 1', '조작법 2', '조작법 3'],
  url: BASE + 'my-game/', repo: 'https://github.com/Sunlitkoreakorea/my-game',
  art: artMyGame,   // 400×240 SVG 문자열을 돌려주는 함수 (없으면 artBowling처럼 하나 만들어 주세요)
},
```

## 내 컴퓨터에서 보기

```bash
python -m http.server 8765
# http://localhost:8765/ 열기
```

게임 주소는 배포된 사이트(`sunlitkoreakorea.github.io`)를 그대로 불러와요.
