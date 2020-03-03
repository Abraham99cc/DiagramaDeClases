Viajes
===

```mermaid
classDiagram
    Vuelo "0..*" -- "1" Avion : es realizado
    Persona "pasajero" -- "0...*" Vuelo : viaja
    Vuelo :: Billete
    Persona :: Billete
    
    
    class Vuelo{
                -plazas : Integer
                -fecha : Date
            }
    class Billete{
                -asiento : Integer
            }
    class Avion{
                -modelo : String
                -capacidad : Integer
            }
    class Persona{
                -nombre : String
                -apellidos : String
                -fechaNacimiento: Date
                -sexo : Genero
            }
    class  Género {
                <<enumeration>>
                -hombre
                -mujer
            }


```