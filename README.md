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

아직 없음.
