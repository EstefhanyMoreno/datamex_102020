WEB PROJECT

Se realizarón dos notebooks diferentes, uno para API y otro para Web scraping.

Api Yahoo

Se decidió usar la API de yahoo ya que iba acorde a lo que se buscaba,
obtener información de los mercados financieros.

Durante la búsqueda se encontró una librería llamada yfinance con la cuál era muy sencillo
obtener la información deseada, por lo que se uso en este proyecto, incluyéndola dentro de 
una función en la que los parámetros son  los tickers de los que quieres obtener la información,
el périodo de información que buscas, en donde los valores permitidos son: 1d,5d,1mo,3mo,6mo,1y,
2y,5y,10y,ytd,max, y el último parámetro es save en dnde por default es False.

Se realizó una función de apoyo que devuelve el data frame, y se usó en otra función que devuelve
la gráfica de velas, solo si es que se guardó el CSV previamente, 
que muestra la fluctuación del precio en un día.


Web scrapping Reuters

Se decidió usar la página de Reuters para obtener el tipo de cambio del USD respecto a otras monedas,

Se trajó cada columna individualmente por su etiqueta y clase y se pasó a un data frame.

Hubo problemas técnicos con la columna de time por lo que se decidió eliminarla y sustituir ppor la hora 
en que se extrajó la información.
