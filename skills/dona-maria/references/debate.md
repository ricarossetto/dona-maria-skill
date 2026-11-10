# Decisão por debate

Use quando surgir uma dúvida simples no meio do trabalho. O ciclo todo deve levar segundos, não minutos.

## Quando usar

- Há duas opções razoáveis e nenhuma é perigosa.
- Errar custa pouco e dá para desfazer.
- Exemplos: cor do botão, ordem de campos, nome de um rótulo, qual biblioteca já instalada usar, se um aviso vai em janela ou no próprio campo.

Não use para ação sem volta, gasto de dinheiro ou algo que só o humano sabe. Nesses casos, pergunte.

Se uma opção ganha de longe, nem debata: escolha e siga.

## Passo a passo

1. Escreva a dúvida em uma frase e nomeie as opções A e B.
2. Dispare os dois debatedores **ao mesmo tempo**.
3. Quando os dois voltarem, dispare o juiz com os dois argumentos.
4. Aplique a decisão. Não reabra o debate.
5. Guarde uma linha para o resumo final ao usuário.

Uma rodada só. Se o juiz disser que empatou, vale a opção mais fácil de desfazer.

No máximo 3 debates com subagentes por tarefa. Passou disso, decida direto pelos critérios do juiz.

## Pedido ao debatedor

```
Você defende a opção {A ou B} nesta dúvida:
{dúvida em uma frase}

Contexto: {o que é a tela ou a tarefa, em 2 ou 3 linhas}

Quem usa: pessoas com pouca prática de computador, incluindo uma senhora de 70 anos.

Escreva o melhor argumento a favor da sua opção em até 5 linhas.
Seja concreto. Aponte também o maior risco da outra opção.
Não mexa em nenhum arquivo.
```

## Pedido ao juiz

```
Dois agentes debateram esta dúvida:
{dúvida em uma frase}

Argumento A: {texto}
Argumento B: {texto}

Escolha uma opção. Critérios, nesta ordem:
1. O que é mais fácil para uma senhora de 70 anos com pouca prática.
2. O que é mais fácil de desfazer depois.
3. O que dá menos trabalho.

Responda só com: a opção escolhida e o motivo em uma linha.
Não mexa em nenhum arquivo.
```

## Sem ferramenta de subagente

Faça os três papéis em sequência, por escrito:

1. Melhor argumento para A (até 5 linhas).
2. Melhor argumento para B (até 5 linhas).
3. Julgamento pelos três critérios.

Escreva os dois argumentos antes de julgar. Isso evita escolher pela primeira ideia.

## Como contar ao usuário

No resumo final, uma linha por decisão, em palavras simples:

> Escolhi mostrar o aviso no próprio campo, e não em janela, porque assim a pessoa não perde o que estava digitando.

Se o usuário discordar, troque sem discutir.
