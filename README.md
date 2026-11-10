# Aprendizaje supervisado

Cuadernos de Jupyter para aprender y practicar algoritmos de **aprendizaje supervisado** con
scikit-learn. Cada cuaderno explica un modelo paso a paso: se generan o cargan los datos, se
entrena el modelo, se hacen predicciones y se dibujan los resultados para ver qué está haciendo
el modelo por dentro.

## Contenido

| Cuaderno | Qué se ve |
|---|---|
| [`linear_regression.ipynb`](linear_regression.ipynb) | **Regresión lineal.** Se simulan 30 trabajadores con su salario según los años de experiencia, se entrena un `LinearRegression`, se obtienen la pendiente y el término independiente de la recta y se predicen salarios para nuevos valores. |
| [`decision_trees.ipynb`](decision_trees.ipynb) | **Árboles de decisión.** Un `DecisionTreeClassifier` sobre el conjunto de datos *Iris* (con el árbol dibujado y los cortes que elige sobre los pétalos) y un `DecisionTreeRegressor` sobre los mismos datos de salarios, siguiendo una predicción hoja a hoja y comparándolo con la regresión lineal: predicciones en escalera, sobreajuste en hojas pequeñas y ausencia de extrapolación. |

## Requisitos

- [mise](https://mise.jdx.dev/), que instala las versiones fijadas de Python (3.13) y
  [uv](https://docs.astral.sh/uv/) definidas en `mise.toml`.

Las dependencias (NumPy, pandas, SciPy, scikit-learn, Matplotlib, seaborn y JupyterLab) están en
`pyproject.toml` y sus versiones exactas en `uv.lock`.

## Puesta en marcha

```bash
mise install        # instala Python y uv
mise run install    # crea .venv e instala las dependencias (uv sync)
mise run lab        # abre los cuadernos en JupyterLab
```

Al entrar en la carpeta, mise activa automáticamente el entorno virtual `.venv`.

Sin mise, con uv instalado:

```bash
uv sync
uv run jupyter lab
```

## Estructura

```
.
├── linear_regression.ipynb   # regresión lineal
├── decision_trees.ipynb      # árboles de decisión (clasificación y regresión)
├── pyproject.toml            # dependencias del proyecto
├── uv.lock                   # versiones exactas de las dependencias
└── mise.toml                 # versiones de Python/uv y tareas (install, lab)
```
