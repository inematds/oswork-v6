# OSWork v6 — edição iniciante 30+ (formato-curso-v6)

Curso estático INEMA.CLUB PRO sobre organizar o próprio ambiente de IA. Piloto do `formato-curso-v6`.
Conteúdo convertido do `../oswork-v5` (que continua publicado e intocado). Não compartilha estado com ele
(`<meta name="curso" content="oswork6">`).

- **Conta e autoria:** `inematds <inematds@gmail.com>`, author e committer.
- **Profissões-alvo:** gestora e professor. Currículo de origem: `context/curriculo-v5.md`.

## Estrutura

- `aulas/aula-N.html` — fonte de cada aula (edite aqui). `curso.html` é **montado**, não edite à mão.
- `curso.json` — título, lead, imagem da trilha. `landing.html` — a lista de aulas é regenerada na montagem.
- `assets/aula.css`, `assets/curso.js` — copiados da skill v6, sem edição local.
- `assets/img/aula-N.webp` — cenas (flux2-klein, sem texto). `trilha.webp` na trilha e na landing.

## Fluxo

```bash
S=~/.claude/skills/formato-curso-v6/scripts
python3 $S/montar-curso.py .          # monta curso.html e a lista da landing
node $S/auditar-curso.cjs curso.html  # rubrica 9/10 por aula (portão)
node $S/testar-motor.cjs curso.html   # comportamentos do motor
```

Publicar = commit + push (GitHub Pages na raiz). Não usar Vercel.
