# Taller_Constructores_this_metodos

Etapa 1. El objeto sin constructor
* Porque todavía no se le han dado valores al paquete. Como no tiene constructor, Java pone automáticamente unos valores por defecto: los textos quedan en null, el peso en 0.0 y asegurado en false.

Etapa 2. Constructor con parámetros y this
* Se imprime así porque el constructor guarda bien los datos usando this. Por eso aparece el código P-001, el destino Manizales, el peso 3.0 kg y que está asegurado: true.

Etapa 3. Sobrecarga de constructores y this(...)
*Se imprimen así porque los constructores ya tienen esos valores por defecto. El P-002 queda con destino Pereira y el P-003 queda con “Por asignar”. Los dos tienen 1.0 kg y no tienen seguro.

Etapa 4. Métodos con parámetros y valor de retorno
El costo se calcula según el peso de cada paquete. P1 cuesta 23.000, P2 5.000 y P3 12.500. Al sumar los tres, da un total de 40.500.

Etapa 5. Sobrecarga de métodos
Se imprimen 20.000 y 4.000 porque se está usando la tarifa de 4.000 por kilo. La tercera llamada no funciona porque el método no está hecho para recibir un texto (String).

## 10. Preguntas de comprensión

1. ¿Qué diferencias hay entre un constructor y un método? Menciona al menos tres.

2. ¿Por qué new Paquete() dejó de compilar en la Etapa 2? ¿Qué harías si la empresa necesitara seguir creando
paquetes sin datos?

3. ¿Qué ocurriría si en el constructor de Paquete escribieras peso = peso; en lugar de this.peso = peso;? ¿El
programa compilaría?

4. ¿Qué es la firma de un método y por qué el tipo de retorno no sirve para distinguir dos versiones
sobrecargadas?

5. ¿Qué ventaja tiene que los constructores abreviados de Paquete deleguen con this(...) en lugar de asignar los
atributos ellos mismos?

# Desarrollo.
 
 1. Un constructor sirve para crear y darle los valores iniciales a un objeto. En cambio, un método sirve para realizar alguna acción después de que el objeto ya fue creado. Además, el constructor tiene el mismo nombre de la clase y no lleva tipo de retorno.

 2. Dejó de funcionar porque al crear un constructor con parámetros, Java ya no crea automáticamente el constructor vacío. Si se necesitaran paquetes sin datos, agregaría un constructor Paquete() vacío.

 3. Sí, el programa compilaría, pero el atributo no recibiría correctamente el valor. peso = peso estaría usando el parámetro en los dos lados. Por eso se usa this.peso = peso, para diferenciar el atributo del parámetro.

 4. La firma es el nombre del método junto con la cantidad y los tipos de parámetros que recibe. El tipo de retorno no sirve para diferenciar métodos porque Java necesita saber cuál ejecutar basándose en los parámetros.

 5. La principal ventaja es que no toca repetir el mismo código. Un constructor puede llamar al otro y aprovechar lo que ya está programado, haciendo el código más corto y ordenado.

 
