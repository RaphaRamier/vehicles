# Introdução
## Precificação de Veículos 🚗

---

O projeto visa analisar uma lista de veículos publicados em um site de propagandas gratuitas de veículos. 

Os dados serão analisados de forma a determinar, com base nas informações apresentadas, os fatores que influenciam no preço de um veículo.

---

### Descrição de dados:


- `price` — preço do veículo
- `model_year` — ano do modelo
- `model` — o modelo
- `condition` — as condições
- `cylinders` — quantidade de cilindros
- `fuel` — gasolina, diesel etc.
- `odometer` — a quilometragem do veículo quando a propaganda foi publicada 
- `transmission` — o tipo de transmissão
- `paint_color` — a cor
- `is_4wd` — Se o veículo é 4 por 4 (tipo Booleano)
- `date_posted` — a data que a propaganda foi publicada
- `days_listed` — dias desde a publicação até a retirada



---


O projeto tem por finalidade descobrir quais fatores influenciam na formação do preço do veículo.

Caracteristicas como: 

- ano do modelo
- modelo
- condições
- quilometragem do veículo
- cor

Serão analisadas.

---


## Pré-processamento os dados:

* Identificar e preencher os valores ausentes.
* Excluir dados duplicados.
* Categorizar os dados.

### Explicar:

* quais valores ausentes você foram identificados;
* possíveis razões que esses valores ausentes estavam presentes;
* qual método foi usado para preencher os valores ausentes;
* qual método foi usado para localizar e excluir dados duplicados;
* possíveis razões para a presença de dados duplicados;
* qual método foi usado para alterar o tipo de dados;
* quais dicionários biblotecas foram selecionadas para este conjunto de dados.

Os dados podem conter valores que não correspondem à realidade – por exemplo, um número negativo de quilometragem ou de idade do veículo.

## Perguntas sobre os dados:

* Existe alguma correlação entre os dados?
* Existe um tipo de carro mais anunciado ou vendido que o outro (SUV e Sedan)?


# Metodologia

Esse projeto procura avaliar e descobrir os fatores de formação de preço dos veículos listados na base de dados fornecida. Para esse fim, serão abordadas duas estratégias:

- Análise exploratória;

- Realização de análise estatística, utilizando técnicas de análise descritiva e visualização gráfica, como, por exemplo:
> - Gráficos de Dispersão
> - Boxplots
> - Histogramas

# Conclusão


No decorrer da análise, houveram a ocorrência alguns valores eivados de erros, que foram solucionados no decorrer da análise conforme saltavam às vistas, como por exemplo, duplicatas implícitas, valores ausentes, valores atípicos e etc. O dados com valores ausentes que mais predominaram foram os da coluna “is_4wd”, que possuíam um pouco mais de 50% de sua totalidade como ausente, devido ao fato de ser uma coluna de boelanos que só numera o valor “True” como 1, o False não foi atribuído nenhum valor, logo, essa coluna foi corrigida por lógica. 

Elementos chaves foram criados no DataFrame para auxiliar na obtenção de êxito da análise proposta, como a coluna de ano e idade do veículo. Foi necessário também a criação de intervalos interquartis (IQR) para a identificação e tratamento dos valores atípicos, presentes no DataFrame.

Após a criação desses elementos que ajudaram na consecução da análise, o DataFrame original foi filtrado criando outro com os dados limpos. Uma vez emendado, o DataFrame, verificou-se através de análise gráfica dos dados, de caixa, histogramas e de barras, que os tipos de veículos com mais anúncios eram os SUVs e sedans, com uma contagem de 12405 e 12154 de anúncios, respectivamente, no DataFrame Original.

Verificou-se também que a média de dias que um veículo fica em anúncio é de 40 dias. Tendo seus valores atípicos acima de 104 dias, e seu atípico máximo em 271 dias.
Os veículos com os preços médias mais altos foram, respectivamente, ônibus, caminhão, e pick-ups. No gráfico de caixa que foi plotado ficou bem clara essa informação. 
Também fora observado a correlação das cores com o preço, bem, os carros mais caros da base de dados foram os veículos das cores laranja e amarelo, o que pode destoar da realidade já que havia muitos dados ausentes nessa coluna. 

A condição de novo são os carros com os maiores valores dentro dessa coluna o que já era esperado. 
Por último a matriz de correlação trouxe à tona as principais variáveis que afetam o preço dos veículos. Diante de todo o exposto dessa análise dos dados fornecidos pela concessionária, conclui-se que os fatores que mais impactam no preço do veículo são:
    - O ano do modelo, com uma correlação positiva de 0,71;
    - A quilometragem com uma correlação negativa de 0,62;
    - E a idade do veículo como uma correlação negativa de 0,7.

A utilização de gráficos como boxplot, heatmap, histogramas, barras e a matriz de correlação, corroborou para a identificar tais fatores que atuam na formação de preço dos veículos.
