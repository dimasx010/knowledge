# Graph database - NoSQL

Graph databases are part of the NoSQL family. These models are gaining a lot of interest among the public thanks to their features. They have multiple data modeling tools.

Graph databases are expressly designed to store and navigate relationships. Relationships are first-class citizens in graph databases, and most of the value of graph databases derives from these relationships. Graph databases use nodes to store data entities and edges to store relationships between entities. An edge always has a start node, an end node, a type, and an address, and can describe primary and secondary relationships, actions, ownership, and the like. There is no limit to the number and type of relationships a node can have.

A graph in a graph database can be scrolled along specific types of edges, or along the entire graph. In graph databases, traversing joins or relations is very fast because relations between nodes are not computed at query times, but are maintained in the database.
They have advantages over use cases such as social networks, recommendation engines and fraud detection, where relationships between data need to be created and queried quickly.

The following is an example of a social network graph. Given the people (nodes) and their relationships (edges), you can find out who are the "friends of friends" of a particular person, for example, the friends of Sebastian's friends.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/2cfe8a45-07eb-4eb9-a675-b2ac08537133">
</p>

## Use cases

### Fraud detection

Graph databases are capable of providing sophisticated fraud prevention. With graph databases, you can use relationships to process financial and purchase transactions in near real-time. With fast graph queries, you can detect whether, for example, a prospective buyer is using the same e-mail address and credit card as a known fraud case. Graph databases can also help you easily detect relationship patterns, such as multiple people having the same personal email address associated with them, or multiple people sharing the same IP address even though they live at different physical addresses.

### Recommendation engines

Graph databases are a good choice for recommendation applications. With graph databases, you can store relationships between categories of information, such as customer interests, friends, and purchase history, in a graph. You can use a highly available graph database to recommend products to a user based on products purchased by other users who follow the same sport or have a similar purchase history. You can also identify people who have a friend in common, but have not yet met, and send them a friend recommendation.

## References
- https://aws.amazon.com/es/nosql/graph/#:~:text=Las%20bases%20de%20datos%20de%20gr%C3%A1ficos%20usan%20nodos%20para%20almacenar,la%20propiedad%20y%20cosas%20similares.
