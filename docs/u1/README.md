# 1. Introducción a ROS

## Herramientas de software y control de versiones.
  - Tutorial en ingles de [git](https://git-scm.com/docs/gittutorial)
  - La [lista de YT](https://www.youtube.com/playlist?list=PLOMsmeV5s0QMioRvbwDAXvtOMRMtkBhp1) para los becarios. Están los mismo videos del pelado, pero con un video extra de como instalar git en windows y unos primeros pasos.

Los siguientes temas están explicados [en este repo](https://github.com/eborghi10/ros-workshop.git).

## Nodos.Tópicos. Topología publicador-suscriptor.
## Servicios. Acciones. Introspección.
## Introducción a Gazebo. Plugins. Creación de entornos y sensores. Principios básicos de simulación.
## Ejemplos con Turtlesim y iRobot Create 2.


## Dockerfile
Escritorio y notebook en ventanas del explorador.
La imágen es armada a partir de [este](https://github.com/Tiryoh/docker-ros-desktop-vnc) y [este](https://github.com/eborghi10/ros-workshop) repo.
![](https://martinnievas.com/images/jupyter-ros.png)

Para correr el container, ejecutar en una terminal:
```bash
cd path_to/robotica_aplicada_docker/docs/u1
docker build -t ros_tutorial:0.1 .
docker run -p 6080:80 -p 8888:8888 --shm-size=512m ros_tutorial:0.1
```

