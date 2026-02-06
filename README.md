# Product Mix Optimization — Estudo de Caso (Lua Smart Tech)

Projeto de otimização de mix de produtos com **programação linear** para apoiar decisões de produção. O foco é mostrar
como Analytics conecta restrições operacionais a impacto financeiro, com uma abordagem típica de Engenharia Química
(otimização de processo, gargalos e uso de capacidade).

## Contexto de negócio
A Lua Smart Tech fabrica dois modelos de smartphone (Lua1 e Lua2). O time de operações precisa definir o plano de
produção mensal considerando demanda, custo de componentes e capacidade de mão de obra (montagem e teste).

## Decisão suportada
- Mix ótimo de produção (quantidade por modelo)
- Lucro máximo esperado
- Gargalos de capacidade e folgas disponíveis

## Premissas e dados (síntese)
Valores em R$ e horas.

| Parâmetro | Lua1 | Lua2 |
| --- | ---:| ---:|
| Demanda máxima (unid.) | 600 | 1200 |
| Preço de venda | 300 | 450 |
| Custo de componentes | 150 | 225 |
| Horas de montagem | 5 | 6 |
| Horas de teste | 1 | 2 |

Capacidade mensal:
- Montagem: 10.000 h
- Teste: 3.000 h

## Resultado do modelo
- **Plano ótimo:** 560 unidades Lua1 e 1200 unidades Lua2
- **Lucro máximo estimado:** R$ 199.600
- **Gargalo:** montagem (100% utilizada)
- **Folga:** teste (40 h) e demanda de Lua1 (40 unidades)

## Por que isso importa para o negócio?
- Direciona a produção para o maior retorno dado o gargalo real.
- Indica onde expandir capacidade gera mais valor (montagem).
- Transforma restrições operacionais em decisão financeira clara.

## Conexão com Engenharia Química + Analytics
A abordagem é análoga à otimização de processos industriais: recursos limitados, custos variáveis, demanda e decisão
sobre o mix ótimo. A análise traduz o problema físico em um modelo matemático replicável.

## Como executar
Dependências principais:
- `pulp`
- `pandas`
- `matplotlib`

Abra o notebook:
- `Mix of products Optimization.ipynb`

## Estrutura do projeto
- `Mix of products Optimization.ipynb`: estudo de caso completo, com modelo, solução e insights

## Próximos passos sugeridos
- Sensibilidade a demanda, preços e capacidade
- Inclusão de custos fixos e setup
- Expansão para mais linhas de produto
