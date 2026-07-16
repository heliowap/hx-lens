# Design de UX e superfície de produto

Projetar a superfície a partir de atores e jobs, não de uma lista de telas. Usar a cadeia:

```text
Ator → Contexto → Objetivo → Responsabilidade → Decisão → Restrição
→ Workflow → Superfície → Contrato → Evidência
```

## Enquadramento

Definir:

- intenção do produto e resultado observável;
- atores diretos, indiretos, operadores, aprovadores e integrações;
- job, frequência, contexto, entrada, decisão, saída e exceção;
- responsabilidades no frontstage, backstage e sistema;
- restrições de negócio, técnicas, regulatórias e de acesso.

Usar JTBD para motivação, análise de tarefas para o trabalho concreto, service blueprint para handoffs, RACI para responsabilidade e use cases para fluxos e exceções. Aplicar somente os métodos necessários.

Executar em ciclo: compreender contexto de uso → especificar requisitos humanos e de negócio → produzir solução → avaliar contra os requisitos → iterar. Planejar owner e evidência de cada atividade; lista de métodos não substitui execução.

## Mapa de papéis e jobs

Para cada ator, registrar:

```text
Job e resultado:
Contexto e gatilho:
Responsabilidade:
Decisões e aprovações:
Informação necessária:
Fricção e influência:
Consequência e próxima ação:
```

## Jornada e workflow

Mapear antes → interação → depois. Em cada etapa, ligar:

- ação e decisão do usuário;
- superfície visível e feedback;
- operação humana ou automação de bastidor;
- sistema, contrato ou integração;
- estado, evidência, log ou auditoria;
- falha, recuperação e canal humano quando aplicável.

## Superfícies

Para cada tela, mensagem, configuração, fila, painel ou canal, definir:

- ator, job e ponto de entrada;
- informação visível e prioridade;
- estados vazio, carregando, sucesso, pendente, bloqueado, expirado e falha que sejam aplicáveis;
- ações permitidas, decisão material e confirmação;
- regra de acesso e owner da configuração;
- contrato backend, evento ou job correspondente;
- erro, recuperação, suporte e continuidade entre canais;
- métrica de uso, conclusão, qualidade ou risco.

Detectar capacidade backend sem superfície, superfície sem contrato, ação sem permissão, permissão sem ação, rota sem entrada e configuração sem owner.

## Acesso

Modelar autorização como combinação, não apenas papel:

```text
Role + Permission + Tenant/Scope + Relationship
+ Workflow State + Plan Entitlement
```

Usar RBAC para papéis estáveis, ABAC para atributos, ReBAC para relações, entitlement para plano e regra de workflow para ações dependentes de estado. Alinhar visibilidade no frontend com enforcement no backend. Registrar ações em nome de terceiros, overrides e aprovações quando materiais.

## Compreensão e recuperação

- Tornar estado, consequência, custo e próxima ação reconhecíveis.
- Preferir uma decisão material por momento e divulgação progressiva.
- Usar linguagem do ator, preservando precisão operacional.
- Projetar para teclado, leitor de tela, zoom, contraste, idioma, conectividade e interrupção conforme o público.
- Para Web, definir alvo e escopo WCAG antes da solução; rastrear critérios aplicáveis por processo completo, combinando teste automatizado e avaliação humana qualificada.
- Em tarefas críticas, validar compreensão pelo resultado demonstrado, não por confirmação vazia.
- Dizer o que ocorreu, o que permaneceu seguro, o que fazer agora e como obter ajuda.

## Saída

1. Intenção, premissas e restrições.
2. Mapa de atores, jobs e responsabilidades.
3. Jornada ou service blueprint.
4. Mapa de superfícies, estados e decisões.
5. Modelo de acesso e ownership.
6. Contratos backend, eventos e auditoria.
7. Erros, recuperação, copy decisiva e suporte.
8. Validação, métricas, guardrails operacionais e, para Web, alvo e cobertura WCAG.

Concluir quando todo job material tiver superfície ou canal humano; toda ação tiver regra de acesso e contrato; todo estado terminal ou de falha tiver consequência e recuperação; e todo requisito ou hipótese relevante tiver avaliação e evidência. Para Web, incluir alvo WCAG, processos cobertos e plano de teste automatizado e humano qualificado.

Fundamentação, status e limites: `references/foundations.md`, seção “UX e produto”.
