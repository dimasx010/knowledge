# HashiCorp Configuration Language

HashiCorp Configuration Language (HCL) is a unique configuration language. It was designed for use with HashiCorp tools, especially Terraform, but HCL has been expanded as a more general configuration language. It is visually similar to JSON with additional data structures and capabilities built in.


<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/2ba1a2a0-1f7a-4094-a00a-8c30909847fb">
</p>

HCL consists of three sublanguages:

- Structural
- Expression
- Templates

When combined, the sublanguages form a well-structured HCL configuration file. This structure helps to accurately and easily describe the environmental settings needed for the Terraform tool.

Recently, HCL has discontinued version 1 of the language in favor of version 2. HCL2 is a combination of HCL and HashiCorp Interpolation Language (HIL). HIL adds string interpolation and a greater ability to use functions in variable declarations.

HCL can also be used with other tools in addition to Terraform. Over time, different parsers have become available, such as Go, Java, and Python. In this post, I discuss how to get started with HCL and which tools take advantage of its unique features.

## References
- https://recluit.com/que-es-hcl/
