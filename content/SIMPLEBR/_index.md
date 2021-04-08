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
O SIMPLE-BR é uma variação do modelo original SIMPLE (Baldos & Hertel, 2013; Hertel & Baldos 2016). O SIMPLE é um modelo de equilíbrio parcial do comércio e produção agrícola global e foi validado para estudos de sustentabilidade e segurança alimentar (Hertel & Baldos 2016; Baldos & Hertel, 2014). Na atual versão, amplia-se o detalhamento do modelo tornando o Brasil uma região explícita e não mais como parte da região América do Sul.

O desenvolvimento do SIMPLE-BR é norteado para manter o foco nos principais *drivers* da agricultura mundial: crescimento populacional, crescimento da renda per capita, e produtividade total dos fatores de produção, enquanto introduz um maior detalhamento empírico ao desagregar a demanda e oferta dos produtos agrícolas. Cada região $r$ do modelo produz uma única *commodity* agregada denominada ***crop*** (ver o Box 1 para mais informações). De modo similar, a demanda dos produtos agrícolas (***crop***) é derivada do consumo em cada região que é governado pelo nível de renda per capita e nível populacional. Essas diferenciações regionais permitem capturar diferentes impactos do crescimento da renda regional sobre a demanda em diferentes regiões do mundo, bem como produtividade agrícola e mudança na oferta de terra. O SIMPLE-BR desagrega a economia mundial em 17 (dezessete) regiões, abrangendo 177 países.

![png](/img/SIMPLE17.png)
**Figura 1**. Mapa da agregação regional do modelo SIMPLE-BR. **AUS_NZ**: Austrália e Nova ZeLandia; **BRA**: Brasil; **C_Asia**: Ásia Central; **CAN**: Canadá, **CC_Amer**: América Central e Caribe; **CHINA**: China e Mongólia; **E_Euro**: Leste Europeu; **EU**: União Européia com Reino Unido; **JPN_KR**: Japão e Coréia; **M_East**: Oriente Médio; **N_Afr**: Norte da África; **S_Afr**: Sul da África; **S_Amer**: América do Sul; **S_Asia**: Sul da Ásia; **SE_Asia**: Sudeste Asiático; **SSA**: África Subsariana; **US**: Estados Unidos.

Em cada região, os consumidores demandam quatro commodities, incluindo produtos não-alimentares ($NFOOD$) e produtos alimentares. Há diferenciação entre o consumo direto dos produtos agrícolas ($CROPS$) e consumo indireto através da demanda de produtos da pecuária ($LVSTK$) e indústria de alimentos ($PFOOD$). As duas últimas categorias são importantes uma vez que um aumento da eficiência desses setores – que utilizam produção agrícola em sua produção – podem ter um significante impacto na demanda global por novas áreas de lavoura. O consumo total ($Q$) é igual ao produto da população ($POP$) e do consumo per capita ($Q_{PC}$). Os drivers do consumo per capita são os preços ($P$) e a renda per capita ($Y_{PC}$). Mudanças nesses drivers são ponderadas pela elasticidade preço ($\xi_P$) e elasticidade renda ($\xi_Y$) da demanda.

A demanda por alimentos ($PFOOD$) é sensível a preço e renda das famílias, entretanto se torna menos sensível à medida que a renda per capita aumenta (Muhammad et al., 2011). Uma maior renda também faz com que as famílias diversifiquem suas dietas, assim em estágios iniciais de desenvolvimento econômico há uma menor parcela relativa de alimentos oriundos da pecuária e alimentos processados – a demanda por esses produtos pode ser alterada por progresso tecnológico nesses setores (por exemplo, alimentação animal mais eficiente ou melhoramento genético). Essa dinâmica é introduzida no modelo ao permitir que as elasticidades preço e renda da demanda para cada commodity oscile com mudanças na renda através de estimativas de uma regressão linear entre renda e as respectivas elasticidades.

![png](/img/simple-struct-1.png)
**Figura 2**. Estrutura do modelo SIMPLE-BR.

