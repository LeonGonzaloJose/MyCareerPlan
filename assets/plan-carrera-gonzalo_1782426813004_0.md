# Plan de Carrera Backend — Gonzalo
> De Laravel a referente técnico · 9 etapas · ~18–20 meses · 4+ horas diarias

---

## 📖 Cómo usar este archivo

Este archivo está pensado para **editores de texto** (VS Code, Zed, Neovim, etc.) con soporte de Markdown y checkboxes. Podés:

- Marcar cada tema con `[x]` cuando lo dominás
- Editar las fechas reales de inicio/fin de cada etapa
- Commitearlo a un repo Git privado para tenerlo sincronizado entre PC laboral y PC propia

**Flujo por etapa:**
1. Leer el libro principal de corrido
2. Practicar con el proyecto integrador
3. Usar el resto de la bibliografía como referencia cuando surja la necesidad

**Lectura transversal (todo el plan, 1 capítulo por semana):**
- *The Pragmatic Programmer* — Hunt & Thomas

---

## Resumen de etapas

| # | Etapa                         | Meses     | Foco principal                              |
|---|-------------------------------|-----------|---------------------------------------------|
| 1 | Fundamentos de ingeniería     | 1–2       | SOLID, patrones, clean code, algoritmos     |
| 2 | Testing: de cero a TDD        | 2–3       | Unit, integración, TDD                      |
| 3 | Bases de datos en profundidad | 3–4       | SQL avanzado, indexing, Redis               |
| 4 | Arquitectura de software real | 4–6       | Clean Architecture, DDD, REST, CQRS        |
| 5 | Docker, Kubernetes y CI/CD    | 6–9       | Contenedores, orquestación, pipelines, AWS  |
| 6 | Node.js y TypeScript          | 9–12      | TS avanzado, NestJS, Kafka                  |
| 7 | Go: del tutorial a producción | 12–16     | Go idiomático, concurrencia, gRPC           |
| 8 | Fundamentos de IA aplicada    | 16–18     | LLMs, contexto, memoria, agentes, MCP      |
| 9 | IA en producción con Go/Node  | 18–20     | RAG, tool calling, servidores MCP propios   |

---

## Etapa 1 — Fundamentos que nunca te enseñaron
> Meses 1–2 · La base real de la ingeniería de software

**Inicio real:** `____-__-__` · **Fin real:** `____-__-__`

Esta etapa te da el "por qué" de todo lo que ya hacés intuitivamente. El síndrome del impostor se alimenta exactamente de saber usar herramientas sin entender por qué funcionan. Acá rompemos eso.

### Objetivos
- [ ] Entender SOLID con ejemplos en PHP real de tu trabajo diario
- [ ] Conocer los 23 patrones del GoF y cuándo usarlos (no memorizarlos)
- [ ] Leer y escribir código limpio con intención, no intuición
- [ ] Comprender complejidad algorítmica O(n) para tomar mejores decisiones

### Temas
- [ ] Principios SOLID uno por uno, con refactoring de código PHP tuyo
- [ ] Patrones creacionales: Factory, Builder, Singleton (y cuándo NO usarlo)
- [ ] Patrones estructurales: Adapter, Decorator, Facade, Repository
- [ ] Patrones de comportamiento: Observer, Strategy, Command, Iterator
- [ ] Big O notation: arrays, hash maps, búsqueda, ordenamiento
- [ ] Clean Code: nombres, funciones, comentarios, formateo
- [ ] Principios DRY, YAGNI, KISS aplicados al día a día

### Bibliografía
| Libro | Autor | Rol |
|-------|-------|-----|
| *Clean Code* | Robert C. Martin | **Principal — empezá por acá** |
| *Design Patterns (GoF)* | Gang of Four | Referencia de patrones |
| *Head First Design Patterns* | Freeman & Robson | Alternativa más accesible al GoF |
| *A Philosophy of Software Design* | John Ousterhout | Complemento moderno (200 págs.) |

