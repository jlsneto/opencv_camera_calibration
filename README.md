# Calibração
Algumas Câmeras introduzem distorção nas imagens (distorção radial e a distorção tangencial)

1. Distorção Radial
    * Faz com que as linhas retas pareçam curvas. [Saiba mais...](https://en.wikipedia.org/wiki/Distortion_%28optics%29)
2. Distorção Tangencial
    * Faz com que a lente de captura de imagem não esteja alinhada perfeitamente paralela ao plano de imagem.
    Portanto, algumas áreas da imagem podem estar mais próximas do que o esperado

3. Parâmetros Intrínsicos
    * São específicos de cada câmera. Incluem informações como distância focal e centros ópticos,
    ambos serão utilizados para criar uma matriz de câmera, que será utilizada para remover a distorção devido às lentes de uma câmera específica.
    * Os parâmetros INTRÍNSICOS, são exclusivos para cada câmera, portanto, ***podem ser reutilizados*** em outras imagens
    captadas pela mesma câmera.

4. Parâmetros Extrínsicos
    * Correspondem a vetores de rotação e translação que traduzem coordenadas de um ponto 3D para um sistema de coordenadas.
    * Para aplicações ***estéreo***, essas distorções precisam ser corrigidas primeiro.
    * Para encontrar esses parâmetros, devemos fornecer algumas imagens de amostra de um padrão bem definido (por exemplo, um tabuleiro de xadrez)
    * Conhecemos as coordenadas desses pontos no espaço do mundo real e sabemos as coordenadas na imagem, para que possamos resolver os coeficientes de distorção.

> Disponível em [Docs OpenCv](https://docs.opencv.org/3.4.7/dc/dbb/tutorial_py_calibration.html)