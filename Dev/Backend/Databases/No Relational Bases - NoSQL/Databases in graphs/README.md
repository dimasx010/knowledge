# Base de datos de Graficos - NoSQL

Las bases de datos en grafos forman parte la familia NoSQL. Estos modelos están ganando mucho interés entre el público gracias a sus características. Cuentan con múltiples herramientas de modelado de datos.

Las bases de datos de gráficos están diseñadas expresamente para almacenar relaciones y navegar por ellas. Las relaciones son ciudadanos de primera clase en las bases de datos de gráficos, y la mayor parte del valor de las bases de datos de gráficos deriva de estas relaciones. Las bases de datos de gráficos usan nodos para almacenar entidades de datos y bordes para almacenar relaciones entre entidades. Un borde siempre tiene un nodo de inicio, un nodo final, un tipo y una dirección, y puede describir las relaciones principales y secundarias, las acciones, la propiedad y cosas similares. No hay límite para la cantidad y el tipo de relaciones que un nodo puede tener.

Un gráfico de una base de datos de gráficos se puede desplazar a lo largo de tipos de bordes específicos, o por todo el gráfico. En las bases de datos de gráficos, atravesar las uniones o las relaciones es muy rápido porque las relaciones entre los nodos no se calculan en los tiempos de consulta, sino que se mantienen en la base de datos.
Presentan ventajas con respecto a los casos de uso como las redes sociales, los motores de recomendaciones y la detección del fraude, donde se necesita crear relaciones entre los datos y consultarlas rápidamente.

El siguiente es un ejemplo de un gráfico de red social. Dadas las personas (nodos) y sus relaciones (bordes), puede averiguar quiénes son los "amigos de los amigos" de una persona en particular, por ejemplo, los amigos de los amigos de Sebastián.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/2cfe8a45-07eb-4eb9-a675-b2ac08537133">
</p>

## Casos de uso

### Detección del fraude

Las bases de datos de gráficos son capaces de ofrecer una sofisticada prevención del fraude. Con las bases de datos de gráficos, puede usar las relaciones para procesar transacciones financieras y de compras casi en tiempo real. Con consultas de gráficos rápidas, podrá detectar si, por ejemplo, un posible comprador está utilizando la misma dirección de correo electrónico y tarjeta de crédito que un caso de fraude conocido. Las bases de datos de gráficos también puede ayudarle a detectar con facilidad patrones de relaciones como, por ejemplo, que varias personas tengan asociadas la misma dirección de correo electrónico personal o que varias personas compartan la misma dirección IP aunque vivan en direcciones físicas distintas.

### Motores de recomendaciones

Las bases de datos de gráficos son una buena opción para aplicaciones de recomendaciones. Con las bases de datos de gráficos, puede almacenar en un gráfico las relaciones entre las categorías de información, como intereses del cliente, amigos e historial de compras. Puede utilizar una base de datos de gráficos de alta disponibilidad para recomendar productos a un usuario a partir de los productos que han comprado otros usuarios que siguen el mismo deporte o presentan un historial de compras similar. También puede identificar a las personas que tienen un amigo en común, pero que todavía no se conocen, y enviarles una recomendación de amistad.

## References
- https://aws.amazon.com/es/nosql/graph/#:~:text=Las%20bases%20de%20datos%20de%20gr%C3%A1ficos%20usan%20nodos%20para%20almacenar,la%20propiedad%20y%20cosas%20similares.
