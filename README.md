<div align= "center">
  <img width="492" height="328" alt="f9eaca2e-9e92-4a5e-ae67-bb0f28157377" src="https://github.com/user-attachments/assets/a9111d35-3279-4a26-a7d3-6f811ec54cc4" />
</div>

# 📊 Análisis de Evasión de Clientes 📉

<div align="center">
  
![Python](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-Cloud-yellow?logo=googlecolab&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-Repo-black?logo=github&logoColor=white)

</div>

Este proyecto contiene un análisis detallado sobre los factores que contribuyen a la evasión de clientes (**Churn**) a partir de la base de datos de la empresa Telecom X. El objetivo fue identificar patrones y características de los clientes que cancelan sus servicios para identificar cuáles son los factores que influyen de mayor manera en la cancelación.

---

## 🔹 Introducción

La evasión de clientes, o **Churn**, representa una amenaza significativa para la rentabilidad de las empresas de telecomunicaciones. Comprender por qué los clientes se van es el primer paso para mitigar este problema. Este análisis explora un conjunto de datos para descubrir las variables clave asociadas con la pérdida de clientes y proporcionar recomendaciones estratégicas.

---

## 🔹 Limpieza y Tratamiento de Datos

El análisis se realizó sobre una base de datos de clientes de la empresa Telecom X, siguiendo estos pasos de preprocesamiento:

- **Carga de Datos:** Se importó el conjunto de datos de clientes de telecomunicaciones a partir de una base de datos con formato de archivo json.
- **Tratamiento de la información** Por medio de la biblioteca de Pandas y Numpy se fueron evaluando y transformando los datos de cada columna de acuerdo al objetivo para evaluar de cada una.
- **Conversión de Tipos:** Modificación del formato en el cual se obtiene la información para facilitar el procesamiento de los datos en las próximas etapas.
- **Manejo de Nulos:** Se evalúo cada caso de las columnas que presentaban valores nulos para determinar si se transformaban o se eliminaban los datos de acuerdo a las características del Data set.

---

## 🔹 Análisis de los datos

Se realizaron visualizaciones por medio de Plotly express y estadísticas para identificar correlaciones entre las características de los clientes y la tasa de Churn. Este análisis abarcó los siguientes datos.

<details>
  <summary>
    Evaluación del perfil de los clientes con relación a la tasa de cancelación.
  </summary>
  Podemos resaltar los siguientes puntos: 
  
- Un 26.5% de los clientes en el conjunto de datos han cancelado sus   servicios.
  
- Se descartan que el factor de la edad influya en la cancelación.
  <img width="600" height="600" alt="newplot (2)" src="https://github.com/user-attachments/assets/7e995c28-b869-4e0c-8f77-ff7dbc173a52" />

- En general, nuestros clientes no cuentan con dependientes. Esta caracterización tampoco influye en la cancelación.
<img width="600" height="600" alt="newplot (3)" src="https://github.com/user-attachments/assets/97917b93-f3b2-485b-996b-9cf97e88af59" />

- Alrededor del 90% de nuestros usuarios cuentan con el servicio telefónico. Al no observarse variación de esta relación entre los clientes que cancelan con los que permanecen en la compañía podemos determinar que este servicio influya en el índice de cancelación general.
<img width="1100" height="600" alt="newplot (4)" src="https://github.com/user-attachments/assets/e8468467-4904-4363-8b6b-d2c63eb12438" />

- Entre el 50% y el 60% de los usuarios no cuentan con el servicio de StreamingTV. Al igual que el caso anterior, este servicio no presenta impacto directo con la cancelación.
<img width="1100" height="600" alt="newplot (5)" src="https://github.com/user-attachments/assets/9551b568-9559-4224-a2c6-83676ea66973" />

</details>

<details>
  <summary> Impacto del Servicio de Internet. </summary>
De manera general, podemos indicar lo siguiente:
  
- La empresa cuenta con 5 tipos de servicios diferentes. Solo en uno de ellos no presta el servicio de internet, el cual corresponde al 21.7% de los usuarios. Estos cuentan únicamente con el servicio telefónico. La proporción de cancelación de estos clientes con respecto a los que cuentan con el servicio general de internet representa apenas el 6% general y su índice de cancelación parece estar influido por el método de pago a través de MailedCheck, el periodo de permanencia en la empresa (a menor tiempo, mayor índice de cancelación) y el tipo de contrato (mes a mes), reflejando esto último en la columna total gastado.
<img width="700" height="600" alt="newplot (8)" src="https://github.com/user-attachments/assets/c4f9d7ae-6ea7-4def-9bbe-63b86468e0f6" />

<img width="600" height="700" alt="newplot (9)" src="https://github.com/user-attachments/assets/a2c53e18-6785-4ddc-b3ad-defe0309b588" />

- Comparando todos ambos tipos de servicios de internet, encontramo que los clientes que cancelan el servicio cuentan, en su mayoría, con el servicio de fibra óptica contratado. Por lo que se sugeriría evaluar la experiencia de los usuarios que cuentan con este servicio y el tipo de servicios complementarios relacionados con este tipo de internet que, como veremos más adelante, impacta a la calidad del servicio.
<img width="700" height="600" alt="newplot (11)" src="https://github.com/user-attachments/assets/b7ff48b7-ad31-42a8-a395-3f54c2706640" />


