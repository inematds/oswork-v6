# OSWork v5 — currículo travado

Formato: `formato-curso-v5`. Página única `curso.html`, 7 aulas, uma trilha.
`<meta name="curso" content="oswork5">`.

## Protocolo de descoberta (Passo 0 — respondido pelo usuário em 21/09/2026)

1. **Público específico:** profissionais de 40+ anos, iniciantes em IA, que já usam
   um chat de IA de vez em quando e querem parar de improvisar.
2. **Profissões-alvo (≥2):** **gestora** (coordena equipe e processos) e
   **professor** (prepara material e devolutivas). Todo exemplo cita uma das duas.
3. **Familiaridade com tecnologia:** baixa. Usa computador e celular no trabalho,
   nunca programou, nunca abriu uma tela preta de comandos.
4. **Resultado prático esperado:** sair com o **próprio ambiente de IA organizado** —
   pastas por contexto, um documento de orientação, um molde de pedido reutilizável
   e uma rotina de conferência.
5. **Tempo por sessão:** 20 a 25 minutos.

## Transformação a partir do OSWork v2 (mesmo assunto, outro público)

O v2 é "do chat ao ambiente de agentes" para quem encara terminal, Git e VPS. O assunto
se mantém; o **caminho técnico não**, porque módulos inteiros do v2 são feitos de
jargão-sentinela (terminal, instalar, repositório, commit, servidor). Mapa:

| v2 | v5 | o que acontece |
|---|---|---|
| M2 Chat, Work e Desktop | Aula 1 | vira "pedido completo" vs. pergunta solta |
| M1 Modelos: escolha pela tarefa | Aula 2 | vira "régua de conferência" — escolher e conferir |
| M4 Pastas, Markdown e segredos | Aula 3 | pasta por contexto + o que nunca entra num pedido |
| M5 AGENTS.md | Aula 4 | vira "ficha de orientação" do projeto |
| M5 Skills | Aula 5 | vira "molde de pedido reutilizável" |
| M6 Git e GitHub | Aula 6 | **transformado**: cópia datada antes de mudar, não Git |
| M3 Terminal/Codex | — | **descartado** (tela de comandos, fora do público) |
| M7 Telegram bot | Aula 7 (parcial) | vira "o que dá pra delegar e o que exige você" |
| M8 VPS 24/7 | Aula 7 (parcial) | vira "rotina de conferência", sem máquina remota |

Nada de terminal, nada de comando, nada de código. Sem `.termdemo` no curso inteiro
(decisão registrada: não existe comando real neste currículo — CHECKLIST §5.1).

## As 7 aulas

Legenda: **tipo** define a linha da matriz de dosagem (`RETENCAO-V5.md` §3).

---

### Aula 1 — Pedido completo, não pergunta solta
- **tipo:** FUNDAMENTO · **tempo:** 21min · **steps:** 4
- **promessa:** Ao fim desta aula você consegue transformar uma pergunta solta num
  pedido completo — com material, formato de saída e critério de pronto — e receber
  de volta algo que você usa sem reescrever.
- **por que agora:** o retrabalho cai no fim da tarde, quando o tempo bom do dia já foi.
  A causa está no que ficou de fora na hora de pedir — e isso só aparece depois de ler
  a resposta. (Reescrito na auditoria anti-clone; ver seção no fim deste arquivo.)
- **steps:** (1) a IA não sabe nada do seu contexto · (2) material, saída e critério —
  o que o pedido carrega · (3) o critério de pronto é seu, não dela · (4) pedir a
  revisão do próprio pedido antes de executar
- **prática:** modo **prompt**, ~10min — molde de pedido completo colável, com os
  trechos a trocar marcados.
- **dosagem (teto 5):** teste-se · cartões · antes/depois · frase-âncora = **4 tipos**.
  O opcional foi cortado: 4 steps toleram no máximo 2 quadros funcionais (densidade
  ≤1 a cada 2 steps), e antes/depois + frase-âncora já ocupam os dois.
- **gancho →** Aula 2: o pedido ficou bom e a resposta ainda pode estar errada.

### Aula 2 — A régua de conferência
- **tipo:** FUNDAMENTO · **tempo:** 22min · **steps:** 4
- **promessa:** Ao fim desta aula você consegue conferir uma resposta de IA em menos de
  dois minutos, usando uma régua de três itens que você mesma escreve antes de pedir.
- **por que agora:** a resposta errada chega com o mesmo tom seguro da resposta certa.
  Sem uma régua escrita antes, você confere pelo que "parece bem escrito".
- **steps:** (1) confiança não é sinal de acerto · (2) escreva a régua antes de pedir ·
  (3) ferramenta diferente, mesma régua · (4) o que você nunca terceiriza
