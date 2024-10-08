# Primer-dia-en-la-oficina
Este reto de algoritmos implica la planificación y optimización de tareas con dependencias temporales y de recursos. Vamos a resolverlo paso a paso:

### **1. Definir el Objetivo del Proyecto:**
El objetivo principal del proyecto es asegurar que el CEO llegue a tiempo al vuelo a Barcelona desde Madrid, con todos los documentos necesarios y las maletas, para asistir a la reunión crucial a las 19:30. Esto implica completar todas las tareas necesarias antes de que cierre la facturación del vuelo en un máximo de 100 minutos.

### **2. Diagrama de Flujo del Cronograma:**
Para representar correctamente el flujo de las tareas, primero debemos identificar las dependencias entre ellas. Algunas tareas son independientes, mientras que otras requieren que una tarea previa esté completada. A continuación, organizamos las tareas con sus respectivas duraciones:

- **A:** Reserva de vuelo (20 min)
- **B:** Informar a casa para empacar (5 min) → Necesario antes de **C** y **G**
- **C:** Empacar maletas (40 min) → Depende de **B**
- **D:** Preparación del billete por la agencia (10 min) → Antes de **E**
- **E:** Recoger el billete de la agencia (5 min) → Después de **D**
- **F:** Llevar el billete a la oficina (10 min) → Después de **E**
- **G:** Recoger maletas de casa (20 min) → Después de **C**
- **H:** Llevar maletas a la oficina (25 min) → Después de **G**
- **I:** Conversación sobre documentos requeridos (35 min)
- **J:** Dictar instrucciones para ausencia (25 min)
- **K:** Reunir documentos (15 min) → Antes de **L**
- **L:** Organizar documentos (5 min) → Después de **K**
- **M:** Viajar al aeropuerto y facturar (25 min) → Última tarea

### **Dependencias Identificadas:**
- **B → C → G → H**
- **D → E → F**
- **K → L**
- **M** es la última tarea en completarse.

### **Diagrama de Flujo:**
El diagrama de flujo sería una representación visual, pero de manera simplificada podemos describirlo:

1. **B (5 min)** → **C (40 min)** → **G (20 min)** → **H (25 min)**
2. **D (10 min)** → **E (5 min)** → **F (10 min)**
3. **I (35 min)**, **J (25 min)** (independientes)
4. **K (15 min)** → **L (5 min)**
5. **M (25 min)** (final task)

### **3. Nivelación de Recursos:**
Ahora vamos a optimizar el uso de los recursos minimizando el tiempo total. Primero, tenemos que identificar cuáles tareas se pueden hacer en paralelo y cuáles deben ser secuenciales.

#### Tareas que se pueden hacer en paralelo:
- **A:** Reserva del vuelo es independiente, puede ocurrir en paralelo con otras tareas.
- **B**, **C**, **D**, y **K** no dependen entre sí, por lo que pueden comenzar simultáneamente.
- **I** y **J** también son independientes.

#### Cronograma Optimizado:
Vamos a asignar tareas que pueden ejecutarse en paralelo y secuenciar aquellas con dependencias claras. Nuestro objetivo es completar todo en menos de 100 minutos.

1. **Minuto 0:**
   - **A (20 min)**: Reserva de vuelo.
   - **B (5 min)**: Informar a casa para empacar.
   - **D (10 min)**: Preparación del billete por la agencia.
   - **K (15 min)**: Reunir documentos.
   
2. **Minuto 5:**
   - **C (40 min)**: Empacar maletas (inicia después de **B**).

3. **Minuto 15:**
   - **E (5 min)**: Recoger el billete de la agencia (inicia después de **D**).

4. **Minuto 20:**
   - **F (10 min)**: Llevar el billete a la oficina (inicia después de **E**).
   - **I (35 min)**: Conversación sobre documentos requeridos.

5. **Minuto 40:**
   - **G (20 min)**: Recoger maletas de casa (inicia después de **C**).
   - **L (5 min)**: Organizar documentos (inicia después de **K**).

6. **Minuto 60:**
   - **H (25 min)**: Llevar maletas a la oficina (inicia después de **G**).
   - **J (25 min)**: Dictar instrucciones para ausencia.

7. **Minuto 85:**
   - **M (25 min)**: Viajar al aeropuerto y facturar.

### **Duración Total:**
El tiempo total mínimo, siguiendo este esquema optimizado, es **85 minutos**. Esto asegura que el CEO llega a tiempo al aeropuerto con todos los preparativos listos.

### **Conclusión:**
La planificación óptima ha permitido que todas las tareas se completen en **85 minutos**, lo que cumple con el objetivo de tener suficiente tiempo antes de que cierre la facturación del vuelo, utilizando un enfoque paralelo cuando es posible para maximizar la eficiencia.
