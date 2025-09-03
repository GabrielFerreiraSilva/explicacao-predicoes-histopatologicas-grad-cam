# Explicando Previsões de Câncer de Mama com ResNet-50 e Grad-CAM

Este repositório demonstra a aplicação da técnica **Grad-CAM (Gradient-weighted Class Activation Mapping)** no campo da Inteligência Artificial Explicável (XAI) para interpretar as previsões de um modelo ResNet-50 treinado para classificar imagens histopatológicas de câncer de mama.

### 🔍 O Problema: A "Caixa-Preta" em Deep Learning

Modelos de redes neurais profundas, apesar de sua alta acurácia, são frequentemente considerados "caixas-pretas". Suas decisões complexas são difíceis de interpretar por humanos, o que representa um grande obstáculo para sua adoção em áreas críticas como a medicina, onde a confiança e a validação do raciocínio do modelo são fundamentais.

### 💡 A Solução: Explainable AI com Grad-CAM

Este projeto utiliza a técnica Grad-CAM para trazer transparência ao processo de decisão do modelo. O Grad-CAM gera "mapas de calor" (heatmaps) que destacam visualmente as regiões de uma imagem que mais influenciaram a predição, respondendo à pergunta:

> *"Quais partes da imagem levaram o modelo a classificar esta amostra como benigna ou maligna?"*

### 🔗 Pré-requisito: Modelo Treinado

Este notebook não realiza o treinamento do modelo. Ele carrega e utiliza um classificador ResNet-50 treinado anteriormente. Para mais detalhes sobre o treinamento, consulte o repositório original.

*   **Repositório do Modelo:** [classficacao-imagens-histopatologicas-resnet-50](https://github.com/GabrielFerreiraSilva/classficacao-imagens-histopatologicas-resnet-50)

### 🛠️ Pipeline de Execução

O processo detalhado no notebook segue quatro etapas principais:

1.  **Carregamento do Modelo:** Uma rede neural ResNet-50 já treinada é carregada a partir de um arquivo de pesos.
2.  **Implementação do Grad-CAM:** A classe é construída para extrair os gradientes e as ativações da última camada convolucional do modelo.
3.  **Análise de Amostras:** A técnica é aplicada a imagens de exemplo de ambas as classes (benigna e maligna).
4.  **Visualização e Interpretação:** Geração de mapas de calor que se sobrepõem às imagens originais, permitindo uma análise direta das áreas de interesse do modelo.

### 🚀 Como Usar

1.  Clone este repositório:
    ```bash
    git clone https://github.com/GabrielFerreiraSilva/explicacao-predicoes-histopatologicas-grad-cam
    cd explicacao-predicoes-histopatologicas-grad-cam
    ```
2.  Certifique-se de ter o arquivo de pesos (`.pth`) do modelo treinado. Coloque-o no diretório apropriado, configurando corretamente a variável `CAMINHO_PESOS`.
3.  Abra o Jupyter Notebook.
4.  Execute as células para gerar as explicações visuais para as imagens de exemplo.
