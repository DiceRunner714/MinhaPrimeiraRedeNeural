# Minha Primeira Rede Neural

Projeto acadêmico com o objetivo de entender os fundamentos de redes neurais feedforward, desenvolvido e executado no Google Colab.

---

## Objetivo

> Este projeto foi criado com fins **exclusivamente educacionais**. A ideia é aprender na prática como uma rede neural é construída, treinada e avaliada, usando um problema simples e bem definido: **classificar conjuntos de 4 comprimentos** como triângulo, retângulo ou nenhum dos dois.

---

## O Problema

Dada uma entrada com 4 valores inteiros representando comprimentos de lados, a rede deve classificar:

| Classe | Descrição | Exemplo de entrada |
|--------|-----------|-------------------|
| `0` | Triângulo | `[0, 3, 4, 5]` |
| `1` | Retângulo | `[2, 2, 7, 7]` |
| `2` | Nenhum dos dois | `[1, 2, 3, 4]` |

> **Observação:** Um dos quatro valores deve ser `0` para indicar que apenas três lados são usados (caso triângulo).

---

## Estrutura do Repositório

```
📦 MinhaPrimeiraRedeNeural
 ┣ 📓 NN1.ipynb          # Notebook principal (rodar no Google Colab)
 ┣ 📄 dados1.csv         # Dataset pequeno (1 exemplo por classe)
 ┣ 📄 dados10.csv        # Dataset com 10 exemplos
 ┣ 📄 dados100.csv       # Dataset com 100 exemplos
 ┣ 📄 dados1000.csv      # Dataset com 1.000 exemplos
 ┣ 📄 dados10000.csv     # Dataset com 10.000 exemplos
 ┗ 📄 README.md
```

---

## Como Executar

Este projeto foi desenvolvido para rodar no **Google Colab**. Para utilizá-lo:

1. Acesse [colab.research.google.com](https://colab.research.google.com)
2. Faça upload do arquivo `NN1.ipynb`
3. Faça upload do arquivo CSV desejado (ex: `dados10000.csv`)
4. Execute as células em ordem

> Nenhuma instalação local é necessária. O Colab já possui TensorFlow, NumPy e scikit-learn disponíveis.

---

## O que o Notebook Faz

O notebook está dividido nas seguintes etapas:

1. **Importação de bibliotecas** - NumPy, CSV, TensorFlow Keras e scikit-learn
2. **Geração de dados** - Cria amostras balanceadas das três classes usando regras lógicas
3. **Preparação dos dados** - Separação em treino/teste e conversão para one-hot encoding
4. **Criação do modelo** - Rede feedforward com 2 camadas ocultas (16 neurônios cada, ReLU) e saída softmax
5. **Treinamento** - 50 épocas, batch size 32, com validação em tempo real
6. **Teste interativo** - Loop que aceita entradas manuais e exibe a predição

---

## Arquitetura da Rede

```
Entrada (4 neurônios)
       ↓
Camada Oculta 1 - 16 neurônios, ReLU
       ↓
Camada Oculta 2 - 16 neurônios, ReLU
       ↓
Saída (3 neurônios, Softmax)
```

- **Otimizador:** Adam  
- **Função de perda:** Categorical Crossentropy  
- **Métrica:** Acurácia

---

## Datasets Disponíveis

Os arquivos CSV foram gerados automaticamente pelo próprio notebook, com distribuição **equilibrada entre as três classes**. Cada linha contém 5 valores: os 4 comprimentos e o rótulo da classe.

| Arquivo | Exemplos por classe | Total |
|---------|-------------------|-------|
| `dados1.csv` | 1 | ~3 |
| `dados10.csv` | 10 | ~30 |
| `dados100.csv` | 100 | ~300 |
| `dados1000.csv` | 1.000 | ~3.000 |
| `dados10000.csv` | 10.000 | ~30.000 |

---

## Conceitos Abordados

- Redes neurais feedforward (MLP)
- Funções de ativação (ReLU, Softmax)
- Otimização com Adam
- Categorical Crossentropy
- One-hot encoding
- Divisão treino/teste
- Overfitting e validação
- Geração de dados sintéticos balanceados

---

## Aviso

Este repositório tem **fins acadêmicos**. O código foi escrito com foco em clareza e aprendizado, não em performance ou uso em produção.

---

*Desenvolvido como parte de um estudo introdutório sobre redes neurais artificiais.*
