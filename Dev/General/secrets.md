# Management of Secrets

Today's digital enterprises rely on commercial, in-house developed and open source applications to conduct business and are increasingly leveraging automated IT infrastructure and DevOps methodologies to accelerate development and innovation. While application and IT environments vary considerably from organization to organization, one thing remains constant: every application, script, automation tool and other non-human identity depends on some form of privileged credential to access other tools, applications and data.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/c916cffb-9812-4cc9-8366-4cc8eab3a0ca">
</p>

## What is a secret?

These non-human privileged credentials are often referred to as "secrets" and refer to private information that acts as a key to unlock protected resources or sensitive information in tools, applications, containers, DevOps and cloud-native environments.

Common types of secrets include:

Privileged account credentials
- Passwords
- Certificates
- SSH keys
- API keys
- Encryption keys

## Principal challenges in managing secrets

A non-human user with access to a secret automatically gains real-time access and permissions to any resource belonging to the owner of the secret. Cybercriminals are aware of this and target their attacks on secrets to gain unauthorized access to other secrets and hosts in order to complete their mission. A cyberattack targeting secrets often extends far beyond the scope of the initial breach.

Secrets are pervasive. They include credentials embedded in the source code of container applications (e.g., Red Hat OpenShift, Kubernetes or Pivotal); automation processes (e.g., Ansible Playbooks, Puppet or Chef); business-critical applications, both internally developed and commercial off-the-shelf (COTS); security software, such as vulnerability scanners; application servers and IT management software; robotic process automation (RPA) platforms; and the continuous integration/continuous deployment (CI/CD) tool chain.

Automated processes are incredibly powerful. They can access protected data, scale at unprecedented speed, leverage cloud resources and execute business processes instantaneously. But as headline-grabbing cybersecurity leaks have shown, automated processes are susceptible to sophisticated cyberattacks, which can occur suddenly and spread rapidly. Organizations must protect the secrets assigned to non-human identities to defend against attacks and mitigate risks.

## What is secrets management?

Secrecy management, one of the cybersecurity best practices for digital enterprises, enables organizations to systematically enforce security policies for non-human identities. Secrecy management ensures that only authenticated and authorized entities can access resources in tool stacks, platforms and cloud environments.

The following steps are typically included in a secrets management initiative. Many of these approaches and techniques are also used to protect privileged access by human users.

- Authenticate all access requests using non-human credentials.
- Implement the principle of least privilege.
- Enforce role-based access control (RBAC) and regularly rotate secrets and credentials.
- Automate the management of secrets and enforce consistent access policies.
- Track all access and maintain a complete audit trail.
- Eliminate secrets from code, configuration files and other unprotected areas.

## Common use cases in the management of secrets

### Secrecy management to protect CI/CD processes.

Popular CI/CD process tools such as Jenkins, Ansible, Puppet and Chef are designed for efficiency and speed, but can present new security challenges. These automated configuration management tools require secrets to access protected resources such as databases, SSH servers and HTTP services. These secrets are often embedded in source code in an unsecured manner or stored in configuration files or code for these tools (e.g., JenkinsFiles, playbooks, scripts or source code). Effective secrets management enables organizations to remove these hard-coded DevOps tool secrets from CI/CD processes, while providing comprehensive audit trails, policy-based RBAC and secrets rotation.

### Management of secrets to protect containers.

DevOps and engineering teams are increasingly relying on containers to accelerate development and improve portability and productivity. Containers require secrets to access critical and sensitive information. However, because containers are ephemeral (or short-lived), they can be difficult to monitor and access to specific resources can be difficult to manage and protect. Secrets management security measures allow teams to authenticate container requests for secrets with native container platform attributes and manage secrets with RBAC policies for granular control.

### Management of secrets to manage elastic and auto-scaling environments.

Cloud providers offer automatic scaling features that enable elasticity (ephemerality) and the pay-as-you-grow model. While this improves efficiency, it also creates new security management challenges, particularly with regard to scalability. By implementing best practices for managing secrets, organizations can eliminate the need for human operators to manually apply policies to each new host by assigning an identity to the host in real time and securely authenticating the calling application based on the predefined security policy.

### Secrecy management to protect internally developed applications and COTS applications.

Internally developed applications and scripts, along with third-party tools and solutions such as security tools, RPA, automation and IT management tools, often require high levels of privileged access across the enterprise infrastructure to complete their defined tasks. Effective secrets management practices require that credentials embedded in the source code of internally developed applications and scripts are removed and that all secrets are centrally stored, managed and rotated to minimize risk.

## References
- https://www.cyberark.com/es/what-is/secrets-management/#:~:text=%C2%BFQu%C3%A9%20es%20un%20secreto%3F,entornos%20nativos%20en%20la%20nube.