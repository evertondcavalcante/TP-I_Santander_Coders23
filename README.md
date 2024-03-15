# Projeto: Sistema para Edição de imagens e áudios

Este projeto faz parte da avaliação do Módulo 03 - Técnicas de Programação I do programa Santander Coders 2023. O objetivo é validar os conhecimentos adquiridos em aula através da implementação de um programa em Python para manipulação de imagens e áudios. Abaixo está um [índice](#índice) de conteúdo que lista alguns dos tópicos aprendidos em aula e onde eles foram aplicados no projeto.


## Conteúdo desse projeto 

Nesse projeto temos três scripts python:
  - image_process.ipynb
  - audio_process.ipynb
  - log_analysis.ipynb

Cada script aborda diferentes aspectos do processamento de imagens e áudios, proporcionando uma experiência completa de aprendizado e prática dos conceitos apresentados no curso. A seguir decreve-se o contéudo apresentado em cada script:

#### `image_process.ipynb`

Este script realiza diversas operações de processamento de imagens, incluindo rotação, inversão horizontal, deslocamento e zoom. Além disso, o script também registra informações sobre as operações realizadas em um arquivo de log ***log_image.csv***.

#### `audio_process.ipynb` 

Este script implementa as seguintes operações de processamento de áudio:

   - **Leitura de arquivo WAV**: Utiliza a função `scipy.io.wavfile.read()` para carregar um arquivo WAV em uma variável numpy array, contendo os dados de áudio e a taxa de amostragem;

   - **Inversão de áudio**: Inverte o áudio original;

   - **Convolução de áudio**: A convolução é uma operação matemática comum em processamento de sinais que combina duas funções para produzir uma terceira, representando como uma é afetada pela outra ao longo do tempo;

   - **Normalização de áudio**: Normaliza o áudio para ajustar os níveis de amplitude;

   - **Corte de áudio**: Recorta parte do áudio, selecionando apenas uma parte específica;

   - **Concatenação de áudio**: Junta dois arquivos de áudio em um único arquivo;

   - **Mistura de áudio**: Mistura dois arquivos de áudio em um único arquivo;

   - **Filtragem de áudio**: Aplica filtros, para redução de ruído no áudio original.

   - **Espectograma**: Criação de um espectograma para analizar a amplitude de um áudio

Assim como no script de processamento de imagens, este script também registra informações em um arquivo de log ***log_audio.csv***.


----------------------------------------------------------------------------------------------------------------------------------------------
<div style="background-color: #f2f2f2; padding: 10px;">

**`Arquivos de Log`**

Os arquivos de log ( *log_image.csv* | *log_audio.csv* ) irão incluir as seguintes informações:

- **Data e hora**: Registrar a data e hora em que o processamento foi realizado;

- **Tipo de processamento**: Indicar o tipo de processamento de imagem/áudio realizado (rotação, deslocamento, corte, concatenação, etc.);

- **Tempo de processamento**: Indicar o tempo de processamento em milissegundos;

- **Nome do arquivo de imagem**: Indicar o nome do arquivo de imagem/áudio processado;

- **Tamanho do arquivo**: Indicar o tamanho em KB do arquivo processado;

- **Resultado do processamento**: Indicar se o processamento foi bem-sucedido ou se ocorreu algum erro;

- **Mensagem de erro**: Em caso de erro, registrar a mensagem de erro específica.

</div>

----------------------------------------------------------------------------------------------------------------------------------------------

#### `log_analysis.ipynb`

Este script realiza análises dos arquivos de log de processamento de imagens e áudios usando a biblioteca Pandas. As análises incluem:

- **Tempo médio de processamento por tipo de processamento** (identificação das manipulações que exigem mais performance);
- **Distribuição do tempo de processamento** (visualização da distribuição do tempo de processamento para identificar outliers ou padrões incomuns);
- **Arquivos com tempo de processamento abaixo da média**;
- **Comparação de desempenho entre tipos de processamento** (comparação do tempo médio de processamento entre diferentes tipos para identificar os mais demorados e que podem precisar de otimização);
- **Análise de correlação entre tamanho do arquivo e tempo de processamento** (verificação de correlação entre o tamanho do arquivo e o tempo de processamento);
- **Análise de frequência por tipo de processamento** (identificação dos tipos de processamento mais frequentes e se há algum padrão relacionado a eles);
- **Análise de erros por tipo de processamento** (verificação se há tipos de processamento com mais erros e investigação das causas desses erros).

&nbsp;

> **Observação**:
--------------------------------------------
Para a criação do arquivo de log do processamento das imagens ( *log_image.csv* ), utilizamos um conjunto de dados de imagens obtido do TensorFlow. O conjunto de dados utilizado é o de imagens de flores (*flower_photos*), especificamente a pasta '*dandelion*' desse conjunto. Essa pasta contém 898 arquivos de imagem no formato JPG. Para preencher o arquivo de log, utiliza-se uma lista de parâmetros (ângulos, deslocamentos, fatores de zoom) e uma lista de operações de processamento (rotação, inversão horizontal, deslocamento, zoom) para aplicar transformações aleatórias às imagens. Alguns parâmetros são preenchidos com valores que causam erros propositalmente.

&nbsp;

## Índice

- Script image_process.ipynb
  - Função para criar ou abrir arquivo de log
  - Função para registrar log
  - Função carregar imagem
  - Função Rotacionar imagem
  - Função Inverter horizontalmente a imagem
  - Função Deslocar a imagem
  - Função Zoom

- Script audio_process.ipynb
  - Função para criar ou abrir arquivo de log
  - Função para registrar log
  - Função Ler arquivo WAV
  - Função Convolução de áudio
  - Função Normalização de áudio
  - Função Corte de áudio
  - Função Concatenação de áudio
  - Função Filtragem de áudio
  - Espectograma

- Script log_analysis.ipynb
  - Carregar arquivo de log (pandas.read_csv())
  - Tempo de processamento médio por tipo (imagem ou áudio) (groupby() e mean())
  - Distribuição do tempo de processamento (matplotlib.pyplot.hist(), matplotlib.pyplot.gca().set_yticklabels(), matplotlib.pyplot.xlabel(), matplotlib.pyplot.ylabel(), matplotlib.pyplot.title() e matplotlib.pyplot.show())
  - Arquivos com tempo de processamento abaixo da média (mean())
  - Análise de correlação (corr())
  - Análise de frequência por tipo de processamento (value_counts())
  - Análise de erros por tipo de processamento (pandas.unique(), matplotlib.pyplot.subplots(), ax.bar(), ax.set_xlabel(), ax.set_ylabel(), ax.set_title(), ax.set_xticks(), ax.set_xticklabels() e matplotlib.pyplot.show())
  - Arquivos com tempo de processamento abaixo da média (mean())
  - Análise de correlação entre tamanho do arquivo e tempo de processamento
  - Análise de frequência por tipo de processamento
  - Análise de resultado por tipo de processamento
  - Análise de erros por tipo de processamento



&nbsp;

## Autores

- [@andreaseliass](https://github.com/andreaseliass)
- [@AnthonyHeimlich](https://github.com/AnthonyHeimlich)
- [@evertondcavalcante](https://github.com/evertondcavalcante)
- [@JuliaMidoriRW](https://github.com/JuliaMidoriRW)
- [@luana-kruger](https://github.com/luana-kruger)
