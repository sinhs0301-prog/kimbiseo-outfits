# 김비서 펫 옷 저장소 (kimbiseo-outfits)

[김비서](https://github.com/sinhs0301-prog/kimbiseo) 바탕화면 펫이 입는 **옷 꾸러미 목록**입니다.
옷은 하나가 수백 MB 라서 프로그램 안에 넣지 않고, 이곳에 따로 둡니다. 필요한 옷만 골라 받으면 됩니다.

## 옷 받는 법

1. 김비서를 켜고, 바탕화면의 펫을 **오른쪽 클릭**합니다.
2. **옷 더 받기**를 누릅니다.
3. 목록에서 옷의 미리보기를 보고, 마음에 드는 옷의 **받기**를 누릅니다.

받은 파일은 펫이 직접 확인합니다(sha256 값과 정품 서명이 맞아야만 넣음). 받다가 끊기거나 인터넷이 안 되면 아무것도 바뀌지 않고, 이미 넣은 옷은 그대로 둡니다.

## 이 저장소에 있는 것

| 파일 | 뜻 |
|---|---|
| `outfits.json` | 옷 목록(펫이 읽음). 옷마다 이름·성별·설명·미리보기·크기·sha256·서명·받는 주소 |
| `previews/` | 옷 미리보기 그림 |
| [Releases](https://github.com/sinhs0301-prog/kimbiseo-outfits/releases) | 옷 꾸러미 파일(`.hipcpet`). 옷 한 벌(판)마다 릴리스 하나 |

목록 모양:

```json
{
  "format": "kimbiseo-outfits/1",
  "outfits": [
    {"id": "kimbiseo_f", "name": "김비서(여)", "version": "…", "gender": "여성", "description": "…",
     "size": 0, "sha256": "…", "signed": true, "sign_key": "kimbiseo-pack-1",
     "url": "https://github.com/sinhs0301-prog/kimbiseo-outfits/releases/download/<태그>/<꾸러미>.hipcpet",
     "preview": "previews/<그림>.png", "default": true, "songs": false}
  ]
}
```

- `signed: true` 인 옷은 김비서 공개판 서명 키(`kimbiseo-pack-1`)로 서명돼 있습니다. 펫이 공개키로 확인하고, 틀리면 넣지 않습니다.
- `soon: true` 는 아직 준비 중인 옷입니다(목록에 '준비 중'으로만 보임).

## 옷 올리기

옷은 김비서 만든 곳에서만 올립니다(다른 분의 옷 올리기 요청·끌어오기 요청은 받지 않습니다).

## 사용 조건

옷 꾸러미·미리보기 그림은 코드와 다른 **캐릭터 자산 조건**([ASSETS-LICENSE.md](ASSETS-LICENSE.md), 본 저장소와 같은 문서)을 따릅니다.
요약: 개인이 자기 PC 에서 김비서와 함께 쓰는 것만 허용 · 재배포·판매·AI 학습 금지.
옷의 움직임은 AI 영상 도구(MiniMax H3)로 만든 영상입니다.
