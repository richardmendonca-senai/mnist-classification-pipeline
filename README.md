# Pipeline Preditivo Multiclasse para Classificação MNIST

## 📝 Descrição do Projeto
Este projeto consiste em um **Pipeline de Machine Learning ponta a ponta** para classificação de dígitos manuscritos (0 a 9) a partir do dataset benchmark **MNIST** (`mnist_784`). 

O sistema contrasta modelos clássicos de aprendizado estatístico com redes neurais profundas (MLP), avaliando o desempenho por meio de métricas multiclasse consolidadas e testando a robustez dos classificadores em cenários adversos de generalização extrema (*Out-of-Distribution - OOD*) e inferência com imagens próprias digitalizadas.

---

## 🛠️ Tecnologias e Bibliotecas
* **Linguagem**: Python 3.10+
* **Manipulação e Análise de Dados**: `numpy`, `pandas`
* **Visualização de Dados**: `matplotlib`, `seaborn`
* **Machine Learning & Pré-processamento**: `scikit-learn` (`RandomForestClassifier`, `MLPClassifier`, `LogisticRegression`, `train_test_split`)
* **Processamento de Imagens**: `Pillow` (`PIL`)

---

## 📂 Estrutura do Repositório
```text
mnist-classification-pipeline/
├── data/
│   └── meu_numero.jpeg       # Imagem manuscrita própria utilizada na Fase 5.3
├── pipeline_mnist.ipynb      # Notebook contendo o pipeline executável completo
├── requirements.txt          # Dependências do projeto para reproduzibilidade
└── README.md                 # Documentação do projeto

## Como Executar o Projeto
Clonar o Repositório:
git clone https://github.com/SEU_USUARIO/mnist-classification-pipeline.git
cd mnist-classification-pipeline
Instalar as Dependências:
pip install -r requirements.txt
Executar o Notebook: Abra o arquivo pipeline_mnist.ipynb no VS Code ou Jupyter Notebook e execute as células em sequência.


## Estrutura de Branches (Fluxo Git)
O controle de versionamento seguiu as boas práticas do Git Flow:
main: Código estável e versão final unificada do projeto.
develop: Branch de integração para consolidação das funcionalidades.
feature/fase1-eda: Carregamento e análise exploratória de imagens.
feature/fase2-preprocessing: Divisão estratificada e normalização dos pixels.
feature/fase3-model-training: Treinamento e ajuste de hiperparâmetros dos 3 modelos.
feature/fase4-evaluation: Matrizes de confusão e tabela comparativa de métricas.
feature/fase5-robustness: Testes OOD (Class Masking) e inferência com imagem própria.


## Principais Resultados
Melhor Desempenho: O Random Forest e a Rede Neural (MLP) obtiveram excelente capacidade de generalização no conjunto de teste independente.
Equilíbrio Custo x Benefício: O Random Forest apresentou o melhor equilíbrio entre velocidade de treinamento (~21s) e acurácia.
Achados OOD: Diante de dígitos ocultados no treino (4 e 7), o modelo apresentou o fenômeno da falsa certeza (overconfidence), atribuindo alta probabilidade às classes conhecidas morfologicamente semelhantes (ex: 4 predito como 9).


## Vídeo de Apresentação
Link do Vídeo (Google Drive): [Cole aqui o link compartilhado do seu vídeo no Google Drive]
