# Visão Computacional - Detecção de Bananas

Este projeto utiliza técnicas de visão computacional para detectar bananas em imagens utilizando o framework YOLO (You Only Look Once) da Ultralytics.

## Base do Projeto

Este projeto foi desenvolvido com base nos materiais e arquivos do curso de graduação em Visão Computacional com YOLO, ministrado pelo Professor Saulo Santos. Os arquivos originais estão disponíveis no repositório: [https://github.com/Prof-Saulo-Santos/curso-graduacao-visao-computacional-YOLO](https://github.com/Prof-Saulo-Santos/curso-graduacao-visao-computacional-YOLO).

## Características

- **Detecção de Objetos**: Modelo treinado para identificar bananas em imagens
- **Framework YOLO**: Utiliza YOLOv8 para detecção em tempo real
- **Dataset Roboflow**: Conjunto de dados proveniente do Roboflow Universe
- **Jupyter Notebooks**: Notebooks interativos para treinamento e inferência
- **Python Moderno**: Desenvolvido com Python 3.12+

## Instalação

### Pré-requisitos

- Python >= 3.12
- Poetry (para gerenciamento de dependências)

### Passos de Instalação

1. Clone o repositório:
```bash
git clone https://github.com/MagaseAiko/VisaoComputacional.git
cd VisaoComputacional
```

2. Instale as dependências usando Poetry:
```bash
poetry install
```

3. Instale as dependências de desenvolvimento (opcional, para notebooks):
```bash
poetry install --with dev
```

## Uso

### Treinamento do Modelo

Execute o notebook `notebooks/Treinamento.ipynb` para treinar o modelo YOLO no dataset de bananas.

### Inferência

Use o notebook `notebooks/Inferencia.ipynb` para realizar detecções em novas imagens.

### Execução via Terminal

Ative o ambiente virtual:
```bash
poetry shell
```

Execute scripts Python conforme necessário.

## Dataset

O dataset utilizado é o **Banana Ripe Detection** do Roboflow Universe, criado por kipleytaylor.

- **Fonte**: [https://universe.roboflow.com/kipleytaylor/banana-rzonz](https://universe.roboflow.com/kipleytaylor/banana-rzonz)
- **Classes**: 1 (Platano/Banana)
- **Estrutura**: Formato YOLO com divisões train/val/test
- **Licença**: CC BY 4.0

### Estrutura do Dataset

```
dataset_banana/
├── data.yaml          # Configuração do dataset
├── train/
│   ├── images/        # Imagens de treinamento
│   └── labels/        # Anotações YOLO
├── valid/
│   ├── images/        # Imagens de validação
│   └── labels/        # Anotações YOLO
└── test/
    ├── images/        # Imagens de teste
    └── labels/        # Anotações YOLO
```

## Modelos

- `yolov8n.pt`: Modelo YOLOv8 nano pré-treinado
- `yolo26n.pt`: Modelo YOLOv2.6 nano
- `model_banana.pt`: Modelo treinado especificamente para detecção de bananas

## Dependências

### Principais
- `ultralytics >= 8.4.48`: Framework YOLO
- `opencv-python >= 4.13.0`: Processamento de imagens
- `numpy >= 2.4.4`: Computação numérica
- `pandas >= 3.0.2`: Manipulação de dados
- `requests >= 2.33.1`: Requisições HTTP

### Desenvolvimento
- `jupyter >= 1.1.1`: Notebooks interativos
- `ipykernel >= 7.2.0`: Kernel Jupyter para Python

## Estrutura do Projeto

```
VisaoComputacional/
├── pyproject.toml          # Configuração do projeto (Poetry)
├── README.md              # Este arquivo
├── dataset_banana/        # Dataset de bananas
├── notebooks/
│   ├── Treinamento.ipynb  # Notebook de treinamento
│   └── Inferencia.ipynb   # Notebook de inferência
├── model_banana.pt        # Modelo treinado
├── yolov8n.pt            # Modelo YOLOv8 nano
├── yolo26n.pt            # Modelo YOLOv2.6 nano
└── runs/                 # Resultados de detecções
    └── detect/
``` 