### ✅ Proyecto integrador
**Refactoring de un módulo de APERNET.**
Tomá el módulo más caótico que encuentres y refactorizalo aplicando SOLID y al menos 3 patrones de diseño. Documentá antes/después.

- [ ] Módulo elegido: `_______________`
- [ ] SOLID aplicado
- [ ] 3+ patrones de diseño
- [ ] Documentación antes/después

---

## Etapa 2 — Testing: de cero a TDD
> Mes 2–3 · El hábito más diferenciador de un senior

**Inicio real:** `____-__-__` · **Fin real:** `____-__-__`

### Objetivos
- [ ] Escribir tests unitarios con PHPUnit para código PHP/Laravel existente
- [ ] Entender qué testear y qué NO testear
- [ ] Practicar el ciclo Red-Green-Refactor de TDD
- [ ] Escribir tests de integración para APIs REST

### Temas
- [ ] Anatomía de un test: Arrange, Act, Assert
- [ ] Mocks, stubs y fakes: cuándo usar cada uno
- [ ] PHPUnit avanzado: data providers, setUp, excepciones
- [ ] Testing en Laravel: RefreshDatabase, HTTP tests, factories
- [ ] TDD desde cero: ciclo Red-Green-Refactor
- [ ] Cobertura de código: qué significa y por qué el 100% es una trampa
- [ ] Testing de APIs con supertest (Node) y httptest (Go)

### Bibliografía
| Libro | Autor | Rol |
|-------|-------|-----|
| *Test-Driven Development: By Example* | Kent Beck | **Principal — el creador de TDD** |
| *The Art of Unit Testing* | Roy Osherove | Referencia completa multi-lenguaje |
| *Growing Object-Oriented Software, Guided by Tests* | Freeman & Pryce | Avanzado: TDD a nivel de sistema |

### ✅ Proyecto integrador
**Suite de tests para el marketplace de APERNET.**
Tests para un flujo crítico (órdenes, pagos, integración bancaria). Meta: 60%+ de cobertura en ese módulo.

- [ ] Flujo elegido: `_______________`
- [ ] Tests unitarios
- [ ] Tests de integración
- [ ] 60%+ cobertura alcanzada
- [ ] Factories y mocks reales

---

## Etapa 3 — Bases de datos en profundidad
> Mes 3–4 · De ORM a DBA consciente

**Inicio real:** `____-__-__` · **Fin real:** `____-__-__`

### Objetivos
- [ ] Escribir queries SQL complejas sin ORM cuando sea necesario
- [ ] Entender índices, EXPLAIN y optimización de queries
- [ ] Diseñar esquemas relacionales correctamente (normalización)
- [ ] Usar Redis como caché, colas y pub/sub

### Temas
- [ ] JOINs complejos, subqueries, CTEs, window functions
- [ ] EXPLAIN ANALYZE: cómo leer el plan de ejecución
- [ ] Índices: B-tree, hash, parciales, compuestos — cuándo crearlos y cuándo no
- [ ] Transacciones, niveles de aislamiento, deadlocks
- [ ] Normalización: 1NF → 3NF y cuándo desnormalizar conscientemente
- [ ] Redis: strings, hashes, sets, sorted sets, pub/sub, TTL, eviction
- [ ] Migraciones seguras en producción sin downtime
- [ ] Introducción a NoSQL: cuándo usar MongoDB vs relacional

### Bibliografía
| Libro | Autor | Rol |
|-------|-------|-----|
| *Designing Data-Intensive Applications* | Martin Kleppmann | **Principal — el más importante de la etapa** |
| *Database Internals* | Alex Petrov | Cómo funcionan las DBs por dentro |
| *Learning SQL* | Alan Beaulieu | Si tenés huecos en SQL básico-intermedio |

### ✅ Proyecto integrador
**Sistema de reportes con SQL puro y Redis.**
Un endpoint de reportes para APERNET sin ORM. Caché con Redis con TTL por marketplace. EXPLAIN + optimización de al menos una query lenta real.

