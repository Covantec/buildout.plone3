.. -*- coding: utf-8 -*-

Introducción
============

Este es un ejemplo de la configuración básica de `zc.buildout`_ usada en el articulo 
`Buildout y Plone 3`_, el cual explica como instalar y configurar la ultima versión 
estable `Plone 3.3.6`_ usando un esquema de instalación para desarrollos personalizados.

Sugerencia seguir los pasos descritos en en el articulo en su sección de `Requisitos previos`_.

Instalación
-----------

La instalación la realiza con los siguientes comandos: ::

  $ git clone https://github.com/plone-ve/buildout.plone3.git
  $ cd ./buildout.plone3
  $ python bootstrap.py
  $ ./bin/buildout -vN
  
Inicie su instancia Zope, con el siguiente comando: ::
  
  $ ./bin/instance fg
  
.. _zc.buildout: http://plone-spanish-docs.readthedocs.org/en/latest/buildout/replicacion_proyectos_python.html
.. _Buildout y Plone 3: http://plone-spanish-docs.readthedocs.org/en/latest/buildout/plone3_zcbuildout.html
.. _Requisitos previos: http://plone-spanish-docs.readthedocs.org/en/latest/buildout/plone3_zcbuildout.html#requisitos-previos
.. _Plone 3.3.6: http://plone.org/products/plone/releases/3.3.6
