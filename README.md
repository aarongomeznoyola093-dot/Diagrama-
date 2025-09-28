# Proyecto MASTER GARAGE

Este es el sistema para la gestión de refacciones y servicios.

## Diagrama de Casos de Uso

```mermaid
graph TD
    subgraph Sistema MASTER GARAGE
        UC1(Diagnosticar Falla de Vehículo)
        UC2(Gestionar Catálogo de Productos y Servicios)
        UC3(Gestionar Carrito de Compras)
        UC4(Finalizar Compra)
        UC5(Gestionar Cuenta)
        UC6(Iniciar Sesión)

        UC4 -->>|<<include>>| UC6
        UC3 -->>|<<include>>| UC6
        UC5 -->>|<<include>>| UC6
    end

    subgraph "Actores"
      Cliente
      Empleado
      Admin(Administrador)
    end


    Cliente --> UC1
    Cliente --> UC2
    Cliente --> UC3
    Cliente --> UC4
    Cliente --> UC5

    Empleado --> UC7(Registrar Venta en Tienda)
    Empleado --> UC8(Consultar Inventario)

    Admin --> UC9(Gestionar Catálogo)
    Admin --> UC10(Administrar Usuarios)
    Admin --> UC11(Ver Reportes de Venta)