- [ ] Endpoint sin ORM implementado
- [ ] Caché Redis con TTL por marketplace
- [ ] Al menos una query analizada con EXPLAIN y optimizada

---

## Etapa 4 — Arquitectura de software real
> Mes 4–6 · Clean Architecture, DDD y APIs que duran

**Inicio real:** `____-__-__` · **Fin real:** `____-__-__`

### Objetivos
- [ ] Diseñar aplicaciones con Hexagonal/Clean Architecture
- [ ] Entender DDD: Aggregates, Value Objects, Bounded Contexts
- [ ] Diseñar APIs REST profesionales con versionado, autenticación y documentación
- [ ] Comprender CQRS y cuándo tiene sentido aplicarlo

### Temas
- [ ] Arquitectura en capas vs hexagonal vs clean: diferencias reales
- [ ] Ports & Adapters: desacoplar el dominio de la infraestructura
- [ ] DDD táctico: Entities, Value Objects, Aggregates, Domain Events
- [ ] DDD estratégico: Bounded Contexts, Context Maps, Ubiquitous Language
- [ ] REST maduro: códigos HTTP correctos, HATEOAS, versionado
- [ ] OpenAPI 3.0: documentación como contrato
- [ ] Autenticación: JWT, OAuth2, refresh tokens, seguridad real
- [ ] CQRS: separar lecturas de escrituras, cuándo y cuándo no

### Bibliografía
| Libro | Autor | Rol |
|-------|-------|-----|
| *Clean Architecture* | Robert C. Martin | **Principal** |
| *Implementing Domain-Driven Design* | Vaughn Vernon | DDD práctico y moderno |
| *Domain-Driven Design* | Eric Evans | El libro azul original (referencia) |
| *RESTful Web APIs* | Richardson & Amundsen | El estándar para APIs REST |

### ✅ Proyecto integrador
**API de marketplace con Clean Architecture en PHP.**
Reescribir un módulo de APERNET con capas claras: Domain / Application / Infrastructure. Tests en cada capa, documentación OpenAPI y versionado.

- [ ] Módulo elegido: `_______________`
- [ ] Capas Domain / Application / Infrastructure separadas
- [ ] Tests en cada capa
- [ ] Documentación OpenAPI
- [ ] Versionado de API

---

## Etapa 5 — Docker, Kubernetes y CI/CD
> Mes 6–9 · Infra que todo backend senior debe dominar

**Inicio real:** `____-__-__` · **Fin real:** `____-__-__`

### Objetivos
- [ ] Escribir Dockerfiles eficientes con multi-stage builds
- [ ] Orquestar servicios con Docker Compose
- [ ] Deployar aplicaciones en Kubernetes
- [ ] Armar un pipeline CI/CD completo con GitHub Actions
- [ ] Entender AWS: EC2, RDS, S3, ECR, ECS/EKS básico

### Temas
- [ ] Docker: imágenes, capas, volúmenes, networking, multi-stage
- [ ] Docker Compose: servicios dependientes, healthchecks, perfiles
- [ ] Kubernetes: arquitectura del cluster, kubectl, manifiestos YAML
- [ ] Pods, ReplicaSets, Deployments, Services, ConfigMaps, Secrets
- [ ] Ingress controllers, namespaces, RBAC básico
- [ ] Helm: charts para deployar aplicaciones
- [ ] GitHub Actions: workflows, secrets, artifacts, matrix builds
- [ ] AWS: IAM roles/policies, ECR, ECS, RDS, S3
- [ ] Monitoreo: CloudWatch, Prometheus + Grafana básico

### Bibliografía
| Libro | Autor | Rol |
|-------|-------|-----|
| *Docker Deep Dive* | Nigel Poulton | **Principal — corto, claro, actualizado** |
| *Kubernetes in Action* | Marko Luksa | El más completo de Kubernetes |
| *The DevOps Handbook* | Gene Kim et al. | Cultura y principios DevOps |
| *AWS in Action* | Andreas & Michael Wittig | AWS práctico para developers |

