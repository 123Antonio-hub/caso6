# caso 6 

Ciclo de comprensión: Predicción vs. Realidad

1. Predicción inicial (intuición): Se esperaría que B terminara primero y recorriera menos distancia por colocar las categorías más pedidas (\(X\) e \(Y\)) en los estantes más cercanos (\(L_{1}\) y \(L_{2}\)), cumpliendo fácilmente el minuto 38.
2. Contraste con el cálculo: La intuición acierta en que B recorre menos distancia (968 m), pero falla en la puntualidad. Al agrupar las categorías frecuentes en el mismo corredor, la congestión de B dispara su tiempo total a 40,70 min, convirtiéndola en la más lenta. C recorre un poco más (1.040 m), pero reparte el tráfico, reduce la congestión y termina primero (37,67 min).
3. Explicación (agregado vs. terminación): El trabajo manual es fijo (108 s/pedido). En B, la suma agregada es 119,73 min-persona (aparentemente menor al límite de 120 min-persona del equipo), pero como los pedidos no se dividen equitativamente (17, 17 y 16) y las esperas se concentran en los pedidos \(XY\), las personas 1 y 2 rebasan los 40 minutos.

Parte 1: Análisis de Operaciones y Cronograma


1. Plano, matriz de distancias y frecuencia de viajes

El plano tiene origen en \(O=(0,0)\) y estantes en \(L_1=(2,0)\), \(L_2=(8,0)\), \(L_3=(2,6)\) y \(L_4=(8,6)\). Usando distancia Manhattan (\(\vert{}x_2-x_1\vert{}+\vert{}y_2-y_1\vert{}\)):

Desde / Hasta	\(O (0,0)\)	\(L_1 (2,0)\)	\(L_2 (8,0)\)	\(L_3 (2,6)\)	\(L_4 (8,6)\)
\(O (0,0)\)	0 m	2 m	8 m	8 m	14 m
\(L_1 (2,0)\)	2 m	0 m	6 m	6 m	12 m
\(L_2 (8,0)\)	8 m	6 m	0 m	12 m	6 m
\(L_3 (2,6)\)	8 m	6 m	12 m	0 m	6 m
\(L_4 (8,6)\)	14 m	12 m	6 m	6 m	0 m

• Frecuencia de categorías (100 retiros en total): \(X\) aparece en 42 pedidos (\(24+12+6\)), \(Y\) en 32 (\(24+8\)), \(Z\) en 20 (\(12+8\)) y \(W\) en 6.
• Frecuencia de viajes completos (50 ciclos \(O \to C_1 \to C_2 \to O\)): \(XY = 24\) viajes (48 %), \(XZ = 12\) viajes (24 %), \(YZ = 8\) viajes (16 %) y \(XW = 6\) viajes (12 %). El recorrido depende de la combinación del par, no de cada categoría aislada.
Cursograma analítico por pedido (estructura base):
• Operaciones (5): Leer/identificar en \(O\) (pasos 1–2), retirar libro 1 (paso 4), retirar libro 2 (paso 6), empacar/marcar en \(O\) (paso 9) y registrar (paso 10).
• Inspección (1): Cotejar títulos y cantidades en \(O\) (paso 8).
• Transportes (3): Ir de \(O\) a estante 1 (paso 3), ir de estante 1 a estante 2 (paso 5) y regresar de estante 2 a \(O\) (paso 7).
• Demoras (1): Espera por congestión en pasillos/estantes durante el recorrido.

2. Tiempo manual estándar (\(TE\)) y distancias ponderadas

Sumando los promedios de los 5 elementos manuales (\(10 + 15 + 15 + 20 + 30 = 90\text{ s}\)):
• Tiempo Normal (\(TN\)): \(90\text{ s/pedido}\).
• Tiempo Estándar (\(TE\)): \(90 \times 1,20 = \mathbf{108\text{ s/pedido}}\) (\(5.400\text{ s} = 90\text{ min-persona}\) para los 50 pedidos).
Al caminar a \(1\text{ m/s}\), cada metro equivale a \(1\text{ s}\):

Tipo pedido (Cant.)	Ruta A (\(L_4,L_3,L_2,L_1\))	Dist. A	Ruta B (\(L_1,L_2,L_3,L_4\))	Dist. B	Ruta C (\(L_1,L_3,L_4,L_2\))	Dist. C
XY (24)	\(O-L_4-L_3-O\)	\(28\text{ m}\)	\(O-L_1-L_2-O\)	\(16\text{ m}\)	\(O-L_1-L_3-O\)	\(16\text{ m}\)
XZ (12)	\(O-L_4-L_2-O\)	\(28\text{ m}\)	\(O-L_1-L_3-O\)	\(16\text{ m}\)	\(O-L_1-L_4-O\)	\(28\text{ m}\)
YZ (8)	\(O-L_3-L_2-O\)	\(28\text{ m}\)	\(O-L_2-L_3-O\)	\(28\text{ m}\)	\(O-L_3-L_4-O\)	\(28\text{ m}\)
XW (6)	\(O-L_4-L_1-O\)	\(28\text{ m}\)	\(O-L_1-L_4-O\)	\(28\text{ m}\)	\(O-L_1-L_2-O\)	\(16\text{ m}\)
Total 50 pedidos	—	1.400 m	—	968 m	—	1.040 m


