# Diagramas de flujo

Lo que se hace en estos diagramas al momento de realizar el diseño es trasladar los requerimientos del brief a elementos tangibles o componentes.

***Ejemplo 1*** Equivalentes entre requerimientos del brief y componentes o secciones de una página.

| Requerimientos | Sección |
| -------------- | ------- |
| Dar a conocer sus productos | Menú y promociones |
| Aumentar la presencia en línea | Redes sociales |
| Hacer pedidos online | Pedidos |
| Dar a conocer su marca | Contacto y sucursales |

## Diagrama de Flujo

Primero se debe estructurar en forma de árbol o cuadro sinóptico los componentes.

***Ejemplo 2*** Árbol del ejemplo 1

~~~tree
Home
|
├ Menú
|  |
|  ├ Promociones
|  └ Categorías
|       |
|       ├ Hamburguesas 
|       ├ Acompañamientos
|       ├ Bebidas
|       └ Postres
|
├ Pedidos
|  |
|  ├ Resumen
|  ├ Datos de envío
|  └ Confirmación
|
├ Contacto
|  |
|  └ Sucursales
|
└ Páginas externas
   |
   ├ * Instagram
   ├ * TikTok
   ├ * Facebook
   └ * Pagos
~~~

Después se estructura el flujo del funcionamiento, utilizando recueadros para representar instrucciones y rombos para representar decisiones como en el siguiente ejemplo:

~~~flow
┌─────────┐
│1. Inicio│◄───────────────────────────────────────────────────────────┐
└────┬────┘                                                            │
     │                                                                 │
     ▼                                                                 │
┌───────┐  ┌────────────────────────┐  ┌───────────────────┐           │
│2. Menu├─►│3. Detalles del producto├─►│4. Añadir al pedido├─┐         │
└───────┘  └────────────────────────┘  └───────────────────┘ │         │
                                                             ▼         │
                                                      ┌─────────────┐  │
                                                      │5. Ver pedido│  │
                                                      └──────┬──────┘  │
                                                             │         │
                                                             ▼         │
                    ┌─────────────────────────────┐  ┌───────────────┐ │
    ┌────────────►┌─┤7. Diligenciar datos de envío│◄─┤6. Pagar pedido│ │
    │             │ └─────────────────────────────┘  └───────────────┘ │
 ┌──┴──┐          ▼                                                    │
 │Error│          #                                                    │
 └─────┘        #   #                                                  │
    ▲  No     # Datos #    Sí   ┌───────────────────┐                  │
    └────── #  válidos  # ────► │Plataforma de pagos│                  │
     ▲        #       #         └─────────┬─────────┘                  │
     │          #   #                     │                            │
     │            #                       ▼                            │
     │                                    #                            │
     │                                  #   #                          │
     │                        No      # Pago  #     Sí  ┌────────────┐ │
     └───────────────────────────── #  exitoso  # ─────►│Confirmación├─┘
                                      #       #         └────────────┘
                                        #   #
                                          #
~~~  
