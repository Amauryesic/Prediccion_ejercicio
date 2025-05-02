He puesto todo los comentarios necesarios para entender la EDA y el model_selection directament en los notebooks. Abajo es solo la conclusion de la EDA.





- Se puede ver que tenemos datos faltantes y que hay que limpiarlo (caso de los "?")
- Tenemos que tomar en cuenta que es un dataset de Estados Unidos y que el mundo laboral es diferente del nuestro y asi tenemos valores extranas con la edad o el numero de horas trabajadas.
- Con Capital-gain y Capital-loss se puede ver que la moyoria de la gente no inverten en el mercado pero hay algunas personas que ganan mas de 50K que inverten mucho. Hemos creado una variable P&L (profit and loss) para juntar las dos columnas.
- Tenemos variables categorias con redundancias asi hemos eliminido alguna para no tener problema de multicolinealidad. 
- visualmente, las variables age, hour-per-week y educational-num parecen aportar mucha informacion a nuestra target Income.
- Con las variables catgoricas, una pareja tiene mas suerte de tener un sueldo de mas de 50K asi la variable relationship aporta informacion.
- No tenemos un sesgo con la raza y el genero
- Cosa interesente es la correlacion entre una persona qui tiene una gran apetencia con la inversion y un sueldo importante.

- Edad : he mos visto que cuanto mayor mas una persona tiene probabilidad de tener mas de 50K
- Educational-num : hemos eliminado educational para no tener redundancia. Hemos visto que salario esta correlado al pretigio.
- Relationship : hemos decidido de guardar relationship y eliminar marrital-status para no tener redundancia. Una pareja tiene mas probabilidad de tener un sueldo de mas de 50K
- Gender y Race : no hay parece haber tan sesgos en nuetro dataset aunque esta debalanceado. No aportan mucho informacion pero se podra guardarlos en nuestro model_selection.
- Continent : misma cosa con el continente porque tenemos una surrepresentatividad de la gente de origen de america de norte asi no es tan interesente guardarla.
-P&L : la variable P&L es muy interesente y se puede ver que las personas con un P&L de zero son los que no tienen un sueldo mayor a 50K. Las personas que tienen un sueldo de mas de 50K parecen ser los que tienen una apetencia a invertir. Son tambien personas que no le duele mucho perder dinero (P&L negativo pero mas de 50)
- Hours-per-week : hay una correlacion positiva entre en nombre de horas trabajadas y el nivel de sueldo pero no tan alta. 

