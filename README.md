[![PyPI - Python](https://img.shields.io/badge/python-v3.6+-blue.svg)](https://pypi.org/project/bertopic/)
[![PyPI - License](https://img.shields.io/badge/license-MIT-green.svg)](https://github.com/mediote/twAnalytics/blob/main/LICENSE)
[![Lattes](https://img.shields.io/badge/Lattes-CNPq-blueviolet)](http://lattes.cnpq.br/2455024624300452)


## Colab 

| Nome  | Link  |
|---|---|
| KNN  | [![Abrir no Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mediote/knn/blob/main/knn.ipynb)  |


# Implementação própria do algoritmo KNN (k-Nearest Neighbors) 

## 1 - Objetivos da análise


<ul>
    <li>Fazer uma implementação própria do algoritmo KNN para classificação</li>
    <li>Avaliar o uso do algoritmo KNN com diferentes valores de k, através do
método holdout</li>
    <li>Implementar uma função para fazer a divisão dos dados em treino e teste, de
acordo com o método holdout. </li>
    <li>Implementar normalização de dados e verificar o seu efeito sobre os
resultados da classificação</li>
</ul> 

Mais informação no <a href="">arquivo</a> .

## 2 - Entendimento dos dados

Os dados se referem à classificação de tumores de mama em maligno (1) ou benigno (0), de acordo com a coluna target. Os atributos (29 ao total) descrevem características dos núcleos celulares presentes em uma imagem digitalizada do material coletado na biópsia pelo método fine needle aspirate (FNA). Estes dados foram obtidos do  <a href="https://biodatamining.biomedcentral.com/articles/10.1186/s13040-017-0154-4
">repositório</a> PLMB.

## 3 - Instruções para execução

Para executar o arquivo localmente com Jupyter Notebook, ou ambinte de sua preferência, basta clonar o <a href="https://github.com/mediote/knn.git">repositório</a> e comentar as linhas na  <a href="https://colab.research.google.com/drive/1CLJ45koDzznmEnDcf_TAkKHCRajc3LRH#scrollTo=c05dfc81&line=4&uniqifier=1">célula</a> 11. A base de dados encontra-se no mesmo diretório do projeto.

Para executar pelo <a href="https://colab.research.google.com/drive/1CLJ45koDzznmEnDcf_TAkKHCRajc3LRH#scrollTo=51d0805d">Colab</a>, basta descomentar as linhas na  <a href="https://colab.research.google.com/drive/1CLJ45koDzznmEnDcf_TAkKHCRajc3LRH#scrollTo=c05dfc81&line=4&uniqifier=1">célula</a> 11, acessar o menu "Ambiente de execução", opção "Executar tudo".

## 4 -  Resumo

Nesta análise, foi feita uma implementação própria do algoritimo KNN para classificar dados de tumores de mama em maligno (1) ou benigno (0), de acordo com a coluna target. Os dados foram balanceados, e, divididos em amostras de treino e teste na proporção 80/20, observando o método holdout. Inicialmente, os dados não normalizados, foram classificados com os valores de k=1, 2, 5, 7, apresentando resultados de acurácia e tempo de execução conforme a tablea abaixo:

<table>
  <tr>
    <th style="text-align: left">Acurácia</th>
    <th style="text-align: left">Tempo Execução</th> 
  </tr>
  <tr>
    <td>K = 1 : 0.9058823529411765</td>
    <td style="text-align: left">3.617668390274048</td>
  </tr>
  <tr>
    <td>K = 3 : 0.9294117647058824</td>
    <td style="text-align: left">3.6672239303588867</td>
  </tr>
  <tr>
    <td>K = 5 : 0.9411764705882353</td>
    <td style="text-align: left">3.690131902694702</td>
  </tr>
   <tr>
    <td>K = 7 : 0.9411764705882353</td>
    <td style="text-align: left">3.7978484630584717</td>
  </tr>
</table>

Em um segundo momento, os dados de treino e teste foram normalizados e o processo de classificação foi repetido observando os mesmos crtérios nos valores de k descritos acima.

<table>
  <tr>
    <th style="text-align: left">Acurácia</th>
    <th style="text-align: left">Tempo Execução</th> 
  </tr>
  <tr>
    <td>K = 1 : 0.9647058823529412</td>
    <td style="text-align: left">3.7629382610321045</td>
  </tr>
  <tr>
    <td>K = 3 : 0.9529411764705882</td>
    <td style="text-align: left">3.6761677265167236</td>
  </tr>
  <tr>
    <td>K = 5 : 0.9529411764705882</td>
    <td style="text-align: left">3.930488109588623</td>
  </tr>
   <tr>
    <td>K = 7 : 0.9411764705882353</td>
    <td style="text-align: left">3.802830696105957</td>
  </tr>
</table>

Conclui-se que, o tempo de execução total do algorítimo varia pouco com a mudança dos valores de k, e que, após a normalização dos dados, a acurácia do obtida melhorou razoavelmente.




