EJERCICIO 1
def sumando(num):
    sum = 0
    for numero in num:
        sum += numero
    return sum

num = [1, 2, 3, 4, 5]
Total= sumando(num)
print(f"Total de la suma es: {Total}")

EJERCICIO 2
def fib(n):
    # Lista para almacenar la sucesión
    fibonacci = [0, 1]  # Los dos primeros números de la sucesión
    for _ in range(2, n):
        # Agregar el siguiente número como la suma de los dos anteriores
        fibonacci.append(fibonacci['1] + fibonacci[-2])
    return fibonacci
n = 15

resultado = fib(n)
print(f"Los primeros {n} números de la sucesión de Fibonacci son: {resultado}")


EJERCICIO 3
def elementos(lista):
    return list(set(lista))

lista = [1, 1, 2,2, 3, 4, 4, 5, 6, 6, 7, 8, 8]

resultado = elementos(lista)
print(f"Lista de elementos únicos: {resultado}")

EJERCICIO 4
def almacenar_productos():
    productos = {}  # Diccionario para almacenar productos y precios
    while True:
        # Solicitar el nombre del producto
        producto = input("Ingrese el nombre del producto (o escriba 'salir' para terminar): ").strip()
        if producto.lower() == 'salir':
            break
        
        # Solicitar el precio del producto
        try:
            precio = float(input(f"Ingrese el precio del producto '{producto}': "))
        except ValueError:
            print("Por favor, ingrese un precio válido.")
            continue
        
        # Agregar al diccionario
        productos[producto] = precio
    
    return productos
    
productos_almacenados = almacenar_productos()

print("\nProductos y precios registrados:")
for producto, precio in productos_almacenados.items():
    print(f"{producto}: ${precio:.2f}")

EJERCICIO 5
data = {
    'Ciudad': ['Nueva York', 'Los Ángeles', 'Nueva York', 'Chicago'],
    'Ventas': [100, 150, 200, 50]
}
ventasciudad = {}


for ciudad, venta in zip(data['Ciudad'], data['Ventas']):
    if ciudad in ventasciudad:
        ventasciudad[ciudad] += venta
    else:
        ventasciudad[ciudad] = venta


print("Ventas por ciudad:")
for ciudad, suma in ventasciudad.items():
    print(f"{ciudad}: {suma}")
