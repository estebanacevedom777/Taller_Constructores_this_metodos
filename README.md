# Taller_Constructores_this_metodos

Etapa 1. El objeto sin constructor
* Porque todavía no se le han dado valores al paquete. Como no tiene constructor, Java pone automáticamente unos valores por defecto: los textos quedan en null, el peso en 0.0 y asegurado en false.

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

 
