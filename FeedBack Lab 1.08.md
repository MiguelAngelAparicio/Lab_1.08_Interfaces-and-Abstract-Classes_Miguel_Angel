## Lab 1.08: Interfaces y Clases Abstractas (202302)

Your submitted this lab on  April 13th 2024.

**Operaciones BigDecimal**

Excelente implementación de las operaciones con  `BigDecimal`. Has seguido correctamente las directrices de la documentación para realizar redondeos y negaciones de los valores correctamente. Tu uso de  `setScale`  y  `RoundingMode.HALF_EVEN`  fue adecuado para lograr la precisión requerida. Aquí tienes un ejemplo de cómo podrías haber implementado uno de los métodos:

`1 2 3 4` `private static double bigDecimalRedondeo(BigDecimal bd){
    bd = bd.setScale(2, RoundingMode.HALF_EVEN);
    return bd.doubleValue();
}`

¡Sigue así!


**Sistema de inventario de automóviles**

Has hecho un buen trabajo definiendo la clase abstracta  `Car`  y sus subclases. Sin embargo, has incluido métodos  `setter`  que no estaban especificados en los requisitos. Aunque esto no es un problema mayor, y la lógica crucial está bien implementada, ten en cuenta leer las instrucciones detenidamente para cumplir con las especificaciones exactas. Por lo demás, ¡buen trabajo!


**Servicio de transmisión de video**

Tu implementación de las clases abstractas  `Video`,  `TvSeries`  y  `Movie`  está perfecta. Has definido las propiedades y comportamientos requeridos y las subclases cumplen con las reglas de negocio establecidas. Los métodos  `getInfo()`  proporcionan una salida clara y bien formateada de la información de los videos. ¡Muy bien hecho!


**Interfaz IntList**

Parece que hay un par de errores en tus implementaciones de  `IntArrayList`  y  `IntVector`. En  `IntArrayList`, el método  `add`  no aumenta correctamente el tamaño del array ni añade elementos de la manera esperada, lo cual será un problema al agregar más números. Por otro lado,  `IntVector`  maneja mejor el crecimiento dinámico del array. Aquí tienes un código de ejemplo que podría ayudarte a corregir  `IntArrayList`:

`1 2 3 4 5 6 7` `@Override
public void add(int number) {
    if (size == numbers.length) {
        numbers = Arrays.copyOf(numbers, size + size / 2);
    }
    numbers[size++] = number;
}`

Recuerda realizar pruebas exhaustivas para asegurarte de que tu código maneje correctamente todos los casos posibles.

**Explanación eficiencia IntArrayList vs IntVector**

No se ha proporcionado una explicación de cuándo  `IntArrayList`  sería más eficiente y cuándo  `IntVector`  sería más eficiente. Es importante incluir estas comparaciones en tu  `README.md`  para demostrar la comprensión de las estructuras de datos que has implementado. No realizado.