### ✅ Proyecto integrador
**Pipeline completo de deployment para APERNET.**
Dockerizar una API con multi-stage build. Docker Compose de desarrollo. GitHub Actions que: corra tests → buildee imagen → pushee a ECR → deploye en ECS/EC2.

- [ ] Dockerfile con multi-stage build
- [ ] Docker Compose de desarrollo
- [ ] GitHub Actions: tests → build → push a ECR → deploy

---

## Etapa 6 — Node.js y TypeScript profesional
> Mes 9–12 · Backend moderno con el ecosistema JS

**Inicio real:** `____-__-__` · **Fin real:** `____-__-__`

### Objetivos
- [ ] Dominar TypeScript: tipos, generics, decorators, utility types
- [ ] Construir APIs REST y GraphQL con NestJS
- [ ] Entender el event loop de Node.js y cuándo es la herramienta correcta
- [ ] Integrar message brokers (RabbitMQ, Kafka) en servicios Node

### Temas
- [ ] TypeScript avanzado: interfaces vs types, generics, mapped types, conditional types
- [ ] Node.js internals: event loop, libuv, streams, buffers
- [ ] NestJS: módulos, controllers, providers, interceptors, guards, pipes
- [ ] Prisma ORM con TypeScript: type-safe queries
- [ ] GraphQL con Apollo Server: schema-first vs code-first
- [ ] RabbitMQ: exchanges, queues, routing keys, dead letter queues
- [ ] Kafka: topics, partitions, consumer groups, exactly-once semantics
- [ ] WebSockets con Socket.io: casos de uso reales
- [ ] Testing en Node: Jest, Supertest, mocking de módulos

### Bibliografía
| Libro | Autor | Rol |
|-------|-------|-----|
| *Node.js Design Patterns* | Casciaro & Mammino | **Principal — definitivo de Node avanzado** |
| *Programming TypeScript* | Boris Cherny | El mejor libro de TypeScript |
| *Kafka: The Definitive Guide* | Gwen Shapira et al. | Kafka como modelo de datos |

### ✅ Proyecto integrador
**Microservicio de notificaciones con Node.js y Kafka.**
NestJS + Kafka para recibir eventos de otros servicios (email, push, webhook). Docker. OpenAPI. Tests de integración.

- [ ] Microservicio NestJS operativo
- [ ] Integración con Kafka
- [ ] Deployado con Docker
- [ ] Documentación OpenAPI
- [ ] Tests de integración

---

## Etapa 7 — Go: del tutorial a producción
> Mes 12–16 · El lenguaje del ecosistema distribuido

**Inicio real:** `____-__-__` · **Fin real:** `____-__-__`

### Objetivos
- [ ] Dominar Go: interfaces, goroutines, channels, error handling idiomático
- [ ] Construir APIs REST y gRPC con Go
- [ ] Entender el modelo de concurrencia de Go y usarlo correctamente
- [ ] Deployar servicios Go en producción con Kubernetes

### Temas
- [ ] Go fundamentos: tipos, interfaces, structs, punteros, slices, maps
- [ ] Error handling idiomático: errors.Is, errors.As, custom errors
- [ ] Goroutines y channels: comunicación, select, patrones de concurrencia
- [ ] Context: cancellation, timeouts, propagación en servicios
- [ ] HTTP con net/http + frameworks (Gin, Chi, Fiber)
- [ ] gRPC: Protocol Buffers, unary, streaming, interceptors
- [ ] Testing en Go: testing package, table-driven tests, benchmarks
- [ ] Profiling con pprof: memory leaks, CPU bottlenecks
- [ ] go-kit / go-micro para microservicios

### Bibliografía
| Libro | Autor | Rol |
|-------|-------|-----|
| *Learning Go* | Jon Bodner | **Principal — Go idiomático moderno** |
| *The Go Programming Language* | Donovan & Kernighan | La biblia de Go (referencia completa) |
| *Concurrency in Go* | Katherine Cox-Buday | Goroutines, channels y patrones |
| *Building Microservices* | Sam Newman | Referencia de arquitectura de microservicios |

