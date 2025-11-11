Análise de Dados do Airbnb - Rio de Janeiro (2025)
Este repositório contém uma análise exploratória de dados (EDA) do mercado de Airbnb na cidade do Rio de Janeiro, utilizando dados de 2025. O projeto foi desenvolvido em Python, com foco nas bibliotecas Pandas, Matplotlib e Seaborn.

O notebook (Data_Analyisis_AirBnb_Rio_de_Janeiro.ipynb) investiga os fatores que influenciam os preços, a disponibilidade e a composição do mercado, culminando na resolução de um "paradoxo" sobre os preços da Zona Sul vs. Zona Oeste.

🚀 Tecnologias Utilizadas
Python 3.13

Pandas: Para manipulação, limpeza e agrupamento dos dados.

Matplotlib & Seaborn: Para a criação de todas as visualizações de dados.

NumPy: Para suporte a cálculos numéricos.

Jupyter Notebook: Como ambiente de análise.

📈 A Análise: O Paradoxo "Zona Sul vs. Zona Oeste"
A intuição sugere que a Zona Sul, lar dos bairros mais famosos, seria a mais cara. No entanto, os dados revelaram uma história muito mais complexa.

O Paradoxo
Após uma limpeza inicial para remover outliers extremos (preços > R$ 2000), o gráfico de preço médio mostrou um resultado surpreendente:

Zona Oeste: Preço Médio de R$ 534,12

Zona Sul: Preço Médio de R$ 398,00

Isso levantou a questão central da análise: por que a Zona Oeste parece ser significativamente mais cara?

A Investigação (As Pistas)
A investigação foi focada em dois pontos: Volume e Composição.

Volume (Contagem de Anúncios): A Zona Sul é um mercado massivo e diverso, com 19.249 anúncios,  2x mais que a Zona Oeste (9.431).

Composição (Tipos de Imóvel):

A Zona Sul possui milhares de anúncios de Private room (Quarto Privado) e Shared room (Quarto Compartilhado), que são opções muito mais baratas.

A Zona Oeste é um mercado mais homogêneo, focado quase exclusivamente em Entire home/apt (Apartamento Inteiro), que é a categoria mais cara.

A média da Zona Sul estava sendo "puxada para baixo" por sua enorme diversidade de anúncios baratos.

O Veredito (A Solução)
Para uma comparação justa ("maçãs com maçãs"), foi criado um gráfico final usando a Mediana (resistente a outliers) e filtrando apenas por Entire home/apt.

O resultado confirmou a suspeita:

Zona Oeste: Preço Mediano (Apartamentos) de R$ 550,00

Zona Sul: Preço Mediano (Apartamentos) de R$ 336,00

Conclusão Final: A intuição inicial estava incorreta. A Zona Oeste tem, de fato, um preço mediano mais alto para apartamentos inteiros, pois seu tipo de imóvel predominante é de categoria superior, enquanto o mercado da Zona Sul é muito mais diversificado.

📊 Outras Descobertas da Análise
Distribuição de Preços: O mercado é extremamente assimétrico, com a vasta maioria dos anúncios (12.700+) na faixa de preço mais baixa.

Disponibilidade: O mercado é polarizado em "U". Os anúncios se concentram em 0 dias (uso pessoal) ou 365 dias (negócio profissional).

Correlação: Não há correlação linear forte entre preço e popularidade (nº de reviews). Os imóveis mais caros têm poucas avaliações.

Geografia: Os mapas de latitude/longitude confirmam visualmente a densidade da Zona Sul e sua dominância por "Apartamentos Inteiros".

🚀 Como Executar este Projeto
Clone este repositório:

Bash

git clone https://github.com/Viniciustoc/Analise-Airbnb-Rio-de-Janeiro.git
Navegue até a pasta do projeto:

Bash

cd Analise-Airbnb-Rio-de-Janeiro
Abra o arquivo Data_Analyisis_AirBnb_Rio_de_Janeiro.ipynb em um ambiente Jupyter (como Jupyter Notebook, Jupyter Lab ou VS Code).

Certifique-se de ter as bibliotecas necessárias instaladas:

Bash

pip install pandas matplotlib seaborn
Execute as células do notebook. O arquivo listings_summary.csv (os dados) já está incluído.


### Limitações e Pontos de Atenção

É importante notar que, como toda análise baseada em um dataset público, esta tem suas limitações:

* **Viés de Coleta (Sampling Bias):** O dataset é um "scrape" de um dia específico (30/10/2025) e pode não representar 100% de todos os anúncios ativos, podendo ter capturado mais anúncios em certas áreas do que em outras.*** * 
* **Sazonalidade:** Os preços refletem uma "foto" do final de outubro, o que pode influenciar os valores (preparação para alta temporada, pós-feriado, etc.).* * 
* **Escopo da Plataforma:** A análise se limita aos dados do Airbnb. Imóveis de super-luxo, que são alugados em plataformas de nicho, podem não estar presentes nesta amostra.

---


👨‍💻 Sobre o Autor
Vinicius Stoc

GitHub: github.com/Viniciustoc

LinkedIn: https://www.linkedin.com/in/vinicius-stoc-100959267/