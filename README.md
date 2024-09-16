# Diagramas

```plantuml
@startuml
actor Cliente
actor Bibliotecário

Cliente --> (Emprestar Livro ou Revista)
Cliente --> (Devolver Livro ou Revista)
Cliente --> (Reservar Livro ou Revista)
Cliente --> (Cancelar Reserva)

(Bibliotecário) --> (Gerenciar Títulos) : <<include>>
(Bibliotecário) --> (Gerenciar Clientes) : <<include>>
(Bibliotecário) --> (Gerenciar Empréstimos e Reservas) : <<include>>
(Bibliotecário) --> (Controlar Compra de Novos Títulos) : <<include>>
(Bibliotecário) --> (Remover Títulos Ultrapassados ou Deteriorados) : <<include>>

(Reservar Livro ou Revista) --> (Notificar Disponibilidade de Título Reservado) : <<include>>
(Remover Títulos Ultrapassados ou Deteriorados) --> (Checar Se Título Está Ultrapassado ou Deteriorado) : <<include>>

@enduml
