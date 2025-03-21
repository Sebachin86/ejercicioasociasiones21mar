```mermaid
classDiagram
    class Hotel {
        - string nombre
        - vector~Habitacion~ habitaciones
        - vector~Cliente*~ clientes
        + Hotel(string nombre)
        + Hotel()
        + void agregarHabitacion(int numero, string tipo)
        + void registrarCliente(Cliente* cliente)
        + void mostrarInfo()
    }

    class Habitacion {
        - int numero
        - string tipo
        - bool ocupada
        - Cliente* cliente
        + Habitacion(int numero, string tipo)
        + Habitacion()
        + int getNumero()
        + string getTipo()
        + bool estaOcupada()
        + void ocupar(Cliente* cliente)
        + void desocupar()
    }

    class Cliente {
        - int id
        - string nombre
        + Cliente(int id, string nombre)
        + Cliente()
        + int getId()
        + string getNombre()
    }
Habitacion --> Hotel
Cliente --> Hotel
```