A produção agrícola – ***crop*** – no modelo SIMPLE-BR tem quatro usos potenciais: consumo direto ($Q_{CROP}$), consumo como ração no setor de pecuária ($X_{LVSTK}^{CRP}$), processamento de alimentos ($X_{PFOOD}^{CRP}$) e biomassa para fabricação de biocombustível ($X_{BIOF}^{CRP}$) - exógeno ao modelo (**Figura 2**). A produção no modelo utiliza funções do tipo “Constant Elasticity of Substitution” (CES). Outros insumos exceto ***crop*** ($NCROP$) são utilizados para a produção nos setores de pecuária e de alimentos processados ($X_{LVSTK}^{NCRP}$, $X_{PFOOD}^{NCRP}$). Os parâmetros $\sigma_{LVSTK}$ e $\sigma_{PFOOD}$ governam a substituição entre ***crop*** e outros insumos exceto ***crop*** nesses setores. No caso específico da produção da pecuária é esperado que uma redução no preço do insumo ***crop*** pode resultar em uma intensificação no uso de ração por unidade de produção da pecuária.

![png](/img/simple-struct-2.png)
**Figura 3**. Diagrama do modelo SIMPLE-BR: o painel inferior (verde) refere-se a produção regional da *commodity* agregada ***crop***. O painel superior (vermelho) refere-se a demanda regional da mesma *commodity*. O destino da produção agrícola compreende consumo direto, uso para ração de animais e processamento, bem como biocombustíveis. Sob a hipótese de mercados segmentados, consumidores e produtores se relacionam tanto no mercado doméstico como no mercado internacional. Já na hipótese de mercados integrados existe apenas um mercado global e um único preço para todas as regiões.

Nessa representação do modelo SIMPLE-BR, a oferta global da produção ***crop*** se iguala à demanda global, sendo o preço a variável que equilibra o mercado ($P_{CROP}$). Portanto, o equilíbrio de longo prazo no modelo SIMPLE-BR é atingido quando a oferta global de ***crop*** se igual com a demanda global de ***crop*** onde existe apenas um preço de equilíbrio. Vale lembrar que o modelo SIMPLE-BR é um modelo de equilíbrio parcial estático. Portanto, as projeções são determinadas apenas a partir de um ponto no tempo, em que um determinado choque é aplicado, para outro, em que os ajustes sobre as forças de oferta e de demanda se processam e ocorre um equilíbrio de preços (por exemplo, o período de 2017 à 2030). O modelo não tem como objetivo predizer um caminho ou trajetória de expansão no comportamento dos insumos e dos fatores de produção e preço.  .

A oferta global da produção de ***crop*** ($X_{CROP}$) é determinada pela soma da oferta individual de cada região no modelo, sendo que cada região possui distintas dotações de terra e produtividade. Cada região produz uma commodity agrícola denominada ***crop*** utilizando para isso terra ($LAND$) e demais insumos de produção exceto terra ($NONLAND$). O parâmetro $\sigma_{CROP}$ determina as possibilidades de substituição entre esses insumos. Quanto maior essa elasticidade, maior será a margem intensiva de resposta da oferta de ***crop***. A substituição dos demais insumos (por exemplo, fertilizantes, maquinário e trabalho) por terra na produção de ***crop*** possibilita a intensificação endógena da produção, permitindo crescimento da produtividade agrícola mesmo na ausência de mudança tecnológica e de escassez de recursos. Adicionalmente, o modelo permite o crescimento exógeno da produtividade agrícola, na qual é determinada por investimentos em pesquisa e desenvolvimento agrícola, políticas agro-ambientais e mudanças no clima. A oferta de terra para as culturas é sensível ao preço, ou seja, uma desvalorização (valorização) da renda da terra implica em um efeito expansão (retração) na oferta de terra – margem extensiva ($\sigma_{LAND}$ e $\sigma_{NLAND}$). A área de culturas varia de acordo com os diferentes usos da terra, com a resposta em área variando entre as regiões geográficas  .

Assume-se, na implementação inicial do modelo SIMPLE-BR, duas hipótese quanto aos mercados: mercados totalmente integrados e mercados segmentados (**Figura 3**). Sob a primeira hipótese (mercados integrados) existe apenas um mercado global para a demanda e oferta de “crop” e, portanto, um preço de equilíbrio entre todas as regiões do modelo. A segunda hipótese (mercados segmentados) é amplamente utilizada em modelos globais de comércio (Hertel, 1997). A especificação de mercados segmentados segue a proposta por Armington (1969) em que produtos domésticos e importados são tratados como bens diferenciados embora substitutos potenciais. Essa especificação possui uma vasta aplicação empírica no comércio agrícola (Villoria & Hertel, 2011). Quanto maior a diferenciação entre os mercados doméstico e internacional, mais segmentado são os mercados para as culturas agrícolas.

# Base de dados

# Validação Histórica


#
