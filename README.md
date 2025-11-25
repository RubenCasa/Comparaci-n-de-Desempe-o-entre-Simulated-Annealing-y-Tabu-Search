# Comparación de Desempeño entre Simulated Annealing (SA) y Tabu Search (TS)

Este documento presenta un análisis comparativo entre los algoritmos **Simulated Annealing (SA)** y **Tabu Search (TS)** aplicados a un problema con un espacio de búsqueda reducido. Se evaluaron tres criterios principales: **precisión**, **eficiencia** y **robustez**.

---

##  Resultados Experimentales

| Algoritmo | Ejecución | Costo (Fitness) | Tiempo (s) | Iteraciones |
|-----------|-----------|------------------|------------|-------------|
| SA | 1 | 85 | 0.000997 | 270 |
| SA | 2 | 85 | 0.000999 | 270 |
| SA | 3 | 85 | 0.002148 | 270 |
| SA | 4 | 85 | 0.001011 | 270 |
| SA | 5 | 85 | 0.001987 | 270 |
| **Promedio SA** | - | **85** | **0.001428** | **270** |
| TS | 1 | 85 | 0.004510 | 100 |
| TS | 2 | 85 | 0.005555 | 100 |
| TS | 3 | 85 | 0.004518 | 100 |
| TS | 4 | 85 | 0.005012 | 100 |
| TS | 5 | 85 | 0.003999 | 100 |
| **Promedio TS** | - | **85** | **0.004719** | **100** |

---

## A. Precisión (Calidad)

Ambos algoritmos alcanzaron el **óptimo global (costo = 85)** en el 100% de las ejecuciones.

Esto se debe a que el **espacio de búsqueda es pequeño**, permitiendo que tanto SA como TS encuentren fácilmente la mejor solución posible.

**Resultado:** Empate técnico.

---

##  B. Eficiencia (Velocidad)

El ganador es **Simulated Annealing (SA)**.

- Fue aproximadamente **3 veces más rápido** que Tabu Search.
- TS requiere más carga computacional por iteración:
  - evalúa múltiples vecinos,
  - revisa la lista tabú.
- SA evalúa **solo un vecino por paso**, lo que lo hace más ligero.

**Resultado:** SA es más eficiente en tiempo.

---

##  C. Robustez (Estabilidad)

Ambos algoritmos mostraron **robustez perfecta en calidad**: todas las ejecuciones encontraron la misma solución.

Sin embargo:

- **Tabu Search (TS)** fue más estable en tiempo de ejecución.
- **Simulated Annealing (SA)** tuvo pequeñas fluctuaciones temporales atribuibles al sistema operativo.

**Resultado:**  
- En calidad → Empate  
- En consistencia temporal → Ventaja ligera para TS

---

## Conclusión General

| Criterio | Ganador |
|---------|---------|
| Precisión | Empate |
| Eficiencia | **SA** |
| Robustez Temporal | **TS** |

En escenarios pequeños, **ambos algoritmos funcionan perfectamente**, pero **SA ofrece la mejor velocidad**, mientras que **TS mantiene tiempos más consistentes**.

---

## Autor / Proyecto
Este documento forma parte de un análisis académico sobre metaheurísticas para optimización.

