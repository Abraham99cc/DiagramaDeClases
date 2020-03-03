Biblioteca
===

```mermaid
classDiagram
    Libro "obra" -- "autor" Autor
    Copia "ejemplar" -- "libro" Libro
    Socio "lector" -- "0..3" Copia : Prestamo
    Multa "sancion" -- "sancionado" Socio : recibe
    Copia :: Prestamo
    Socio :: Prestamo
    
    
    class Libro{
                -Título : String
                -editorial : String
                -year : Integer
                -tipo : Genero
            }
    class Autor{
                -Nombre : String
                -nacionalidad : String
                -fechaNacimiento : Date
            }
    class Copia{
                -referencia : Integer
                -estado : EstadoCopia
            }
    class Socio{
                -numero : Integer
                -nombre : String
                -direccion : String
                -telefono : String
            }
    class Multa{
                -inicio : Date
                -fin : Date
            }
    
    class  Género {
                <<enumeration>>
                novela
                teatro
                poesia
                ensayo
            }

    class EstadoCopia{
                <<enumeration>>
                prestado
                retraso
                biblioteca
                reparacion
            }
    class Prestamo{
        -inicio : Date
        -fin : Date
    }


```