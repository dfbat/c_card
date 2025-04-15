# Hito 1
## Parte Teórica:

## ¿Qué es una red neuronal?
Una red neuronal es un modelo computacional inspirado en la estructura y el funcionamiento del cerebro humano. Se compone de nodos (neuronas artificiales) organizados en capas y conectados mediante pesos sinápticos. Estas redes son utilizadas para tareas de aprendizaje automático como clasificación, regresión y reconocimiento de patrones.

### Componentes principales de una red neuronal:
1. **Neuronas**: Elementos fundamentales que procesan la información.
2. **Capas**:
   - **Capa de entrada**: Recibe los datos de entrada.
   - **Capas ocultas**: Procesan la información aplicando funciones de activación.
   - **Capa de salida**: Genera el resultado final.
3. **Pesos y sesgos**: Parámetros ajustables que determinan la influencia de cada conexión.
4. **Funciones de activación**: Transforman la entrada de cada neurona y permiten la modelización de relaciones no lineales.
5. **Algoritmo de entrenamiento**: Método para ajustar los pesos y mejorar la precisión del modelo.

## Proceso de Backpropagation
El **backpropagation** es un algoritmo de optimización utilizado para entrenar redes neuronales. Su objetivo es ajustar los pesos de la red para minimizar el error en la predicción.

### Pasos del backpropagation:
1. **Propagación hacia adelante**: Se calcula la salida de la red neuronal mediante los valores actuales de los pesos.
2. **Cálculo del error**: Se compara la salida obtenida con la salida esperada y se calcula el error utilizando una función de pérdida.
3. **Propagación hacia atrás**:
   - Se calcula el gradiente del error con respecto a los pesos de la red.
   - Se actualizan los pesos mediante el algoritmo de optimización (ej. descenso de gradiente).
4. **Repetición**: El proceso se repite hasta que el error sea mínimo y la red alcance un buen desempeño.

### Importancia del Backpropagation:
- Permite el ajuste eficiente de los pesos de la red.
- Es fundamental para el entrenamiento de redes neuronales profundas.
- Ayuda a mejorar la precisión del modelo en tareas complejas.

## Funciones de Activación Comunes
Las funciones de activación transforman la entrada de cada neurona y permiten modelar relaciones no lineales. A continuación, se describen tres funciones populares:

1. **Sigmoide**
   - Rango de salida: (0, 1)
   - Suaviza los valores de entrada y es útil para problemas de clasificación binaria.
   - Desventaja: Puede causar problemas de gradientes pequeños, ralentizando el entrenamiento.

2. **ReLU (Rectified Linear Unit)**
   - Define la salida como: f(x) = max(0, x).
   - Ventajas: Simple, eficiente y mitiga el problema del gradiente que desaparece.
   - Desventaja: No activa neuronas con entradas negativas ("Neuronas muertas").

3. **Tangente Hiperbólica (Tanh)**
   - Rango de salida: (-1, 1).
   - Proporciona valores más amplios que la sigmoide, lo que mejora la propagación del gradiente.
   - Útil en redes que requieren modelar relaciones más complejas.
  
# Hito 1
## Parte Práctica:

**Nota, la carpeta comprimida archive.zip contiene la data llamada creditcard.csv. se recomienda descomprimir el archivo csv dentro de la carpeta Data para una correcta visualización**

1. Se realiza la carga de los datos y de las librerías vistas en clase, así como detallar información del dataframe y valores faltantes.
2. Se Preprocesan los datos, incluyendo la normalización de las características (StandardScaler)
3. Se Construye una red neuronal simple utilizando Keras (capa de entrega, capa oculta y capa de salida):
 - Compilar modelo (Adam)
 - Entrenar modelo: Loss: 0.0016371813835576177, Accuracy: 0.999575138092041
 - Evaluar modelo con datos de prueba: Loss en datos de prueba: 0.002944009844213724, Accuracy en datos de prueba: 0.9995786547660828
4. Visualizaciones:
   
    **Análisis de las Gráficas de Pérdida y Precisión durante el Entrenamiento del Modelo**

 **Evolución de la Pérdida**
Teniendo en cuenta las 10 épocas de entrenamiento, Se observa:

- **Entrenamiento (Azul):** La pérdida en el conjunto de entrenamiento disminuye , se manteienen en valores  bajos (~0.0012 a 0.0009), minimizando el error en los datos de entrenamiento.
- **Validación (Naranja):** La pérdida en validación presenta cambios con un pequeño aumento hacia las últimas épocas. posible **sobreajuste**.


 **Evolución de la Precisión**
Se observa:

- **Entrenamiento (Azul):** La precisión del modelo en entrenamiento es alta (~99.97%)**.
- **Validación (Naranja):** La precisión en validación también es alta (~99.94% - 99.96%), pero muestra una disminución en las últimas épocas. Otro indicio de **sobreajuste**.

