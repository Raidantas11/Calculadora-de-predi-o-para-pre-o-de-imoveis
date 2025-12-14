Calculadora de Preço de Imóvel

Este projeto consiste em uma calculadora que utiliza um modelo preditivo de Machine Learning para auxiliar na tomada de decisão de compra de um imóvel, estimando o seu preço com base em variáveis previamente treinadas.

Foram utilizadas 7 variáveis de entrada (X) que apresentaram alta correlação com o valor do imóvel (Y – Preço_Casa), sendo elas:

Área construída (m²)

Quantidade de quartos

Quantidade de banheiros

Ano de construção

Tamanho do lote

Vagas de garagem

Qualidade da vizinhança (classificada de 1 a 10)

Importante: A variável Área refere-se à área construída do imóvel, enquanto Tamanho do lote refere-se à área total do terreno

Modelos: foram usados dois modelos de regressão, sendo eles Random Forest e Linear Regression. Após avaliação, o Linear Regression mostrou um maior valor de R² e um Erro Médio Absoluto (MAE) menor, sendo então escolhido para aplicação. Nestes modelos, foi utilizada a base de dados original.

Na análise de dados, iniciamente foi feita uma matriz de correlação, permitindo entender como as variaveis se relacionam com a variavel Y(Preço_Casa). Isso já bastava para definir quais variaveis usar para treinar o modelo, porém não explicava como as variaveis impactavam no modelo, e foi então que criei um modelo de análise, para poder auxiliar quem for fazer a consulta. Este modelo foi normalizado, possibilitando interpretar o impacto relativo de cada variavel no preço do imóvel. Nesse modelo de análise, os coeficientes representam o impacto no preço do imóvel a cada 1 desvio padrão de variação em cada variável, mantendo as demais constantes.

Link do Colab: https://colab.research.google.com/drive/1MtQnNqKn0TctYv9KTvUdQ3aaMdjVpwW3?usp=sharing

Interface construída com: HTML e CSS Backend com: Flask(python) Modelo: Machine Learning carregado via joblib

Pré-requisitos Python 3.10 pip

Para:

Abra o terminal no VS Code. Ative o ambiente virtual venv: .venv\Scripts\activate

Instale as dependências com:

pip install -r req.txt ou pip install flask joblib numpy scikit-learn no VS Code.

Execute o Flask: python app.py, depois acesse a página que o terminal devolve.
