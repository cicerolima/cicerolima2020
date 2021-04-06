---
title: Simplified International Model of agricultural Prices, Land use, and the Environment - Brazil

# View.
#   1 = List
#   2 = Compact
#   3 = Card
view: 3

# Optional header image (relative to `static/media/` folder).
header:
  caption: ""
  image: ""
diagram: true
---
[English version [here](http://cicerolima.com/SIMPLEBR-eng/) ]

# O Modelo SIMPLE-BR
O SIMPLE-BR é uma variação do modelo original SIMPLE (Baldos & Hertel, 2013; Hertel & Baldos 2016). O SIMPLE é um modelo de equilíbrio parcial do comércio e produção agrícola global e foi validado para estudos de sustentabilidade e segurança alimentar (Hertel & Baldos 2016; Baldos & Hertel, 2014). Na atual versão, amplia-se o detalhamento do modelo SIMPLE, tornando o Brasil uma região explícita no modelo – e não mais como parte da região América do Sul.

# Abordagem teórica
O modelo SIMPLE é baseado no modelo teórico desenvolvido por Hertel (2011). O autor propôs um modelo de equilíbrio parcial para analisar os determinantes de longo prazo, tanto da oferta quanto da demanda global de uso da terra agrícola e preço das commodities agrícolas. Há no modelo três determinantes (drivers) exógenos. Primeiramente, o crescimento da demanda agregada por produtos agrícolas ($\Delta_A^D$) captura o aumento da demanda global por consumo de alimentos e por matéria-prima para uso na indústria de biocombustíveis. Em segundo lugar, um parâmetro (shifter) da oferta global de terra agrícola ($\Delta_L^S$) consistente com fatores que limitam a disponibilidade de terras agrícolas. Esses fatores incluem, por exemplo, a expansão de áreas urbanas sobre áreas agrícolas e crescimento da demanda por terra nos serviços ecossistêmicos de biodiversidade. Por fim, mudanças na produtividade agrícola ($\Delta_L^D$) influenciam a demanda por terra. Resolvendo o modelo para o equilíbrio de longo prazo (em variação percentual) e para o uso da terra global ($q_L^{\ast}$)  e preço ($p_A^{\ast}$), como função dos três determinantes exógenos nos dá as seguintes expressões:

$$q_L^{\ast} = \frac{(\Delta_A^D + \Delta_L^S + \Delta_L^D)}{(1+\frac{\eta_A^{S,I}}{\eta_A^{S,E}}+\frac{\eta_A^{D}}{\eta_A^{S,E}})} - \Delta_L^S$$

$$p_A^{\ast} = \frac{(\Delta_A^D + \Delta_L^S + \Delta_L^D)}{(\eta_A^{S,I} + \eta_A^{S,E} + \eta_A^{D})}$$

# Abordagem Empírica
O desenvolvimento do SIMPLE, e portanto do SIMPLE-BR, é norteado para manter o foco nas três margens apresentadas na seção anterior, enquanto introduz um maior detalhamento empírico ao desagregar a demanda e oferta dos produtos agrícolas (**Figura 1**). Assim como no modelo apresentado em Hertel (2011), há apenas um mercado global de equilíbrio entre oferta e demanda dos produtos agrícolas. Cada região  r do modelo produz uma única commodity agregada denominada crop (ver o Box 1 para mais informações). De modo similar, a demanda dos produtos agrícolas (crop) é derivada do consumo em cada região que é governado pelo nível de renda per capita  e nível populacional. Essas diferenciações regionais permitem capturar diferentes impactos do crescimento da renda regional sobre a demanda em diferentes regiões do mundo, bem como produtividade agrícola e mudança na oferta de terra. O SIMPLE-BR desagrega a economia mundial em 17 (dezessete) regiões, abrangendo 177 países.

Em cada região, os consumidores demandam quatro commodities, incluindo produtos não-alimentares ($NFOOD$) e produtos alimentares. Há diferenciação entre o consumo direto dos produtos agrícolas ($CROPS$) e consumo indireto através da demanda de produtos da pecuária ($LVSTK$) e indústria de alimentos ($PFOOD$). As duas últimas categorias são importantes uma vez que um aumento da eficiência desses setores – que utilizam produção agrícola em sua produção – podem ter um significante impacto na demanda global por novas áreas de lavoura. O consumo total ($Q$) é igual ao produto da população ($POP$) e do consumo per capita ($Q_{PC}$). Os drivers do consumo per capita são os preços ($P$) e a renda per capita ($Y_{PC}$). Mudanças nesses drivers são ponderadas pela elasticidade preço ($\xi_P$) e elasticidade renda ($\xi_Y$) da demanda.

A demanda por alimentos ($PFOOD$) é sensível a preço e renda das famílias, entretanto se torna menos sensível à medida que a renda per capita aumenta (Muhammad et al., 2011). Uma maior renda também faz com que as famílias diversifiquem suas dietas, assim em estágios iniciais de desenvolvimento econômico há uma menor parcela relativa de alimentos oriundos da pecuária e alimentos processados – a demanda por esses produtos pode ser alterada por progresso tecnológico nesses setores (por exemplo, alimentação animal mais eficiente ou melhoramento genético). Essa dinâmica é introduzida no modelo ao permitir que as elasticidades preço e renda da demanda para cada commodity oscile com mudanças na renda através de estimativas de uma regressão linear entre renda e as respectivas elasticidades.

A produção agrícola – “crop” – no modelo SIMPLE-BR tem quatro usos potenciais: consumo direto ($Q_{CROP}$), consumo como ração no setor de pecuária ($X_{LVSTK}^{CRP}$), processamento de alimentos ($X_{PFOOD}^{CRP}$) e biomassa para fabricação de biocombustível ($X_{BIOF}^{CRP}$) - exógeno ao modelo (**Figura 2**). A produção no modelo utiliza funções do tipo “Constant Elasticity of Substitution” (CES). Outros insumos exceto “crop” ($NCROP$) são utilizados para a produção nos setores de pecuária e de alimentos processados ($X_{LVSTK}^{NCRP}$, $X_{PFOOD}^{NCRP}$). Os parâmetros $\sigma_{LVSTK}$ e $\sigma_{PFOOD}$ governam a substituição entre “crop” e outros insumos exceto “crop” nesses setores. No caso específico da produção da pecuária é esperado que uma redução no preço do insumo “crop” pode resultar em uma intensificação no uso de ração por unidade de produção da pecuária.

Nessa representação do modelo SIMPLE-BR, a oferta global da produção “crop” se iguala à demanda global, sendo o preço a variável que equilibra o mercado ($P_{CROP}$). Portanto, o equilíbrio de longo prazo no modelo SIMPLE-BR é atingido quando a oferta global de “crop” se igual com a demanda global de “crop” onde existe apenas um preço de equilíbrio. Vale lembrar que o modelo SIMPLE-BR é um modelo de equilíbrio parcial estático. Portanto, as projeções são determinadas apenas a partir de um ponto no tempo, em que um determinado choque é aplicado, para outro, em que os ajustes sobre as forças de oferta e de demanda se processam e ocorre um equilíbrio de preços (por exemplo, o período de 2017 à 2030). O modelo não tem como objetivo predizer um caminho ou trajetória de expansão no comportamento dos insumos e dos fatores de produção e preço.  .

A oferta global da produção de “crop” ($X_{CROP}$) é determinada pela soma da oferta individual de cada região no modelo, sendo que cada região possui distintas dotações de terra e produtividade. Cada região produz uma commodity agrícola denominada “crop” utilizando para isso terra ($LAND$) e demais insumos de produção exceto terra ($NONLAND$). O parâmetro $\sigma_{CROP}$ determina as possibilidades de substituição entre esses insumos. Quanto maior essa elasticidade, maior será a margem intensiva de resposta da oferta de “crop”. A substituição dos demais insumos (por exemplo, fertilizantes, maquinário e trabalho) por terra na produção de “crop” possibilita a intensificação endógena da produção, permitindo crescimento da produtividade agrícola mesmo na ausência de mudança tecnológica e de escassez de recursos. Adicionalmente, o modelo permite o crescimento exógeno da produtividade agrícola, na qual é determinada por investimentos em pesquisa e desenvolvimento agrícola, políticas agro-ambientais e mudanças no clima. A oferta de terra para as culturas é sensível ao preço, ou seja, uma desvalorização (valorização) da renda da terra implica em um efeito expansão (retração) na oferta de terra – margem extensiva ($\sigma_{LAND}$ e $\sigma_{NLAND}$). A área de culturas varia de acordo com os diferentes usos da terra, com a resposta em área variando entre as regiões geográficas  .

Assume-se, na implementação inicial do modelo SIMPLE-BR, duas hipótese quanto aos mercados: mercados totalmente integrados e mercados segmentados (**Figura 2**). Sob a primeira hipótese (mercados integrados) existe apenas um mercado global para a demanda e oferta de “crop” e, portanto, um preço de equilíbrio entre todas as regiões do modelo. A segunda hipótese (mercados segmentados) é amplamente utilizada em modelos globais de comércio (Hertel, 1997). A especificação de mercados segmentados segue a proposta por Armington (1969) em que produtos domésticos e importados são tratados como bens diferenciados embora substitutos potenciais. Essa especificação possui uma vasta aplicação empírica no comércio agrícola (Villoria & Hertel, 2011). Quanto maior a diferenciação entre os mercados doméstico e internacional, mais segmentado são os mercados para as culturas agrícolas.

# Base de dados


# Validação Histórica


#
