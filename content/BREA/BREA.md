---
title: Brazilian Economic Analysis
subtitle: Learn how to blog in Academic using Jupyter notebooks
summary: Learn how to blog in Academic using Jupyter notebooks
authors:
- admin
tags: []
categories: []
date: "2019-02-05T00:00:00Z"
lastMod: "2019-09-05T00:00:00Z"
featured: false
draft: false
date: "2021-01-28"
diagram: true
# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  caption: ""
  focal_point: ""
---
O modelo BREA (Brazilian Economic Analysis) é caracterizado em seu núcleo central
como um modelo estático multi-regional de equilíbrio geral computável (LIMA, 2017).
O modelo representa o Brasil em 6 (seis) regiões: Sul, Sudeste, Centro-Oeste, Nordeste, MATOPIBA e Norte.
A Figura 1, a seguir, mostra que a agregação regional é uma combinação das principais
agregações geopolíticas do Brasil com diferenciação para regiões de fronteira agrícola –
como é o caso da representação da região MATOPIBA e a explícita separação do estado do
Mato Grosso em biomas (Cerrado e Amazônia) agregados, respectivamente,
às regiões Centro-Oeste e Norte.

```
graph TD
A[Produção] -->|CES|
A --> B[Capital-Trabalho]
A --> C[Recurso-intensivo]
C --> D[Terra]
C --> E[Energia-materiais]
E --> F[Energia agregada]
E --> G[Insumos-intermediários]
F --> H[Eletricidade]
F --> I[Outras fontes de energia]
```

![png](/img/breareg.png)
**Figura 1.** Biomas brasileiros (esquerda) e agregação regional do modelo (direita).

O modelo segue o fluxo circular da renda de uma economia. A estrutura da demanda final é composta pelos gastos público (governo) e privado (famílias), ambos para consumo e investimento entre os bens e serviços do modelo. O comportamento dos agentes no modelo segue a maximização da sua função de utilidade. Pelo lado das famílias, elas demandam bens e serviços dado sua restrição orçamentária. As preferências são hipoteticamente contínuas e convexas, portanto, as demandas derivadas são homogêneas de grau zero com relação aos preços, ou seja, somente os preços relativos podem ser determinados.

As firmas demandam fatores de produção (por exemplo, capital e trabalho) para a produção de bens e serviços. As famílias recebem a renda dos fatores de produção e transformam em demanda de bens e serviços produzidos pelas firmas. A igualdade entre oferta e demanda determina os preços de equilíbrio dos fatores de produção, bens e serviços. O modelo BREA em sua versão estática é resolvido para a projeção de diferentes cenários definidos pelo usuário para responder questões específicas, onde os fatores de produção são considerados exógenos.
No lado da produção, a tecnologia é baseada nos retornos constantes à escala combinando bens intermediários e fatores de produção. No equilíbrio do modelo o lucro econômico das firmas é zero. Cada firma (setor) pode ter uma específica tecnologia de produção e demanda de insumos e fatores de produção para minimizar seus custos de produção.
O modelo BREA utiliza uma nomenclatura similar a outros tradicionais modelos derivados do GTAPinGAMS como os modelos PAEG, GTAP, e o próprio GTAPinGAMS. O núcleo central do modelo é escrito em linguagem de programação MPSGE (mathematical programming system for general equilibrium analysis), com design e solução como um sistema de complementariedade mista em linguagem de programação GAMS (General Algebraic Modeling System) (RUTHERFORD, 2005; RUTHERFORD; PALTSEV, 2000).

A Figura 2, a seguir, apresenta um esboço da estrutura econômica do modelo. Os símbolos correspondem a variáveis no modelo econômico. $Y_{ir}$ representa a produção do bem ou serviço $i$ na região $r$, já $C_r$, $I_r$, e $G_r$ representam, respectivamente, o consumo privado, investimento e demanda pública de bens e serviços. $XR_{ir}$  e $MR_{ir}$ representam o comércio inter-regional do bem $i$ na região $r$. Já $M_{ir}$ representa a importação do bem $i$ da região $r$ com origem no resto do mundo ($ROW$). Já as exportações do bem $i$ para o resto do mundo são representadas pelo fluxo $vxmd_{irrow}$. $RA$ e $GOVT$ são os agentes representativos – famílias e governo – respectivamente. E, $FT_r$, é o mercado onde os fatores de produção do tipo sluggish são alocados aos seus respectivos setores. O fluxo dos bens e serviços aparecem como as linhas sólidas e as linhas pontilhadas representam os fluxos de impostos e tributos.

![png](/img/breastruct.png)
**Figura 2.** Estrutura da economia regional do modelo.

A produção doméstica $vom_{ir}$ é distribuída em demanda intermediária ($vdfm_{ijr}$) e para o vetor de demanda final, tal como consumo das famílias ($vdpm_{ir}$), investimento ($vdim_{ir}$), demanda do governo e exportações ($vxmd_{irrow}$). A identidade contábil na base de dados é:

$$vom_{ir} = \sum_i vdfm_{ijr} + vdpm_{ir} + vdim_{ir} + vdgm_{ir} + \sum_s vxmdr_{irs} + vxmd_{irrow}$$

Os insumos de produção incluem insumos intermediários (doméstico e importado), fatores móveis de produção ($f ∈ m$) e fatores setor-específico ($f ∈ s$). A remuneração dos fatores é destinada às famílias e o equilíbrio no mercado de fatores é dado pela identidade que relaciona valor dos pagamentos com a renda total:

$$\sum_i vfm_{fir} = evom_{fr}$$

O mercado internacional é governado pelos bens e serviços importados e exportados. Bens importados tem um agregado $vim_{ir}$ composto pela demanda intermediária ($vifm_{ijr}$), consumo privado ($vipm_{ir}$), e investimento ($viim_{ir}$). A identidade contábil na base de dados é:

$$vim_{ir} = \sum_j vifm_{ijr} + vipm_{ir} + viim_{ir}$$

$$vimr_{ir} = \sum_j vifmr_{ijr} + vipmr_{ir} + viimr_{ir}$$

```
**BOX 1.** Agregação dos impostos e tarifas para definição das condições de lucro zero.
$$R_{ir}^Y = rto_{ir} + \sum_f rtf_{fir} + \sum_j (rtfi_{jir} + rtfd_{jir}) \\\\
R_{ir}^M = rtms_{irrow}\\\\
R_{ir}^C = rtpd_{ir} + rtpi_{ir}\\\\\
R_{ir}^I = rtid_{ir} + rtii_{ir}$$
```


$$Y_{ir} &:& \sum_f vfm_{fir} + \sum_j(vifm_{jir} + vdfm_{jir} + vifmr_{jir}) + R_{ir}^Y = vom_{ir}\\\\
M_{ir} &:& vxmd_{irowr} + R_{ir}^M = vim_{ir}\\\\
Mr_{ir} &:& \sum_j vifmr_{ijr} + vipmr_{ir} + viimr_{ir} = vimr_{ir}\\\\
C_r &:& \sum_i (vdpm_{ir} + vipm_{ir} + vipmr_{ir} + R_{ir}^C) = vpm_r\\\\
G_r &:& \sum_i vdgm_{ir} = vgm_r\\\\
I_r &:& \sum_i (vdim_{ir} + viim_{ir} + viimr_{ir} + R_{ir}^I) = vimi_r\\\\
FT_{fr} &:& evom_{fr} = \sum_j vfm_{fjr}$$

# Representação Tecnológica
