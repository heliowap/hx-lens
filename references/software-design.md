# Design de software

Projetar módulos profundos: muito comportamento atrás de uma interface pequena, colocada em um seam claro e testável pela mesma interface usada por callers.

## Vocabulário

- **Módulo:** interface e implementação tratadas como uma unidade de design.
- **Interface:** tudo que o caller precisa saber: operações, tipos, invariantes, ordem, erros, configuração e desempenho.
- **Seam:** ponto onde o comportamento pode variar sem editar o caller.
- **Adapter:** implementação concreta que satisfaz uma interface no seam.
- **Profundidade:** comportamento e complexidade ocultos por unidade de interface.

## Enquadramento

Definir antes da solução:

- resultado técnico, humano e de negócio;
- callers, operadores e sistemas externos;
- requisitos funcionais e atributos de qualidade;
- invariantes e estados que não podem ocorrer;
- volume, latência, consistência, disponibilidade e custo esperados;
- dados sensíveis, ameaças, falhas caras e recuperação exigida;
- dependências existentes e restrições do repositório.

Expressar todo atributo de qualidade material como cenário mensurável: `fonte do estímulo → estímulo → ambiente → artefato → resposta → medida`. Usar os cenários priorizados como drivers, critérios de comparação e testes; registrar efeitos colaterais entre atributos.

## Módulo e interface

1. Escolher o seam que concentra mudança e conhecimento.
2. Definir uma interface pequena, orientada ao resultado do caller.
3. Declarar invariantes, ordem, idempotência, erros, configuração e desempenho como parte da interface.
4. Ocultar parsing, coordenação, política, retries, persistência e detalhes de fornecedor na implementação quando não servirem ao caller.
5. Aplicar o teste de exclusão: ao remover o módulo, a complexidade deve reaparecer nos callers; caso contrário, ele é pass-through.

Em decisão material ou incerta, desenhar ao menos duas interfaces realmente diferentes. Comparar profundidade, localidade, seam, caso comum, extensibilidade, erros e testabilidade antes de recomendar uma.

Em arquitetura ampla, iterar: drivers → objetivo da iteração → conceitos candidatos → elementos e interfaces → decisão e rationale → análise → refinamento. Adaptar o rito ao tamanho da decisão.

## Dependências e adapters

Classificar cada dependência:

- **in-process:** computação ou estado local; testar diretamente;
- **local substituível:** banco, filesystem ou broker com implementação local fiel;
- **remota própria:** definir port no seam e adapters de produção e teste;
- **externa:** injetar port e usar mock ou sandbox contratual.

Criar seam somente quando a variação for real. Manter seams internos privados à implementação; teste não justifica ampliar a interface externa.

## Estado, dados e concorrência

Definir quando aplicável:

- máquina de estados, transições, terminais e eventos;
- identidade, ownership, versionamento e retenção dos dados;
- limites transacionais e efeitos externos;
- idempotência, deduplicação, ordenação e replay;
- concorrência, locks, isolamento, leases ou resolução de conflito;
- migração, compatibilidade e rollback.

## Falhas e operação

Para cada dependência e transição material, especificar:

- timeout, indisponibilidade, entrada inválida e resultado parcial;
- erro retryable, terminal, de configuração ou de regra;
- retry, backoff, limite, circuit breaker ou compensação;
- estado visível ao caller e ação de recuperação;
- logs estruturados, métricas, traces, auditoria e alerta;
- segredo, dado sensível e redução de exposição.

Quando segurança de lifecycle for material, cobrir preparação, proteção do ambiente e artefatos, produção segura e resposta a vulnerabilidades. Ligar cada prática escolhida a owner, gate e evidência; incluir componentes de terceiros e release quando fizerem parte do risco.

## Testes

Usar a interface como superfície de teste. Cobrir:

- comportamento nominal, invariantes e erros observáveis;
- transições, concorrência, repetição e ordem;
- falhas em cada seam e recuperação após crash;
- contratos de adapters e compatibilidade;
- propriedades, limites de carga e orçamento de desempenho;
- banco, fila ou runtime real quando o risco depende de sua semântica.

Testes devem sobreviver à troca da implementação que preserva a interface.

## Saída

1. Contexto, drivers, requisitos, restrições e cenários mensuráveis de atributos de qualidade.
2. Módulo, seam e interface completa.
3. Estados, dados, invariantes e transações.
4. Dependências, ports e adapters.
5. Falhas, recuperação e observabilidade.
6. Alternativas e recomendação com trade-offs.
7. Uso pelo caller e estratégia de testes.

Concluir quando todo caller material puder usar a interface sem conhecer a implementação; todo atributo de qualidade material tiver fonte, estímulo, ambiente, artefato, resposta e medida; todo efeito tiver regra de consistência; toda falha relevante tiver estado e recuperação; e cada garantia depender de teste executável ou evidência identificada.

Fundamentação, status e limites: `references/foundations.md`, seção “Design de software”.
