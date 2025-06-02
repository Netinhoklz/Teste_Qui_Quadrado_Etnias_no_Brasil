# Estatística para a Ciência de Dados - Análise Populacional Étnica

<img src='https://www.unifor.br/o/unifor-theme/images/unifor-logo-horizontal.svg' width="250px">

**Disciplina:** Estatística para a Ciência de Dados
**Professores:** Furlan e Hygor
**Aluno:** José Freitas Alves Neto
**Matrícula:** 2519203
**Laboratório:** Laboratório de Ciência de Dados e Inteligência Artificial (LCDIA)
**Instituição:** Universidade de Fortaleza

## 📝 Descrição do Projeto

Este projeto realiza uma análise estatística sobre a distribuição populacional étnica em municípios brasileiros. Utiliza-se o teste Qui-Quadrado de independência para verificar se existe associação significativa entre diferentes categorizações geográficas/demográficas e a distribuição das populações autodeclaradas como Amarela, Branca, Indígena, Parda e Preta.

## 📊 Dataset

O dataset utilizado é o `Filtered_Population_Attributes_from_DBF.csv`, contendo dados populacionais de municípios brasileiros.

**Colunas de População Residente por Etnia:**
*   `PopResidAm`: População residente Amarela
*   `PopResidBr`: População residente Branca
*   `PopResidIn`: População residente Indígena
*   `PopResidPa`: População residente Parda
*   `PopResidPr`: População residente Preta
*   `PopResidTo`: População residente Total

O dataset é baixado diretamente no ambiente Colab através do seguinte comando:
```bash
!gdown 1tZw5d5n4lQaI6eLhqhGsbU5pWwc70Flz
🛠️ Análises Realizadas
O notebook realiza as seguintes análises principais:
Leitura e Preparação dos Dados:
Carregamento do dataset.
Separação da coluna Nome em UF (sigla do estado) e Estados (nome do município).
Análise da Distribuição Étnica nas Capitais Brasileiras:
Filtra o dataset para incluir apenas as capitais dos estados brasileiros.
Monta uma tabela de contingência com a população de cada etnia por capital.
Teste Qui-Quadrado de Independência:
Estatística Qui-Quadrado (χ²): 6283652.2984
Valor-p: 0.000000e+00
Conclusão: Rejeita-se a hipótese nula (H0). Há evidência estatística de que existe uma associação significativa entre as capitais e a distribuição das populações étnicas.
Visualização: Geração de um gráfico de barras 100% empilhadas mostrando a proporção de etnias por capital.
Análise da Distribuição Étnica por Faixas Populacionais dos Municípios:
Classifica os municípios em faixas de tamanho ('Pequeno', 'Médio', 'Grande') com base na PopResidTo.
Agrupa os dados de população étnica por essas faixas.
Teste Qui-Quadrado de Independência:
Estatística Qui-Quadrado (χ²): 1797035.7061
Valor-p: 0.000000e+00
Conclusão: Rejeita-se a hipótese nula (H0). Há evidência estatística de que existe uma associação significativa entre o tamanho dos municípios e a distribuição das populações étnicas.
Visualização: Geração de um gráfico de barras 100% empilhadas mostrando a proporção de etnias por faixa de tamanho do município.
Análise da Distribuição Étnica por Regiões do Brasil:
Mapeia as UFs para suas respectivas regiões (Norte, Nordeste, Sul, Sudeste, Centro-Oeste).
Agrupa os dados de população étnica por região.
Teste Qui-Quadrado de Independência:
Estatística Qui-Quadrado (χ²): 25146791.3804
Valor-p: 0.000000e+00
Conclusão: Rejeita-se a hipótese nula (H0). Há evidência estatística de que existe uma associação significativa entre as regiões do Brasil e a distribuição das populações étnicas.
Visualização: Geração de um gráfico de barras 100% empilhadas mostrando a proporção de etnias por região.
📈 Conclusões Gerais
Em todas as análises realizadas (capitais, faixas populacionais e regiões), o teste Qui-Quadrado indicou, com um nível de significância de 0.05, a rejeição da hipótese nula. Isso sugere que a distribuição étnica da população não é aleatória em relação a essas categorias, existindo associações estatisticamente significativas.
🚀 Tecnologias Utilizadas
Python
Pandas
Matplotlib
NumPy
SciPy (para o teste Qui-Quadrado)
Google Colab (ambiente de desenvolvimento)
⚙️ Como Usar
Clone este repositório.
Abra o arquivo .ipynb em um ambiente Jupyter (como Google Colab, Jupyter Lab ou Jupyter Notebook).
Execute as células sequencialmente. O dataset será baixado automaticamente na primeira execução da célula de importação.
Os gráficos gerados são salvos como proporcao_etnias_por_estado_empilhado_vermelho.png (atenção: o nome do arquivo é o mesmo para os diferentes gráficos, o que pode causar sobrescrita se não for ajustado no notebook).
