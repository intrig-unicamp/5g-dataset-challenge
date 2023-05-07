# Desafios
> Essa pasta contém os desafios propostos para a _Hackathon SMARTNESS / 5G Dataset Challenge_

A edição mais recente do [Relatório de Mobilidade Ericsson](https://www.ericsson.com/en/reports-and-papers/mobility-report/dataforecasts/traffic-by-application) apontou que, no ano de 2022, 71% do tráfego da rede móvel mundial foi constituído por transmissão de vídeo e até 2028 esta demanda deverá aumentar em 9%. Nesse cenário, o gerenciamento e análise de redes móveis se mostram elementos fundamentais para promover uma melhor experiência de uso desse tipo de serviço, fator este que tende a proporcionar novas oportunidades de negócio e pesquisa à medida em que o uso da rede 5G se expande.

Em vista disso, a Hackathon SMARTNESS apresenta os seguintes desafios que podem contribuir para o desenvolvimento de novas soluções de gerenciamento e análise de redes móveis, visando atender a crescente demanda de tráfego de vídeo e a otimização da qualidade de experiência do usuário.

- 📊🔍 **Visualização usando o PathsViewer**

  **A ferramenta**: PathsViewer é uma interface para visualização de dados espaço-temporais em tempo real ou pós-eventos. Essa ferramenta busca suprir a demanda por ferramentas de visualização de trajetórias de objetos, em vista do grande interesse em pesquisas nesse tipo de dado.

  É possível utilizar conjuntos de dados variados, com estruturas diversas, tais como traces de 5G georeferenciados e trajetórias de veículos.

  **O desafio**: Esse desafio tem como objetivo usar a ferramenta PathViewer para apresentar os conjuntos de dados fornecidos (não é necessário utilizar todos eles).

  As equipes devem explorar as funcionalidades do PathViewer, como ajuste de escala, visualização em mapa 2D ou satélite, envio de múltiplos conjuntos de dados, entre outras. Com isso, é possível gerar visualizações claras e informativas que ajudem os usuários a visualizar as informações contidas nos dados de trajetórias de objetos.

  **A entrega**: De modo que esse desafio em específico não envolve a aplicação de técnicas de aprendizado de máquina (tal como os demais a seguir), não é solicitado a entrega de um Jupyter Notebook/Colab. Em vez disso, espera-se que a submissão desse desafio seja composta de uma descrição do que foi realizado pela equipe, os insights obtidos, sugestões de melhorias para a ferramenta, eventuais códigos produzidos para o tratamento de dados acompanhado de um vídeo ou capturas de tela que mostrem a interface do PathsViewer com os conjuntos de dados fornecidos. É importante que a entrega mostre as funcionalidades utilizadas da ferramenta.

---
- 🔮📶 **Predição de qualidade de sinal em determinado local**

  Com o objetivo de prever a qualidade de sinal dado um ponto `(latitude, longitude)`, as equipes devem empregar técnicas de aprendizado de máquina no conjunto de dados `g-nettrack-pro`. Uma estratégia pode ser a combinação de diferentes conjuntos de dados para enriquecimento de dados, como, por exemplo, usar a base `g-nettrack-pro` enriquecida com o `mosaico` para prover informações das antenas na proximidade, como a localização, azimute, densidade de antenas, frequência e tecnologia.

  As equipes deverão utilizar técnicas de aprendizado de máquina, como predição mono-variada e multi-variada, para prever os valores de um indicador de qualidade de sinal de escolha, tal como QUAL, CQI e SNNR.

---
- 🔮🚗 **Predição do tipo de mobilidade**

  Esse desafio consiste em utilizar métodos não-supervisionados de aprendizado de máquina para prever o tipo de mobilidade (pedestre, veículo, metrô/trem) de um dispositivo móvel com base nos dados de localização não rotulados fornecidos pelo conjunto de dados `g-nettrack-pro`. Essa tarefa pode ser abordada de diversas formas, como, por exemplo, na forma de um problema de classificação baseada em clusterização (classificação não-supervisionada), onde o modelo de aprendizado de máquina deve classificar cada registro do conjunto de dados em uma das classes de mobilidade possíveis.

---
- 🔮🎬 **Predição da qualidade de transmissão de vídeo**

  O desafio de predição da qualidade de transmissão de vídeo adaptativo (YouTube) consiste em utilizar técnicas de aprendizado de máquina para prever a qualidade da transmissão de vídeo em dispositivos móveis. A base `youtube-qoe` fornece as métricas de qualidade de transmissão. O objetivo é criar dois modelos de predição que levem em conta informações como as coordenadas do celular, as características da rede, a tecnologia utilizada, entre outras variáveis, para estimar a qualidade de transmissão de vídeo. Com isso, é possível melhorar a experiência do usuário, garantindo que a transmissão de vídeo seja realizada com a melhor qualidade possível, considerando as condições da rede e do ambiente em que o usuário está localizado.

  Os modelos devem prever a qualidade de transmissão de vídeo com base em entradas distintas:
  - Modelo 1: faz a predição com base nos dados de localização, obtidos no conjunto `g-nettrack-pro` correlacionado com o `mosaico` para obter as antenas na proximidade; e
  - Modelo 2: faz a predição com base nas métricas da rede (como qualidade do sinal, tecnologia, frequência), obtidos no conjunto `g-nettrack-pro`.

---
- 🔮📡 **Inferir a qual Célula/Estação Rádio Base um celular está conectado**

  O desafio proposto é inferir a qual Célula/Estação Rádio Base (ERB) o dispositivo móvel está conectado, com base nas coordenadas do celular, usando o conjunto de dados `g-nettrack-pro` correlacionado com a base `mosaico` para obter as antenas na proximidade. Isso envolve o uso de técnicas de processamento de dados e aprendizado de máquina para analisar os dados de localização e antenas próximas, além de conhecimento básico de implantação da arquitetura física de redes móveis.

  Deve ser levado em consideração que as antenas de uma ERB podem ser direcionais (Azimute > 0) ou omnidirecionais (Azimute = 0), isto é, podem direcionar o sinal transmitido para uma determinada direção ou transmitir sinal para todas as direções ao seu redor, respectivamente.

# Critérios de avaliação
- Os participantes devem resolver o maior número possível dos desafios fornecidos
- Pré-processamento dos dados
- Representação dos dados e estratégia de composição de atributos
- Estratégia de seleção do modelo escolhido
- Estratégia de validação
- Qualidade do modelo em relação as métricas de qualidade (acurácia, precisão, revocação, F1-score, etc)
- Interpretabilidade do modelo sugerido
- Storytelling dos dados, incluindo conclusões
- Potencial impacto e viabilidade da solução apresentada
- Criatividade da solução e apresentação
