# Введение в искусственный интеллект

Практические работы по курсу «Введение в ИИ» (ДВФУ, Прикладная математика и информатика): от базовых операций в NumPy и Pandas до классификации, регрессии, кластеризации и подбора гиперпараметров градиентного бустинга на данных с Kaggle.

![Python](https://img.shields.io/badge/Python-3-3776AB?logo=python&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?logo=pandas&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?logo=scikitlearn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-189FDD)
![Optuna](https://img.shields.io/badge/Optuna-2C5BB4)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?logo=jupyter&logoColor=white)

## Работы

| № | Ноутбук | Задача | Методы | Результат |
|---|---------|--------|--------|-----------|
| 1 | [`1_task.ipynb`](1_task.ipynb) | Пять прикладных мини-задач: детектор хайпа, «зрение беспилотника», фильтр плохих слов, генератор лиц, рекомендательная система | NumPy, Pandas, векторные операции, работа с текстом | — |
| 2 | [`2_task.ipynb`](2_task.ipynb) | Классификация: есть ли у респондента депрессия по анкете (возраст, нагрузка, сон, питание, удовлетворённость учёбой/работой) | заполнение пропусков, объединение парных признаков, XGBoost и Random Forest с учётом дисбаланса классов (`scale_pos_weight`) | XGBoost: **accuracy 0.95, ROC-AUC 0.988** |
| 3 | [`3_task.ipynb`](3_task.ipynb) | Регрессия: цена рюкзака по его характеристикам ([Kaggle Playground S5E2](https://www.kaggle.com/competitions/playground-series-s5e2)) | кодирование бинарных, порядковых и категориальных признаков, анализ корреляций, Random Forest | MAE 33.66, R² ≈ 0 — признаки почти не связаны с ценой, что подтверждает корреляционный анализ |
| 4 | [`4_task.ipynb`](4_task.ipynb) | Кластеризация дел невинно осуждённых в США | Label Encoding, StandardScaler, метод локтя, K-Means++ | 7 кластеров с интерпретацией: исторические дела XIX века, современные дела с ДНК-оправданием и др. |
| 5 | [`5_task.ipynb`](5_task.ipynb) | Регрессия: риск ДТП на участке дороги, ~518 тыс. строк ([Kaggle Playground S5E10](https://www.kaggle.com/competitions/playground-series-s5e10)) | генерация признаков, нативные категории XGBoost, подбор гиперпараметров Optuna, 5-fold CV, early stopping | **OOF RMSE 0.0561** |

## Данные

Датасеты в репозиторий не включены (см. `.gitignore`). Чтобы перезапустить ноутбук, положите нужный CSV рядом с ним:

| Ноутбук | Файлы |
|---|---|
| `2_task` | `final_depression_dataset_1.csv` |
| `3_task` | `backpack.csv` (train из Playground S5E2) |
| `4_task` | `Convictions_in_US.csv` |
| `5_task` | `train.csv`, `test.csv`, `sample_submission.csv` из Playground S5E10 |

## Запуск

```bash
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook
```

## Автор

Куценко Игорь — [@igr43](https://github.com/igr43)
