´´´mermaid
classDiagram
    class Doctor {
        - string nombre
        + Doctor(string n)
        + string obtenerNombre() const
        + void realizarRevision(Consulta&) const
    }

    class Paciente {
        - string nombre
        + Paciente(string n)
        + string obtenerNombre() const
        + void recibirRevision(Consulta&) const
    }

    class Consulta {
        - string fecha
        - string descripcion
        + Consulta(string f, string d)
        + string obtenerFecha() const
        + string obtenerDescripcion() const
    }

    Doctor --> Consulta 
    Paciente --> Consulta 