</details>

<details>
  <summary>
    Relación con el Tipo de Contrato
  </summary>
- En su mayoría los clientes cuentan con un tipo de contrato mes a mes. Sin embargo, existe una relación directa entre los clientes que cuentan con este tipo de contrato con la cancelación, los cuales representan el 88.6%. Caso contrario ocurre con los clientes que cuentan con el tipo de contrato de 2 años, los cuales han cancelado únicamente el 2.8%.
<img width="600" height="600" alt="newplot (12)" src="https://github.com/user-attachments/assets/7ff35f55-d885-4295-842c-8603503d78cc" />

<img width="700" height="600" alt="newplot (13)" src="https://github.com/user-attachments/assets/380b0081-7554-4694-b95d-db9b25b9637f" />

- Esto se visualiza directamente en el índice de cancelación que se obtiene durante los primeros meses, el cual cae drásticamente conforme mayor es el tiempo de contrato que un cliente ha permanecido en la compañía, lo cual se estudia en la columna ternure.
<img width="1100" height="600" alt="newplot (14)" src="https://github.com/user-attachments/assets/2cf73b8e-7836-40db-a5ba-b1964e68e680" />

<img width="1100" height="600" alt="newplot (15)" src="https://github.com/user-attachments/assets/8dd74608-da94-42ff-a737-722e462dd2b8" />

</details>

<details>
  <summary>
    Influencia del Método de Pago
  </summary>
- De manera general y, con excepción de los usuarios que únicamente tienen el servicio telefónico, los clientes que cancelan más son aquellos que cuentan con el método de pago Electronic check. Se recomienda evaluar este con respecto al tipo de contrato de mes a mes para determinar el grado de influencia que tienen con la cancelación.
<img width="700" height="600" alt="newplot (16)" src="https://github.com/user-attachments/assets/c86d0820-62c4-4f1d-96dd-4b3a4d35d100" />

- De igual manera, entre los clientes que cancelan se presenta en su mayoría la opción de paperless billing. Si bien de manera general se observa este caso, se ve en mayor cantidad entre los clientes que cancelan, lo que permite caracterizar su comportamiento.
<img width="1100" height="600" alt="newplot (18)" src="https://github.com/user-attachments/assets/e1d5056c-bfae-4dc7-8871-00b80178da74" />

</details>

<details>
  <summary>
    Servicios Adicionales
  </summary>
- Dada la alta cantidad de usuarios que cuentan con el servicio de internet, el cual representa aproximadamente el 78.3%, se detectó que existe una relación directa entre los clientes que cancelan el servicio con el uso de estos de los servicios complementarios de `OnlineSecurity`, `OnlineBackup`,  `DeviceProtection` y `TechSupport`.
Por lo que parte de la estrategia comercial de la empresa pudiera estar enfocada en la promoción de estos.
<img width="1100" height="600" alt="newplot (19)" src="https://github.com/user-attachments/assets/82a75095-8a29-4ffe-ae20-3eb80fa6d768" />

<img width="1100" height="600" alt="newplot (20)" src="https://github.com/user-attachments/assets/a90b4293-9b2c-4daf-a5f6-fce39e029db2" />

<img width="1100" height="600" alt="newplot (21)" src="https://github.com/user-attachments/assets/05c8a73c-b668-451b-9a33-bbe6b70fa27f" />

<img width="1100" height="600" alt="newplot (22)" src="https://github.com/user-attachments/assets/037afa06-922f-4557-8f98-927ec0278526" />

</details>

---

## 🔹 Conclusiones e Insights

El análisis ha revelado que la evasión no es un evento aleatorio, sino que está influenciada por factores específicos:

- Los clientes más propensos a la evasión son aquellos que tienen **contratos mensuales**, utilizan **fibra óptica** y pagan con **cheque electrónico**.
- La ausencia de **servicios de seguridad y soporte** reduce la lealtad del cliente.
- El **tipo de contrato** es uno de los predictores más fuertes de la lealtad del cliente, ya que encontramos 

---

## 🔹 Recomendaciones 🚀

Basado en los hallazgos, se sugieren las siguientes estrategias para la retención de clientes:

1.  **Ofertas de Fidelización:** Proponer a clientes de alto riesgo (contrato mensual, fibra óptica) planes de contrato de un año o dos a precios competitivos.
2.  **Paquetes de Valor:** Promocionar los servicios de seguridad y soporte técnico a clientes con contratos cortos para aumentar la "fricción" de cambio de proveedor.
3.  **Investigación de Causa Raíz:** Realizar encuestas o análisis cualitativos para entender la insatisfacción de los clientes de fibra óptica y mejorar la calidad del servicio.
4.  **Implementación de Alertas Proactivas:** Crear un sistema para identificar automáticamente a los clientes en riesgo de Churn y permitir que el equipo de retención actúe de manera oportuna.
