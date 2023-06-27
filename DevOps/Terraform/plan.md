# Terraform Plan

Plan is another of the most important Terraform commands in the platform, because it has the ability to review the entire function and compare it with the current infrastructure. The so-called Terraform Plan command has the function of creating an execution plan. In addition, it is responsible for performing an update, unless the user specifically disables this option.

Basically terraform generates an execution plan that describes what it will do to reach the desired state and then executes it to build the described infrastructure.


<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/9d51bb9c-354e-4c93-8030-d2566231bb4c">
</p>

Optional parameters for Terraform commands include:

- lock=true: locks the status file when locking is supported.
- lock-timeout=0s : refers to the duration set to retry a status lock.
- module-depth=n: used to specify the modules to be displayed in the output. This does not affect the plan itself, only the output displayed. By default, this is -1, which will expand everything.

## References
- https://terraform-infraestructura.readthedocs.io/es/latest/comandos/
- https://galvarado.com.mx/post/tutorial-infraestructura-como-c%C3%B3digo-con-terraform/