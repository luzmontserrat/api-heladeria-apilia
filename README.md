# Heladería Via Apilia - API

Esta especificación de API proporciona acceso a la Heladería Via Apilia, donde se pueden consultar los gustos de helado disponibles y realizar pedidos.

## Descripción

La **API de la Heladería Via Apilia** permite a los usuarios interactuar con el sistema de pedidos de la heladería. A través de esta API, puedes:

- Consultar los gustos de helado disponibles.
- Realizar y gestionar pedidos.
- Obtener información sobre los potes de helado en un pedido específico.

## Endpoints

### Consultar pote de helado en un pedido

- **GET** `/pedidos/{idPedido}/potes/{idPote}`
  - **Descripción:** Obtiene la información de un pote específico dentro de un pedido.
  - **Parámetros:**
    - `idPedido`: El ID del pedido que se desea consultar (requerido).
    - `idPote`: El ID del pote de helado dentro del pedido (requerido).
  - **Respuestas:**
    - `200`: Éxito, devuelve la información del pote solicitado.
    - `404`: No se encontró el pedido o el pote.

### Eliminar pote de un pedido

- **DELETE** `/pedidos/{idPedido}/potes/{idPote}`
  - **Descripción:** Elimina un pote de helado específico dentro de un pedido.
  - **Parámetros:**
    - `idPedido`: El ID del pedido (requerido).
    - `idPote`: El ID del pote que se desea eliminar (requerido).
  - **Respuestas:**
    - `204`: Éxito, el pote ha sido eliminado.
    - `404`: No se encontró el pedido o el pote.

