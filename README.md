# 🌳 Gramáticas y Árboles de Derivación Sintáctica

Documento de resolución y análisis de los diagramas sintácticos en forma de árbol correspondientes a la Filmina 11 de **Lenguajes y Autómatas** (*Técnicas de Procesamiento del Habla*).

---

## 📑 Resumen General de Oraciones

| N° | Oración | Estructura Principal del Sintagma Nominal (SN) | Estructura Principal del Sintagma Verbal (SV) |
|---|---|---|---|
| **1** | *Los aztecas hablaban náhuatl.* | `Det + N` | `V + SN` |
| **2** | *La dominación islámica disminuyó progresivamente.* | `Det + N + SAdj` | `V + SAdv` |
| **3** | *Los reyes católicos conquistaron Granada.* | `Det + N + SAdj` | `V + SN` |
| **4** | *El catalán es una lengua romance.* | `Det + N` | `V + SN (Det + N + SAdj)` |
| **5** | *Los mayas resistieron la colonización española.* | `Det + N` | `V + SN (Det + N + SAdj)` |
| **6** | *Los sacerdotes evangelizaban a los indígenas.* | `Det + N` | `V + SP (P + SN)` |
| **7** | *Las lenguas minoritarias de España han entrado en una nueva etapa.* | `Det + N + SAdj + SP` | `V + SP (P + SN)` |
| **8** | *El español es lengua oficial en diecinueve países de Latinoamérica.* | `Det + N` | `V + SN + SP (P + SN + SP)` |
| **9** | *El terreno de Paraguay representaba desafíos de envergadura para los españoles.* | `Det + N + SP` | `V + SN (N + SP) + SP` |
| **10** | *Los niños monolingües de desarrollo normal pasan por varias etapas.* | `Det + N + SAdj + SP` | `V + SP (P + SN)` |

---

## 🔍 Análisis Detallado de Árboles de Derivación

### 1. Oración: *"Los aztecas hablaban náhuatl."*

* **Estructura jerárquica:**
  * **O (Oración)** $\rightarrow$ **SN + SV**
  * **SN (Sintagma Nominal)** $\rightarrow$ **Det** (*Los*) + **N** (*aztecas*)
  * **SV (Sintagma Verbal)** $\rightarrow$ **V** (*hablaban*) + **SN** $\rightarrow$ **N** (*náhuatl*)

```
               O
       ________|________
      |                 |
     SN                SV
   ___|___          ____|____
  |       |        |         |
 Det      N        V        SN
  |       |        |         |
Los    aztecas  hablaban     N
                             |
                          náhuatl
```

---

### 2. Oración: *"La dominación islámica disminuyó progresivamente."*

* **Estructura jerárquica:**
  * **O** $\rightarrow$ **SN + SV**
  * **SN** $\rightarrow$ **Det** (*La*) + **N** (*dominación*) + **SAdj** $\rightarrow$ **Adj** (*islámica*)
  * **SV** $\rightarrow$ **V** (*disminuyó*) + **SAdv** $\rightarrow$ **Adv** (*progresivamente*)

```
                     O
        _____________|_____________
       |                           |
      SN                          SV
   ___|________                ____|____
  |   |        |              |         |
 Det  N      SAdj             V       SAdv
  |   |        |              |         |
 La dominación Adj        disminuyó    Adv
               |                        |
            islámica              progresivamente
```

---

### 3. Oración: *"Los reyes católicos conquistaron Granada."*

* **Estructura jerárquica:**
  * **O** $\rightarrow$ **SN + SV**
  * **SN** $\rightarrow$ **Det** (*Los*) + **N** (*reyes*) + **SAdj** $\rightarrow$ **Adj** (*católicos*)
  * **SV** $\rightarrow$ **V** (*conquistaron*) + **SN** $\rightarrow$ **N** (*Granada*)

```
                     O
        _____________|_____________
       |                           |
      SN                          SV
   ___|________                ____|____
  |   |        |              |         |
 Det  N      SAdj             V        SN
  |   |        |              |         |
Los reyes     Adj        conquistaron   N
               |                        |
            católicos                Granada
```

---

### 4. Oración: *"El catalán es una lengua romance."*

* **Estructura jerárquica:**
  * **O** $\rightarrow$ **SN + SV**
  * **SN** $\rightarrow$ **Det** (*El*) + **N** (*catalán*)
  * **SV** $\rightarrow$ **V** (*es*) + **SN**
    * **SN** $\rightarrow$ **Det** (*una*) + **N** (*lengua*) + **SAdj** $\rightarrow$ **Adj** (*romance*)

```
            O
     _______|____________________
    |                            |
   SN                           SV
 __|__                   ________|________
|     |                 |                 |
Det   N                 V                 SN
|     |                 |       __________|__________
El  catalán             es     |          |          |
                              Det         N         SAdj
                               |          |          |
                              una       lengua      Adj
                                                     |
                                                  romance
```

---

### 5. Oración: *"Los mayas resistieron la colonización española."*

* **Estructura jerárquica:**
  * **O** $\rightarrow$ **SN + SV**
  * **SN** $\rightarrow$ **Det** (*Los*) + **N** (*mayas*)
  * **SV** $\rightarrow$ **V** (*resistieron*) + **SN**
    * **SN** $\rightarrow$ **Det** (*la*) + **N** (*colonización*) + **SAdj** $\rightarrow$ **Adj** (*española*)

```
            O
     _______|_________________________
    |                                 |
   SN                                SV
 __|__                      __________|__________
|     |                    |                     |
Det   N                    V                     SN
|     |                    |            _________|_________
Los  mayas            resistieron      |         |         |
                                      Det        N        SAdj
                                       |         |         |
                                       la   colonización  Adj
                                                           |
                                                        española
```

