# Econometrics_project_2

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Scrapy](https://img.shields.io/badge/scrapy-%2360a839.svg?style=for-the-badge&logo=scrapy&logoColor=d1d2d3)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
[![Built with Statsmodels](https://img.shields.io/badge/Built%20with-Statsmodels-orange)](https://www.statsmodels.org/)

![Plotly Dash](https://img.shields.io/badge/plotly-3F4F75.svg?style=for-the-badge&logo=plotly&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)

## Project structure
* Folders:
  * Data - папка с данными проекта:
    * flats.json - данные после первичного парсинга в формате json
    * final_data_raw.csv - данные после первичной предобработки
    * final_df.csv - данные после вторичной предобработки
    * final_encoded_with_distance.csv - данные с наложение one-hot-encoding, а также добавлением расстояния
    * data_after_normality.csv - дата после процедуры нормализации остатков
    * FINAL_data.csv - итоговые данные, используемые в проекте errors_normality.ipynb и далее
       
 * Parser - папка с инструментами для парсинга данных о квартирах с ЦИАН
	  * Data_parsing_temp.ipynb - парсер посредством selenium
	  * Scrapy.zip - scrapy парсер, результаты от него
   
* Files:
  * data_preprocessing.ipynb - обработка данных
  * Descriptive_statistics_and_visual_analysis.ipynb - первичный графический анализ, расчет основных статистик
  * multicoliarity.ipynb - блокнот с проверкой на мультиколлинеарность
  * errors_normality.ipynb - блокнот с проверкой остатков на нормальность, анализом выбросов методом DFFITS, (первичная спецификация) тестирование полу-логарифмической модели
  * homoscedasticity.ipynb - блокнот с проверкой на гомоскедастичность
  * Ramsey_test.ipynb - блокнот с проверкой на специификацию тестом Рамсея
  * Estimation.ipynb - блокнот с оценкой модели и доп. проверки
  * Quantile_regression.ipynb - блокнот с построением квантильной регрессии
  * requirements.txt - файл с зависимостями для запуска кода



## Run locally
### Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install dependencies.

```bash
pip install requirements.txt
```
### Notebooks
`.ipynb` files can be run as usual Jyputer notebooks.
### Parser
The main, in production is a [Scrapy](https://docs.scrapy.org/en/latest/intro/tutorial.html) parcer:
* unzip the /Parser/Scrapy.zip/
* locate the spider in the folder: `cd /folder_path/cian_scraper/cian_scraper/spiders/`
* run: `scrapy crawl flats` (use appropriate flags to save the files)