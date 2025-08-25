Diferencia núcleo:

* **RAG**: añade *conocimiento externo* a un LLM en tiempo de consulta. Fórmula: $y = \mathrm{LLM}\big(x \;\Vert\; \mathrm{retrieve}(x, \mathcal{D})\big)$. RAG significa *Retrieval-Augmented Generation*, en español *Generación Aumentada por Recuperación*.
* **Agentes**: hacen *planificación y acción* con bucle de herramientas. Fórmula: política $\pi(a\mid s)$ con ciclo *observar→razonar→actuar* hasta meta. Se llaman agentes porque actúan en un entorno y toman decisiones basadas en la información disponible.
* **IA multimodal**: *integra o produce varias modalidades* (texto, imagen, audio, video). Fórmula: $p(y\mid x^{\text{text}}, x^{\text{img}}, x^{\text{aud}},\ldots)$.

Tabla breve

| Aspecto        | RAG                                                                   | Agentes                                                          | Multimodal                                                |
| -------------- | --------------------------------------------------------------------- | ---------------------------------------------------------------- | --------------------------------------------------------- |
| Objetivo       | Reducir alucinación. Responder con base documental.                   | Resolver tareas compuestas con llamadas a herramientas.          | Entender y generar más de una modalidad.                  |
| Núcleo técnico | *Retriever* + *index* (embeddings, BM25, reranker) + *prompt fusion*. | Planificador + memoria + ejecutor de herramientas/APIs.          | Encoders/decoders con atención cruzada entre modalidades. |
| Bucle          | 1–2 pasos.                                                            | Iterativo.                                                       | No implica bucle por sí mismo.                            |
| Conocimiento   | Traído desde $\mathcal{D}$ en consulta.                               | Puede leer, escribir, llamar APIs y crear conocimiento derivado. | Contenido visual/sonoro asociado a texto.                 |
| Riesgo típico  | *Recall* pobre, *chunking* deficiente.                                | Deriva, costos altos, errores de herramienta.                    | Desalineación modal, *hallucination* visual.              |
| Métrica clave  | EM/F1, *Retrieval\@k*, *Faithfulness*.                                | Tasa de éxito por tarea, coste, latencia.                        | VQA accuracy, BLEU/CIDEr, WER, CLIP-score.                |

Cuándo usar

* **Usa RAG**: preguntas sobre corpus propio, cumplimiento, soporte con base de conocimiento, búsqueda semántica → respuesta citada.
* **Usa agentes**: flujos multi-paso con decisiones y herramientas: ETL, operar hojas de cálculo, reservar, ejecutar código, cadenas de razonamiento accionables.
* **Usa multimodal**: VQA, extracción de datos en facturas, captioning, grounding visual, ASR/TTS, video QA.

Combinaciones útiles

* **Multimodal-RAG**: recuperar imágenes, tablas o audio relevantes y condicionarlos: $y=\mathrm{LLM}(x\Vert \mathrm{retrieve}(x,\mathcal{D}^{\text{img,txt}}))$.
* **RAG con agente**: el agente decide *cuándo* y *cómo* recuperar, limpiar y citar.
* **Agente multimodal**: observa imágenes o audio, elige herramientas OCR/ASR, planifica, actúa.

Arquitecturas mínimas

* **RAG**: *Embedder* $E$, índice $I$, *retriever* $R$, *reranker* $Q$, LLM $F$. Pipeline: $q\!\to\!E(q)\!\to\!R(I,E(q))\!\to\!Q\!\to\!F$.
* **Agente**: estado $s_t=(x, m_t, o_t)$. Acción $a_t\in\{\text{tool}_i, \text{answer}\}$. Transición por *tool call*. Termina al emitir *answer*.
* **Multimodal**: proyectores $\phi_k$ por modalidad y fusión por atención: $h=\mathrm{Fuse}\big(\phi_{\text{text}}(x_t),\phi_{\text{img}}(x_i),\ldots\big)$.

Coste y control

* **RAG**: coste bajo y estable. Control por *retrieval* y *prompting*. Datos gobernados.
* **Agentes**: coste variable por longitud del bucle. Requiere *guardrails* y tests de herramienta.
* **Multimodal**: coste por tamaño de entrada visual/sonora. Requiere *pre-processing*.

Ejemplos rápidos

* **RAG**: “Responde con citas desde mi manual ISO.”
* **Agente**: “Analiza CSV, crea gráfico, envía resumen por API.”
* **Multimodal**: “Lee esta factura escaneada y extrae total.”

Regla práctica

* Si el *input* es pregunta sobre conocimiento fijo → **RAG**.
* Si hay decisiones, estado y acciones encadenadas → **agente**.
* Si hay imágenes, audio o video como señal primaria → **multimodal**.
