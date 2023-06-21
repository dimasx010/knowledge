# Content Delivery Network(CDN)

Una CDN (Content Delivery Network o Red de Distribución de Contenido en español) es básicamente un conjunto de servidores ubicados en diferentes puntos de una red que contienen copias locales de ciertos contenidos (vídeos, imágenes, música, documentos, webs, etc.) que están almacenados en otros servidores generalmente alejados geográficamente, de forma que sea posible servir dichos contenidos de manera más eficiente.

Esta mejora en la eficiencia se logra con un mejor balanceo de la carga a la que están sometidos tanto los servidores que alojan los contenidos como los enlaces que interconectan las distintas secciones de la red, eliminando posibles cuellos de botella y sirviendo los datos en función de la cercanía geográfica del usuario final.


<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/76ae6800-a792-4498-99d8-8fae8c5fba69">
</p>

La idea es que haya una copia del contenido cerca del usuario para mejorar la velocidad de acceso

Es decir, en estos CDNs se replican los contenidos en diferentes redes y países, dirigiendo las solicitudes de los usuarios hasta las copias más cercanas a su red. De este modo se evita que algunos servidores se colapsen por exceso de peticiones, gracias a la distribución geográfica de los datos, y se minimizan los retardos, ya que el camino hasta el contenido es el mínimo posible.

Por ejemplo, supongamos que desde Madrid queremos ver un vídeo de YouTube que originalmente esté alojado en EEUU. Podríamos acceder directamente a él junto con otros millones de usuarios de todo el mundo a través de los cada vez más saturados enlaces intercontinentales, o bien podríamos acceder a una copia local en un servidor de la red CDN que una empresa tuviera instalado en Madrid, lo que mejoraría la velocidad de acceso y reduciría la latencia.

Uno de los CDN más populares a nivel mundial es Cloudflare. Por eso cuando Cloudflare se cae o falla, una enorme cantidad de páginas webs se vienen abajo. Cloudflare actúa como intermediaria entre el cliente y el servidor, usando unos sistemas llamados proxies reversos (reverse proxies) para crear copias y cachés de sitios web.

## Referencias
- https://www.xatakamovil.com/conectividad/cdn-que-es-para-que-sirve-y-por-que-no-rompe-con-la-neutralidad-de-la-red
