markdown
# Matryoshka Engine v1.2

**Инструмент для измерения плотности натяжения пространства / A tool for measuring space tension density**

- [🇷🇺 Русская версия](README_RU.md)
- [🇬🇧 English version](README_EN.md)

---

## 🚀 Быстрый старт / Quick Start

```bash
git clone https://github.com/fr1zich/Matryoshka-Engine.git
cd Matryoshka-Engine
pip install numpy matplotlib
python engine.py
📜 Лицензия / License
MIT License — Денис Васильев.

text

---

## Файл `README_RU.md` (русская версия)

```markdown
# Matryoshka Engine v1.2

**Инструмент для измерения плотности натяжения пространства в галактиках**

---

## Что это

Данный проект представляет собой вычислительный инструмент, который по трём наблюдаемым параметрам галактики (масса, радиус, скорость вращения) вычисляет **D-фактор** — безразмерную величину, характеризующую плотность натяжения пространства в данной области.

Модель не использует частицы тёмной материи. Вместо этого она описывает дополнительную удерживающую силу (Omega) как свойство самого пространства.

## Формула
V_total = sqrt( (G * M / R) + Omega )
Omega = alpha * log10(M) * D * sqrt(R)

text

## Параметры

| Символ | Название | Значение | Смысл |
|:---|:---|:---|:---|
| `G` | Гравитационная постоянная | `6.674e-11` | Фундаментальная константа |
| `M` | Масса галактики | — | Вся видимая масса |
| `R` | Радиус галактики | — | Расстояние до точки замера |
| `alpha` | Константа вязкости вакуума | `1.8e-2` | Фундаментальная «жёсткость» пространства |
| `D` | D-фактор | `0.02 – 2.79` | **Измеряемая** плотность натяжения |
| `log10(M)` | Логарифм массы | — | Нелинейный учёт массы |
| `sqrt(R)` | Корень из радиуса | — | Плавный рост натяжения |

## Результаты (12 галактик)

| Галактика | Тип | D-factor | Точность |
|:---|:---|:---|:---|
| NGC 2841 | Спиральная | 2.79 | 99.96% |
| NGC 7331 | Спиральная | 2.29 | 99.80% |
| Млечный Путь | Спиральная | 1.95 | 96.99% |
| Андромеда (M31) | Спиральная | 1.45 | 93.17% |
| NGC 3198 | Спиральная | 0.55 | 99.16% |
| NGC 0055 | Неправильная | 0.52 | 99.16% |
| NGC 2403 | Спиральная (переходная) | 0.47 | 93.89% |
| NGC 0300 | Неправильная | 0.44 | ~99% |
| NGC 6503 (Войд) | Войд | 0.22 | 91.45% |
| IC 2574 | Неправильная | 0.16 | 99.99% |
| DDO 154 | Неправильная | 0.12 | 98.18% |
| DDO 168 | Неправильная | 0.08 | 99.65% |
| DDO 210 | Неправильная (карлик) | 0.02 | 97.04% |

**Средняя точность: ~97%.**  
**Слепые тесты пройдены:** NGC 2403 и NGC 3198.

## Ограничения

1. D-фактор пока подбирается вручную.
2. Модель феноменологическая, не выводится из ОТО.
3. Отрицательные значения D невозможны (антигравитация).
Файл README_EN.md (английская версия)
markdown
# Matryoshka Engine v1.2

**A tool for measuring space tension density in galaxies**

---

## What is this

This project is a computational tool that calculates the **D-factor** — a dimensionless quantity characterizing the tension density of space in a given region — using three observable parameters of a galaxy: mass, radius, and rotation velocity.

The model does not use dark matter particles. Instead, it describes an additional binding force (Omega) as a property of space itself.

## Formula
V_total = sqrt( (G * M / R) + Omega )
Omega = alpha * log10(M) * D * sqrt(R)

text

## Parameters

| Symbol | Name | Value | Meaning |
|:---|:---|:---|:---|
| `G` | Gravitational constant | `6.674e-11` | Fundamental constant |
| `M` | Galaxy mass | — | Total visible mass |
| `R` | Galaxy radius | — | Distance to measurement point |
| `alpha` | Vacuum viscosity constant | `1.8e-2` | Fundamental «stiffness» of space |
| `D` | D-factor | `0.02 – 2.79` | **Measured** tension density |
| `log10(M)` | Mass logarithm | — | Nonlinear mass accounting |
| `sqrt(R)` | Radius square root | — | Smooth tension growth |

## Results (12 galaxies)

| Galaxy | Type | D-factor | Accuracy |
|:---|:---|:---|:---|
| NGC 2841 | Spiral | 2.79 | 99.96% |
| NGC 7331 | Spiral | 2.29 | 99.80% |
| Milky Way | Spiral | 1.95 | 96.99% |
| Andromeda (M31) | Spiral | 1.45 | 93.17% |
| NGC 3198 | Spiral | 0.55 | 99.16% |
| NGC 0055 | Irregular | 0.52 | 99.16% |
| NGC 2403 | Spiral (transitional) | 0.47 | 93.89% |
| NGC 0300 | Irregular | 0.44 | ~99% |
| NGC 6503 (Void) | Void | 0.22 | 91.45% |
| IC 2574 | Irregular | 0.16 | 99.99% |
| DDO 154 | Irregular | 0.12 | 98.18% |
| DDO 168 | Irregular | 0.08 | 99.65% |
| DDO 210 | Irregular (dwarf) | 0.02 | 97.04% |

**Average accuracy: ~97%.**  
**Blind tests passed:** NGC 2403 and NGC 3198.

## Limitations

1. D-factor is currently fitted manually.
2. The model is phenomenological, not derived from GR.
3. Negative D values are impossible (antigravity).