- **prática:** modo **análise**, ~12min — dois textos de IA sobre o mesmo material,
  um com um dado inventado; aplicar a régua e comparar com o gabarito.
  *Justificativa do modo análise:* conferir uma resposta contra a realidade exige um
  caso com erro plantado e verdade conhecida — impossível garantir numa geração ao vivo.
- **dosagem (teto 5):** teste-se · cartões · antes/depois · frase-âncora = **4 tipos**
  (opcional cortado pela mesma regra de densidade da Aula 1).
- **gancho →** Aula 3: conferir toda vez cansa — o próximo ganho vem de guardar o contexto.

### Aula 3 — Uma pasta por contexto
- **tipo:** FERRAMENTA · **tempo:** 20min · **steps:** 4
- **promessa:** Ao fim desta aula você tem no seu computador uma pasta por frente de
  trabalho, com o material que a IA precisa ler — e sabe dizer o que nunca entra ali.
- **por que agora:** hoje o material está espalhado entre e-mail, área de trabalho e
  anexos. Você reexplica tudo em cada conversa nova porque não há um lugar só.
- **steps:** (1) um contexto, uma pasta · (2) o que colocar dentro · (3) o que nunca
  entra: dado pessoal e senha · (4) a limpeza de dez minutos
- **prática:** modo **tarefa**, ~12min — criar uma pasta real para uma frente de
  trabalho em andamento e mover três materiais para dentro.
- **dosagem (teto 5):** erro comum · checklist `.qsteps` · cartões = **3 tipos**
  (os 2 quadros permitidos já são os obrigatórios de FERRAMENTA).
- **gancho →** Aula 4: a pasta guarda o material, mas não guarda as suas regras.

### Aula 4 — A ficha de orientação do projeto
- **tipo:** FERRAMENTA · **tempo:** 22min · **steps:** 4
- **promessa:** Ao fim desta aula você tem uma ficha de orientação escrita para uma
  frente de trabalho sua, que dispensa repetir suas regras a cada pedido.
- **por que agora:** você repete "seja formal", "não invente número", "assine como
  coordenação" em toda conversa — e esquece uma delas justo no dia corrido.
- **steps:** (1) o que é uma ficha de orientação · (2) as quatro perguntas que ela
  responde · (3) regra geral e regra de projeto · (4) a ficha envelhece — revise
- **prática:** modo **tarefa**, ~12min — escrever a ficha da pasta criada na Aula 3.
- **dosagem (teto 5):** erro comum · checklist `.qsteps` · teste-se · cartões = **4 tipos**
  (teste-se não é quadro funcional, então não pesa na densidade).
- **gancho →** Aula 5: a ficha vale para a frente inteira; falta o molde da tarefa que
  você repete toda semana.

### Aula 5 — O molde que você reusa
- **tipo:** FERRAMENTA · **tempo:** 21min · **steps:** 4
- **promessa:** Ao fim desta aula você tem um molde de pedido guardado para a tarefa
  que mais se repete no seu mês, pronto para usar trocando só o que muda.
- **por que agora:** toda semana você reescreve quase o mesmo pedido do zero, e o
  resultado varia conforme o dia e a pressa.
- **steps:** (1) o que se repete vira molde · (2) o que fica fixo e o que é lacuna ·
  (3) o molde carrega o critério de pronto · (4) guardar onde você acha depois
- **prática:** modo **prompt**, ~12min — montar o próprio molde a partir do último
  pedido real, e rodá-lo duas vezes com conteúdos diferentes.
- **dosagem (teto 5):** erro comum · checklist `.qsteps` · teste-se · cartões = **4 tipos**.
- **gancho →** Aula 6: o molde melhora a cada uso — se você não perder a versão boa.

### Aula 6 — Não perder o que já funcionava
- **tipo:** FUNDAMENTO · **tempo:** 20min · **steps:** 4
- **promessa:** Ao fim desta aula você consegue mudar um material de trabalho sabendo
  que dá para voltar exatamente à versão anterior, sem depender de lembrar o que mudou.
- **por que agora:** você melhora a ficha, o resultado piora, e a versão boa já foi
  salva por cima. Não é descuido — é falta de um ponto de retorno.
- **steps:** (1) toda melhora é uma aposta · (2) cópia datada antes de mudar ·
  (3) anote o porquê, não o quê · (4) uma linha por falha
- **prática:** modo **tarefa**, ~10min — fazer a cópia datada da ficha da Aula 4,
  alterar uma regra e registrar o porquê em uma linha.
