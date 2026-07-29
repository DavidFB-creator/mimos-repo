# Canal de paquetes de MimOS

Repositorio pacman con los paquetes propios de **MimOS**, firmados con la clave
`MimOS Package Signing <packages@mimoslinux.org>`, huella
`77E1176695E14EBFA3A03B93CE5181401267126E`.

La mitad pública de esa clave viaja dentro de la imagen, en el paquete
`mimos-keyring`. Un sistema MimOS instalado puede por tanto verificar este
repositorio sin haberlo visitado nunca antes.

## Uso

MimOS lo configura por su cuenta a través de `mimos-release`. A mano:

```ini
[mimos]
SigLevel = Required TrustedOnly
Include = /etc/pacman.d/mimos-mirrorlist
```

`Required TrustedOnly` no es adorno: sin firma verificada, este repositorio no
debe usarse. Nunca `TrustAll` sobre una red.

## Qué hay aquí, y qué no

Solo paquetes compilados, sus firmas separadas y las bases de datos firmadas.
El código fuente, las recetas y el historial viven en otro sitio; este
repositorio existe únicamente para que `pacman` descargue y verifique.

`SHA256SUMS` cubre el árbol entero, pero es una comodidad para comprobar una
copia, no la garantía de origen. La garantía son las firmas.

## Advertencia

Estos paquetes son experimentales y acompañan a una versión **alpha** de MimOS.
No los instale en un equipo que le importe.

---

MimOS lo desarrolla **XI14** (David y Jan).