### ✅ Proyecto integrador
**Servicio de pagos en Go con gRPC.**
Microservicio de procesamiento de pagos con API gRPC. Circuit breaker, retries con backoff exponencial, distributed tracing. Deploy en Kubernetes con health checks y readiness probes.

- [ ] API gRPC implementada
- [ ] Circuit breaker + retries con backoff exponencial
- [ ] Distributed tracing
- [ ] Deploy en Kubernetes con health checks y readiness probes

---

## Etapa 8 — Fundamentos de IA aplicada
> Mes 16–18 · LLMs, contexto, memoria, agentes y MCP

**Inicio real:** `____-__-__` · **Fin real:** `____-__-__`

Esta es la etapa donde entendés de verdad cómo funcionan las herramientas que ya usás todos los días (Claude Code, Gentle-AI, Engram, MCP).

### Objetivos
- [ ] Entender cómo funciona un LLM desde adentro (ventana de contexto, tokens)
- [ ] Comprender las 4 estrategias de memoria en sistemas con LLMs
- [ ] Entender tool calling, agentes y subagentes
- [ ] Comprender qué son skills, harness y SDD
- [ ] Entender MCP y cómo conecta modelos con el mundo

---

### 8.1 — Cómo funciona un LLM

**La idea más importante:** un LLM es una función sin estado. Recibe texto, devuelve texto. No tiene memoria entre conversaciones. Todo lo demás son capas que el sistema construye encima.

```
System prompt + Historial de mensajes + Mensaje actual + Documentos inyectados
= Contexto completo
```

El modelo genera la respuesta prediciendo el siguiente token más probable dado ese contexto.

| Concepto | Detalle |
|----------|---------|
| Ventana de contexto | El bloque de texto que el modelo recibe en cada llamada |
| Token | Aprox. 0.75 palabras. Claude: ~200k tokens · GPT-4o: ~128k |
| System prompt | Texto inicial que define rol, instrucciones, tools disponibles |

- [ ] Entiendo qué es la ventana de contexto y cómo se arma
- [ ] Entiendo qué es un token y el límite de contexto
- [ ] Entiendo el rol del system prompt

---

### 8.2 — Memoria: el problema central de los LLMs

El modelo es stateless. La memoria la construye el sistema que lo rodea. Hay 4 estrategias:

| Estrategia | Mecanismo | Limitación |
|------------|-----------|------------|
| **In-context** | El historial completo va en cada llamada | Consume tokens, tiene límite |
| **Externa (RAG)** | Hechos guardados en DB; se recuperan y se inyectan | Requiere embeddings/retrieval |
| **Semántica** | El LLM resume el historial periódicamente | Pérdida de precisión |
| **Paramétrica** | Conocimiento "quemado" en los pesos (fine-tuning) | Costoso, difícil de actualizar |

**Engram en tu setup:**

```
Escritura: Conversación Claude Code → Engram intercepta → Extrae hechos → Guarda en DB local
Lectura:   Nueva sesión → Engram recupera contexto → Lo inyecta al system prompt → Claude "recuerda"
```

- [ ] Conozco las 4 estrategias de memoria
- [ ] Entiendo cómo Engram implementa memoria externa
- [ ] Entiendo qué es RAG a nivel conceptual

---

### 8.3 — Tool calling, agentes y subagentes

**Tool calling:** vos le declarás al modelo qué herramientas existen (nombre, descripción, parámetros). El modelo decide cuándo llamarlas. Tu código las ejecuta y devuelve el resultado al contexto.

```
Usuario: "¿cuántas órdenes hoy?"
→ Modelo decide: llamar get_orders(date=hoy)
→ Tu backend ejecuta la query
→ Resultado vuelve al contexto
→ Modelo responde con datos reales
```

**Agente = un loop:**

