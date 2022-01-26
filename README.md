[![PyPI - Python](https://img.shields.io/badge/python-v3.6+-blue.svg)](https://pypi.org/project/bertopic/)
[![PyPI - License](https://img.shields.io/badge/license-MIT-green.svg)](https://github.com/mediote/twAnalytics/blob/main/LICENSE)
[![Lattes](https://img.shields.io/badge/Lattes-CNPq-blueviolet)](http://lattes.cnpq.br/2455024624300452)

## Colab

| Nome | Link                                                                                                                                                    |
| ---- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| KNN  | [![Abrir no Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mediote/knn/blob/main/knn.ipynb) |

# Implementação própria do algoritmo KNN (k-Nearest Neighbors)

## 1 - Objetivos da análise

<ul>
    <li>Fazer uma implementação própria do algoritmo KNN para classificação</li>
    <li>Avaliar o uso do algoritmo KNN com diferentes valores de k</li>
    <li>Implementar uma função para fazer a divisão dos dados em treino e teste, de
acordo com o método holdout. </li>
    <li>Normalizar os dados e verificar o seu efeito sobre os
resultados da classificação</li>
</ul>

Mais informação no <a href="https://github.com/mediote/knn/blob/main/instrucoes.pdf">arquivo</a>.

## 2 - Entendimento dos dados

Os dados se referem à classificação de tumores de mama em maligno (1) ou benigno (0), de acordo com a coluna target. Os atributos (29 ao total) descrevem características dos núcleos celulares presentes em uma imagem digitalizada do material coletado na biópsia pelo método fine needle aspirate (FNA). Estes dados foram obtidos do <a href="https://biodatamining.biomedcentral.com/articles/10.1186/s13040-017-0154-4
">repositório</a> PLMB.

## 3 - Instruções para execução

Para executar o arquivo localmente com Jupyter Notebook, ou ambinte de sua preferência, basta clonar o <a href="https://github.com/mediote/knn.git">repositório</a> e comentar as linhas na <a href="https://colab.research.google.com/drive/1CLJ45koDzznmEnDcf_TAkKHCRajc3LRH#scrollTo=c05dfc81&line=4&uniqifier=1">célula</a> 11. A base de dados encontra-se no mesmo diretório do projeto.

Para executar pelo <a href="https://colab.research.google.com/drive/1CLJ45koDzznmEnDcf_TAkKHCRajc3LRH#scrollTo=51d0805d">Colab</a>, basta descomentar as linhas na <a href="https://colab.research.google.com/drive/1CLJ45koDzznmEnDcf_TAkKHCRajc3LRH#scrollTo=c05dfc81&line=4&uniqifier=1">célula</a> 11, acessar o menu "Ambiente de execução", opção "Executar tudo".

## 4 - Resumo

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

Em um segundo momento, os dados de treino e teste foram normalizados e o processo de classificação foi repetido observando os mesmos critérios nos valores de k descritos acima.

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



# Solr

<aside>
📌 O Apache Solr é um mecanismo de busca gratuito de código aberto, baseado na biblioteca Apache Lucene. 
Escrito em Java, o Solr está disponível desde 2004, e é um dos mecanismos de pesquisa mais populares disponíveis hoje em todo o mundo.
Também é frequentemente usado como um banco de dados NoSQL baseado em  documento, com suporte transacional que pode ser usado para fins de armazenamento.
É usado como mecanismo de busca em grandes empresas como: Apple, Netflix, Disney, AT&T, CNET, Cisco.

</aside>

## O Solr fornece recursos como:

- Suporte nativo a stemmers, consultas booleanas, consultas de frase, consultas difusas, verificação ortográfica, curingas, query re-ranking.
- Interface web responsiva integrada que permite que você execute tarefas administrativas, como gerenciamento de indices ou pesquisa de documentos.
- Replicação de índice automatizada, distribuição, balanceamento de carga e failover e recuperação automatizados. O Solr pode ser implantado em qualquer tipo de sistema, como autônomo, distribuído, nuvem.
- Suporte multilingue com detecção de idioma embutida e fornecendo ferramentas de análise de texto específicas para cada idioma.

## Instalação

- [x]  Instalar Java

```bash
java -version
sudo apt install openjdk-11-jdk
```

- [x]  Baixar o Solr

```bash
cd /opt
sudo wget https://dlcdn.apache.org/lucene/solr/8.10.0/solr-8.10.0.tgz

```

- [x]  Descompactar e Instalar

```bash
sudo tar xzf solr-8.10.0.tgz solr-8.10.0/bin/install_solr_service.sh --strip-components=2
sudo bash ./install_solr_service.sh solr-8.10.0.tgz

sudo service solr start
sudo service solr stop
sudo service solr status
```

192.168.0.30

- **solrconfig.xml**
    
    É o arquivo de configuração que controla o comportamento de alto nível do Solr.
    
- **managed-schema ou schema.xml**
    
    O esquema define um documento como uma coleção de campos.
    

## Uso

- [x]  Indexar
Os formatos que o Solr pode indexar são: json, xml, csv, pdf, doc, docx, ppt, pptx, xls, xlsx, odt, odp, ods, ott, otp, ots, rtf, htm, html, txt e log.

```bash
sudo su - solr -c "/opt/solr/bin/solr create -c fsp -n data_driven_schema_configs"
/opt/solr/bin/post -c fsp diretoriodosarquivos/*

/home/andremediote/Documentos/Workspace/mestrado/notebooks/CMP269/solr/FSP95/json/*
```

- [ ]  Consultas
Podem ser feitas diretamente pelo painel de administração, ou usando o manipulador de consulta. As consultas no Solr, são solicitações HTTP simples e a resposta padrão é um documento no formato JSON.
Qualquer plataforma capaz de HTTP pode se comunicar com o Solr.
- [ ]  Ranqueamento
Ranqueados por relevancia.
