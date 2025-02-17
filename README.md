# meli_challenge
Repo challenge ML


Este repositorio contiene el código para el **Desafío 1 y Desafío 2**.  A continuación se detallan los pasos necesarios para instalar las dependencias, configurar el entorno y ejecutar el proyecto.

## Requisitos

- [Poetry](https://python-poetry.org/) (gestor de dependencias y entornos virtuales)
- [Python 3.8+](https://www.python.org/)
- [Jupyter Notebook](https://jupyter.org/)

## Instalación

1. **Clonar el repositorio:**

   Si aún no has clonado el repositorio, puedes hacerlo con el siguiente comando:

   ```bash
   git clone https://github.com/sralex/meli_challenge.git
   cd meli_challenge
   ```

2. **Instalar las dependencias:**

Entra al ejercicio que desees ejecutar:

```bash
   cd Desafio2
   ```

Usa Poetry para instalar todas las dependencias necesarias para el proyecto. Asegúrate de tener Poetry instalado antes de proceder (ver sección de instalación de Poetry si es necesario).

```bash
poetry install
```

Esto te permitirá trabajar dentro del entorno virtual donde todas las dependencias están disponibles.

3. **Uso**

Abrir Jupyter Notebook
Una vez que las dependencias estén instaladas y el entorno esté activado, puedes abrir Jupyter Notebook con el siguiente comando:

```bash
poetry run jupyter notebook
```
4. **Desafio 1**

La solución propuesta consistió en entrenar un modelo de clasificación basado en BERT para predecir seis etiquetas distintas: 'urgent', 'artificial intelligence', 'computer', 'travel', 'animal' y 'fiction'. Los datos utilizados para entrenar el modelo fueron generados a partir de GPT-2.

Para replicar este proceso, no es indispensable volver a ejecutar GPT-2, ya que el archivo gpt2_database_4k.parquet ya contiene la base de datos generada, con 4,000 ejemplos por clase. Si aún se desea generar nuevos datos, se puede ejecutar el notebook generate_data, que emplea GPT-2 para crear la base de datos.

Posteriormente, se debe ejecutar el notebook train-classes-2, el cual utiliza los datos generados por GPT-2 para entrenar el modelo basado en BERT.

El notebook train-classes-2 se enfoca exclusivamente en descongelar las capas de clasificación y la última capa de BERT. Esta estrategia permitió obtener excelentes resultados en un tiempo de entrenamiento considerablemente más corto.

En una fase inicial, se probó entrenar el modelo completo en el notebook train-classes, lo cual resultó en un proceso más largo, pero también produjo buenos resultados.

El archivo gpt2_database_4k.parquet contiene la base de datos generada, que incluye 4,000 registros por clase, sumando un total de 24,000 registros.

5. **Desafio 2**

Para el desafío 2 solo hay un notebook, este se puede abrir luego de ejecutar el comando antes mencionado, no es necesario hacer nada más.



