# Redução de Dimensionalidade em Imagens para Redes Neurais

Implementação da binarização (preto e branco) sem usar biblioteca para o cálculo.

## Imagem usada

Foto de gato do dataset próprio:  
https://github.com/lfleites/dataset-caes-gatos/blob/main/dataset/gatos/000002.jpeg

## Como funciona

1. A imagem é aberta e convertida para RGB.
2. Cada pixel (R, G, B) vira cinza com a média: `(R + G + B) // 3`.
3. Se o cinza for maior ou igual a 128, o pixel vira branco (255). Senão, preto (0).
4. A imagem binária é montada e salva.

## Sobre o uso do PIL

`from PIL import Image` foi usado apenas para:

- abrir a imagem
- ler os pixels
- criar e salvar a imagem de saída

A função `binarizar` foi escrita na mão, sem uso de outras bibliotecas prontas.

## Como reproduzir

1. Abrir o notebook no Google Colab.
2. Executar as células na ordem.
3. A imagem `gato_binario.jpg` é gerada no final.
