# Fundamentos primários da HX Lens

Pesquisa concluída em 16 de julho de 2026. O objetivo é fundamentar apenas mecanismos que alteram o processo da skill, não montar uma bibliografia ornamental.

## Sumário

- [Régua de avaliação](#régua-de-avaliação)
- [UX e produto](#1-ux-e-produto)
- [Design de software](#2-design-de-software)
- [Engenharia de sistemas](#3-engenharia-de-sistemas)
- [Gestão comercial](#4-gestão-comercial)
- [Síntese para incorporação](#síntese-para-incorporação)

## Régua de avaliação

Cada fonte foi avaliada por:

- autoridade de quem publica sobre o assunto;
- tipo documental e força normativa;
- versão e status disponíveis na fonte oficial;
- escopo e limitações declaradas;
- mecanismo que acrescenta uma decisão, artefato, gate ou evidência ao processo da HX Lens.

### Bibliometria

| Fonte | Tipo | Número de citações | Fator de impacto | Régua adequada |
|---|---|---:|---:|---|
| ISO 9241-210 | norma internacional | N/A | N/A | status da norma, revisão sistemática, consenso e adoção normativa |
| WCAG 2.2 | W3C Recommendation e padrão Web | N/A | N/A | maturidade no processo W3C, testabilidade, implementação e adoção normativa |
| SEI Quality Attribute Scenarios / ADD | relatório técnico, material técnico e apresentação de método | N/A | N/A | autoridade técnica da instituição, rastreabilidade do método e uso profissional |
| NIST SP 800-218 | publicação especial governamental | N/A | N/A | status final, processo NIST e aplicabilidade ao risco de software |
| NASA/SP-2016-6105 Rev 2 | publicação especial e handbook governamental | N/A | N/A | autoria institucional, uso operacional, alinhamento com processos NASA e status oficial |
| Salesforce Forecasting | documentação de produto e guia de boas práticas do fornecedor | N/A | N/A | autoridade sobre a semântica do produto, atualidade e adequação ao processo comercial local |

Nenhum item acima é artigo de periódico. Portanto, **fator de impacto de revista não se aplica**. Contagens de citações variam entre bases, não são exibidas pelas fontes donas e misturariam normas, relatórios, apresentações e documentação viva sem denominador comparável. Sem uma base bibliométrica única, acessível e adequada a todos os tipos documentais, registrar um número seria falsa precisão. Para estas fontes, a força vem de autoridade normativa ou institucional, status documental, adoção e utilidade operacional.

## 1. UX e produto

### ISO 9241-210:2019

**Fonte primária:** [ISO 9241-210:2019 — Human-centred design for interactive systems](https://www.iso.org/standard/77520.html)

- **Autoridade:** a ISO é uma organização internacional independente e não governamental composta por organismos nacionais de normalização; a norma foi preparada pelo comitê técnico ISO/TC 159/SC 4. [Estrutura e governança da ISO](https://www.iso.org/structure.html)
- **Status e versão:** International Standard, edição 2, publicada em julho de 2019. A própria página informa que a versão foi revisada e confirmada em 2025 e permanece vigente. A edição de 2010 foi retirada.
- **Tipo e escopo:** requisitos e recomendações para princípios e atividades de design centrado no ser humano durante o ciclo de vida de sistemas interativos baseados em computador. Destina-se também a quem planeja e gerencia o processo de design.
- **Limitações declaradas:** oferece visão geral; não detalha métodos e técnicas, não cobre saúde ou segurança em profundidade e não substitui gestão de projeto completa. O texto integral é pago; a página pública oficial confirma escopo e status, mas não deve ser usada para alegar conformidade cláusula a cláusula.
- **Bibliometria:** citações N/A; fator de impacto N/A. A régua é vigência, consenso e adoção como norma internacional.

**Mecanismos que mudam o processo da HX Lens:**

1. Tratar o design centrado no ser humano como ciclo de vida, não como uma etapa de interface.
2. Exigir evidência de contexto de uso e requisitos humanos antes de selecionar a solução.
3. Produzir solução e avaliá-la contra os requisitos, repetindo o ciclo quando a evidência contradizer premissas.
4. Planejar responsáveis, recursos e evidências das atividades humanas; não presumir que uma lista de métodos equivale a executar o processo.

**Mudança mínima recomendada:** no ramo de UX, tornar explícito o loop `contexto de uso → requisitos do usuário → solução → avaliação contra requisitos → iteração`, mantendo a escolha de técnicas adaptativa ao caso.

### WCAG 2.2

**Fonte primária:** [Web Content Accessibility Guidelines (WCAG) 2.2](https://www.w3.org/TR/WCAG22/)

- **Autoridade:** W3C Recommendations são padrões Web produzidos em processo público de consenso, revisão por membros e política de patentes royalty-free. [Sobre os padrões W3C](https://www.w3.org/standards/about/)
- **Status e versão:** W3C Recommendation de 12 de dezembro de 2024; a URL indicada acima é a versão publicada mais recente. O W3C recomenda WCAG 2.2 para maximizar aplicabilidade futura. Em 2025, WCAG 2.2 também foi aprovada como ISO/IEC 40500:2025. A página ISO dessa adoção já indica revisão futura; para a HX Lens, a fonte atual deve continuar sendo a latest W3C Recommendation. [Anúncio oficial W3C](https://www.w3.org/press-releases/2025/wcag22-iso-pas/) e [registro ISO/IEC 40500:2025](https://www.iso.org/standard/91029.html)
- **Tipo e escopo:** critérios de sucesso testáveis e não específicos a tecnologia para acessibilidade de conteúdo Web em diferentes dispositivos. A conformidade é definida por níveis A, AA e AAA.
- **Limitações declaradas:** não atende a toda necessidade de toda pessoa com deficiência. Conformidade técnica não demonstra, por si, usabilidade ampla. Documentos “Understanding” e técnicas são informativos; os critérios de sucesso são a base normativa.
- **Bibliometria:** citações N/A; fator de impacto N/A. A régua é status de Recommendation, implementação, testabilidade e adoção como padrão.

**Mecanismos que mudam o processo da HX Lens:**

1. Definir o nível de conformidade aplicável como requisito antes do design; não escolher critérios isolados depois da solução.
2. Verificar páginas inteiras e processos completos, incluindo todas as etapas necessárias para concluir uma atividade, não apenas componentes felizes ou isolados.
3. Combinar teste automatizado e avaliação humana qualificada; ferramenta isolada não determina conformidade. Incluir pessoas com deficiência na avaliação de usabilidade quando material. [W3C — Evaluating Web Accessibility](https://www.w3.org/WAI/test-evaluate/)
4. Rastrear cada critério aplicável para superfície, estado, teste, resultado e correção. Avaliar também variações responsivas e conteúdo que possa interferir com o restante da página.
5. Tratar WCAG como piso verificável, não como substituto de pesquisa de compreensão, tarefa e contexto humano. [W3C — Understanding Conformance](https://www.w3.org/WAI/WCAG22/Understanding/conformance.html)

**Mudança mínima recomendada:** acrescentar ao ramo de UX um gate de acessibilidade: `alvo e escopo → critérios aplicáveis → cobertura de página/processo completo → teste automatizado + humano → evidência e falhas → correção`. Não exigir AAA como política geral sem justificativa; o próprio W3C alerta que todos os critérios AAA podem ser inviáveis para certos conteúdos.

## 2. Design de software

### SEI — cenários de atributos de qualidade

**Fontes primárias:**

- [Reasoning About Software Quality Attributes](https://www.sei.cmu.edu/library/reasoning-about-software-quality-attributes/)
- [Achieving Product Qualities Through Software Architecture Practices](https://www.sei.cmu.edu/documents/2993/2004_017_001_22862.pdf)

- **Autoridade:** o Software Engineering Institute (SEI) é um centro de pesquisa e desenvolvimento financiado pelo governo federal dos Estados Unidos e administrado pela Carnegie Mellon University. Atua em pesquisa aplicada e transição de práticas de engenharia de software. [Sobre o SEI](https://www.sei.cmu.edu/about/)
- **Status e versão:** os cenários não constituem norma nem produto versionado vigente. A fonte oficial reúne relatório técnico de 2001 e material técnico de 2004; são fundamentos metodológicos mantidos na biblioteca do SEI.
- **Tipo e escopo:** método para tornar atributos como desempenho, disponibilidade, modificabilidade, segurança, testabilidade e usabilidade específicos o bastante para orientar arquitetura e análise.
- **Limitações:** cenários caracterizam requisitos; não provam que uma arquitetura os satisfaz. A seleção dos atributos e das medidas continua dependente do contexto e dos stakeholders.
- **Bibliometria:** citações N/A; fator de impacto N/A. São relatório/material técnico institucional, não artigos de periódico. A régua adequada é autoridade do SEI, clareza operacional e rastreabilidade entre requisito e análise.

**Mecanismos que mudam o processo da HX Lens:**

1. Proibir atributos soltos como “rápido”, “seguro” ou “escalável” como requisito suficiente.
2. Especificar cada atributo material em seis partes: `fonte do estímulo → estímulo → ambiente → artefato afetado → resposta → medida da resposta`.
3. Priorizar os cenários com stakeholders e usá-los como drivers de arquitetura, critérios de comparação e testes.
4. Registrar efeitos colaterais entre atributos; uma tática que melhora disponibilidade pode afetar custo, complexidade, desempenho ou modificabilidade.

**Mudança mínima recomendada:** incluir um bloco obrigatório de cenário de atributo de qualidade para toda garantia não funcional material, com medida e ambiente de teste explícitos.

### SEI — Attribute-Driven Design

**Fontes primárias:**

- [ADD 3.0: Rethinking Drivers and Decisions in the Design Process](https://www.sei.cmu.edu/library/add-30-rethinking-drivers-and-decisions-in-the-design-process/)
- [Slides oficiais do ADD 3.0](https://www.sei.cmu.edu/documents/5832/ADD.3.0.Final_ki9IsLf.pdf)
- [Attribute-Driven Design Method Collection](https://www.sei.cmu.edu/library/attribute-driven-design-method-collection/)

- **Autoridade:** método originado e publicado no ecossistema técnico do SEI; a coleção oficial liga ADD a requisitos funcionais, restrições e cenários de atributos de qualidade.
- **Status e versão:** ADD 2.0 possui relatório técnico formal de 2006. ADD 3.0 foi apresentado em 2015 como evolução voltada a iterações, drivers e decisões; a página oficial o classifica como apresentação, não como norma ou relatório técnico substitutivo.
- **Tipo e escopo:** método iterativo de desenho arquitetural orientado por drivers, com decomposição, escolha de conceitos, definição de responsabilidades e interfaces, registro de decisões, análise e refinamento.
- **Limitações:** a página do ADD 3.0 avisa que conteúdo de conferência não representa necessariamente posições institucionais do SEI. O método organiza raciocínio; não substitui conhecimento do domínio, análise quantitativa nem validação executável.
- **Bibliometria:** citações N/A; fator de impacto N/A. A apresentação não pertence a periódico; o relatório ADD 2.0 tampouco tem fator de impacto de revista.

**Mecanismos que mudam o processo da HX Lens:**

1. Iniciar cada iteração com drivers explícitos: objetivo de design, requisitos funcionais primários, cenários de qualidade, restrições e concerns.
2. Definir um objetivo de iteração e o subproblema antes de decompor o sistema.
3. Escolher conceitos de design para satisfazer drivers; então instanciar elementos, responsabilidades e interfaces.
4. Registrar decisão e rationale, analisar o desenho contra o objetivo e refinar quando a análise não sustentar a garantia.

**Mudança mínima recomendada:** substituir desenho arquitetural “de uma vez” por microciclos `drivers → objetivo da iteração → alternativas/conceitos → elementos e interfaces → decisão/rationale → análise → refinamento`. Não importar o ritual completo quando a decisão for local e simples.

### NIST SP 800-218 — inclusão condicional

**Fontes primárias:**

- [NIST SP 800-218, SSDF Version 1.1 — página oficial](https://csrc.nist.gov/pubs/sp/800/218/final)
- [NIST SP 800-218 — PDF oficial](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-218.pdf)
- [Publicações do projeto SSDF](https://csrc.nist.gov/projects/ssdf/publications)

- **Autoridade:** publicação do National Institute of Standards and Technology (NIST), órgão técnico do governo dos Estados Unidos, com DOI oficial e histórico documental público.
- **Status e versão:** versão 1.1, Final, publicada em fevereiro de 2022. Em 16 de julho de 2026, a versão 1.2 aparece como draft de dezembro de 2025; portanto, não deve ser tratada como substituta final da 1.1.
- **Tipo e escopo:** NIST Special Publication com práticas de desenvolvimento seguro integráveis a qualquer ciclo de desenvolvimento. Organiza resultados em preparar a organização, proteger o software, produzir software bem protegido e responder a vulnerabilidades.
- **Limitações declaradas:** é alto nível, orientado a resultados e não prescreve ferramenta ou técnica. Define apenas um subconjunto do necessário; nem toda prática se aplica a todo caso, e a seleção deve ser baseada em risco.
- **Bibliometria:** citações N/A; fator de impacto N/A. A régua é status final, processo NIST, DOI, aderência ao risco e aplicabilidade ao ciclo de vida.

**Materialidade para a HX Lens:** **sim, mas somente quando segurança de software for material.** A referência atual de software cobre ameaça, segredo e falhas em runtime, mas não força a examinar ambiente de desenvolvimento, integridade dos artefatos, release, fornecedores e resposta pós-release.

**Mecanismos que mudam o processo da HX Lens:**

1. Acrescentar requisitos de segurança ao ciclo de desenvolvimento, não apenas à arquitetura executada.
2. Para risco material, mapear prática escolhida para owner, atividade, gate e evidência nos quatro resultados: preparar, proteger, produzir e responder.
3. Cobrir componentes de terceiros e requisitos comunicados a fornecedores quando fizerem parte da solução.
4. Planejar identificação, correção e prevenção de recorrência de vulnerabilidades residuais após release.

**Mudança mínima recomendada:** usar SSDF como overlay condicional de lifecycle security. Não carregar sua taxonomia completa em todo design de módulo e não alegar conformidade apenas por citar as quatro categorias.

## 3. Engenharia de sistemas

### NASA Systems Engineering Handbook

**Fontes primárias:**

- [NASA Systems Engineering Handbook — versão Web oficial](https://www.nasa.gov/reference/systems-engineering-handbook/)
- [NASA/SP-2016-6105 Rev 2 — PDF oficial](https://www.nasa.gov/wp-content/uploads/2018/09/nasa_systems_engineering_handbook_0.pdf)
- [NASA Technical Reports Server — registro 20170001761](https://ntrs.nasa.gov/citations/20170001761)

- **Autoridade:** handbook produzido no âmbito da NASA Office of the Chief Engineer, consolidando processos, lições e práticas da agência. O NTRS identifica autoria, tipo, número do relatório e distribuição pública.
- **Status e versão:** NASA/SP-2016-6105 Rev 2; Special Publication de 2016, publicada no NTRS em 17 de fevereiro de 2017, substituindo a Rev 1 de 2007. A NASA ainda mantém o conteúdo em sua página oficial.
- **Tipo e força:** handbook de orientação e boas práticas. O próprio prefácio afirma que é orientação de alto nível e não uma diretiva. Para obrigações internas da NASA, a fonte normativa separada é o [NPR 7123.1D](https://nodis3.gsfc.nasa.gov/displayDir.cfm?c=7123&s=1C&t=NPR), vigente desde 2023; não confundir handbook com requisito obrigatório.
- **Escopo:** ciclo completo de engenharia de sistemas, da definição de expectativas e design à realização, integração, operação, gestão técnica e retirada.
- **Limitações:** foi escrito para programas e projetos NASA. Profundidade, revisões, baselines e governança devem ser adaptados ao tamanho, complexidade, risco e ciclo de vida do sistema; importar toda a burocracia seria desproporcional.
- **Bibliometria:** citações N/A; fator de impacto N/A. É publicação especial governamental, não artigo. A régua é autoria oficial, uso operacional, rastreabilidade com processos da agência e adequação ao risco.

**Mecanismos que mudam o processo da HX Lens:**

1. Criar um **Concept of Operations (ConOps)** antes de fechar requisitos: cenários de uso e operação, atores, ambiente, interfaces, modos degradados, suporte, manutenção e descarte, sem antecipar a solução.
2. Executar de forma iterativa os quatro movimentos de design: expectativas dos stakeholders, requisitos técnicos, decomposição lógica e solução. Manter ConOps, requisitos e arquitetura coerentes entre si. [NASA — System Design Processes](https://www.nasa.gov/reference/4-0-system-design-processes/)
3. Diferenciar medidas em cadeia: **Measure of Effectiveness (MOE)** para efetividade percebida no contexto operacional, **Measure of Performance (MOP)** para características técnicas necessárias, e **Technical Performance Measure (TPM)** para acompanhar tendência real/estimada contra o valor esperado e acionar correção antes da falha final.
4. Baselinear somente produtos coerentes e maduros o bastante para a fase. Depois do baseline, toda mudança material deve ter proposta, impacto, autoridade decisória, aprovação, atualização de documentação e verificação da implementação. [NASA — Crosscutting Technical Management](https://www.nasa.gov/reference/6-0-crosscutting-technical-management/)
5. Manter um encadeamento auditável: `necessidade/ConOps → requisito → arquitetura responsável → alternativa e decisão → método de verificação → evidência → validação no uso real`.
6. Separar **verificação** da conformidade ao requisito de **validação** da utilidade no contexto operacional. Cobrir integração, operação, manutenção, estados degradados e handoffs, não apenas o caso nominal. [NASA — Product Realization](https://www.nasa.gov/reference/5-0-product-realization/)

**Mudança mínima recomendada:** no ramo de engenharia, adicionar quatro artefatos proporcionais ao risco: ConOps enxuto, baseline com change control, tabela `MOE → MOP → TPM`, e matriz integrada de rastreabilidade/verificação/validação. O trade study existente deve registrar decisão, critérios, incertezas e impacto sobre o baseline quando material.

## 4. Gestão comercial

### Salesforce Forecasting e pipeline

**Fontes primárias:**

- [Salesforce Forecasting Elements](https://help.salesforce.com/s/articleView?id=sales.forecasts3_definitions.htm&language=en_US&type=5)
- [Opportunity Stage to Forecast Category Mappings](https://help.salesforce.com/s/articleView?id=sales.faq_forecasts_category_mapping.htm&language=en_US&type=5)
- [Customize Pipeline Forecast Categories](https://help.salesforce.com/s/articleView?id=sf.forecasts3_customizing_forecasts_categories.htm&language=en_US&type=5)
- [Pipeline Forecasting Best Practices](https://help.salesforce.com/s/articleView?id=sales.forecasts3_best_practices.htm&language=en_US&type=5)
- [Collaborative Forecasts Implementation Guide](https://resources.docs.salesforce.com/latest/latest/en-us/sfdc/pdf/forecasts.pdf)

- **Autoridade:** Salesforce é a fonte dona da semântica e do comportamento do próprio produto de CRM e forecasting. Sua escala e experiência operacional aumentam a utilidade prática, mas não transformam documentação de produto em pesquisa científica independente.
- **Status e versão:** documentação viva da linha Salesforce Sales, com aplicabilidade por edição e release. As páginas oficiais consultadas estavam correntes em 16 de julho de 2026, mas não oferecem um identificador bibliográfico estável equivalente a uma norma; configuração e comportamento devem ser reconfirmados na release implantada.
- **Tipo e escopo:** documentação de produto e guia de implementação para oportunidades, categorias, hierarquia, rollups e ajustes de forecast.
- **Limitações:** descreve o modelo Salesforce e suas recomendações. Não demonstra que a taxonomia padrão maximiza forecast accuracy em todo mercado, motion ou organização. Probabilidades e gates precisam ser calibrados com dados e regras locais.
- **Bibliometria:** citações N/A; fator de impacto N/A. É vendor documentation. A régua é autoridade sobre o produto, atualidade, clareza da semântica e ajuste ao processo comercial real.

**Mecanismos que mudam o processo da HX Lens:**

1. Separar conceitualmente **Opportunity Stage** de **Forecast Category**. O estágio representa o estado atual da oportunidade no processo; a categoria determina como seu valor contribui para a previsão. São campos distintos, porém relacionados por um mapeamento configurável — não independentes.
2. Documentar `estágio → probabilidade → categoria padrão`, além de quem pode fazer override, com qual evidência e como o override será auditado. No Salesforce, mudança de estágio atualiza probabilidade e categoria conforme o mapping; o owner pode sobrescrever categoria em configurações suportadas.
3. Definir evidência de entrada e saída para cada estágio e evidência mínima para cada categoria. As categorias padrão são Pipeline, Best Case, Commit, Omitted e Closed; Most Likely é opcional. Os nomes não devem ser importados se não corresponderem ao vocabulário e à decisão local.
4. Declarar o método de rollup: **single category** ou **cumulative**, data-base do forecast, medida, moeda, hierarquia e período. O mesmo rótulo pode produzir totais diferentes conforme o rollup.
5. Separar gross rollup calculado das oportunidades de ajuste gerencial. Todo ajuste deve ter owner, valor anterior, valor novo, rationale, data e revisão; não reescrever silenciosamente a evidência do deal.
6. Calibrar probabilidades com histórico e revisar semanalmente ajustes e oportunidades voláteis. Manter próxima ação e data na oportunidade, sem confundir atividade com compromisso do comprador.

**Mudança mínima recomendada:** acrescentar ao ramo comercial uma tabela obrigatória `estágio → critério de entrada/saída → categoria padrão → evidência de override` e um contrato de forecast `período + data + medida + moeda + rollup + hierarquia + ajustes`. Salesforce sustenta a semântica e a mecânica, não metas universais.

## Síntese para incorporação

As adições de maior valor processual são:

1. **UX:** ciclo de design centrado no ser humano e gate WCAG por processo completo, com teste humano e automatizado.
2. **Software:** cenários mensuráveis de atributos de qualidade e iterações arquiteturais guiadas por drivers, decisões e análise.
3. **Engenharia:** ConOps, baseline/change control, cadeia MOE–MOP–TPM e rastreabilidade até verificação e validação.
4. **Comercial:** distinção mapeada entre estágio e categoria de forecast, contrato de rollup e ajustes auditáveis.
5. **Segurança:** SSDF apenas como overlay quando o risco material exigir evidência do ciclo de desenvolvimento, supply chain, release e resposta a vulnerabilidades.

Não há ganho em adicionar contagens de citação ou fatores de impacto fictícios. A manutenção correta é revisar periodicamente status, versão e links, e testar se cada mecanismo melhora entregáveis cegos da HX Lens sem exigir prompts excessivamente detalhados.