---

### 6. Oración: *"Los sacerdotes evangelizaban a los indígenas."*

* **Estructura jerárquica:**
  * **O** $\rightarrow$ **SN + SV**
  * **SN** $\rightarrow$ **Det** (*Los*) + **N** (*sacerdotes*)
  * **SV** $\rightarrow$ **V** (*evangelizaban*) + **SP (Sintagma Preposicional)**
    * **SP** $\rightarrow$ **P** (*a*) + **SN** $\rightarrow$ **Det** (*los*) + **N** (*indígenas*)

```
            O
     _______|________________________
    |                                |
   SN                               SV
 __|__                      ________|________
|     |                    |                 |
Det   N                    V                 SP
|     |                    |            _____|_____
Los sacerdotes        evangelizaban    |           |
                                       P          SN
                                       |       ____|____
                                       a      |         |
                                             Det        N
                                              |         |
                                             los    indígenas
```

---

### 7. Oración: *"Las lenguas minoritarias de España han entrado en una nueva etapa."*

* **Estructura jerárquica:**
  * **SN** $\rightarrow$ **Det** (*Las*) + **N** (*lenguas*) + **SAdj** (*minoritarias*) + **SP** (*de España*)
  * **SV** $\rightarrow$ **V** (*han entrado*) + **SP** (*en una nueva etapa*)

```
                                          O
        __________________________________|_________________________________
       |                                                                    |
      SN                                                                   SV
   ____|_______________________                                     _______|_______
  |    |        |              |                                   |               |
 Det   N      SAdj             SP                                  V               SP
  |    |        |           ___|___                                |            ___|___
 Las lenguas   Adj         |       |                          han entrado      |       |
                |          P      SN                                           P       SN
           minoritarias    |       |                                           |    ___|________
                          de       N                                          en   |   |        |
                                   |                                              Det SAdj      N
                                 España                                            |   |        |
                                                                                  una Adj     etapa
                                                                                       |
                                                                                     nueva
```

---

### 8. Oración: *"El español es lengua oficial en diecinueve países de Latinoamérica."*

* **Estructura jerárquica:**
  * **SN** $\rightarrow$ **Det** (*El*) + **N** (*español*)
  * **SV** $\rightarrow$ **V** (*es*) + **SN** (*lengua oficial*) + **SP** (*en diecinueve países de Latinoamérica*)

```
            O
     _______|__________________________________________________________________
    |                                                                          |
   SN                                                                          SV
 __|__                                  _______________________________________|___________________
|     |                                |                                       |                   |
Det   N                                V                                      SN                   SP
|     |                                |                                  ____|____             ___|___
El  español                            es                                |         |           |       |
                                                                         N        SAdj         P       SN
                                                                         |         |           |    ___|________
                                                                      lengua      Adj          en  |   |        |
                                                                                   |              Det  N        SP
                                                                                oficial            |   |     ___|___
                                                                                              diecinueve países P   SN
                                                                                                                |    |
                                                                                                               de    N
                                                                                                                     |
                                                                                                               Latinoamérica
```

---

### 9. Oración: *"El terreno de Paraguay representaba desafíos de envergadura para los españoles."*

* **Estructura jerárquica:**
  * **SN** $\rightarrow$ **Det** (*El*) + **N** (*terreno*) + **SP** (*de Paraguay*)
  * **SV** $\rightarrow$ **V** (*representaba*) + **SN** (*desafíos de envergadura*) + **SP** (*para los españoles*)

```
                        O
   _____________________|________________________________________________________________________________
  |                                                                                                      |
 SN                                                                                                     SV
 _|___________                                         __________________________________________________|__________________
| |           |                                       |                                                 |                  |
Det N         SP                                      V                                                SN                  SP
| |        ___|___                                    |                                        _________|________       ___|___
El terreno|       |                              representaba                                 |                  |     |       |
          P      SN                                                                           N                 SP     P      SN
          |       |                                                                           |              ___|___   |   ____|____
         de       N                                                                        desafíos         |       | para|    |    |
                  |                                                                                         P      SN    Det   N    ...
               Paraguay                                                                                     |       |     |    |
                                                                                                           de       N    los españoles
                                                                                                                    |
                                                                                                               envergadura
```

---

### 10. Oración: *"Los niños monolingües de desarrollo normal pasan por varias etapas."*

* **Estructura jerárquica:**
  * **SN** $\rightarrow$ **Det** (*Los*) + **N** (*niños*) + **SAdj** (*monolingües*) + **SP** (*de desarrollo normal*)
  * **SV** $\rightarrow$ **V** (*pasan*) + **SP** (*por varias etapas*)

```
                                               O
        _______________________________________|_______________________________________
       |                                                                               |
      SN                                                                              SV
   ____|____________________________________                                   _______|_______
  |    |        |                           |                                 |               |
 Det   N      SAdj                          SP                                V               SP
  |    |        |                        ___|___                              |            ___|___
 Los niños     Adj                      |       |                           pasan         |       |
                |                       P      SN                                         P       SN
           monolingües                  |    ___|________                                 |    ___|___
                                       de   |            |                               por  |       |
                                            N          SAdj                                  Det      N
                                            |            |                                    |       |
                                        desarrollo      Adj                                 varias  etapas
                                                         |
                                                       normal
```

---

## 🏆 Certificaciones Adjuntas

El documento original incluye las acreditaciones del alumno **Bautista Limer**:
* **Nivel Principiante:** *Diagrama sintáctico en forma de árbol* (Completado el 21 de Mayo de 2026).
* **Nivel Intermedio:** *Diagrama sintáctico en forma de árbol* (Completado el 21 de Mayo de 2026).
