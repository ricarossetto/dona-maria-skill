---
name: dona-maria
description: Faz o agente construir telas que qualquer pessoa consegue usar — a senhora de 70 anos, o jovem do TikTok, quem nunca mexeu em sistema — e trabalhar sem cansar o humano. Use sempre que criar, alterar ou revisar qualquer tela, página, formulário, botão, lista, painel, aplicativo ou site, e também ao responder o usuário, dividir trabalho e resolver dúvidas pequenas. Cobre simplicidade, linguagem fácil, alinhamento de botões e caixas, remoção de cara de IA, respostas sem jargão, uso de subagentes e decisão por debate em vez de pedir confirmação.
---

# Dona Maria

Imagine a Dona Maria: 70 anos, estudou pouco, enxerga mal de perto, tem medo de clicar errado e estragar tudo. Se ela consegue usar a tela sozinha, todo mundo consegue.

Esta skill tem duas partes. A primeira rege **o que você constrói** (regras 1 a 4). A segunda rege **como você trabalha** (regras 5 a 7). As duas valem ao mesmo tempo.

## Para quem você constrói

Antes de desenhar qualquer tela, passe por estas quatro pessoas. A tela precisa servir às quatro.

| Pessoa | Como ela é | O que ela exige da tela |
|---|---|---|
| Dona Maria, 70 anos | Não sabe bem onde clica, se perde, tem medo de errar | Letra grande, botão grande, um caminho só, sempre dá para voltar |
| Seu João | Pouca escola, lê devagar, não conhece palavra difícil | Palavras do dia a dia, frases curtas, ícone junto do texto |
| Kauã, 17 anos | Cresceu no TikTok, desiste em 3 segundos se travar ou confundir | Resposta imediata ao toque, nada de menu dentro de menu, fluidez |
| Bia, caloura | Nunca precisou usar um sistema e agora precisa fazer algo complexo | Acolhimento: a tela diz o próximo passo, erro não assusta nem culpa |

Nenhuma delas lê manual. Nenhuma sabe o que é "painel", "módulo", "sincronizar" ou "sessão expirada".

## Parte A — O que você constrói

### 1. Simplicidade

O alvo é a tela fácil, não a tela vazia. Tirar demais também confunde.

- **Uma tela, uma tarefa.** Cada tela tem uma ação principal, visível sem rolar. As outras ações ficam visualmente mais discretas.
- **Menos botões.** Conte os cliques da tarefa mais comum e tente tirar um. Ação rara vai para um menu "Mais"; ação que ninguém usa sai.
- **Menos texto.** Corte todo texto que, se sumir, não deixa ninguém perdido. Títulos de até 5 palavras. Frases de até 12 palavras.
- **Não corte o que orienta.** Mantenha sempre: onde estou, o que faço agora, como volto. Ícone sozinho, sem palavra, só para os universais (fechar, voltar, buscar).
- **Pergunte só o necessário.** Campo que o sistema consegue descobrir sozinho não vira pergunta. Formulário longo vira passos curtos com "Passo 2 de 4".
- **Escolha por ela.** Deixe a opção mais comum já marcada. Configuração avançada fica escondida até alguém procurar.

### 2. Dona Maria

**Palavras**

- Use a palavra que ela usa em casa: "entrar" e não "autenticar"; "guardar" ou "salvar" e não "persistir"; "apagar" e não "remover registro".
- Nada de sigla, termo em inglês ou termo técnico na tela. Se o termo for inevitável, explique em uma frase curta na primeira vez.
- O botão diz o que acontece: "Enviar pedido", "Apagar foto". Nunca "OK", "Confirmar" ou "Clique aqui" soltos.
- O mesmo nome para a mesma coisa em todas as telas.

**Tamanho e leitura**

- Texto corrido com no mínimo 16 px; prefira 18 px. Contraste de pelo menos 4,5 para 1.
- Tudo que se clica tem no mínimo 48 × 48 px e 8 px de folga até o vizinho.
- Não dependa só de cor para avisar. Junte ícone ou palavra.

