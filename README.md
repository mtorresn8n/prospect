# Herramienta Interna Rent a Car — Localiza

Este repositorio contiene una **herramienta web interna** para los equipos de Localiza, orientada a facilitar distintos módulos operativos de la gestión de Rent a Car. Por ahora incluye:

- ✅ **Corporativo**  
- ✅ **Reservas & Reportes**

---

## 🎯 Módulo: Corporativo

### ¿Qué es?
Una interfaz de prospección comercial para los ejecutivos de ventas de Localiza.  

### Funcionalidades principales
- **Registro “en caliente”** de clientes actuales o potenciales durante eventos, reuniones o visitas.
- **Envío instantáneo** de información personalizada (descuentos, promociones, info corporativa).
- **Guardado automático** de cada contacto en el histórico.
- **Enriquecimiento de datos** vía IA: detecta y añade emails alternativos, redes sociales, ubicación, rubro, etc.
- **Modo offline**: si no hay conexión, almacena localmente y envía cuando se restablece la red.
- **Reinicio automático** del formulario listo para el siguiente prospecto.

### Flujo de trabajo
1. El ejecutivo elige su nombre y completa datos básicos:  
   `Nombre`, `Empresa`, `Email`, `Teléfono`, `Rubro`, `Comentario`.
2. Selecciona el tipo de información (p. ej. “Voucher de descuento” + porcentaje).  
3. El sistema genera un correo con IA y lo remite al cliente.  
4. La respuesta queda registrada mediante un webhook en Make.  
5. El módulo IA extrae más datos públicos del cliente en internet.  

### Beneficios
- Acelera la carga de leads y evita pérdida de datos.  
- Aumenta la tasa de conversión con envíos instantáneos.  
- Disminuye el trabajo administrativo post-venta.

---

## 🛠️ Módulo: Reservas & Reportes

### ¿Qué es?
Conjunto de herramientas para analizar y comparar periodos de reservas en toda la red de agencias.

### Principales cálculos y métricas
- **Last Year vs Current Year** (LY / Act)  
- **Variaciones (%)** y diferencias absolutas  
- **Segmentos**: Oficial, Promo, Corporativo, Recaudación, Tour, Pendiente, Otorgado, etc.  
- **OT**, **TR**, **PN**, **CO**, **RE**...  
- **Filtros dinámicos** por región, agencia y tipo de reserva.  
- **Tablas interactivas** con expansión de agencias, mostrar/ocultar columnas, estilos y agrupaciones.

### Flujo de trabajo
1. Subir o generar el `reportePorMes` en JSON.  
2. Renderizarlo en HTML+JS con:  
   - Encabezados dinámicos (colspan según métricas).  
   - Ordenación automática por “distribución.Act”.  
   - Botones de filtro y control de visibilidad.  
3. Descargar o publicar el HTML resultante.

### Beneficios
- Visualización rápida de tendencias año vs año.  
- Identificación inmediata de oportunidades o áreas de mejora.  
- Herramienta 100 % web, sin instalaciones adicionales.

---

## 📦 Estructura del proyecto

