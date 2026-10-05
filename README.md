<div align="center">

<img src="assets/banner.png" width="100%" alt="Lead Scraper: scraper B2B que extrae empresas de Kompass y ThomasNet y las exporta a Excel">

# Lead Scraper

![Privado](https://img.shields.io/badge/C%C3%B3digo-Privado%20%C2%B7%20Proyecto%20Interno-red?style=flat)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat&logo=playwright&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![Excel](https://img.shields.io/badge/Excel-217346?style=flat&logo=microsoftexcel&logoColor=white)

**Scraper de leads B2B para directorios industriales: extrae empresas, contactos y datos de Kompass y ThomasNet, y los exporta en formato Excel listo para prospección.**

</div>

> Este es un **portafolio showcase**: el código fuente es propietario y no está incluido.

---

## Contenido

- [El Problema](#el-problema)
- [La Solución](#la-solución)
- [Funcionalidades](#funcionalidades)
- [Vista Previa](#vista-previa)
- [Arquitectura](#arquitectura)
- [Stack Tecnológico](#stack-tecnológico)
- [Instalación local](#instalación-local)
- [Roadmap](#roadmap)
- [Contacto](#contacto)

---

## El Problema

Los equipos de ventas B2B en sectores industriales necesitan listas de prospectos calificados: empresas con nombre, industria, ubicación, tamaño y datos de contacto. Las bases de datos comerciales son costosas y suelen estar desactualizadas. Los directorios públicos como Kompass y ThomasNet tienen la información, pero no exponen una API.

---

## La Solución

Un scraper automatizado con técnicas de evasión de detección que navega los directorios B2B, extrae los datos relevantes de cada empresa y los exporta a Excel con columnas limpias, listas para importar a cualquier CRM.

---

## Funcionalidades

| Funcionalidad | Descripción |
|---------------|-------------|
| Scraping de Kompass | Extracción de empresas por industria, país y tamaño |
| Scraping de ThomasNet | Extracción de proveedores industriales por categoría y ubicación |
| Evasión de detección | Playwright Stealth, Camoufox y rotación de user-agent |
| Exportación a Excel | Salida en `.xlsx` con columnas: empresa, industria, país, contacto, teléfono y web |
| Logs detallados | Registro de progreso y errores con Loguru |
| Reintentos automáticos | Lógica de reintentos con backoff exponencial mediante Tenacity |

---

## Vista Previa

<table>
  <tr>
    <td width="50%">
      <img src="assets/cards/01-directorios-industriales.png" width="100%" alt="Tarjeta sobre los directorios industriales Kompass y ThomasNet">
      <br><b>Directorios industriales</b>: Kompass y ThomasNet como fuentes de datos.
    </td>
    <td width="50%">
      <img src="assets/cards/02-evasion-de-deteccion.png" width="100%" alt="Tarjeta sobre la evasión de detección">
      <br><b>Evasión de detección</b>: Playwright Stealth, Camoufox y rotación de user-agent.
    </td>
  </tr>
  <tr>
    <td width="50%">
      <img src="assets/cards/03-exportacion-a-excel.png" width="100%" alt="Tarjeta sobre la exportación a Excel">
      <br><b>Exportación a Excel</b>: archivo <code>.xlsx</code> con columnas listas para el CRM.
    </td>
    <td></td>
  </tr>
</table>

---

## Arquitectura

```mermaid
graph LR
    SCRAPER["Scraper<br/>Python · Playwright"]
    STEALTH["Evasión de detección<br/>Playwright Stealth · Camoufox · fake-useragent"]
    KOMPASS["Kompass<br/>Directorio B2B global"]
    THOMAS["ThomasNet<br/>Proveedores industriales"]
    DATA["Procesamiento<br/>Pandas · OpenPyXL"]
    XLSX[("Archivo Excel<br/>.xlsx")]

    SCRAPER --> STEALTH
    STEALTH -->|"Navegación"| KOMPASS
    STEALTH -->|"Navegación"| THOMAS
    KOMPASS -->|"Datos de empresas"| DATA
    THOMAS -->|"Datos de proveedores"| DATA
    DATA --> XLSX
```

Los reintentos con backoff exponencial (Tenacity) y el registro de eventos (Loguru) acompañan todo el flujo de extracción.

### Fuentes de datos

| Directorio | Descripción |
|-----------|-------------|
| [Kompass](https://kompass.com) | Directorio B2B global con más de 70 millones de empresas en 70 países |
| [ThomasNet](https://thomasnet.com) | Directorio de proveedores industriales en Norteamérica |

---

## Stack Tecnológico

| Capa | Tecnología |
|------|-----------|
| Automatización | Python · Playwright · Playwright-stealth |
| Anti-detección | Camoufox · fake-useragent |
| Procesamiento | Pandas · OpenPyXL |
| Logs | Loguru |
| Reintentos | Tenacity |

---

## Instalación local

> **Aviso:** el código es privado y propietario. Estos pasos son solo para colaboradores autorizados con acceso al repositorio.

1. Instala Python 3.
2. Crea un entorno virtual e instala las dependencias del proyecto.
3. Instala los navegadores de Playwright:
   ```bash
   playwright install
   ```
4. Ejecuta el scraper y revisa el archivo `.xlsx` generado.

---

## Roadmap

- [ ] Agregar más directorios industriales como fuentes de datos.
- [ ] Exportación directa a CRM además de Excel.
- [ ] Panel para configurar industria, país y categoría sin tocar el código.

---

## Contacto

El código fuente es propietario. Para consultas o propuestas, escríbeme:

[![Email](https://img.shields.io/badge/Email-pablozam1931%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:pablozam1931@gmail.com)
[![WhatsApp](https://img.shields.io/badge/WhatsApp-(507)%206517--1870-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)](https://wa.me/50765171870)
[![GitHub](https://img.shields.io/badge/GitHub-deadlyrat-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/deadlyrat)

- Correo: [pablozam1931@gmail.com](mailto:pablozam1931@gmail.com)
- WhatsApp: [(507) 6517-1870](https://wa.me/50765171870)
- GitHub: [github.com/deadlyrat](https://github.com/deadlyrat)

---

*Parte del portafolio de [deadlyrat](https://github.com/deadlyrat)*
