---
name: hx-lens
description: Aplicar uma lente de Human Experience (HX) a jornadas digitais, sobretudo saúde e contextos sensíveis. Usar quando o usuário invocar explicitamente $hx-lens para avaliar ética, arquitetura de escolhas, contexto físico/social, experiência antes e depois da tela, vulnerabilidade, confiança ou diferença entre o modelo mental humano e o sistema. Não usar para produzir frontend, protótipos, slides, PDFs, imagens, áudio, vídeo ou direção estética.
---

# HX Lens

Avaliar a experiência humana além da interface. Complementar, não substituir, pesquisa com usuários, acessibilidade, revisão clínica, compliance ou skills de implementação.

## Escopo

Examinar:

- contexto antes, durante e depois da interação;
- ambiente físico, estado emocional, apoio social e continuidade da jornada;
- diferença entre linguagem/modelo mental humano e estrutura do sistema;
- arquitetura de escolhas, consentimento, reversibilidade e assimetria;
- riscos ampliados por saúde, urgência, medo, dependência ou baixa literacia;
- evidência necessária para confirmar hipóteses comportamentais.

Não produzir artefatos. Para UI/frontend, usar `impeccable`. Para apresentações, PDFs ou imagens, usar skills oficiais correspondentes.

## Referências

Carregar somente o necessário:

- escolhas, mecanismos e limites de inferência: `references/decision-lenses.md`;
- ética e deceptive patterns: `references/ethical-design.md`;
- saúde e jornadas sensíveis: `references/healthtech-ux.md`;
- formato de análise: `references/critique-lens.md`.

## Método

1. Definir decisão, pessoa afetada e resultado desejado.
2. Mapear jornada antes → interação → depois. Incluir consequências fora da tela.
3. Separar fato observado, hipótese e desconhecido.
4. Identificar pressão, assimetria, irreversibilidade e grupos vulneráveis.
5. Aplicar apenas lentes relevantes. Nunca encaixar um viés por obrigação.
6. Pedir ou propor evidência: entrevista, observação, teste de usabilidade, analytics, experimento ou revisão especializada.
7. Recomendar menor mudança capaz de reduzir risco ou melhorar compreensão.
8. Explicitar trade-off, confiança e risco residual.

## Regras

- Tratar vieses como hipóteses contextuais, não diagnósticos.
- Não inferir motivação, emoção ou comportamento apenas por screenshot.
- Não inventar métricas, estudos, personas ou impacto esperado.
- Não usar coeficientes psicológicos como constantes universais.
- Não recomendar fricção, ocultação, urgência artificial ou sunk cost para prender pessoas.
- Favorecer transparência, escolha real, saída simétrica, recuperação de erro e consentimento informado.
- Em saúde, não substituir julgamento clínico nem apresentar heurística como exigência médica ou legal.
- Distinguir persuasão legítima de manipulação pelo efeito sobre autonomia, não só pela veracidade literal.

## Saída

Usar formato compacto:

1. **Contexto humano** — situação antes/durante/depois.
2. **Achados** — observação concreta e risco.
3. **Hipóteses** — mecanismo possível + confiança.
4. **Evidência necessária** — como confirmar ou refutar.
5. **Recomendação** — mudança, benefício e trade-off.
6. **Limites** — o que permanece incerto ou exige especialista.

Evitar score obrigatório. Se priorização ajudar, usar severidade baseada em dano, frequência, reversibilidade e alcance.
