# 🐳 TechRetail — Docker Swarm on AWS EC2

> Plataforma de comercio electrónico peruana modernizada con arquitectura de
> microservicios contenerizada y orquestada mediante Docker Swarm sobre
> infraestructura cloud en Amazon Web Services.

![Docker](https://img.shields.io/badge/Docker-29.1.3-2496ED?style=flat-square&logo=docker&logoColor=white)
![Docker Swarm](https://img.shields.io/badge/Docker%20Swarm-Enabled-2496ED?style=flat-square&logo=docker&logoColor=white)
![AWS EC2](https://img.shields.io/badge/AWS-EC2%20t3.micro-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![Ubuntu](https://img.shields.io/badge/Ubuntu-24.04%20LTS-E95420?style=flat-square&logo=ubuntu&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-18%20Alpine-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?style=flat-square&logo=mysql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-7%20Alpine-DC382D?style=flat-square&logo=redis&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-Alpine-009639?style=flat-square&logo=nginx&logoColor=white)

---

## 📑 Tabla de contenidos

- [Contexto del proyecto](#-contexto-del-proyecto)
- [Arquitectura del sistema](#-arquitectura-del-sistema)
- [Infraestructura en AWS](#-infraestructura-en-aws)
- [Servicios desplegados](#-servicios-desplegados)
- [Estructura del repositorio](#-estructura-del-repositorio)
- [Prerrequisitos](#-prerrequisitos)
- [Guía de despliegue](#-guía-de-despliegue)
- [Escalado dinámico](#-escalado-dinámico)
- [Seguridad](#-seguridad)
- [Monitoreo](#-monitoreo)
- [Comandos de referencia](#-comandos-de-referencia)
- [Problemas conocidos y soluciones](#-problemas-conocidos-y-soluciones)
- [Autor](#-autor)

---

## 📌 Contexto del proyecto

**TechRetail** es una empresa peruana de comercio electrónico fundada en 2020
que operaba su plataforma sobre un único servidor físico. Con el crecimiento
acelerado de usuarios durante campañas como el **Buen Fin** y los
**Cyber Days**, la arquitectura monolítica comenzó a mostrar sus límites:

| Problema | Impacto |
|---|---|
| Caídas frecuentes en horas pico | Pérdida de ventas y reputación |
| Tiempos de respuesta > 8 segundos | Abandono de carrito elevado |
| Imposibilidad de escalar rápidamente | Capacidad limitada ante demanda |
| Sin alta disponibilidad | S/. 15,000 por hora de inactividad |

Este repositorio documenta la solución implementada: migración a una
arquitectura de **microservicios contenerizada y orquestada con Docker Swarm**
desplegada sobre AWS EC2, resolviendo todos los problemas anteriores con
escalado horizontal automático, alta disponibilidad y balanceo de carga.

---

## 🏗️ Arquitectura del sistema
