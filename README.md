# Bootcamp_BairesDev
Bootcamp BairesDev - Machine Learning Practitioner - desafios

Descrição do Projeto Desafio 1

Este projeto implementa uma solução de aprendizado profundo para classificar dígitos manuscritos usando o conjunto de dados MNIST. Ele combina a simplicidade do MNIST com a sofisticação de redes neurais convolucionais modernas através de transfer learning utilizando a MobileNetV2. O pipeline do projeto pode ser descrito em etapas principais:

Carregamento e Pré-processamento dos Dados:

O conjunto de dados MNIST é carregado, contendo imagens de dígitos manuscritos de tamanho 28x28 pixels.
As imagens são normalizadas para valores entre 0 e 1 e convertidas para um formato compatível com redes convolucionais (28x28x1).
As labels dos dígitos são transformadas em formato categórico para classificação de 10 classes (dígitos de 0 a 9).
Transfer Learning com MobileNetV2:

A MobileNetV2, uma arquitetura moderna pré-treinada na ImageNet, é utilizada como base.
As camadas da MobileNetV2 são congeladas para reutilizar seus recursos extraídos sem treinamento adicional.
As imagens MNIST, originalmente monocromáticas (1 canal), são redimensionadas para 224x224 pixels e convertidas para 3 canais (RGB) para compatibilidade com a MobileNetV2.
Construção do Modelo:

O modelo consiste em camadas adicionais para ajustar as entradas do MNIST à MobileNetV2 e processar sua saída.
Inclui uma camada de pooling global e uma camada densa com ativação softmax para produzir as probabilidades das 10 classes.
Treinamento e Avaliação:

O modelo é treinado por 10 épocas usando o otimizador Adam e a função de perda de entropia cruzada categórica.
O desempenho é avaliado no conjunto de teste, com a métrica de acurácia como principal indicador.
Visualização:

A evolução da acurácia no conjunto de treinamento e validação é plotada para analisar o desempenho ao longo das épocas.
Objetivo do Projeto: Explorar a aplicação de transfer learning em tarefas simples como a classificação de dígitos manuscritos, utilizando uma arquitetura moderna e eficiente como a MobileNetV2 para acelerar o desenvolvimento e melhorar a precisão do modelo.

Resultados Esperados:

Uma alta acurácia na classificação dos dígitos do MNIST.
Demonstração da eficácia de transfer learning mesmo em problemas com dados diferentes do domínio da ImageNet.
O projeto é ideal para estudantes ou profissionais que desejam aprender sobre transfer learning e combinar redes modernas com datasets clássicos.
