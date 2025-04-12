# Econometrics_project_2

* Folders:
  * Data - папка с данными проекта:
     * flats.json - данные после первичного парсинга в формате json
     * final_data_raw.csv - данные после первичной предобработки
     * final_df.csv - данные после вторичной предобработки
     * final_encoded_with_distance.csv - данные с наложение one-hot-encoding, а также добавлением расстояния
     * data_after_normality.csv - дата после процедуры нормализации остатков
     * FINAL_data.csv - итоговые данные, используемые в проектеerrors_normality.ipynb
       
 * Other stuff
  * Data_parsing.ipynb - парсер посредством selenium
  * Scrapy.zip - scrapy парсер
   
* Files:
  * data_preprocessing.ipynb - первичная предобработка данных
  * Data_preprocessing_2.ipynb - вторичная предобработка данных
  * Descriptive_statistics_and_visual_analysis.ipynb - первичный графический анализ, расчет основных статистик
  * multicoliarity.ipynb - блокнот с проверкой на мультиколлинеарность
  * errors_normality.ipynb - блокнот с проверкой остатков на нормальность, анализом выбросов методом DFFITS, (первичная спецификация) тестирование полу-логарифмической модели
  * homoscedasticity.ipynb - блокнот с проверкой на гомоскедастичность
  * Ramsey_test.ipynb - блокнот с проверкой на специификацию тестом Рамсея
