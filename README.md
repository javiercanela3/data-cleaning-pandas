#JAVIER CANELA

Tras importar la base de datos, es muy importante tener claro el objetivo del estudio que vamos a realizar pues en funcion de ello, requeriremos mas o menos precision en ciertas magnitudes. 

En las actividades más frecuentes (Natacion, Pesca, Deporte de tabla, Buceo y Baño), analizaremos las tendencias de los ataques, mirando similitudes entre ellas para intentar asi concluir cual es la mejor region para practicar estas actividades y en que epoca del año.

Empezamos viendo la cantidad de datos nulos que contiene la tabla (nos ayudamos de la funcion check_nan que hemos definido previamente).

Anulando duplicados, la tabla se reduce considerablemente pero aun así quedan muchas anomalias en la base de datos resultante

Normalizamos las diversas actividades que contiene la tabla, filtrando aquellas que no nos interesan para nuestro estudio.

Eliminamos tambien aquellas filas cuya informacion no podemos contrastar fiablemente por falta de autor de la investigacion o documento que certifiqu el caso

En nuestro caso, la especie de tiburon que ataca no es relevante por lo que podemos rellenarla con valores desconocidos sin problema.

Eliminamos todos las filas cuya informacion sobre el sexo desconocemos.

De la misma manera, como queremos hacer un estudio por Areas, todas aquellas en las que no este especificada el Area, tambien las descartaremos.

Eliminaremos todos los casos en los que el accidente ha tenido lugar en menos de 10 ocasiones en la misma area. Pues los consideramos como poco frecuentes y casos demasiado puntuales

Finalmente filtramos los outlayers de las variables numericas Year y Age eliminado todos aquellos datos que no pasen el test de Tukey.
