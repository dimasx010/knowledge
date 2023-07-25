# Kubernetes ConfigMaps

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/cebf4929-e512-456f-9fca-de80a7a1bdc8">
</p>

A ConfigMap is a dictionary of configuration settings. This dictionary consists of key-value string pairs. Kubernetes provides these values to your containers. As with other dictionaries (maps, hashes, ...), the key allows you to get and set the configuration value.

## Why would I use a ConfigMap in Kubernetes?

Use a ConfigMap to keep your application code separate from your configuration.

This is an important part of creating a two-factor application.

This allows you to easily change the configuration according to the environment (development, production, test) and dynamically change the configuration at runtime.

## What is a ConfigMap used for?

A ConfigMap stores configuration settings for your code. Store connection strings, public credentials, host names and URLs in your ConfigMap.

## References
- https://matthewpalmer.net/kubernetes-app-developer/articles/ultimate-configmap-guide-kubernetes.html#:~:text=A%20ConfigMap%20is%20a%20dictionary,and%20set%20the%20configuration%20value.