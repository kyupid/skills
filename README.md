# skills

작업 방식을 글로 적어둔 스킬 모음.

스킬 하나는 "이런 상황이면 이렇게 한다"를 적은 문서 한 장이다. 사람이 읽어도 되고, 코딩 에이전트에게 읽혀도 된다. 매번 같은 설명을 다시 하지 않으려고 모아둔다.

```
skills/
  <skill-name>/
    SKILL.md        # 프론트매터(name, description) + 본문
    template.html   # (선택) 스킬이 쓰는 파일
```

`SKILL.md` 는 YAML 프론트매터에 `name` 과 `description` 을 두고 본문에 절차를 적는 형식이다. Anthropic 이 정한 [Agent Skills](https://code.claude.com/docs/en/skills) 규격을 따르지만, 특별한 게 없는 마크다운이라 다른 도구에 붙이거나 그냥 읽어도 된다.

## 쓰는 법

클론해서 원하는 스킬만 도구가 보는 자리에 링크한다.

```bash
git clone git@github.com:kyupid/skills.git ~/git/skills
```

Claude Code 라면 `~/.claude/skills/` 다.

```bash
ln -s ~/git/skills/<skill-name> ~/.claude/skills/<skill-name>
# 전부 쓰려면
for d in ~/git/skills/*/; do ln -sfn "$d" ~/.claude/skills/; done
```

다른 에이전트를 쓴다면 그 도구가 읽는 경로에 같은 식으로 걸거나, `SKILL.md` 를 프롬프트에 그대로 붙여 넣어도 된다.

## 목록

| 스킬 | 무엇을 하나 |
|---|---|
| [stacked-architecture](stacked-architecture/) | 시스템 구조를 "한 겹씩 쌓아 올리는" 방식으로 소개하는 자료를 만든다. 아무것도 없는 상태에서 시작해 문제 하나마다 부품 하나가 붙고 그 대가를 같이 적는다. 스크롤에 따라 다이어그램이 자라고, 비유 표기와 기술용어 표기를 버튼으로 갈아끼우는 단일 HTML 아티팩트가 나온다 |
