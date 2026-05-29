# Product Decision Example

```text
/llm-council

Decision:
Should I build this project as a Claude Code skill, a CLI tool, or a full web app?

Context:
I want a lightweight open-source tool that helps people make better decisions inside Claude. I care more about usefulness and adoption than monetization.

Options:
A. Claude Code skill
B. CLI tool
C. Full web app
cd ~/.claude/skills/llm-council

mkdir -p examples

cat > examples/technical-decision.md <<'EOF'
# Technical Decision Example

```text
/llm-council

Decision:
Should I use Supabase, Firebase, or a custom backend for my MVP?

Context:
I am building a web app quickly and want authentication, database, storage, and easy deployment. I am a solo builder and want to avoid unnecessary backend complexity.

Options:
A. Supabase
B. Firebase
C. Custom backend
```
