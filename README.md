![HX Lens — experiência humana, produto, engenharia e negócio](assets/hx-lens-cover.png)

# HX Lens

**Enxergue o sistema inteiro antes de desenhar uma parte.**

[![Licença MIT](https://img.shields.io/badge/licen%C3%A7a-MIT-D18A32.svg)](LICENSE)
[![Repositório público](https://img.shields.io/badge/GitHub-p%C3%BAblico-111111.svg)](https://github.com/heliowap/hx-lens)

HX Lens é uma skill aberta para agentes de inteligência artificial projetarem e avaliarem experiências, produtos, sistemas, software, marketing e operações comerciais pela mesma unidade de análise: a experiência humana completa.

Ela conecta o que normalmente aparece separado — atores, decisões, restrições, fricções, influência, interfaces, handoffs e resultados — e transforma esse mapa em análise, especificação, operação ou material pronto para uso.

## O que ela resolve

Uma interface pode ser clara e ainda pertencer a uma jornada ruim. Um módulo pode estar correto e ainda transferir custo para suporte. Uma campanha pode gerar atenção e entregar oportunidades sem qualidade. Um pipeline pode parecer eficiente enquanto esconde decisões, estados e responsabilidades.

A HX Lens força cada parte a responder ao sistema:

```text
ator → contexto → objetivo → restrição → decisão
     → workflow → interface/superfície → consequência
```

O resultado não é uma opinião genérica. É um artefato com premissas, evidências, trade-offs, falhas possíveis, validação e métricas.

## Quatro ramos, uma lente

| Ramo | O que projeta ou avalia |
| --- | --- |
| **UX e produto** | Jornadas, papéis, jobs, superfícies, estados, acesso, compreensão, erros e recuperação |
| **Software e engenharia** | Requisitos, arquitetura, módulos, interfaces, dependências, confiabilidade, testes e validação |
| **Marketing** | Posicionamento, ofertas, campanhas, copy, roteiros, chamadas para ação, influência e testes |
| **Gestão comercial** | Segmentação, pipeline, qualificação, cadências, CRM, handoffs, forecast, governança e métricas |

Os ramos podem operar isoladamente ou em conjunto. Isso permite seguir uma decisão desde a promessa comercial até a interface, o contrato de software, a operação e o resultado observado.

## Quando usar

Use a HX Lens para:

- transformar um problema difuso em requisitos, estados, decisões e responsabilidades;
- criticar uma jornada sem limitar a análise às telas;
- projetar UX, superfícies de produto ou arquitetura de módulos;
- comparar alternativas de engenharia e seus trade-offs;
- criar posicionamento, campanha, oferta, copy ou roteiro;
- redesenhar pipeline, qualificação, cadências e governança comercial;
- localizar fricção acidental, necessária, transferida ou deliberada;
- alinhar resultado humano, resultado técnico e resultado de negócio.

Para implementar código, frontend ou mídia, a HX Lens entrega a direção e a especificação para a skill de produção apropriada.

## Experimente

A invocação é manual para evitar acionamento fora de contexto.

No Codex:

```text
Use $hx-lens para analisar este produto de ponta a ponta: atores, decisões,
fricções, interfaces, falhas, resultados e métricas.
```

```text
Use $hx-lens para projetar a arquitetura, os estados, os contratos e a
estratégia de validação deste módulo.
```

```text
Use $hx-lens para transformar esta proposta de valor em posicionamento,
landing page, campanha e plano de testes.
```

```text
Use $hx-lens para redesenhar o pipeline comercial, os critérios de passagem,
os handoffs, o forecast e a governança.
```

No Claude Code:

```text
/hx-lens avalie esta jornada e proponha uma solução de UX verificável.
```

## O que esperar da saída

Cada entrega é adaptada ao ramo, mas preserva o mesmo núcleo:

1. problema, atores e resultados esperados;
2. forças, motivações, fricções e restrições;
3. decisões, estados, interfaces e handoffs;
4. alternativas e trade-offs materiais;
5. verificação, métricas e evidências necessárias;
6. falhas possíveis e risco residual.

A skill separa evidência, requisito, hipótese, premissa e desconhecido. Ela evita scores obrigatórios e prioriza somente quando a decisão se beneficia disso.

## Instalação

Mantenha uma única cópia real global. Use links simbólicos nos diretórios dos agentes e não instale a skill dentro de uma pasta de projetos, salvo quando uma instalação local for intencional.

```bash
mkdir -p ~/.agents/skills ~/.codex/skills ~/.claude/skills
git clone https://github.com/heliowap/hx-lens.git ~/.agents/skills/hx-lens
ln -s ~/.agents/skills/hx-lens ~/.codex/skills/hx-lens
ln -s ~/.agents/skills/hx-lens ~/.claude/skills/hx-lens
```

Reinicie o agente ou abra uma nova sessão para atualizar o catálogo de skills.

Para atualizar:

```bash
git -C ~/.agents/skills/hx-lens pull --ff-only
```

## Como a skill permanece enxuta

```text
hx-lens/
├── SKILL.md                 método, roteamento e contrato de saída
├── agents/openai.yaml       metadados de interface e invocação
└── references/              conhecimento carregado somente sob demanda
    ├── product-ux-design.md
    ├── software-design.md
    ├── engineering-design.md
    ├── marketing-influence.md
    ├── commercial-operations.md
    └── ...
```

O `SKILL.md` carrega apenas a referência necessária para cada tarefa. Design de UX não consome o repertório comercial; engenharia não carrega marketing; contextos regulados adicionam os limites aplicáveis. Essa divulgação progressiva preserva contexto sem empobrecer a análise.

## Fundamentos

A HX Lens combina referências de experiência humana, acessibilidade, engenharia de sistemas, design de software, fricção, influência e operação comercial. Entre as bases estão ISO 9241-210, WCAG 2.2, NASA Systems Engineering Handbook, NIST Secure Software Development Framework, Software Engineering Institute e literatura especializada em fricção e persuasão.

Mecanismos de influência são tratados como repertório criativo e hipóteses testáveis. Materiais destinados à publicação devem observar as leis, normas e regulamentações aplicáveis à jurisdição, ao setor, ao público e ao canal.

## Contribua

Issues e pull requests são bem-vindos. Boas contribuições:

- ampliam capacidade sem transformar o `SKILL.md` em enciclopédia;
- colocam conhecimento especializado em `references/`;
- preservam rastreabilidade entre requisito, decisão e evidência;
- distinguem fundamento confiável de hipótese operacional;
- mantêm a invocação manual e o escopo multidisciplinar.

## Licença

HX Lens é software livre distribuído sob a [licença MIT](LICENSE).
