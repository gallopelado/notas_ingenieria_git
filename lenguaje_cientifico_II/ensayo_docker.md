#### Índice
- [Un poco de historia](#un-poco-de-historia)
  - [Línea de tiempo](#línea-de-tiempo)
  - [1979: Unix V7](#1979-unix-v7)
  - [2000: FreeBSD Jails](#2000-freebsd-jails)
  - [2001: Linux VServer](#2001-linux-vserver)
  - [2004: Solaris Containers](#2004-solaris-containers)
  - [2005: Open VZ (Open Virtuzzo)](#2005-open-vz-open-virtuzzo)
  - [2006: Process Containers](#2006-process-containers)
  - [2008: LXC](#2008-lxc)
  - [2011: Warden](#2011-warden)
  - [2013: LMCTFY](#2013-lmctfy)
  - [2013: Docker](#2013-docker)
- [¿Qué es Docker?](#qué-es-docker)
- [La plataforma de Docker](#la-plataforma-de-docker)
- [¿Para qué puedo usar Docker?](#para-qué-puedo-usar-docker)
    - [Rápido, distribución consistente para tus aplicaciones](#rápido-distribución-consistente-para-tus-aplicaciones)
    - [Despliegue responsivo y escalable](#despliegue-responsivo-y-escalable)
    - [Ejecutando más cargas de trabajo en el mismo hardware](#ejecutando-más-cargas-de-trabajo-en-el-mismo-hardware)
- [La arquitectura de Docker](#la-arquitectura-de-docker)

### Un poco de historia
[Recuperado del inglés - 9 de Octubre, 2022 - "Aqua Blog"](https://blog.aquasec.com/a-brief-history-of-containers-from-1970s-chroot-to-docker-2016)

#### Línea de tiempo
![linea de tiempo](./img/timeline.drawio.png)

#### 1979: Unix V7
Durante el desarrollo del Unix V7 en 1979, un sistema llamado *chroot* fue introducido, cambiando el directorio raíz(root) de un proceso y sus hijos(children) a una nueva ubicación en el sistema de archivos. Este progreso fue el inicio del proceso de aislamiento: separando el acceso de ficheros por cada proceso. *Chroot* fue agregado a [BSD](https://en.wikipedia.org/wiki/Berkeley_Software_Distribution) en 1982.

#### 2000: FreeBSD Jails
Luego de casi dos décadas, cuando un pequeño proveedor de entorno-compartido llegó con las jaulas de FreeBSD para lograr una clara separación entre sus servicios y estos de sus clientes por seguridad y facilitar la administración. Las jaulas de FreeBSD permiten a los administradores particionar un sistema FreeBSD dentro de otro independiente, pequeños sistemas llamados - "jails o jaulas" - con la habilidad de asignar una dirección IP por cada sistema y configuración.

#### 2001: Linux VServer
Como FreeBSD Jails, [Linux VServer](https://en.wikipedia.org/wiki/Linux-VServer) es un mecanismo que puede particionar recursos(sistemas de archivos, direcciones de red, memoria) en un sistema informático. Introducido en 2001, este sistema operativo de virtualización que es implementado agregando un parche al kernel de Linux. Parches experimentales están todavía disponibles, pero el último parche estable fue liberado en 2006.

#### 2004: Solaris Containers
En 2004, la primera beta pública de [Solaris Containers](https://en.wikipedia.org/wiki/Solaris_Containers) fue liberada, esta combina un sistema de recursos de controles y una separación de límites proveídos por zonas, el cual eran capaces de aprovechar características como *snapshots* y clonados desde *ZFS*.

#### 2005: Open VZ (Open Virtuzzo)
Es una tecnología de virtualización de sistemas operativos multinivel para Linux el cual usa un núcleo de Linux modificado para virtualización, aislamiento, gestión y verificación de recursos. El código no fue liberado como una parte del kernel oficial de Linux.

#### 2006: Process Containers
[Contenedores de proceso](https://en.wikipedia.org/wiki/Cgroups)(Lanzado por Google en 2006) fue diseñado para la limitación, contabilidad y aislamiento de los recursos usados(CPU, memoria, I/O discos, redes) de una colección de procesos. Fue renombrado como "Control Groups (cgroups)" un año después y eventualmente fusionado a la versión 2.6.24 del kernel de Linux.

#### 2008: LXC
LXC(LinuX Containers) fue la primera, más completa implementación del administrador de containers de Linux. Este fue implementado en 2008 usando *cgroups* y *Linux namespaces*, y trabaja sobre un single Linux kernel sin ningún parche.

#### 2011: Warden
CloudFoundry inició Warden en 2011, usando *LXC* en los primeros escenarios reemplazandolo con su propia implementación. Warden puede aislar entornos sobre cualquier sistema operativo, ejecutándose como un *daemon* y proveyendo una API para la gestión del contenedor. Desarrollaron un modelo cliente-servidor para gestionar una colección de contenedores a través de multiples hosts, y Warden incluyen un servicio para gestionar *cgroups*, *namespaces* y procesos de ciclo de vida.

#### 2013: LMCTFY
[Let Me Contain That For You](https://github.com/google/lmctfy) salido en 2013 como una version de código abierto de *Google's container stack*, proveyendo contenedores para aplicaciones Linux. Las aplicaciones pueden hacerse de modo "contenedor consciente" creando y gestionando sus propios subcontenedores. El despliegue activo en LMCTFY paró en 2015 luego de que Google empezara a contribuir los conceptos centrales a *libcontainer*, el cual es parte ahora de la [Open Container Foundation](https://github.com/opencontainers/runc/tree/main/libcontainer).

#### 2013: Docker
Cuando Docker emergió en 2013, los contenedores aumentaron su popularidad. No es coincidencia el crecimiento de Docker y el uso del contenedor en un *mano a mano*.
Así como [Warden](#2011-warden) lo hizo, Docker también usó LXC en sus inicios como administrador de contenedores para luego reemplazarlos por su propia biblioteca. Pero no hay duda que Docker por separado ofrece un ecosistema completo de administración de contenedores.

### ¿Qué es Docker?

[Recuperado del inglés - 5 de Octubre, 2022 - Get-started/overview](https://docs.docker.com/get-started/overview/)

Docker es una plataforma abierta para el desarrollo, montaje, y ejecutar aplicaciones. Docker te permite separar tus aplicaciones de la infraestructura para que puedas entregar software rápidamente. Con Docker, puedes gestionar tu infraestructura de la misma forma como gestionas tus aplicaciones. Tomando ventaja de las metodologías para montar, testear y desplegar código rápidamente, puedes disminuir significativamente el retraso de tiempo entre la codificación y ejecución en producción.

### La plataforma de Docker
Docker provee la característica de empaquetar y ejecutar una aplicación en un entorno libremente aislado llamado contenedor. El aislamiento y seguridad te permite ejecutar muchos contenedores simultáneamente en un dado host. Los contenedores son ligeros y contienen todo lo que necesitas para ejecutar la aplicación, de esta manera no necesitas confiar en que está actualmente instalado en el host. Puedes fácilmente compartir contenedores mientras trabajas, y estar seguro que todas las personas comparten contigo el mismo contenedor.

Docker provee herramientas y una plataforma para gestionar el ciclo de vida de tus contenedores:

- Desarrolla tu aplicación y sus componentes usando contenedores.
- El contenedor se convierte en la unidad para distribuir y testear tu aplicación.
- Cuando estés listo, despliega tu aplicación dentro de un entorno de producción, como un contenedor o un servicio orquestado. Funciona de la misma manera si tu entorno de producción es centro local de datos, un proveedor en la nube, o un híbrido de ambos.

### ¿Para qué puedo usar Docker?
##### Rápido, distribución consistente para tus aplicaciones
Docker mejora el ciclo de desarrollo permitiendo a los desarrolladores trabajar en entornos estandarizados usando contenedores locales los cuales proveen tus aplicaciones y servicios. Los contenedores son buenos para la integración continua y entrega continua de flujo de trabajo(CI/CD).

Considera el siguiente escenario de ejemplo:
- Tus desarrolladores escriben código localmente y comparten su trabajo a sus colegas usando los contenedores de Docker.
- Ellos usan docker para subir sus aplicaciones dentro de un entorno de testeo y ejecución automatizada y manual.
- Cuando los desarrolladores encuentran errores(bugs), pueden solucionarlos en el entorno de desarrollo y redistribuirlos hacia el entorno de pruebas para la verificación y validación.
- Cuando la verificación es completa, conseguir un parche para el cliente es tan simple como subir la imagen actualizada para el entorno de producción.

##### Despliegue responsivo y escalable
La plataforma basada en contenedores de Docker permite altas cargas de trabajo portátiles. Los contenedores de docker pueden ejecutarse en una portátil local de desarrollo, en físico o en máquinas virtuales en un centro de datos, en proveedores de servicios en la nube,o en una mezcla de entornos.

La naturaleza portable y ligera de Docker también hace fácil para administrar dinámicamente flujos de trabajo, ampliando o reduciendo aplicaciones y servicios como las necesidades de negocio dictan, en tiempo real.

##### Ejecutando más cargas de trabajo en el mismo hardware
Docker es ligero y rápido. Provee una alternativa viable costo-efectiva de un *hypervisor-based virtual machine*, máquina virtual basada en hipervisor, puedes usar más de tu capacidad de cómputo para lograr tus objetivos de negocio. Docker es perfecto para entornos de alta densidad y para pequeños y medianos despliegues donde tu necesitas hacer más con menos recursos.

### La arquitectura de Docker
...En desarrollo