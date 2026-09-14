# 한국의 시 — a moving anthology

스크롤에 따라 시가 한 행씩 드러나는 웹 앤솔로지. WebGL 배경 연출(성좌·물빛·노을·안개·비·오로라·벚꽃)이 시의 분위기에 맞춰 바뀐다. 빌드 없는 단일 HTML + three.js.

**제작 시간 90분** · 배포 https://poems-one-bay.vercel.app

## 실행

ES 모듈은 `file://`에서 CORS로 막히므로 로컬 서버가 필요하다.

```bash
git clone https://github.com/warren-codeit/poems.git
cd poems
python3 -m http.server 8931
# http://localhost:8931/
```

## 구성

```
index.html                 페이지 전체 (인라인 CSS/JS)
assets/js/three.module.min.js
assets/js/motion.js        스크롤 리빌·이징 유틸
```

## AI 스튜디오 — 본인 API 키가 필요하다

설정(톱니) → **AI 스튜디오**에서 Claude API 키를 넣으면, 시를 붙여넣어 장면으로 연출하거나 제목·시인으로 찾아 무대에 올릴 수 있다.

- 키는 **그 브라우저의 localStorage에만** 저장되고 `api.anthropic.com`으로만 전송된다. 이 저장소에도, 어떤 서버에도 보관되지 않는다.
- 사용량은 키 주인의 Anthropic 계정에 과금된다. 공용 PC에서는 쓰고 나서 **삭제**를 누르면 된다.
- "키 확인"은 `count_tokens`를 호출해 과금 없이 키 유효성만 본다.
- 키 없이도 **제목·시인 검색**과 수록작 감상은 그대로 동작한다.

## 수록작

저작권이 만료된 작품 위주로 수록했다. AI로 회수한 본문은 공개 전에 1차 출처와 대조한다.

## 배포

정적 파일뿐이라 저장소를 그대로 Vercel·Netlify·GitHub Pages에 연결하면 된다. 빌드 명령과 출력 디렉터리는 비워 둔다.
