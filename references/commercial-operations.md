# Operação e gestão comercial

Projetar o sistema comercial como fluxo de decisões, dados e compromissos. Otimizar receita com qualidade, previsibilidade, velocidade e custo de servir explícitos.

## Enquadramento

Definir:

- meta, horizonte, moeda e denominador;
- segmentos, ICP, casos de uso, ticket e ciclo esperado;
- canais de aquisição e motion inbound, outbound, parceiro ou expansão;
- papéis de marketing, SDR, vendas, solução, financeiro, jurídico, implantação e sucesso;
- restrições de capacidade, margem, elegibilidade, compliance e entrega.

## Pipeline

Modelar estágios por compromisso verificável, não por atividade vaga. Para cada estágio:

```text
Objetivo:
Owner:
Critério de entrada:
Trabalho e decisão:
Dados obrigatórios:
Critério de saída:
Prazo máximo e alerta:
Próxima ação:
```

Separar lead, oportunidade qualificada, solução validada, proposta, negociação, compromisso, ganho, perdido e implantação conforme o motion. Evitar avanço baseado apenas em reunião realizada ou intenção declarada.

## Qualificação e dados

Definir gate de qualificação com problema, impacto, fit, urgência, autoridade, processo decisório, orçamento ou capacidade de pagamento e próximo compromisso. Adaptar os critérios ao mercado.

Usar coleta progressiva no CRM: exigir em cada estágio somente o dado necessário à decisão seguinte. Manter um brief comercial canônico para problema, stakeholders, solução, escopo, valor, riscos, concorrência, termos e plano de fechamento.

Definir fonte de verdade, campos calculados, motivos estruturados de perda, higiene, deduplicação, ownership e SLA de atualização. Não usar campos sem decisão associada.

## Handoffs e governança

Para cada passagem entre equipes, definir entrada, pacote mínimo, aceite, rejeição, SLA e owner. Acionar especialistas por gatilho objetivo, como integração complexa, desconto, risco financeiro, cláusula não padrão ou setor regulado.

Estabelecer:

- cadência de prospecção, follow-up, negociação e reativação;
- automação por evento e estado, com saída quando houver resposta ou mudança;
- regras de desconto, alçada, exceção e expiração;
- forecast por evidência de compromisso, não apenas opinião do vendedor;
- revisão semanal de pipeline, negócios críticos, bloqueios, aging e ações;
- retrospectiva de ganhos, perdas e qualidade da implantação.

## Forecast

Separar estágio da oportunidade de categoria de forecast. O estágio representa o estado do processo; a categoria controla como o valor contribui para a previsão. Definir e versionar:

```text
Estágio → entrada/saída → probabilidade calibrada → categoria padrão
→ evidência de override → owner e auditoria
```

Usar Pipeline, Best Case, Commit, Omitted, Closed ou vocabulário local equivalente somente com definição operacional. Declarar período, data-base, medida, moeda, hierarquia e rollup single-category ou cumulativo.

Separar gross rollup calculado de ajuste gerencial. Registrar valor anterior, valor novo, rationale, owner e data; preservar a evidência original da oportunidade.

## Métricas

Definir cálculo, coorte, janela, moeda e fonte. Exemplos:

- conversão A→B = oportunidades que entraram em B / oportunidades que entraram em A;
- win rate = ganhos / (ganhos + perdidos) no conjunto fechado;
- ciclo = mediana e P90 entre entrada qualificada e ganho;
- aging = tempo no estágio atual;
- cobertura = pipeline qualificado ponderado ou não / meta restante, declarando a versão;
- forecast accuracy = diferença entre previsto e realizado / previsto;
- produtividade = resultado por capacidade comercial, sem confundir atividade com valor;
- qualidade = churn inicial, implantação falha, desconto, margem, inadimplência ou suporte por venda.

Segmentar por origem, ICP, vendedor, produto, ticket, região e motivo somente quando houver volume e decisão associados.

## Saída

1. Objetivo, segmentos, motion e premissas.
2. Papéis, responsabilidades e handoffs.
3. Pipeline com critérios de entrada e saída.
4. Qualificação, brief e modelo de dados do CRM.
5. Cadências, automações e alçadas.
6. Contrato de forecast, categorias, rollup e ajustes.
7. Dashboard com definições e denominadores.
8. Plano de implantação, governança e riscos.

Concluir quando toda oportunidade tiver owner, estágio verificável, próximo compromisso e dado mínimo; todo handoff tiver aceite e SLA; toda previsão tiver categoria e evidência; todo ajuste tiver auditoria; e toda métrica tiver fórmula, janela, coorte e fonte.

Fundamentação, status e limites: `references/foundations.md`, seção “Gestão comercial”.
