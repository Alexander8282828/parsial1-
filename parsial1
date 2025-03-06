import sys

# Credenciales de usuario (puedes mejorarlo con almacenamiento en archivo o base de datos)
USUARIO_REGISTRADO = "usuario123"
PIN_REGISTRADO = "1234"

# Saldo inicial
saldo = 1000.0  # Puedes cambiarlo a lectura de archivo si lo deseas

# Función para iniciar sesión
def iniciar_sesion():
    intentos = 3
    while intentos > 0:
        usuario = input("Usuario: ")
        pin = input("PIN (4 dígitos): ")

        if usuario == USUARIO_REGISTRADO and pin == PIN_REGISTRADO:
            print("\nInicio de sesión exitoso.\n")
            return True
        else:
            intentos -= 1
            print(f"Credenciales incorrectas. Intentos restantes: {intentos}\n")

    print("Demasiados intentos fallidos. Saliendo...")
    sys.exit()

# Función para mostrar el menú principal
def menu():
    print("\n--- Menú Principal ---")
    print("1. Consultar saldo")
    print("2. Retirar dinero")
    print("3. Salir")

# Función para consultar saldo
def consultar_saldo():
    print(f"\nTu saldo actual es: ${saldo:.2f}\n")

# Función para retirar dinero
def retirar_dinero():
    global saldo
    try:
        monto = float(input("\nIngrese el monto a retirar: $"))
        if monto <= 0:
            print("El monto debe ser mayor que cero.\n")
        elif monto > saldo:
            print("Saldo insuficiente.\n")
        else:
            saldo -= monto
            print(f"Retiro exitoso. Nuevo saldo: ${saldo:.2f}\n")
    except ValueError:
        print("Entrada inválida. Ingresa un número válido.\n")

# Programa principal
if _name_ == "_main_":
    if iniciar_sesion():
        while True:
            menu()
            opcion = input("Seleccione una opción: ")

            if opcion == "1":
                consultar_saldo()
            elif opcion == "2":
                retirar_dinero()
            elif opcion == "3":
                print("\nGracias por usar el sistema. ¡Hasta luego!\n")
                break
            else:
                print("\nOpción no válida. Inténtelo de nuevo.\n")
