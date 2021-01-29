---
title: Brazilian Economic Analysis
date: "2021-01-28"
draft: false
share: false
commentable: false
editable: false

# Optional header image (relative to `static/media/` folder).
header:
  caption: ""
  image: ""
---

O modelo BREA (Brazilian Economic Analysis) é caracterizado em seu núcleo central
como um modelo estático multi-regional de equilíbrio geral computável (LIMA, 2017).
O modelo representa o Brasil em 6 (seis) regiões: Sul, Sudeste, Centro-Oeste, Nordeste, MATOPIBA e Norte.
A Figura 1, a seguir, mostra que a agregação regional é uma combinação das principais
agregações geopolíticas do Brasil com diferenciação para regiões de fronteira agrícola –
como é o caso da representação da região MATOPIBA e a explícita separação do estado do
Mato Grosso em biomas (Cerrado e Amazônia) agregados, respectivamente,
às regiões Centro-Oeste e Norte.

![](./static/media/breareg.png)
**Figura 1.** Biomas brasileiros (esquerda) e agregação regional do modelo (direita).

O modelo segue o fluxo circular da renda de uma economia. A estrutura da demanda final é composta pelos gastos público (governo) e privado (famílias), ambos para consumo e investimento entre os bens e serviços do modelo. O comportamento dos agentes no modelo segue a maximização da sua função de utilidade. Pelo lado das famílias, elas demandam bens e serviços dado sua restrição orçamentária. As preferências são hipoteticamente contínuas e convexas, portanto, as demandas derivadas são homogêneas de grau zero com relação aos preços, ou seja, somente os preços relativos podem ser determinados.

As firmas demandam fatores de produção (por exemplo, capital e trabalho) para a produção de bens e serviços. As famílias recebem a renda dos fatores de produção e transformam em demanda de bens e serviços produzidos pelas firmas. A igualdade entre oferta e demanda determina os preços de equilíbrio dos fatores de produção, bens e serviços. O modelo BREA em sua versão estática é resolvido para a projeção de diferentes cenários definidos pelo usuário para responder questões específicas, onde os fatores de produção são considerados exógenos.
No lado da produção, a tecnologia é baseada nos retornos constantes à escala combinando bens intermediários e fatores de produção. No equilíbrio do modelo o lucro econômico das firmas é zero. Cada firma (setor) pode ter uma específica tecnologia de produção e demanda de insumos e fatores de produção para minimizar seus custos de produção.
O modelo BREA utiliza uma nomenclatura similar a outros tradicionais modelos derivados do GTAPinGAMS como os modelos PAEG, GTAP, e o próprio GTAPinGAMS. O núcleo central do modelo é escrito em linguagem de programação MPSGE (mathematical programming system for general equilibrium analysis), com design e solução como um sistema de complementariedade mista em linguagem de programação GAMS (General Algebraic Modeling System) (RUTHERFORD, 2005; RUTHERFORD; PALTSEV, 2000).

A Figura 2, a seguir, apresenta um esboço da estrutura econômica do modelo. Os símbolos correspondem a variáveis no modelo econômico. Yir representa a produção do bem ou serviço i na região r, já Cr, Ir, e Gr representam, respectivamente, o consumo privado, investimento e demanda pública de bens e serviços. XRir  e MRir representam o comércio inter-regional do bem i na região r. Já Mir representa a importação do bem i da região r com origem no resto do mundo (ROW). Já as exportações do bem i para o resto do mundo são representadas pelo fluxo vxmdirrow. RA e GOVT são os agentes representativos – famílias e governo – respectivamente. E, FTr¬, é o mercado onde os fatores de produção do tipo sluggish são alocados aos seus respectivos setores. O fluxo dos bens e serviços aparecem como as linhas sólidas e as linhas pontilhadas representam os fluxos de impostos e tributos.