```
Objetivo del usuario → LLM razona → Llama tool → Recibe resultado → (repite hasta end_turn)
```

**Subagentes:** un orquestador divide el trabajo y lo delega a agentes especializados.

```
Agente orquestador → Subagente SQL
                   → Subagente file system
                   → Subagente API externa
```

Patrones: ReAct (Reason+Act), Plan-and-execute, Reflexión/self-critique.
Frameworks: LangGraph, CrewAI, Autogen.

- [ ] Entiendo cómo funciona tool calling a nivel de API
- [ ] Entiendo qué es un agente y cuál es el loop
- [ ] Entiendo la diferencia entre agente orquestador y subagentes

---

### 8.4 — Skills, harness y SDD

| Concepto | Qué es |
|----------|--------|
| **Skill** | Archivo `.md` con instrucciones especializadas que se inyectan al contexto cuando la tarea encaja |
| **Harness** | El sistema que envuelve al LLM: gestiona contexto, carga skills, ejecuta tools, maneja memoria, parsea outputs |
| **SDD** | Spec-Driven Development: antes de codear, el modelo y vos producen una especificación estructurada que queda en el repo |
| **CLAUDE.md** | El archivo raíz que el modelo siempre lee: define el proyecto, las rules y las skills activas |

Componentes típicos de un harness: context manager · tool executor · memory retriever · output parser · error handler · agent loop.

- [ ] Entiendo qué es una skill y cómo vive en el repo
- [ ] Entiendo qué es un harness y qué componentes tiene
- [ ] Entiendo SDD y para qué sirve el CLAUDE.md

---

### 8.5 — MCP: el protocolo que conecta modelos con el mundo

**Model Context Protocol (MCP):** protocolo abierto de Anthropic que estandariza cómo los modelos se conectan a herramientas y fuentes de datos externas. Es el "USB-C de los LLMs" o "REST para tools de IA".

```
Cliente MCP (Claude Code) ↔ Servidor MCP ↔ Recurso externo (Slack, Jira, tu DB, Redash...)
```

| Aspecto | Detalle |
|---------|---------|
| Qué expone | Tools (funciones invocables), Resources (datos legibles), Prompts (templates) |
| Transporte | stdio (local) o HTTP+SSE (remoto/cloud) |
| Tu caso actual | APER MCP-Gateway conecta Claude con Odoo, Redash y otros sistemas de APERNET |

- [ ] Entiendo qué es MCP y qué problema resuelve
- [ ] Entiendo la diferencia entre Tools, Resources y Prompts en MCP
- [ ] Entiendo cómo tu APER MCP-Gateway encaja en esto

---

### Bibliografía Etapa 8

| Libro / Recurso | Autor | Rol |
|-----------------|-------|-----|
| *Hands-On Large Language Models* | Jay Alammar & Maarten Grootendorst | **Principal — visual y práctico** |
| *AI Engineering* | Chip Huyen | El más completo sobre sistemas LLM en producción (2024) |
| Documentación oficial MCP | modelcontextprotocol.io | Referencia del protocolo |
| Documentación API Anthropic | docs.claude.com | Tool use, streaming, batch |

### ✅ Proyecto integrador
**Documentar y extender tu propio setup.**
Escribir una skill nueva desde cero para Claude Code que resuelva una tarea repetitiva en APERNET. Documentar cómo Engram, las skills y el MCP-Gateway interactúan. Objetivo: poder explicarle a un junior cómo funciona todo el harness.

- [ ] Skill nueva escrita y funcional
- [ ] Documentación del harness completo (Engram + skills + MCP-Gateway)
- [ ] Explicación que un junior pueda seguir

---

## Etapa 9 — IA en producción con Go y Node
> Mes 18–20 · RAG, agentes y servidores MCP propios

**Inicio real:** `____-__-__` · **Fin real:** `____-__-__`

