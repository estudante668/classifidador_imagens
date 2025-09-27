# 🐶🐱 Classificador de Imagens: Gatos vs Cachorros com MobileNetV2

Este projeto utiliza Transfer Learning com MobileNetV2 para classificar imagens de gatos e cachorros. O modelo foi treinado no Google Colab, com fine-tuning das camadas superiores para melhorar a acurácia.

## 🚀 Tecnologias Utilizadas

- Python 3
- TensorFlow 2.x
- Keras
- Google Colab
- MobileNetV2 (pré-treinado no ImageNet)
- Matplotlib

## 📁 Estrutura do Projeto
├── dataset/ │   ├── cats/ │   └── dogs/ ├── model/ │   └── saved_model/ ├── notebooks/ │   └── classificacao_gatos_cachorros.ipynb ├── README.m

## 📊 Resultados

- Acurácia de validação após fine-tuning: **~98%**
- Curvas de aprendizado mostram boa generalização com leve risco de overfitting

## 🧠 Etapas do Treinamento

1. Pré-processamento e data augmentation
2. Extração de características com MobileNetV2 congelado
3. Treinamento do classificador superior
4. Fine-tuning das últimas camadas da MobileNetV2
5. Avaliação no conjunto de teste
6. Predição de novas imagens

## 📦 Como usar

```python
from tensorflow.keras.models import load_model
model = load_model('model/saved_model')

# Prever nova imagem
img = prepare_image('minha_imagem.jpg')
pred = model.predict(img)
print("É um cachorro!" if pred[0] > 0.5 else "É um gato!")

# Experiencias
 Alem de colocar a mão na massa aprenendo e aplicando os fundamentos e conceitos apresentados no
curso. Pode, de certa forma, colaborar com o tensorflow em observar um bug, pelo menos na minha maquina kkk
 **NotFoundError no tutorial cats_and_dogs_filtered com tf.keras.utils.get_file(extract=True) (TF 2.19, Colab) #101115**
-Explicando o problema:

# Obsevação: os.path.dirname(path_to_zip) obtém o diretório pai onde o ZIP foi salvo.

-os.path.dirname() é uma função que retorna o nome do diretório de um determinado caminho de arquivo.
-O que faz: Ela pega o caminho do arquivo ZIP e remove o nome do arquivo (cats_and_dogs.zip), deixando apenas o diretório onde ele reside.
-Resultado do exemplo:
/home/user/.keras/datasets

-Porem em certa parte do codigo buga, pq o utlitario pode salvar cache do diretorio com no diferente do padronizado pelo codigo no colab
possivelmente problemas de versão.

-Por se tratar de tutorial as pessoas podem ficar desmotivadas em não conseguir rodar o codigo.

Bom, nunca trabalhei com TI mas me senti um bom profissional na area.

img = prepare_image('minha_imagem.jpg')
pred = model.predict(img)
print("É um cachorro!" if pred[0] > 0.5 else "É um gato!")
