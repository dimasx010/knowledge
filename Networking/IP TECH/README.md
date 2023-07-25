# Direcciones IP

Para dirigir correctamente los mensajes a una ubicación, necesita una dirección. Al igual que cada hogar tiene una dirección postal, cada ordenador tiene una dirección IP. Sin embargo, en lugar de utilizar la combinación de calle, ciudad, estado, código postal y país, la dirección IP utiliza una combinación de bits, 0 y 1.

A continuación, se muestra un ejemplo de una dirección de 32 bits en formato binario:

Se denomina “32 bits” porque tiene 32 dígitos. Puede contarlos.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/25445a63-6a50-4104-ad7e-7f32050dda15">
</p>

## ​Notación IPv4

Normalmente, no se ve una dirección IP en su formato binario. En cambio, se convierte en formato decimal y se anota como una dirección Ipv4.

En el siguiente diagrama, los 32 bits se agrupan en grupos de 8 bits, también denominados “octetos”. Cada uno de estos grupos se convierte en formato decimal separado por un punto.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/3e002ab9-4b89-402a-a452-3a5dcae4476e">
</p>

​Finalmente, es lo que se denomina “dirección Ipv4”. Es importante saberlo al tratar de comunicarse con un solo ordenador. No obstante, recuerde que está trabajando con una red. Aquí es donde entra en juego la notación CIDR.

## ​Notación CIDR

​192.168.1.30 es una única dirección IP. Si quiere expresar direcciones IP entre el intervalo de 192.168.1.0 y 192.168.1.255, ¿cómo puede hacerlo?

Una forma es utilizar la notación de direccionamiento entre dominios sin clase (CIDR). La notación CIDR es una forma comprimida de especificar un intervalo de direcciones IP. La especificación de un intervalo define cuántas direcciones IP están disponibles para usted.

Aquí se muestra la notación CIDR.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/55111c87-165d-45ce-abf9-fa9b04549229">
</p>