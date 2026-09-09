# T·DEV Business OS

Sistema operativo de negocio asistido por IA para T·DEV.

No es una colección de prompts. Es una capa operativa que coordina agentes, skills, comandos, playbooks, reglas, inteligencia comercial y quality gates para convertir oportunidades reales en decisiones, propuestas, entregas y contenido reutilizable.

## Principios

- **Business Crew = quién piensa**: roles especializados con responsabilidad clara.
- **Skills = qué sabe hacer**: capacidades pequeñas, componibles y reutilizables.
- **Commands = qué pedimos**: entradas de alto nivel para ejecutar procesos completos.
- **Playbooks = cómo operamos**: procesos repetibles de captación, auditoría, propuesta, desarrollo y entrega.
- **Workflows = cómo se coordina**: secuencias entre agentes y skills.
- **Quality gates = cuándo está listo**: criterios explícitos antes de publicar, vender o entregar.
- **Intelligence = qué sabemos del mercado**: competencia, nichos, oportunidades y aprendizaje acumulado.

## Objetivo actual

Construir una ventaja operativa para T·DEV combinando:

1. Investigación de negocio y competencia.
2. Captación y venta consultiva.
3. Auditoría web, UX, conversión, SEO/local SEO y rendimiento.
4. Diseño y desarrollo con Claude Code / Codex.
5. Pricing, propuestas y alcance.
6. Legal y riesgos básicos.
7. QA, accesibilidad, performance y pre-launch review.
8. Reutilización del trabajo real como contenido comercial.
9. Mejora continua de la propia landing T·DEV.

## Arquitectura

```text
.
├── agents/          # Roles especialistas
├── skills/          # Capacidades componibles
├── commands/        # Entradas de alto nivel
├── workflows/       # Orquestación de varias capacidades
├── playbooks/       # Procesos operativos completos
├── quality-gates/   # Definition of Done y revisiones
├── intelligence/    # Mercado, competencia y oportunidades
├── templates/       # Propuestas, auditorías, briefs, contratos, contenido
├── config/          # Contexto específico de T·DEV
├── rules/           # Reglas transversales
├── AGENTS.md        # Contrato para agentes compatibles
└── CLAUDE.md        # Instrucciones para Claude Code
```

## Separación importante

El **core debe ser reutilizable**. La información específica de T·DEV vive en `config/` e `intelligence/`.

Esto permite usar el mismo motor para otros proyectos o clientes sin hardcodear la marca, una ciudad o un nicho concreto.

## Flujo principal de una oportunidad

```text
lead / URL / negocio
       ↓
research-business
       ↓
competitor-gap + local-seo + website-audit
       ↓
ux-conversion + technical-quality
       ↓
opportunity-brief
       ↓
pricing + scope
       ↓
proposal
       ↓
build / review / ship
       ↓
case-study + content-repurpose
```

## Flujo de mejora de la landing T·DEV

```text
/landing-audit
  → posicionamiento
  → UX / UI
  → copy / conversión
  → SEO
  → performance
  → accesibilidad
  → diferenciación competitiva
  → plan priorizado
  → build
  → review
  → ship
```

## Estado

**v0.1 — Foundation**

Primera fase: definir contratos, arquitectura, agentes esenciales, skills comerciales/técnicas y quality gates antes de automatizar más.
