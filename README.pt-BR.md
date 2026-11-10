# Dona Maria · Grandma-proof

**Uma skill que faz sua IA construir telas que uma senhora de 70 anos consegue usar, e parar de incomodar você enquanto trabalha.**

🇺🇸 [Read in English](README.md)

![licença MIT](https://img.shields.io/badge/licen%C3%A7a-MIT-green) ![idiomas](https://img.shields.io/badge/idiomas-Portugu%C3%AAs%20%7C%20English-blue) ![funciona com](https://img.shields.io/badge/funciona%20com-Claude%20Code%20%7C%20Codex%20%7C%20Cursor%20%7C%20Gemini%20CLI-black)

Agentes de IA constroem telas para gente parecida com eles: fluente, paciente e técnica. O usuário de verdade não é assim. Esta skill dá ao agente uma pessoa para ter em mente, a Dona Maria, e sete regras para seguir.

## As sete regras

**O que o agente constrói**

| # | Regra | Em uma linha |
|---|---|---|
| 1 | Simplicidade | Uma tela, uma tarefa. Menos botões, menos texto, mas nunca tão pouco que a pessoa se perca. |
| 2 | Dona Maria | Palavras do dia a dia, botões grandes, sempre dá para voltar, erro que não assusta. |
| 3 | Alinhamento | Botões e caixas do mesmo grupo têm o mesmo tamanho, a mesma linha e a mesma proporção. Nada de legenda colada em botão; a explicação fica na dica ao passar o mouse. |
| 4 | Sem cara de IA | Sem degradê roxo, sem prova inventada e sem "página inicial de GPT" com textão centralizado e uma palavra em itálico. |

**Como o agente trabalha**

| # | Regra | Em uma linha |
|---|---|---|
| 5 | Fale simples | Respostas sem jargão. Usar um termo técnico não faz do usuário um programador. |
| 6 | Subagentes | Divide o trabalho e roda as partes ao mesmo tempo, com um revisor que não escreveu o código. |
| 7 | Decisão por debate | Dúvida pequena? Dois agentes debatem, um agente juiz escolhe, o trabalho segue. O humano só é chamado quando importa. |

Toda entrega termina com o **teste da Dona Maria**: dez conferências feitas na tela de verdade, de "dá para saber para que serve em 5 segundos?" até "funciona num celular de 360 px?".

## Instalar

Escolha o idioma. As duas skills têm as mesmas regras, escritas direto em cada língua.

| Skill | Idioma | Pasta |
|---|---|---|
| `dona-maria` | Português (Brasil) | [`skills/dona-maria`](skills/dona-maria) |
| `grandma-proof` | English | [`skills/grandma-proof`](skills/grandma-proof) |

### Claude Code

Windows (PowerShell):

```powershell
git clone https://github.com/ricarossetto/dona-maria-skill
Copy-Item -Recurse dona-maria-skill\skills\dona-maria "$HOME\.claude\skills\"
```

macOS, Linux ou Git Bash:

```bash
git clone https://github.com/ricarossetto/dona-maria-skill
mkdir -p ~/.claude/skills && cp -r dona-maria-skill/skills/dona-maria ~/.claude/skills/
```

Para valer só em um projeto, copie para `.claude/skills/` dentro dele.

### Codex, Cursor, Gemini CLI e outros agentes

Copie a mesma pasta para a pasta de skills que o seu agente lê, em geral `~/.agents/skills/` ou `.agents/skills/` dentro do projeto.

Seu agente não tem skills? Cole o conteúdo do `SKILL.md` no seu `AGENTS.md` ou arquivo de regras.

### Sem git

Baixe o zip do seu idioma na [última versão](https://github.com/ricarossetto/dona-maria-skill/releases/latest) e descompacte na sua pasta de skills.

## Usar

Peça qualquer tela e o agente aciona a skill sozinho. Você também pode chamar pelo nome:

```
/dona-maria monte o formulário de cadastro
/dona-maria revise este painel
```

Para deixar ligada em toda tarefa, coloque uma linha no seu `CLAUDE.md` ou `AGENTS.md`:

```
Siga sempre a skill dona-maria ao construir telas e ao me responder.
```

## O que vem dentro

```
skills/dona-maria/
├── SKILL.md                 as sete regras e o teste da Dona Maria
└── references/
    ├── sinais-de-ia.md      a lista de sinais de cara de IA para tirar
    └── debate.md            pedidos prontos para os dois debatedores e o juiz
```

O arquivo principal é curto para carregar barato. Os dois arquivos de apoio só são lidos quando preciso.

## Limites, sem enrolar

- **Subagentes gastam mais.** A regra 6 faz o agente rodar vários ajudantes ao mesmo tempo. Fica mais rápido e, em geral, melhor, mas consome mais do seu plano. Tarefa de um passo só ele faz direto.
- **O agente ainda pergunta às vezes.** A regra 7 mantém uma lista curta de casos em que ele precisa perguntar: ação sem volta, gasto de dinheiro e o que só você sabe.
- **No celular não existe "passar o mouse".** Por isso a regra é que o nome do botão baste sozinho; a dica é um extra.
- **Ela não refaz a sua marca.** A identidade visual que já existe fica. A skill tira a escolha feita no automático, não a escolha ousada.

## Créditos

Escrita no formato de skills do repositório [skills](https://github.com/anthropics/skills) da Anthropic. A regra contra cara de IA deve muito ao trabalho da comunidade de design, em especial ao [unslop](https://github.com/heydamir/unslop), de Damir Sokolovsky. Todo o texto daqui é original.

## Licença

[MIT](LICENSE). Use, mude e compartilhe.
