Mi recomendación

Recomendamos aprobar con condiciones porque encontramos indicios de posibles sesgos entre grupos, aunque el modelo obtuvo una accuracy aproximada del 85%. La evidencia principal fue que variables como relationship actuaron como proxies de atributos sensibles, además de diferencias en el desempeño entre grupos. Antes de implementarlo debería evaluarse la equidad con métricas por grupo, revisar las variables proxy y realizar pruebas adicionales en distintos contextos.

Hallazgo

El modelo logró un buen rendimiento general, pero algunas variables presentan una fuerte asociación con atributos sensibles, lo que puede generar decisiones desiguales.

Evidencia

La variable capital-gain tuvo el coeficiente positivo más alto (2.302, odds ratio ≈ 9.995), mientras que categorías de relationship y marital-status aparecieron entre las asociaciones más fuertes, indicando posibles variables proxy.

Riesgo/personas afectadas

Personas pertenecientes a determinados grupos demográficos podrían recibir predicciones menos favorables debido a correlaciones presentes en los datos, afectando decisiones relacionadas con ingresos o acceso a oportunidades.

Decisión y controles

Aprobar con condiciones. Antes del despliegue se deben:

Evaluar métricas de equidad por grupos.
Revisar variables que funcionen como proxies.
Documentar las limitaciones del modelo.
Monitorear continuamente el rendimiento y los posibles sesgos.
Lo que aún no sabemos

No se conoce si el modelo mantendrá el mismo desempeño en otros conjuntos de datos o poblaciones distintas, ni si los sesgos aumentarán con datos futuros.

Mi selección inicial y comparación con la referencia
Utilicé variables como education-num, capital-gain, occupation, marital-status y relationship. El rendimiento fue similar al modelo de referencia, aunque observé diferencias en algunas métricas entre grupos. La decisión de selección con mayor impacto fue conservar variables altamente correlacionadas con el ingreso, ya que mejoraron la precisión, pero también incrementaron el riesgo de sesgo indirecto.

Lo que cambiaría después del taller

Eliminaría o analizaría con mayor profundidad las variables proxy, aplicaría métricas de equidad desde el inicio y documentaría todas las decisiones de limpieza y selección de variables.