# Sistema Especialista: Trilha de Estudos

Sistema especialista baseado em regras que monta uma trilha de estudos personalizada. A partir de quantas
horas por dia a pessoa tem, do ritmo desejado e dos dias da semana disponíveis, ele distribui as aulas do
curso em sprints, com percentual de conclusão, dias planejados e duração estimada de cada bloco.

Projeto acadêmico do curso de Análise e Desenvolvimento de Sistemas (IFSC).

**[Abrir a aplicação](https://zalone03.github.io/Sistema-Especialista-Trilha-de-Estudos/)**

## Como funciona

O usuário informa apenas três coisas:

| Entrada | Opções |
|---|---|
| Horas por dia | menos de 1, 1, 2, 3, 4 ou mais de 4 |
| Ritmo | o mais rápido possível, rápido, moderado, a longa data |
| Disponibilidade | quais dias da semana, de domingo a sábado |

Os dados do curso já estão no sistema: 8 módulos, com as aulas e a duração de cada uma em minutos.

A partir daí, a base de regras calcula a carga diária real, aplica o fator do ritmo escolhido (do mais
agressivo ao mais folgado) e agrupa as aulas em sprints, respeitando a fronteira entre módulos. O resultado
mostra o resumo da decisão e as sprints recomendadas, cada uma com percentual, quantidade de dias, lista de
aulas e minutos por aula.

## Cenários prontos

Para testar sem preencher o formulário, a interface traz quatro cenários:

- **Agressivo**: pouco tempo por dia e meta alta
- **Equilibrado**: 3 dias por semana e ritmo moderado
- **Intensivo**: muito tempo disponível e conclusão rápida
- **Longo prazo**: ritmo leve, com mais folga

Eles servem para comparar rapidamente como as regras reagem a perfis bem diferentes de estudante.

## Por que é um sistema especialista

Não há aprendizado de máquina aqui. O comportamento vem de uma base de conhecimento explícita (o curso, as
durações, os fatores de ritmo) e de um conjunto de regras que emula o raciocínio de quem planeja estudos:
quanto cabe em um dia, quando faz sentido fechar uma sprint, quanto tempo a jornada toda leva. É
exatamente o ponto do exercício: a decisão precisa ser rastreável, e não uma caixa preta.

## Tecnologias

HTML, CSS e JavaScript puro, em arquivo único, sem dependências ou build. Basta abrir o `index.html` no
navegador.

## Como executar

```bash
git clone https://github.com/Zalone03/Sistema-Especialista-Trilha-de-Estudos.git
```

Depois é só abrir o `index.html`. Nenhuma instalação é necessária.

## Possíveis evoluções

- Permitir carregar o curso a partir de um JSON, em vez de dados fixos no código
- Considerar feriados e pausas planejadas
- Exportar a trilha gerada em PDF ou agenda
- Registrar o progresso real e recalcular as sprints restantes
