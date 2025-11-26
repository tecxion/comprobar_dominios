# 🌐 Comprobador de Disponibilidad de Dominios - TecXioN

Bienvenido al repositorio del **Comprobador de Disponibilidad de Dominios**, una herramienta ligera y eficiente desarrollada por TecXioN.

Esta herramienta permite a los usuarios **verificar rápidamente si un nombre de dominio** específico, combinado con las extensiones de nivel superior (TLD) más populares, **está disponible para su registro**.

![GitHub commit activity](https://img.shields.io/github/commit-activity/t/tecxion/comprobar_dominios) ![GitHub last commit](https://img.shields.io/github/last-commit/tecxion/comprobar_dominios) ![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/tecxion/comprobar_dominios)


![GitHub forks](https://img.shields.io/github/forks/tecxion/comprobar_dominios) ![GitHub Repo stars](https://img.shields.io/github/stars/tecxion/comprobar_dominios)

![GitHub language count](https://img.shields.io/github/languages/count/tecxion/comprobar_dominios) ![GitHub top language](https://img.shields.io/github/languages/top/tecxion/comprobar_dominios) ![Static Badge](https://img.shields.io/badge/html-css-green?style=flat-square&logo=html5&logoColor=white)






---

## ✨ Características

* **Verificación Rápida:** Utiliza la API pública de Google DNS para consultar el registro `A` del dominio.
* **Múltiples Extensiones:** Permite seleccionar y comprobar simultáneamente una amplia lista de TLDs populares (ej: `.com`, `.es`, `.net`, `.org`, `.dev`, etc.).
* **Interfaz Sencilla:** Diseño limpio e intuitivo, facilitando la entrada del nombre de dominio y la visualización de los resultados.

---

## 🛠️ Cómo Funciona

La herramienta se basa en la lógica de las **consultas DNS (Sistema de Nombres de Dominio)**.

1.  El usuario ingresa el **nombre base** del dominio (ej: `miempresa`).
2.  Selecciona una o varias **extensiones** (TLDs).
3.  Al hacer clic en "Comprobar Disponibilidad", el script JavaScript realiza una consulta a la API `https://dns.google/resolve` para cada dominio completo (ej: `miempresa.com`, `miempresa.es`).
4.  **Lógica de Disponibilidad:**
    * Si la respuesta de la consulta DNS incluye un **registro de respuesta (`Answer`)** con una **dirección IP**, significa que el dominio ya está registrado y tiene una IP asignada. $\rightarrow$ **NO DISPONIBLE**.
    * Si la respuesta **no incluye** un registro de respuesta (`Answer`), se infiere que el dominio no está registrado y, por lo tanto, es probable que esté **DISPONIBLE** (Nota: Esta es una inferencia común para herramientas de disponibilidad simple, pero no sustituye una consulta WHOIS oficial).

---

## 🚀 Uso Local

Para ejecutar esta herramienta localmente, simplemente sigue estos pasos:

1.  Clona o descarga este repositorio.
    ```bash
    git clone [https://github.com/tu_usuario/nombre_del_repo.git](https://github.com/tu_usuario/nombre_del_repo.git)
    ```
2.  Abre el archivo `index.html` en tu navegador web.

> **Importante:** La herramienta realiza peticiones a una API externa (`https://dns.google/resolve`), por lo que necesita una **conexión a internet** para funcionar.

---

## 🔗 Enlaces de Interés de TecX

Además de esta herramienta, en nuestra web encontrarás otras utilidades:

* **[FIT URL](https://www.tecxart.es/fiturl)**: Acortador de enlaces.
* **https://en.wikipedia.org/wiki/IP_address(https://tecxart.es/ipnombre/)**: Convierte una URL a su dirección IP.
* **[Geolocalizar IP](https://tecxart.es/server/public/)**: Herramienta para geolocalizar direcciones IP.
* **[TecXion Github](https://github.com/tecxion)**: Nuestro perfil principal de GitHub.

---

## 👨‍💻 Autor y Licencia

Creado por **TcX** (TecXarT.es) - 2025.

Este proyecto se distribuye bajo la licencia **[Inserta tu licencia aquí, ej: MIT, Apache, etc.]**.