**Não se perder**

- Toda tela mostra onde a pessoa está e tem um "Voltar" no mesmo lugar.
- Troca de tela com transição curta (150 a 250 ms) que mostra de onde veio e para onde foi. Nada pula, pisca ou muda de lugar sozinho.
- Depois de cada ação, a tela responde na hora: "Salvo", "Enviado". Se demorar mais de 1 segundo, mostre que está trabalhando.
- Nada funciona só com gesto escondido (arrastar, segurar, dois toques). Sempre existe um botão visível para a mesma coisa.

**Sem medo de errar**

- Dá para desfazer. Onde não dá, pergunte antes com as duas saídas escritas por extenso: "Apagar foto" e "Manter foto".
- Mensagem de erro diz o que houve e o que fazer, sem culpar: "Não achamos esse CPF. Confira os números e tente de novo."
- Tela vazia diz o próximo passo: "Você ainda não tem pedidos. Toque em Novo pedido para começar."
- Nunca apague o que ela digitou por causa de um erro.

### 3. Alinhamento

IA costuma deixar botão torto, caixa de tamanho diferente e texto colado em botão. Não entregue assim.

- **Mesma linha.** Botões do mesmo grupo ficam na mesma linha de base, com a mesma altura.
- **Mesmo tamanho.** Botões do mesmo grupo têm a mesma altura, o mesmo arredondamento, a mesma letra e o mesmo espaço interno. Se as larguras ficarem muito diferentes, iguale pela maior.
- **Mesma proporção.** Cartões e caixas da mesma lista têm a mesma largura e a mesma altura na linha. Texto longo corta com reticências; não estica a caixa.
- **Uma régua só.** Todo espaço sai de uma escala única (4, 8, 12, 16, 24, 32, 48 px). Nenhum valor solto como 13 px ou 22 px.
- **Um só destaque.** Um botão principal por tela. Os demais usam o estilo secundário, sempre o mesmo.
- **Botão longe do texto.** Pelo menos 24 px entre um botão e qualquer bloco de texto. Não empilhe uma frase logo acima ou abaixo do botão.
- **Botão não tem legenda.** Não escreva texto na tela para explicar um botão. Se o botão precisa de explicação, o nome dele está ruim: troque o nome. Explicação extra vai na dica que aparece ao passar o mouse (`title` ou tooltip, e `aria-label` para leitor de tela).
- **Confira medindo.** Depois de montar, abra a tela, tire um retrato e compare alturas, larguras e espaços. Olhar o código não basta.

### 4. Sem cara de IA

Leia [references/sinais-de-ia.md](references/sinais-de-ia.md) antes de criar página inicial, tela de apresentação ou qualquer texto de divulgação. O resumo:

- **Proibida a "página inicial de GPT":** um textão gigante centralizado, com uma frase de efeito e uma palavra em itálico, etiqueta em cápsula em cima, dois botões embaixo e três cartões com ícone logo depois.
- Proibidos por reflexo: degradê roxo ou azul-arroxeado, brilho neon, vidro fosco, texto em degradê, emoji no lugar de ícone, sombra colorida, cartão dentro de cartão.
- Proibido inventar prova: número, depoimento, logotipo de cliente ou nota que não existem.
- Proibido texto de vendedor: "Transforme", "Eleve", "Revolucione", "sem esforço", "Não é X. É Y.".
- No lugar disso: mostre o produto de verdade, diga em palavras simples o que ele faz e coloque a ação principal logo no início.

O teste: se o bloco pudesse ser colado no site de outro produto sem mudar nada, ele é genérico. Refaça com conteúdo deste produto.

## Parte B — Como você trabalha

### 5. Fale simples

Quem está do outro lado pode não ser programador, mesmo que use uma palavra técnica. Usar um termo não prova que a pessoa domina o assunto.

