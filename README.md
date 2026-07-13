# Algoritmos-q1
este github se creo para la clase de algoritmos de la uk
CASO 3: CONTROL DE STOK DE PRODUCTOS 
este algoritmo resuelve la necesidad de una tienda auditando el inventario de sus productos. El sistema solicita al usuario ingresar la cantidad total  de articulos (N) y el stock actual de cada producto.almacenando estos datos en un arreglo.se valida estrictamente  que ninguna cantidad sea negativa. (valores mayores o iguales a cero) se realizan 2 operaciones principales sumando cada elemento de la coleccion y realiza una busqueda detectando si existe producto en stok. mostrando al final en pantalla el total de inventario acomulado.
PSEUDOCODIGO COMPLETO
Algoritmo ControlStockProductos
    // VARIABLES
    // Se definen los identificadores y sus tipos de datos
    VARIABLES
        N, i, stockTotal, stock : ENTERO
    
    // SOLICITUD DEL TAMAÑO DEL ARREGLO
    ESCRIBIR "Ingrese la cantidad total de productos (N): "
    LEER N

    // DECLARACIÓN DEL ARREGLO (Indexado de 1 a N)
    ARREGLO[N] DE TIPO ENTERO como nombre: inventario

    // INICIALIZACIÓN DE ACUMULADORES (Antes del ciclo)
    stockTotal <- 0

    // CICLO ÚNICO: LECTURA, SUMATORIA Y DETECCIÓN EN UN SOLO RECORRIDO
    PARA i <- 1 HASTA N CON PASO 1 HACER
        ESCRIBIR "Ingrese el stock para el producto en la posicion ", i, ": "
        LEER stock
        
        // Guardar el valor en el arreglo
        inventario[i] <- stock
        
        // Operación 1: Acumulación del stock total
        stockTotal <- stockTotal + stock
        
        // Operación 2: Búsqueda y reporte inmediato si el stock es cero
        SI stock = 0 ENTONCES
            ESCRIBIR "-> Producto agotado detectado en la posicion del arreglo: ", i
        FINSI
    FINPARA

    // IMPRESIÓN DE RESULTADOS FINALES (Después del ciclo)
    ESCRIBIR "==========================================="
    ESCRIBIR "El stock total disponible en la tienda es: ", stockTotal
    ESCRIBIR "==========================================="

FINALGORITMO
