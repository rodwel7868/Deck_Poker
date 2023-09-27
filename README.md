# Deck_Poker
Cartas de Poker
Se realiza dos paqueterías lógicas en la cual en una de ellas se coloca la paquetería LogicaCartas serializa la clase cartas en la cual se realiza de las variables (atributos) privadas de las cartas las especificaciones (palo, color y valor) de manera String.
Se realiza el método público de cartas colocando el this.atributos antes mencionado, y en paréntesis los atributos con su cadena String correspondiente.
Se realiza los métodos get y set de cada uno de los atributos retornando el atributo mencionado en el método cartas, ejemplo (this.palo).
Al final de este paquete se coloca un @Override este método va a retornar el valor de las variables concatenado con un espacio correspondiente para evitar que se empalme la información.
En la otra paquetería con la clase llamada deds se importa los atributos de la primera paquetería de igual manera se importa la librería a utilizar como son (List, collection y ArrayList).
Se realiza el método privado estático List<cartas> Cartas, el cual va realizar la función del atributo para en compañía del ArrayLis que se manda llamar posteriormente creara el listado, posteriormente se visualiza el método main el cual indica que es la paquetería principal la cual va a mandar correr en primer lugar el programa.
Con las variables palo y valor se coloca la información que obtendrá cada una de las variables, ejemplo (palo = (diamante, corazón, etc.), en lo que valor mostrará (A, 2, 3 etc.).
Se coloca un for con la variable pal String se utiliza dentro de este mismo, pero en un if el cual marca las cartas como trebo y pica dentro de otro for el cual sirve como contador e incrementador el cual funciona como el contador de las cartas en mazo y seleccionara las cartas en mesa.
La función shufffle a la par con collection se carga de mezclar las cartas del mazo.
El método hand se utiliza un if el cual removerá las cartas y mostrara las seleccionadas de igual manera mostrara la cantidad de cartas las cuales se encuentran en el mazo de igual manera se cuenta con un contador el cual mostrara el resultado de las cinco cartas siempre y cuando sea mayor o igual a cinco.
Método pick cuenta con un if a la par con Math.random() es el encargado de seleccionar las cartas al sin tener alguna secuencia siempre y cuando sean mayor a cero.
