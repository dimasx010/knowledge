# Helm

## General

Helm is widely known as "the package manager for Kubernetes". Although it is presented as such, its scope goes far beyond that of a simple package manager. However, let's start at the beginning

Helm is an open source project that was originally created by DeisLabs and donated to CNCF, which now maintains it. The original goal of Helm was to provide users with a better way to manage all the Kubernetes YAML files we create in Kubernetes projects

The path Helm took to solve this problem was to create Helm Charts. Each chart is a package with one or more Kubernetes manifests: a chart can have child charts and dependent charts

This means that Helm installs the entire dependency tree for a project if you run the install command for the top-level chart. You only have to run a single command to install your entire application, instead of listing the files to install via kubectl.

Charts also allows you to version your manifest files, just like we do with Node.js or any other package. This allows you to install specific versions of charts, which means maintaining specific configurations for your infrastructure in code form

Helm also keeps a version history of all deployed charts, so you can roll back to a previous version if something goes wrong

Helm supports Kubernetes natively, which means you don't have to write any complex syntax files or anything to start using Helm. Just drop your template files into a new graph and you're done

## Why?

But why should we use it? The management of application manifests can be easily done with a few combinations of commands

But when it comes to deletions, it is often difficult to manage, since you would have to have the manifest as is and perform the deletion

## References

- https://helm.sh/docs/intro/quickstart/
- https://circleci.com/blog/what-is-helm/#:~:text=Helm%20is%20a%20tool%20that,it%20increasingly%20difficult%20to%20manage.