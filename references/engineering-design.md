# Design de engenharia

Projetar sistemas, produtos e processos com rastreabilidade entre necessidade, requisito, arquitetura, risco e verificação. Tratar segurança, confiabilidade e operabilidade como propriedades técnicas do sistema.

## Sumário

- [Enquadramento do sistema](#enquadramento-do-sistema)
- [Requisitos](#requisitos)
- [Arquitetura e interfaces](#arquitetura-e-interfaces)
- [Configuration baseline e mudança](#configuration-baseline-e-mudança)
- [Alternativas e trade study](#alternativas-e-trade-study)
- [Falhas, hazards e confiabilidade](#falhas-hazards-e-confiabilidade)
- [Verificação e validação](#verificação-e-validação)
- [Saída](#saída)

## Enquadramento do sistema

Definir:

- missão, usuários, operadores, mantenedores e partes externas;
- fronteira do sistema, ambiente e ciclo de vida;
- entradas, saídas, interfaces e dependências;
- cenários nominais, degradados, manutenção e descarte;
- resultado humano, técnico, operacional e comercial.

Criar um ConOps proporcional ao risco antes de fechar requisitos: cenários, atores, ambiente, interfaces, operação, suporte, manutenção e descarte, descrevendo o que se espera sem antecipar a solução.

## Requisitos

Escrever requisitos verificáveis, com identificador e fonte. Separar:

- função e comportamento;
- desempenho, capacidade, precisão e tempo;
- dimensões físicas, energia, materiais e ambiente;
- segurança, confiabilidade, disponibilidade e manutenção;
- interfaces humanas, mecânicas, elétricas, digitais e organizacionais;
- fabricação, instalação, operação, suporte e descarte;
- custo, prazo, fornecimento e restrições legais ou regulatórias.

Registrar premissas, desconhecidos e conflitos. Evitar solução disfarçada de requisito, salvo quando a solução for uma restrição real.

## Arquitetura e interfaces

Decompor o sistema apenas até localizar responsabilidade, interação e verificação. Para cada elemento, definir:

- função, owner e limites;
- entradas, saídas, tolerâncias e estados;
- interface, protocolo ou handoff;
- recursos consumidos e margens;
- dependências, modos degradados e manutenção;
- evidência que provará o atendimento.

Usar budgets quando várias partes consomem um limite comum, como massa, energia, latência, custo, erro ou capacidade. Ligar efetividade operacional (MOE), desempenho técnico necessário (MOP) e tendência medida contra o esperado (TPM) quando o acompanhamento antecipado mudar decisões.

## Configuration baseline e mudança

Baselinear ConOps, requisitos, arquitetura e interfaces somente quando estiverem coerentes e maduros para a fase. Registrar conteúdo, versão, gate de maturidade, data e autoridade decisória.

Para toda mudança material após o baseline, registrar:

```text
gatilho → requisitos/interfaces/budgets/riscos afetados → alternativas
→ autoridade e decisão → implantação/rollback → documentos, testes e evidência atualizados
```

## Alternativas e trade study

Gerar alternativas materialmente diferentes. Comparar por critérios ligados aos requisitos:

- desempenho e margem;
- custo total e prazo;
- confiabilidade, segurança e recuperabilidade;
- complexidade de fabricação, integração, operação e manutenção;
- disponibilidade de fornecedores e reversibilidade;
- impacto sobre usuários, operadores e negócio.

Explicitar evidência, incerteza e sensibilidade. Pesos e notas servem à decisão; não substituem argumento técnico nem escondem um critério eliminatório.

## Falhas, hazards e confiabilidade

Para cada função e interface crítica, mapear:

```text
Modo de falha → causa → efeito local → efeito no sistema
→ detecção → prevenção/mitigação → recuperação → risco residual
```

Analisar falha única, causa comum, uso incorreto previsível, perda de energia ou comunicação, degradação, manutenção e erro operacional. Definir estado seguro ou degradado, redundância, inspeção e margem quando exigidos pelo risco ou pela regulamentação.

## Verificação e validação

- **Verificação:** confirmar que a solução atende ao requisito.
- **Validação:** confirmar que o sistema resolve a necessidade no contexto real.

Manter matriz:

```text
Requisito → método → procedimento/ensaio → critério de aceitação
→ ambiente → owner → evidência → status
```

Combinar análise, inspeção, demonstração, teste, simulação e piloto. Validar operação, manutenção, falhas e handoffs, não apenas funcionamento nominal.

## Saída

1. Missão, fronteira, atores, ciclo de vida e ConOps.
2. Requisitos, premissas e restrições.
3. Arquitetura, funções, estados, interfaces, budgets e cadeia `MOE → MOP → TPM` quando material.
4. Alternativas e trade study.
5. Modos de falha, mitigação e risco residual.
6. Configuration baseline, registro de mudança, integração, operação e manutenção.
7. Matriz de verificação e plano de validação.

Concluir quando todo requisito material tiver fonte, owner, arquitetura responsável, critério de aceitação e método de verificação; toda interface crítica tiver contrato; desempenho acompanhado tiver `MOE → MOP → TPM`; o configuration baseline declarar conteúdo, versão, gate e autoridade; toda mudança pós-baseline tiver impacto, decisão e evidência atualizada; e todo risco técnico relevante tiver detecção, resposta e risco residual explícitos.

Fundamentação, status e limites: `references/foundations.md`, seção “Engenharia de sistemas”.
