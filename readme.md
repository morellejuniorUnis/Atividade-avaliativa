# Face Detection Project

Este projeto foi criado para detectar rostos em imagens e vídeos, usando dois métodos populares: OpenCV e dlib. O projeto é executado no Google Colab e permite carregar arquivos diretamente do seu Google Drive ou fazer upload manual de imagens e vídeos.

## Funcionalidades

- **Detecção de Rostos em Imagens**: O projeto consegue identificar rostos em imagens e desenhar retângulos ao redor deles.
- **Detecção de Rostos em Vídeos**: Também pode processar vídeos, identificar rostos e salvar o resultado em um novo vídeo com as detecções.
- **Suporte para Google Drive**: Você pode carregar arquivos diretamente do seu Google Drive para serem processados.

## Como funciona

1. **Carregamento de arquivos**: O usuário pode escolher entre:
   - Fazer o upload manual de imagens ou vídeos.
   - Carregar os arquivos de uma pasta no Google Drive.
2. **Processamento**:
   - As imagens são analisadas e os rostos são detectados usando o algoritmo Haar Cascade ou o detector HOG de dlib.
   - Para vídeos, o processo é semelhante, mas quadro a quadro, com o vídeo final sendo salvo com as detecções visíveis.
3. **Exibição dos Resultados**: O projeto exibe as imagens processadas e também salva o vídeo final (no caso de vídeos) com os rostos detectados.

## Pré-requisitos

- **Google Colab**: O projeto foi desenvolvido para rodar no Google Colab.
- **OpenCV**: Para processar as imagens e vídeos e fazer a detecção de rostos.
- **dlib**: Um outro algoritmo de detecção de rostos baseado em Histogram of Oriented Gradients (HOG).

## Como Usar

1. **Montar o Google Drive**: O projeto permite que você monte seu Google Drive no Google Colab para acessar arquivos.

   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   ```

2. **Upload de arquivos**: Você pode fazer upload de imagens ou vídeos manualmente:

   ```python
   uploaded = files.upload()
   ```

3. **Detecção de Rostos**:
   - Para **imagens**, os rostos são detectados e retângulos verdes são desenhados ao redor dos rostos.
   - Para **vídeos**, os rostos são detectados em cada quadro, e o resultado é salvo em um novo vídeo.

## Resultados

- As imagens processadas são exibidas diretamente no Colab.
- No caso de vídeos, o vídeo final com as detecções é baixado automaticamente como `output_pessoas_detectadas.mp4`.