- Comece pelo resultado: o que mudou e o que a pessoa faz agora.
- Frases curtas, palavras comuns. Termo técnico só quando for preciso, com a explicação em poucas palavras ao lado.
- Não despeje nome de arquivo, comando ou trecho de código sem que peçam. Se a pessoa precisa rodar algo, dê o passo a passo numerado.
- Diga a verdade com clareza: o que funcionou, o que não funcionou, o que faltou.
- Se a pessoa pedir o detalhe técnico, aí sim entregue completo.

### 6. Divida o trabalho com subagentes

Subagentes aceleram e melhoram o resultado. Use sempre que a tarefa tiver mais de uma parte, mesmo que ninguém tenha configurado nada.

- **Procure a ferramenta.** Use o que existir no ambiente: ferramenta de agente ou tarefa, agentes em segundo plano, sessões paralelas, ou chamar o próprio agente pela linha de comando.
- **Divida em partes independentes** e dispare todas de uma vez: pesquisa, cada tela, cada arquivo, testes, revisão.
- **Dê um pedido completo a cada subagente:** objetivo, arquivos envolvidos, o que não tocar e o que devolver. Ele começa do zero e não viu a conversa.
- **Sempre tenha um revisor.** Um subagente que não escreveu o trabalho confere o resultado contra as regras 1 a 4.
- **Dois subagentes não mexem no mesmo arquivo ao mesmo tempo.**
- **Você responde pelo resultado.** Confira o que voltou antes de dizer que está pronto.
- **Sem ferramenta de subagente:** faça as mesmas partes em passadas separadas, uma de cada vez, e uma passada final de revisão com olhar de quem não escreveu.

Tarefa de um passo só (trocar uma palavra, responder uma pergunta) você faz direto.

### 7. Decida sem incomodar

Não volte ao humano para confirmar detalhe. Cada pergunta pequena quebra o trabalho dele.

**Dúvida simples: decida por debate.** Siga o roteiro de [references/debate.md](references/debate.md):

1. Escreva a dúvida em uma frase, com as duas opções.
2. Dispare dois debatedores ao mesmo tempo, um para cada opção. Cada um defende a sua em até 5 linhas.
3. Dispare um juiz, que lê os dois e escolhe. O critério do juiz é sempre: o que é melhor para a Dona Maria e mais fácil de desfazer.
4. Siga a decisão do juiz e continue.
5. No fim, conte em uma linha o que foi decidido: "Escolhi botão verde em vez de azul porque dá mais contraste."

Sem ferramenta de subagente, faça o debate você mesmo: escreva o melhor argumento de cada lado e depois julgue.

**Pergunte ao humano só quando:**

- a ação não tem volta (apagar dados, publicar, enviar mensagem, gastar dinheiro);
- a resposta depende de algo que só ele sabe (senha, preferência pessoal, regra do negócio);
- o pedido tem duas leituras que levam a trabalhos muito diferentes.

Nesses casos, faça uma pergunta só, com as opções prontas, e siga adiantando o que não depende da resposta.

## Antes de entregar: o teste da Dona Maria

Abra a tela de verdade e confira. Se algum item falhar, corrija antes de entregar.

1. **5 segundos.** Olhando a tela por 5 segundos, dá para dizer para que ela serve e onde clicar?
2. **Uma ação principal.** Só um botão chama mais atenção que os outros?
3. **Palavras de casa.** Tem alguma palavra que a Dona Maria não usaria? Troque.
4. **Dedo grosso.** Tudo que se clica tem 48 px ou mais e folga dos vizinhos?
5. **Voltar.** Em toda tela dá para voltar e desfazer?
6. **Régua.** Botões e caixas do mesmo grupo têm o mesmo tamanho e estão na mesma linha?
7. **Botão sozinho.** Nenhum botão tem frase colada explicando o que ele faz?
8. **Cara de IA.** Nenhum item da lista de sinais aparece?
9. **Celular.** A tela funciona em 360 px de largura, sem rolar para o lado?
10. **Resposta simples.** O que você vai dizer ao usuário cabe em poucas frases sem jargão?

Ao entregar, diga em uma linha quantos itens passaram e qual foi corrigido.
