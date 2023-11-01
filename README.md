# ProcessamentoDeImagem
Trabalho UFOPA BSI 2021 Marcelo e Khalil

# Introdução:
Este programa captura imagens em tempo real de uma webcam, processa essas imagens e usa um modelo pré-treinado para classificá-las. Uma vez que uma imagem é classificada, o programa exibe o nome da classe e sua pontuação de confiança correspondente.

# Dependências:

Keras: Para carregar e usar o modelo pré-treinado. (TensorFlow é necessário para que o Keras funcione)

OpenCV (cv2): Para capturar e processar imagens da webcam.

Numpy: Para operações matemáticas e manipulações de array.


# Como funciona:
Carregando o Modelo: O modelo pré-treinado, "keras_Model.h5", é carregado para a variável model.

Carregando os Rótulos: Os rótulos das classes são carregados de um arquivo "labels.txt" para a lista class_names.

Inicializando a Webcam: A webcam é inicializada usando cv2.VideoCapture(0). O índice 0 é geralmente para a câmera padrão, mas pode ser alterado para outros números dependendo de quantas câmeras estão conectadas ao computador.

# Execução Principal:

1. A imagem é capturada da webcam.
2. A imagem capturada é redimensionada para 224x224 pixels (tamanho que o modelo espera).
3. A imagem é exibida em uma janela.
4. A imagem é convertida para um array numpy e remodelada para a forma de entrada do modelo.
4. A imagem é normalizada.
4. O modelo faz uma previsão sobre a imagem.
5. O rótulo da classe e a pontuação de confiança são impressos no console.
6. O programa atende a  um pressionamento de tecla: se a tecla "esc" for pressionada, o loop é interrompido e o programa é encerrado.
Encerrando: A conexão com a câmera é liberada e todas as janelas do OpenCV são fechadas.

# Como executar:
Garanta que todas as dependências estejam instaladas.
Coloque o modelo "keras_Model.h5" e o arquivo "labels.txt" no mesmo diretório do script.
Execute o script.
Para sair do programa, pressione a tecla "esc" enquanto estiver focado na janela da imagem da webcam.






