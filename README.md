# Lead Scraper — B2B Industrial Leads

![Privado](https://img.shields.io/badge/Codigo-Privado%20%C2%B7%20Proyecto%20Interno-red?style=flat)
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/python/python-original.svg" width="18" align="absmiddle" /> ![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat&logo=playwright&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![Excel](https://img.shields.io/badge/Excel-217346?style=flat&logo=microsoftexcel&logoColor=white)

> **Scraper de leads B2B para directorios industriales — extrae empresas, contactos y datos de Kompass y ThomasNet y los exporta en formato Excel listo para prospeccion.**

> Este es un **portfolio showcase** — el codigo fuente es propietario y no esta incluido.

---

## El Problema

Los equipos de ventas B2B en sectores industriales necesitan listas de prospectos calificados: empresas con nombre, industria, ubicacion, tamano y datos de contacto. Las bases de datos comerciales son costosas y generalmente desactualizadas. Los directorios publicos como Kompass y ThomasNet tienen la informacion — pero no exponen una API.

---

## La Solucion

Scraper automatizado con tecnicas de evasion de deteccion que navega los directorios B2B, extrae los datos relevantes de cada empresa y los exporta a Excel con columnas limpias y listas para importar a cualquier CRM.

---

## Funcionalidades

| Funcionalidad | Descripcion |
|--------------|-------------|
| Scraping de Kompass | Extraccion de empresas por industria, pais y tamano |
| Scraping de ThomasNet | Extraccion de proveedores industriales por categoria y ubicacion |
| Evasion de deteccion | Playwright Stealth + Camoufox + rotacion de user-agent |
| Exportacion a Excel | Salida en `.xlsx` con columnas: empresa, industria, pais, contacto, telefono, web |
| Logs detallados | Registro de progreso y errores via Loguru |
| Reintentos automaticos | Logica de reintentos con backoff exponencial via Tenacity |

---

## Stack Tecnologico

| Capa | Tecnologia |
|------|-----------|
| Automatizacion | Python · Playwright · Playwright-stealth |
| Anti-deteccion | Camoufox · fake-useragent |
| Procesamiento | Pandas · OpenPyXL |
| Logs | Loguru |
| Reintentos | Tenacity |

---

## Fuentes de Datos

| Directorio | Descripcion |
|-----------|-------------|
| [Kompass](https://kompass.com) | Directorio B2B global — mas de 70M empresas en 70 paises |
| [ThomasNet](https://thomasnet.com) | Directorio de proveedores industriales en Norteamerica |

---

## Contacto

El codigo fuente es propietario. Para consultas: [pablozam1931@gmail.com](mailto:pablozam1931@gmail.com)

---

*Parte del portfolio [deadlyrat](https://github.com/deadlyrat).*
