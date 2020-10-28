Data cleaning project

Se comenzó por explorar la cantidad de filas y columnas que habían
Después se revisaron aquellas filas en las que todas sus columnas eras valores nulos y se procedío a borrarlas (eso con la ayuda de la columna case number)
Con eso las filas se redujeron a más de la mitad

Después se procedió a examinar columna por columna

La primera columna fue date, se aplico el formato correspondiente para date time y se omitieron aquellos que no cumplian con el formato con un try and except
Las que no cumplían el formato fue porque contenían str o caracteres especiales para lo cuál con el uso de regex se intento homegnizar

La siguiente columna fue year para el cuál se decidío cortar el strg y tomar los últimos 4 caracteres para que cumplieran con el formato 'aaaa'

Para la columna type se remplazaron los valores nulos por 'Unknown' y se corrigieron faltas de ortografía

Para la columna country se decidio borrar las filas nulas ya que se consideró que country era una columna importante porque de ella dependían otras 3,
se transformó todo a upper case y se corrigieron la presencia de caracteres extraños o espacios de más

Para las columnas Area y Location si había valores nulos se sustituyeron por Country es title case y se arreglaron faltas de ortografía

En la columna activity se creo otra columna llamada activity short en donde con ayuda de regex se extrajeron las palabras que terminaran con -ing 
ya que son esas palabras las que denotaban la actividad


Para el name se cambiaron los nulos por valores 'Unknown' y se cambió el texto por title case

En la columna sex en las filas con valores nulos se asignó con un random choice F o M 

En la columna fatal se cambió todo a upper case y se mantuvieron los valores solo entre Y o N

En la columna Injury se utiliz regex para homogenizar los resultados en su mayor parte, buscando por ejemplo leg y remplazando todas las filas
que tuvieran leg por leg damage, así para muchos otros casos

Para la hora se cambió la h por :, se quitaron caracteres extraños y para str que fueran mayores a 4 se cortaban para que cumpleiran ese criterio

En la columna species se utilizo un regex para que solo permaneciera como información la palabra shark y lo que estuviera antes (se tomo en cuenta el espacio tambien)

En la columna Investigator y pdf no se hizó ningún cambio

Las columnas case number1 y 2 se decidieron elimnar por que eran parecidas en la mayoría absoluta a case number

Tambien se eliminó la columna href formula ya que era igual a a href

No se realizó ningún cambio a la columna original order




