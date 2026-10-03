# Taxas Relacionadas — Notebook Interativo (Monitoria de Cálculo 1)

Notebook desenvolvido para a monitoria voluntária de Cálculo 1 (UFLA), usado em uma aula de revisão sobre **Taxas Relacionadas**. Em vez de slides estáticos, o material usa Jupyter + `ipywidgets` para gráficos e animações com parâmetros ajustáveis em tempo real, e inclui **quatro problemas** (dois resolvidos no quadro e dois para os alunos) com figuras, dicas, resoluções e conferência numérica em Python.

O fio condutor é a **Segunda Lei de Kepler** — o raio que liga um planeta ao Sol varre áreas iguais em tempos iguais — observada por Kepler (1609) e demonstrada por Newton no *Principia* (1687). Ela serve de motivação histórica para introduzir taxas relacionadas e volta no Problema 3.


(https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rezendevinicius/Taxas_Relacionadas_Calculo1/blob/main/aulao_taxas_relacionadas_final.ipynb)

## Conteúdo

**Parte 1 — Motivação histórica**
- Resolução numérica da equação de Kepler (M = E − e·sen E) via Newton-Raphson, posicionando o planeta corretamente ao longo da órbita — respeitando velocidades reais (mais rápido no periélio, mais lento no afélio).
- **Demonstração 1**: figura interativa comparando a área varrida pelo raio vetor perto do periélio vs. do afélio, com sliders de excentricidade e Δt.
- **Demonstração 2**: animação de uma órbita completa, gerada sob demanda (não recalcula a cada movimento de slider, para não travar durante a aula).
- Dedução de dA/dt = ½·r²·(dθ/dt), a "ponte" entre a lei de Kepler e taxas relacionadas.

**Parte 2 — Ideia central e método**: receita em 5 passos e o erro mais comum (substituir antes de derivar).

**Parte 3 — Os quatro problemas** (ordem crescente de dificuldade)

| # | Problema | Formato | Figura interativa | Animação |
|---|----------|---------|-------------------|----------|
| 1 | Lente delgada | quadro | esquema óptico + rapidez da imagem em função de p | objeto se aproximando |
| 2 | Braço articulado | alunos | geometria do braço, d(θ) e d′(θ) | braço se abrindo |
| 3 | Cometa e lei das áreas | quadro | órbita real compatível com os dados, componentes da velocidade, θ̇(t) e v_θ(t) | — |
| 4 | Decaimento orbital | alunos | T(a) e extrapolação da perda de altitude | — |

- Nas figuras, a resposta fica oculta até marcar **conferir**.
- Dicas e resoluções ficam em blocos recolhíveis (`<details>`).

**Parte 4 — Conferindo tudo com Python**: todas as respostas refeitas com derivada numérica (diferença central), sem usar nenhuma regra de derivação.

## Como rodar

```bash
pip install numpy matplotlib ipywidgets jupyter
jupyter notebook aulao_taxas_relacionadas.ipynb
```

Para os sliders funcionarem, o suporte a widgets do Jupyter precisa estar habilitado (já vem por padrão em instalações recentes do Jupyter Notebook/Lab e no VS Code).

> O notebook é versionado **sem saídas** (outputs limpos): as animações em JavaScript ocupam alguns MB cada e os widgets não são exibidos pelo visualizador de notebooks do GitHub. Para ver tudo funcionando, rode localmente ou no Google Colab.

## Estrutura do notebook

| Seção | Conteúdo |
|---|---|
| Parte 1 | Contexto histórico — Kepler, Newton e a lei das áreas; motor orbital; demonstrações 1 e 2; ponte matemática |
| Parte 2 | Ideia central de taxas relacionadas e receita em 5 passos |
| Parte 3 | Problemas 1 a 4, cada um com enunciado, figura, animação (1 e 2), dicas e resolução |
| Parte 4 | Conferência numérica de todas as respostas |
| Fechamento | Resumo, armadilhas, desafios extras e referências |

## Contexto

Feito para uso em monitoria de Cálculo 1 (UFLA, 2026/2), como parte de uma série maior de materiais de apoio para a disciplina — cobrindo desde revisão de limites e derivadas até taxas relacionadas.

## Licença

Sinta-se livre para usar, adaptar e reaproveitar este material para fins educacionais.
