# Tipos de imágenes

## Lossy vs Lossless (Con pérdida vs sin pérdida)

Las imágenes se pueden dividir en dos tipos dependiendo de cómo el formato maneja las imágenes. Si un sitio maneja muchas imágenes sin pérdida tarda más en abrir, por lo que no hay una buena experiencia por parte del usuario. 

### Lossless (sin pérdida)

Estos formatos capturan todos los datos del archivo original. A pesar de comprimir el archivo este podrá volver a su estado original. El nombre sin pérdida viene de que el archivo en este formato no pierde calidad en la imagen.

### Lossy (Con pérdida)

Los formatos de imagen con pérdida se aproximan a la imagen original. Estos reducen el tamaño del archivo eliminando datos innecesarios o reduciendo la gama de colores en estos y por lo tanto llegando a reducir la calidad del archivo. Sin embargo esto puede ayudar a evitar largos tiempos de carga y mejorar la experiencia del usuario.

## Formatos

- GIF (Graphics Interchange Format).- Es un formato Lossless, es decir que el formato está tan reducido en la gama de colores que no se puede reducir más la calidad de este.
- PNG 8 (Portable Network Graphics).- Es un formato Lossless, no se pierde la calidad al escalar el archivo por lo que es utilizado para íconos entre otras cosas. Utiliza una gama de 256 colores al igual que GIF y este permite utilizar transparente para solamente considerar la parte visible de la imagen al trabajar en un proyecto.
- PNG 24 .- Es parecido a PNG 8 con la diferencia de que admite una gama casi ilimitada de colores. 
- JPG/JPEG.- Este es un formato Lossy ya que tiene pérdidas al momento de escalarlo. Utiliza una gama casi ilimitada de colores así que es óptimo para fotografía o su uso en la web debido a que al tener pérdidas, una imagen JPG pesa menos que una imagen PNG al comprimirla.
- SVG (Scalable Vector Graphics).- Este es un formato Lossless debido a que no importa cuanto se escale una imagen SVG, esta nunca perderá calidad gracias a un algoritmo matemático. Este formato es ideal para íconos (sobretodo minimalistas) debido a que el algoritmo maneja vectores para escalar las imágenes.

<br/>
<table>
    <tr>
        <td><b>Formato</b></td>
        <td><b>Categoría</b></td>
        <td><b>Paleta</b></td>
        <td><b>Uso</b></td>
    </tr>
    <tr>
        <td>GIF</td>
        <td>Lossless</td>
        <td>Máximo 256 colores</td>
        <td>
            <ul>
                <li>Animaciones simples</li>
                <li>Gráficos con colores planos</li>
            </ul>
        </td>
    </tr>
    <tr>
        <td>PNG 8</td>
        <td>Lossless</td>
        <td>Máximo 256 colores</td>
        <td>
            <ul>
                <li>Uso de transparencia</li>
                <li>Sin animación</li>
                <li>Ideal para íconos</li>
            </ul>
        </td>
    </tr>
    <tr>
        <td>PNG 24</td>
        <td>Lossless</td>
        <td>Colores ilimitados</td>
        <td>
            <ul>
                <li>Similar a PNG 8</li>
                <li>Maneja imágenes fijas de más colores y transparencia</li>
            </ul>
        </td>
    </tr>
    <tr>
        <td>JPG</td>
        <td>Lossy</td>
        <td>Millones de colores</td>
        <td>
            <ul>
                <li>Imágenes fijas</li>
                <li>Fotografía</li>
            </ul>
        </td>
    </tr>
    <tr>
        <td>SVG</td>
        <td>Vector/Lossless</td>
        <td>Colores ilimitados</td>
        <td>
            <ul>
                <li>Gráficos/ logotipos para web</li>
                <li>Retina/ pantallas de alta resolución</li>
            </ul>
        </td>
    </tr>
</table>
