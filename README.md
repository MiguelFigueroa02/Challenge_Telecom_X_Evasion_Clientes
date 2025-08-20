<div align= "center">
  <img width="492" height="328" alt="f9eaca2e-9e92-4a5e-ae67-bb0f28157377" src="https://github.com/user-attachments/assets/a9111d35-3279-4a26-a7d3-6f811ec54cc4" />
</div>

# 📊 Análisis de Evasión de Clientes (Churn) en Telecomunicaciones 📉

Este proyecto contiene un análisis detallado sobre los factores que contribuyen a la evasión de clientes (**Churn**) en la industria de las telecomunicaciones. El objetivo es identificar patrones y características de los clientes que cancelan sus servicios para desarrollar estrategias de retención efectivas.

---

## 🔹 Introducción

La evasión de clientes, o **Churn**, representa una amenaza significativa para la rentabilidad de las empresas de telecomunicaciones. Comprender por qué los clientes se van es el primer paso para mitigar este problema. Este análisis explora un conjunto de datos para descubrir las variables clave asociadas con la pérdida de clientes y proporcionar recomendaciones estratégicas.

---

## 🔹 Limpieza y Tratamiento de Datos

El análisis se realizó sobre una base de datos de clientes, siguiendo estos pasos de preprocesamiento:

- **Carga de Datos:** Se importó el conjunto de datos de clientes de telecomunicaciones.
- **Conversión de Tipos:** La columna `TotalCharges` se convirtió a un tipo numérico para su correcto análisis.
- **Manejo de Nulos:** Los valores nulos en `TotalCharges` se imputaron con `0`, asumiendo que corresponden a clientes nuevos.
- **Validación:** Se verificó la consistencia de los datos en columnas categóricas como `InternetService`, donde se confirmó que los clientes con solo internet tenían servicio `DSL`.

---

## 🔹 Análisis Exploratorio de Datos (EDA)

Se realizaron visualizaciones y estadísticas para identificar correlaciones entre las características de los clientes y la tasa de Churn.

- **Tasa de Churn General:** Un 26.5% de los clientes en el conjunto de datos han cancelado sus servicios.
- **Impacto del Servicio de Internet:** Los clientes con **fibra óptica** (`Fiber optic`) muestran la tasa de Churn más alta (más del 40%).
- **Relación con el Tipo de Contrato:** Los clientes con **contratos mensuales** (`Month-to-month`) son el segmento de mayor riesgo, con una tasa de evasión del 42.7%.
- **Influencia del Método de Pago:** El pago a través de **cheque electrónico** (`Electronic check`) está fuertemente asociado con la evasión de clientes.
- **Servicios Adicionales:** La falta de servicios de valor agregado como `OnlineSecurity`, `DeviceProtection` y `TechSupport` incrementa la probabilidad de que un cliente se vaya.

---

## 🔹 Conclusiones e Insights

El análisis ha revelado que la evasión no es un evento aleatorio, sino que está influenciada por factores específicos:

- Los clientes más propensos a la evasión son aquellos que tienen **contratos mensuales**, utilizan **fibra óptica** y pagan con **cheque electrónico**.
- La ausencia de **servicios de seguridad y soporte** reduce la lealtad del cliente.
- El **tipo de contrato** es uno de los predictores más fuertes de la lealtad del cliente.

---

## 🔹 Recomendaciones 🚀

Basado en los hallazgos, se sugieren las siguientes estrategias para la retención de clientes:

1.  **Ofertas de Fidelización:** Proponer a clientes de alto riesgo (contrato mensual, fibra óptica) planes de contrato de un año o dos a precios competitivos.
2.  **Paquetes de Valor:** Promocionar los servicios de seguridad y soporte técnico a clientes con contratos cortos para aumentar la "fricción" de cambio de proveedor.
3.  **Investigación de Causa Raíz:** Realizar encuestas o análisis cualitativos para entender la insatisfacción de los clientes de fibra óptica y mejorar la calidad del servicio.
4.  **Implementación de Alertas Proactivas:** Crear un sistema para identificar automáticamente a los clientes en riesgo de Churn y permitir que el equipo de retención actúe de manera oportuna.
