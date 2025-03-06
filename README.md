-- Definimos una función pura que suma dos números enteros.
-- En programación funcional, una función pura siempre devuelve el mismo resultado
-- para los mismos argumentos y no tiene efectos secundarios.
sumar :: Int -> Int -> Int
sumar x y = x + y 

-- Definimos una función de orden superior.
-- Esta función recibe otra función como argumento y la aplica a cada elemento de la lista.
-- En programación funcional, las funciones de orden superior permiten una mayor reutilización del código.
aplicarFuncion :: (Int -> Int) -> [Int] -> [Int]
aplicarFuncion f lista = map f lista  -- Usamos 'map', una función clave en programación funcional.

-- Definimos una función pura que eleva un número al cuadrado.
-- Esta función no modifica variables globales ni depende de estados externos.
elevarCuadrado :: Int -> Int
elevarCuadrado x = x * x

-- Definimos una lista de números de ejemplo.
-- En programación funcional, las listas son estructuras inmutables.
numeros :: [Int]
numeros = [1, 2, 3, 4, 5]

-- Aplicamos la función elevarCuadrado a cada elemento de la lista usando la función de orden superior.
-- Esto demuestra la composición de funciones, una característica clave de la programación funcional.
resultado :: [Int]
resultado = aplicarFuncion elevarCuadrado numeros

-- Función principal que imprime los resultados en pantalla.
-- En Haskell, la ejecución del programa comienza en 'main', donde se manejan efectos de entrada y salida (IO).
main :: IO ()
main = do
    putStrLn "Lista de números original:"
    print numeros
    putStrLn "Lista de números elevados al cuadrado:"
    print resultado

