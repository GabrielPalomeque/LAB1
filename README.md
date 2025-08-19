#TABLA DE COMANDOS

| #  | Command          | Use                                                  |
| -- | ---------------- | ---------------------------------------------------- |
| 1  | ls               | List of files and directories                        |
| 2  | ls -l            | Shows files in long format (permissions, size, date) |
| 3  | cd               | Change directory                                     |
| 4  | pwd              | Print work directory (shows current path)            |
| 5  | sudo             | Run a command as superuser                           |
| 6  | sudo su          | Switch to root user                                  |
| 7  | mkdir            | Create a directory                                   |
| 8  | touch            | Create empty file                                    |
| 9  | sudo apt update  | Update package lists                                 |
| 10 | sudo apt upgrade | Upgrade installed packages                           |
| 11 | sudo apt install | Install repositories or packages                     |
| 12 | tree             | Shows directory tree (requires installation)         |
| 13 | rm               | Remove a file                                        |
| 14 | rm -r            | Remove directory and contents                        |
| 15 | mv               | Move or rename files/directories                     |
| 16 | cp               | Copy files or directories                            |
| 17 | chown            | Change ownership of files                            |
| 18 | chmod            | Change file permissions                              |
| 19 | adduser          | Adds a new user                                      |
| 20 | usermod          | Modify existing user settings                        |
| 21 | gpasswd          | Change group configurations                          |
| 22 | cat, nano, gedit | View or edit text files                              |
| -- | -----------------| -----------------------------------------------------|
| 23 | clear            | Clear the terminal screen                            |
| 24 | man              | Show manual/help of a command                        |
| 25 | echo             | Display a message or text in terminal                |
| 26 | head             | Show the first lines of a file                       |
| 27 | tail             | Show the last lines of a file                        |    
| 28 | history          | Display previously used commands                     |



#Ejercicio 1
mkdir -p "ice cream 2023/water flavors"/{Cinnabon,apple,pineaple}"ice cream 2023/milk flavors"/{chocolate,cappucino}
tree
#Ejercicio 2
echo azul>color 
mkdir colors 
mv color/colors 
echo verde >> colors/color 
cat colors/color
#Ejercicio 3
mkdir "student registry"
echo Gabriel > name
cp name "student registry"
gedit "student registry/name"
echo "Palomeque" >"student registry/name"
#2da seccion punto 1
sudo grouppadd Distribution
sudo useradd -m -G Distribution,sudo Company
sudo useradd -m -G Distribution Engineer
sudo useradd -m -G Distribution Operator
getent group Distribution
#2da seccion punto 2
mkdir -p "Designed tasks"/{"Maintenance","Production Line","Fixes","Costs"}
echo "Maintenance - Friday" > "Designed tasks/Maintenance/dates"
echo "Maintenance Line - Monday to Thursday" > "Designed tasks/Fixes/dates"
echo "Costs - at the end of the month" > "Designed tasks/Costs/dates"
echo -e "Canned Beans\nCanned Tuna\nCanned Corn" >"Designed tasks/Products"
tree "Designed tasks"
#2da seccion punto 3
sudo useradd -m Supervisor
sudo usermod -aG Distribution Supervisor
sudo chown -R Supervisor "Designed tasks"
sudo chmod -R 770 "Designed tasks"
ls -l
groups Supervisor 


# 1. Suma de n números
def suma_numeros():
    n = int(input("¿Cuántos números quieres sumar? "))
    total = 0
    for i in range(n):
        num = int(input(f"Ingresa el número {i+1}: "))
        total += num
    print("La suma total es:", total)


# 2. Invertir un número
def invertir_numero():
    num = input("Ingresa un número: ")
    invertido = num[::-1]   # Invierte la cadena
    print("El número invertido es:", invertido)


# 3. Pedir datos personales y mostrar mensaje
def datos_personales():
    nombre = input("Ingresa tu nombre: ")
    edad = input("Ingresa tu edad: ")
    profesion = input("Ingresa tu profesión: ")
    print(f"Hola {nombre}, tienes {edad} años y eres {profesion}.")


# 4. Pedir x números y devolver solo los únicos
def numeros_unicos():
    x = int(input("¿Cuántos números vas a ingresar? "))
    numeros = []
    for i in range(x):
        num = int(input(f"Ingresa el número {i+1}: "))
        numeros.append(num)
    unicos = list(set(numeros))  # Quita repetidos
    print("Los números únicos son:", unicos)


# Menú para probar cada opción
def menu():
    while True:
        print("\nElige una opción:")
        print("1. Sumar n números")
        print("2. Invertir número")
        print("3. Datos personales")
        print("4. Números únicos")
        print("5. Salir")
        
        opcion = input("Opción: ")

        if opcion == "1":
            suma_numeros()
        elif opcion == "2":
            invertir_numero()
        elif opcion == "3":
            datos_personales()
        elif opcion == "4":
            numeros_unicos()
        elif opcion == "5":
            print("Adiós 👋")
            break
        else:
            print("Opción no válida, intenta de nuevo.")


# Ejecutar el programa
menu()
