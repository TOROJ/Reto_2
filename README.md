# Reto_2: Modelar una situacion de la vida real.
Por medio de los diagramas tipo UML vistos en clase, vamos a modelar un evento de la vida cotidiana haciendo uso de clases y objetos vistos previamente. Como la situación a modelar era de libre elección opte por modelar a través de clases y objetos, una interacción de un bici-usuario, con una bicicleta .

## Relacion basica con el usuario y la bicicleta.

```mermaid
classDiagram
   class Bicicleta{
        +modelo : modelo A
        +vehiculo
        +manubrio
        +mover ()
        +frenar ()
        +girar()
    }
    class Bici-usuario{
    }
    Bicicleta <-- Bici-usuario : interaccion
```

    classDiagram
       class Bicicleta{
            +modelo
            +vehiculo
            +manubrio
            +mover ()
            +frenar ()
            +girar()
        }
        class Bici-usuario{
        }
        Bicicleta <-- Bici-usuario : interaccion

   **El usuario (clase) interactua con la bicicleta (otra clase)**

## Reación de la bicicleta y sus componentes

```mermaid
classDiagram
    class Bicicleta{
        +modelo : Modelo A
        +vehiculo
        +manubrio
        +mover ()
        +frenar ()
        +girar()
    }

    class vehiculo {
        +Frenos
        +Ruedas  : llantas 
        +Transporta()
    }
    class Modelo A{
        +Color    : Rojo
        +longitud : 1,67m
        +Tamaño   : 1,30m
    }
    vehiculo<|-- Bicicleta
    Bicicleta--|> Modelo A
    class manubrio {
        +manubrio
        + girar()
    }
    Bicicleta--* manubrio
```
    
    classDiagram
        class Bicicleta{
            +modelo
            +vehiculo
            +manubrio
            +mover ()
            +frenar ()
            +girar()
        }
    
        class vehiculo {
            +Frenos 
            +Ruedas 
            +Transporta()
        }
        class Modelo A{
            +Color 
            +longitud
            +Tamaño
        }
        vehiculo<|-- Bicicleta
        Bicicleta--|> Modelo A
        class manubrio {
            +manubrio
            + girar()
        }
        Bicicleta--* manubrio

   ** la bicicleta es un vehiculo, lo cual hereda sus caracteristicas y acciones. la bicicleta es un modelo 
    