3 y 4. Congestión, diagrama de actividades múltiples y selección

Tiempo total por pedido = \(TE\ (108\text{ s}) + \text{Caminar} + \text{Congestión}\):
• Alternativa A: Todos los pedidos duran \(108 + 28 + 2 = 138\text{ s}\).
• Alternativa B: \(XY = 144\text{ s}\), \(XZ = 140\text{ s}\), \(YZ = 142\text{ s}\), \(XW = 152\text{ s}\).
• Alternativa C: \(XY = 128\text{ s}\), \(XZ = 140\text{ s}\), \(YZ = 140\text{ s}\), \(XW = 128\text{ s}\).
Resumen comparativo y diagrama de actividades múltiples (secuencia fija \(XY \to XZ \to YZ \to XW\)):

Métrica	Alternativa A (Actual)	Alternativa B (Cercana)	Alternativa C (Repartida)
Inversión	0 u. m.	150 u. m.	240 u. m.
Distancia / Caminar	1.400 m (1.400 s)	968 m (968 s)	1.040 m (1.040 s)
Congestión total	100 s	816 s	200 s
Tiempo agregado	6.900 s (115,00 min-p)	7.184 s (119,73 min-p)	6.640 s (110,67 min-p)
Fin Persona 1 (17 ped.)	2.346 s (39,10 min)	2.442 s (40,70 min)	2.260 s (37,67 min)
Fin Persona 2 (17 ped.)	2.346 s (39,10 min)	2.442 s (40,70 min)	2.260 s (37,67 min)
Fin Persona 3 (16 ped.)	2.208 s (36,80 min)	2.300 s (38,33 min)	2.120 s (35,33 min)
Pedidos listos al min 38	48 / 50 (16+16+16)	45 / 50 (15+15+15)	50 / 50 (17+17+16)
Pedidos listos al min 40	50 / 50 (17+17+16)	48 / 50 (16+16+16)	50 / 50 (17+17+16)

