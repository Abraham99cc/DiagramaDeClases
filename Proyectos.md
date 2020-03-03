
```mermaid
classDiagram
      Proyecto o-- "1..*"Ciclo :{oredered}
      Ciclo o-- "4" Fase : {ordered}
      Ciclo -- Ejecutable
      Fase o-- "1..*" Iteracion : {ordered}
      Iteracion -- "1..*"Artefacto : produce
      Artefacto <|-- Documento
      Artefacto <|-- Software
      Iteracion o-- "1..*" Actividad
      Actividad "0..*" o-- "0..*" Recurso
      Recurso <|-- Humano
      Recurso <|-- Material

      class Ciclo{
        }

      class Proyecto{
          -nombre : String
          - / avance : Float
        }
      class Ejecutable{
          -bytes
      }
      class Fase{
          tipo : TipoFase
      }
      class TipoFase{
          inicio
          elaboracion
          construccion
          transicion
      }
      class Iteracion{
          -comienzo : Date
      }
      class Artefacto{
      }
      class Documento{
          -nombre : String
          -unbicacion
      }
      class Software{
          -bytes
      }
      class Actividad{
          -duracion : Integer
          avance : Float
      }
      class Recurso{
      }
      class Humano{
          -nombre : String
      }
      class Material{
          -inventario : String
      }

    
```
  