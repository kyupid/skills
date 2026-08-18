# skills

[Claude Code](https://claude.com/claude-code) 스킬 모음.

스킬 하나는 디렉토리 하나다. 안에 `SKILL.md` 가 있고, 필요하면 템플릿·스크립트를 같이 둔다.

```
skills/
  <skill-name>/
    SKILL.md        # 프론트매터(name, description) + 본문
    template.html   # (선택) 스킬이 쓰는 파일
```

## 쓰는 법

이 저장소를 클론하고, 쓰고 싶은 스킬만 `~/.claude/skills/` 로 링크한다.

```bash
git clone git@github.com:kyupid/skills.git ~/git/skills
ln -s ~/git/skills/<skill-name> ~/.claude/skills/<skill-name>
```

전부 쓰려면 저장소째로 링크해도 된다.

```bash
for d in ~/git/skills/*/; do ln -sfn "$d" ~/.claude/skills/; done
```

`description` 에 적힌 상황이 오면 Claude 가 알아서 불러 쓰고, `/<skill-name>` 으로 직접 부를 수도 있다.

## 목록

| 스킬 | 무엇을 하나 |
|---|---|
| [stacked-architecture](stacked-architecture/) | 시스템 구조를 "한 겹씩 쌓아 올리는" 방식으로 소개하는 자료를 만든다. 아무것도 없는 상태에서 시작해 문제 하나마다 부품 하나가 붙고 그 대가를 같이 적는다. 스크롤에 따라 다이어그램이 자라고, 비유 표기와 기술용어 표기를 버튼으로 갈아끼우는 단일 HTML 아티팩트가 나온다 |