### Objetivos
- [ ] Integrar APIs de OpenAI y Anthropic en servicios backend (Go y Node)
- [ ] Construir flujos agénticos: tool calling, multi-step reasoning
- [ ] Implementar RAG: embeddings, vector databases, retrieval
- [ ] Construir tu propio servidor MCP para conectar Claude con tus APIs
- [ ] Entender qué es fine-tuning y cuándo tiene sentido hacerlo

### Temas
- [ ] APIs de LLMs: completions, chat, function calling, streaming
- [ ] Prompt engineering para developers: system prompts, few-shot, chain-of-thought
- [ ] Tool calling / function calling: conectar LLMs con tus APIs
- [ ] Embeddings: qué son, cómo usarlos, modelos de embeddings
- [ ] Vector databases: Pinecone, Weaviate, pgvector (PostgreSQL)
- [ ] RAG pipeline: chunking, indexing, retrieval, re-ranking
- [ ] Agentes con frameworks (Vercel AI SDK en Node, SDKs nativos en Go)
- [ ] Construcción de un servidor MCP propio
- [ ] Fine-tuning: cuándo y cómo, datasets, evaluación
- [ ] Seguridad con LLMs: prompt injection, jailbreaking, validación de outputs

### Frameworks del ecosistema

| Framework | Ecosistema | Para qué |
|-----------|------------|----------|
| LangChain / LangGraph | Python | Chains y grafos de agentes. Popular, a veces sobreingeniería |
| Vercel AI SDK | Node/TypeScript | Streaming, tool calling, multi-provider. Muy limpio para tu path |
| anthropic-sdk-go / go-openai | Go | SDKs nativos. El harness se construye más a mano: más control |
| LlamaIndex | Python | Especializado en RAG (chunking, indexing, retrieval) |

### Bibliografía

| Libro / Recurso | Autor | Rol |
|-----------------|-------|-----|
| *Building LLM Apps* | Valentina Alto | **Principal** |
| *AI Engineering* | Chip Huyen | Relectura aplicada con foco en producción |
| Documentación Vercel AI SDK | — | Para el path de Node |
| Documentación pgvector | — | Para RAG sobre PostgreSQL |

### ✅ Proyecto integrador final
**Asistente inteligente para marketplace de APERNET.**
Agente que responde preguntas sobre órdenes, productos y métricas usando RAG sobre datos de Redash/MySQL. Tool calling para ejecutar queries. Microservicio en Go o Node con interfaz REST. Bonus: exponer sus capacidades como servidor MCP propio.

- [ ] RAG pipeline operativo sobre datos de Redash/MySQL
- [ ] Tool calling para ejecutar queries
- [ ] Microservicio con interfaz REST (Go o Node)
- [ ] **BONUS:** servidor MCP propio expuesto

---

## Reflexión final

El camino de referente no es lineal ni se termina nunca del todo. Pero si completás los 9 proyectos integradores de esta guía, vas a tener un portafolio que demuestra capacidad real en: fundamentos sólidos, testing, bases de datos, arquitectura, infraestructura, dos lenguajes backend modernos, y sistemas de IA en producción. Eso no es teoría: es evidencia. Y la evidencia es lo único que de verdad silencia al síndrome del impostor.

---

## Progreso general

| Etapa | Estado | Proyecto integrador |
|-------|--------|---------------------|
| 1 — Fundamentos | ⬜ No iniciada | ⬜ |
| 2 — Testing | ⬜ No iniciada | ⬜ |
| 3 — Bases de datos | ⬜ No iniciada | ⬜ |
| 4 — Arquitectura | ⬜ No iniciada | ⬜ |
| 5 — Docker/K8s/CI/CD | ⬜ No iniciada | ⬜ |
| 6 — Node.js/TypeScript | ⬜ No iniciada | ⬜ |
| 7 — Go | ⬜ No iniciada | ⬜ |
| 8 — IA fundamentos | ⬜ No iniciada | ⬜ |
| 9 — IA en producción | ⬜ No iniciada | ⬜ |

> Reemplazá ⬜ por 🟡 (en progreso) o ✅ (completada) a medida que avanzás.