- **dosagem (teto 5):** teste-se · cartões · antes/depois · frase-âncora = **4 tipos**.
- **gancho →** Aula 7: com contexto, regras, molde e ponto de retorno no lugar, dá para
  perguntar o que você ainda precisa fazer à mão.

### Aula 7 — O que você delega e o que continua seu
- **tipo:** PRÁTICA/INTEGRAÇÃO · **tempo:** 24min · **steps:** 5
- **promessa:** Ao fim desta aula você tem o seu ambiente de IA montado por inteiro e
  uma lista escrita do que delega, do que confere e do que não entrega a ninguém.
- **por que agora:** as peças existem separadas. Sem decidir de antemão onde termina a
  delegação, a decisão acaba sendo tomada no dia corrido — sempre pelo lado errado.
- **steps:** (1) delegar tarefa não é delegar responsabilidade · (2) os três níveis:
  faz sozinho, faz e mostra, só sugere · (3) o custo de conferir entra na conta ·
  (4) a rotina de conferência semanal · (5) seu ambiente, montado
- **prática:** modo **tarefa**, ~15min — preencher a lista de delegação das próprias
  tarefas em três colunas e marcar a data da primeira conferência.
- **dosagem (teto 5):** checklist `.qsteps` · mini-caso integrador · aplicar por
  profissão (`.qapply`) · cartões = **4 tipos**. 5 steps toleram 2 quadros; o erro
  comum foi cortado.
- **fecho de trilha:** constatação de capacidade, sem emoji, sem exclamação dupla.

---

## Regras de execução (valem para todas as aulas)

- **Jargão-sentinela proibido no texto do aluno:** terminal · instalar · script ·
  servidor · repositório · commit · branch · Git · JSON · pipeline · arquivo de
  configuração · API · deploy · CLI · diretório · plugin · encoding.
  Substitutos: *pasta* (não diretório), *ativar/abrir* (não instalar),
  *cópia datada* (não commit), *ficha de orientação* (não arquivo de configuração).
- **Jargão de domínio** (define inline + `.gterm` na 1ª aparição): pedido completo,
  contexto, régua de conferência, ficha de orientação, molde, delegação supervisionada.
- **Exemplo por profissão em 100% dos steps** — alternar gestora/professor, situação
  nova a cada step (nunca repetir a mesma cena).
- **Registros visuais:** `.herofig` = metáfora do mundo real (gaveta, molde de costura,
  caderno, placa). `.fig` do trilho = diagrama de mecanismo. Nunca trocados.
  Proibido: robô humanoide, cérebro-circuito, chuva de código, aperto de mão com robô.
- **Densidade:** ≤1 quadro funcional a cada 2 steps, nunca dois em steps adjacentes.
- **Cartões:** só pergunta/decisão/contraste/diagnóstico/aplicação. Zero sobreposição
  de ≥6 palavras com o `.recap-autor`.


## Auditoria anti-clone (executada em 21/09/2026)

Comparada contra `copilot-agentic`, `agi-ready` e `ia-do-zero` (os cursos v5 de 07/09).

**Corrigido:**
- Aula 1 repetia o `ia-do-zero`: metáfora de papel de pedido com campos, o movimento
  retórico "não era a IA, era o pedido" e o enquadramento "as três partes" na aula 1.
  Trocados por ordem de serviço de oficina, um `why` centrado no custo do retrabalho, e
  a nomenclatura própria material / saída / critério de pronto.
- Cenas da gestora na Aula 1 (resumo de reunião, comunicado de mudança de horário)
  colidiam com cenas-assinatura dos antecessores. Trocadas por cronograma de treinamento
  a partir de uma norma, e aviso de nova regra de reembolso.
- A persona "Marta" da Aula 2 é a gestora de RH de `agi-ready` e `ia-do-zero`
  (24 e 14 ocorrências). Renomeada para Sílvia, inédita nos três.

**Aceito como imposição da matriz, não clonagem:**
as aulas FERRAMENTA abrem com `.qerr` + `.qsteps` porque a matriz de dosagem torna os
dois obrigatórios para esse tipo; com 4 steps e densidade ≤1 quadro a cada 2 steps,
sobram apenas as posições {1,3}, {2,4} e {1,4}. O curso usa {2,4} em A1–A3, {1,3} em
A4–A6 e {2,5} em A7 — variação real dentro do que a regra permite. A sequência não é
idêntica à de nenhum curso anterior, que é o critério de reprovação do CHECKLIST §7.3.

**Metáforas de cold-open, todas inéditas:** ordem de serviço de oficina (A1), metro de
carpinteiro (A2), gaveta de pastas suspensas (A3), manual da casa para quem cobre as
férias (A4), forma de bolo (A5), foto do quadro antes de apagar (A6), bancada montada (A7).