• Cronograma de bloques por persona (en minutos acumulados):
	• Alt. A: P1 y P2 terminan \(8\,XY\) (\(18,40'\)), \(4\,XZ\) (\(27,60'\)), \(3\,YZ\) (\(34,50'\)), \(2\,XW\) (\(39,10'\)). P3 termina en \(36,80'\). Al min 38 faltan 2 pedidos \(XW\) (uno de P1 y uno de P2).
	• Alt. B: P1 y P2 terminan \(8\,XY\) (\(19,20'\)), \(4\,XZ\) (\(28,53'\)), \(3\,YZ\) (\(35,63'\)), \(2\,XW\) (\(40,70'\)). P3 termina en \(38,33'\). Al min 38 faltan 5 pedidos; al min 40 aún quedan 2 pedidos \(XW\) sin terminar.
	• Alt. C: P1 y P2 terminan \(8\,XY\) (\(17,07'\)), \(4\,XZ\) (\(26,40'\)), \(3\,YZ\) (\(33,40'\)), \(2\,XW\) (\(37,67'\)). P3 termina en \(35,33'\). Todos terminan antes del minuto 38.
Decisión: Se selecciona la Alternativa C por ser la única que cumple el compromiso de los 50 pedidos antes del minuto 38 y cabe en el presupuesto de 240 u. m.

5. Productividad puntual y efecto de la congestión

El denominador disponible es \(3 \times \frac{40}{60} = \mathbf{2\text{ horas-persona}}\).
• Productividad en la ventana completa de 40 min:
	• A: \(50 / 2 = \mathbf{25,0\text{ pedidos/h-persona}}\).
	• B: \(48 / 2 = \mathbf{24,0\text{ pedidos/h-persona}}\).
	• C: \(50 / 2 = \mathbf{25,0\text{ pedidos/h-persona}}\).
• Productividad puntual al compromiso del minuto 38 (sobre las 2 h-persona disponibles):
	• A: \(48 / 2 = \mathbf{24,0\text{ pedidos/h-persona}}\).
	• B: \(45 / 2 = \mathbf{22,5\text{ pedidos/h-persona}}\).
	• C: \(50 / 2 = \mathbf{25,0\text{ pedidos/h-persona}}\).
¿Qué cambia al incorporar congestión? Si solo se evaluara distancia, B parecería ahorrar 72 segundos frente a C (\(968\text{ s}\) vs. \(1.040\text{ s}\)). Sin embargo, la congestión en B añade \(816\text{ s}\) frente a solo \(200\text{ s}\) en C, generando una penalización neta de \(+616\text{ s}\) que revierte por completo la ventaja del menor recorrido y saca a B de la ventana operativa.

6. Análisis de sensibilidad (\(f = 0,10\) y puntos de igualdad)

Multiplicando las demoras de congestión por \(f = 0,10\) (como escenario hipotético, no mejora demostrada):
• Alternativa B (\(f=0,10\)): Tiempo agregado = \(5.400 + 968 + 81,6 = \mathbf{6.449,6\text{ s}}\) (107,49 min-persona). Última terminación (P1/P2) = \(2.195,4\text{ s}\) (36,59 min).
• Alternativa C (\(f=0,10\)): Tiempo agregado = \(5.400 + 1.040 + 20,0 = \mathbf{6.460,0\text{ s}}\) (107,67 min-persona). Última terminación (P1/P2) = \(2.198,8\text{ s}\) (36,65 min).
Puntos de igualdad entre B y C:
1. En minutos-persona agregados:
\(5.400+968+816f=5.400+1.040+200f\implies 616f=72\implies \mathbf{f=0,1169}\ (11,69\,\%)\)
2. En la última terminación individual (Persona 1 o Persona 2, con 17 pedidos):
	• Persona 1 en B: \(1.836\text{ manual} + 332\text{ caminar} + 274f\text{ congestión}\).
	• Persona 1 en C: \(1.836\text{ manual} + 356\text{ caminar} + 68f\text{ congestión}\).
\(2.168+274f=2.192+68f\implies 206f=24\implies \mathbf{f=0,1165}\ (11,65\,\%)\)
Contraste: Si la congestión de B lograra reducirse a menos del 11,65 % de su valor medido (por ejemplo, en \(f=0,10\)), B superaría ligeramente a C en tiempo agregado y última terminación, cumpliendo ambas el minuto 38 y haciendo preferible a B por ahorrar 90 u. m. de inversión. Como el piloto real tiene \(f = 1,00\), C sigue siendo la decisión correcta.

Parte 2: Muestreo del Trabajo y Antropometría


1. Muestreo piloto de A (\(N = 180\) observaciones)

• Retiro, lectura y empaque: \(117 / 180 = \mathbf{65,0\,\%}\)
• Desplazamiento (caminar): \(36 / 180 = \mathbf{20,0\,\%}\)
• Búsqueda de ubicación: \(18 / 180 = \mathbf{10,0\,\%}\)
• Espera por congestión: \(9 / 180 = \mathbf{5,0\,\%}\)
Categorías mutuamente excluyentes para el muestreo posterior a la redistribución:
1. Trabajo manual productivo en estación (\(O\)) o estante: Leer pedido, tomar libro físico ya localizado, cotejar, empacar o registrar en bandeja.
2. Desplazamiento efectivo: Caminar activamente entre \(O\) y los estantes sin detenerse.
3. Búsqueda visual / desorientación: Detenerse frente al estante o pasillo buscando la nueva ubicación de una categoría sin tomar aún el libro (clave tras reubicar en C).
4. Demora por congestión: Esperar detenido o ceder paso debido a que otra persona bloquea el estante o corredor.
5. Inactividad / suplementos / otros: Pausa personal, recuperación o espera no relacionada con el flujo.

2. Evaluación ergonómica y criterio didáctico

Al comparar las dimensiones físicas del puesto contra los percentiles/valores de las tres personas:

Dimensión del puesto	Medida actual	Valores del personal (P1, P2, P3)	Evaluación ergonómica
Profundidad de paquetes frecuentes	46 cm	Alcance cómodo: 34, 39 y 44 cm	Inadecuada para las 3 personas. Excede incluso el alcance máximo (44 cm), obligando a flexionar el tronco y generando fatiga lumbar.
Altura de mesa fija	98 cm	Altura de codo: 94, 102 y 110 cm	Adecuada para P2 (102 cm) (trabajo ligero justo debajo del codo), ligeramente alta para P1 (94 cm, eleva hombros) y baja para P3 (110 cm, encorva espalda).

Criterio didáctico (ajuste del puesto antes de exigir ritmo): Antes de exigir estándares de tiempo o redistribuir estantes, se debe acercar la zona de paquetes frecuentes a \(\le 34\text{ cm}\) de profundidad para cubrir al operador de menor alcance (principio de diseño para el extremo menor) y colocar un tapete/tarima de 4 cm para P1 o ajustar la superficie de trabajo en \(O\).
Si deseas que prepare algún material entregable para tu equipo, dime si necesitas:
• Un esquema visual en texto/ASCII del plano cartesiano y el diagrama de Gantt (actividades múltiples) listo para copiar a tu documento
• Las fórmulas exactas en Excel para automatizar la tabla de sensibilidad y el cálculo de tiempos por persona
Mostrar el código
