.. -*- coding: utf-8 -*-

buildout.plone3
===============

Configuración de buildout para instalar el CMS Plone 3.3.6.

Este es un ejemplo de la configuración básica de `zc.buildout`_ usada en el articulo 
`Buildout y Plone 3`_, el cual explica como instalar y configurar la ultima versión 
estable `Plone 3.3.6`_ usando un esquema de instalación para desarrollos personalizados.

Sugerencia seguir los pasos descritos en en el articulo en su sección de `Requisitos previos`_.

Descargar código fuente
=======================

Para descargar el código fuente, ejecute el siguiente comando: ::

  $ git clone https://github.com/plone-ve/buildout.plone3.git

Inicialización del proyecto
===========================

Para la inicialización del proyecto Buildout, ejecute el siguiente comando: ::

  $ cd ./buildout.plone3
  $ python bootstrap.py

Construcción del proyecto
=========================

Para la construcción del proyecto Buildout, ejecute el siguiente comando: ::

  $ ./bin/buildout

Ejecutar Zope
=============

Para iniciar la instancia Zope, ejecute el siguiente comando: ::

  (python2.7)$ ./bin/instance start

Puede acceder a la ZMI para crear su sitio Plone en la siguiente dirección http://localhost:8080/manage

Para detener la instancia Zope, ejecute el siguiente comando: ::

  ./bin/instance stop

Otros comandos disponibles
==========================

./bin/repozo

  Es un script de Zope para hacer copias de seguridad incrementales y completas de un archivo Data.fs.

  Para **respaldar** la ZODB *completamente*, ejecute el siguiente comando: ::

    ./bin/repozo -BvzF -r ./backups -f ./var/filestorage/Data.fs

  Para **respaldar** la ZODB de *forma incremental*, ejecute el siguiente comando: ::

    ./bin/repozo -BvzQ -r ./backups -f ./var/filestorage/Data.fs

  Para **restaurar** datos de un respaldo ZODB *a partir de la hora actual*, ejecute el siguiente comando: ::

    ./bin/repozo -Rv -r ./backups -o ./var/filestorage/Data.fs

  Para **restaurar** datos de un respaldo ZODB *a partir de la fecha y hora especifica*, ejecute el siguiente comando: ::

    ./bin/repozo -Rv--date='yyyy-mm-dd' -r ./backups -o ./var/filestorage/Data.fs

  Para mas información consulte la ayuda incluida en el script con el siguiente comando ``./bin/repozo -h``.

.. _zc.buildout: http://plone-spanish-docs.readthedocs.org/en/latest/buildout/replicacion_proyectos_python.html
.. _Buildout y Plone 3: http://plone-spanish-docs.readthedocs.org/en/latest/buildout/plone3_zcbuildout.html
.. _Requisitos previos: http://plone-spanish-docs.readthedocs.org/en/latest/buildout/plone3_zcbuildout.html#requisitos-previos
.. _Plone 3.3.6: http://plone.org/products/plone/releases/3.3.6
