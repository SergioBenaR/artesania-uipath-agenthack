# ArtesanIA

ArtesanIA is an agentic workflow for documenting, validating, and certifying Bolivian artisan heritage.

It was built for UiPath AgentHack using UiPath Apps, UiPath AI Agents, Analyze Files, Action Apps, and Maestro BPMN.

## Demo

Devpost project: https://devpost.com/software/artesania
Demo video: https://youtu.be/Z12n8jF8cVU?si=sPiRh7o730fhb6Yn

## Inspiration

Bolivia has a massive folkloric and creative ecosystem. Major cultural expressions such as the Carnival of Oruro and Gran Poder are recognized by UNESCO as Intangible Cultural Heritage. Behind these festivities there are thousands of artisans, embroiderers, mask makers, designers, dancers, musicians, and fraternity organizers.

However, many artisan works such as costumes, masks, embroidery pieces, and design sketches still lack structured digital documentation, proof of authorship, and a reliable validation process.

ArtesanIA was created to explore how agentic automation can help preserve this cultural knowledge responsibly.

## What it does

ArtesanIA helps document, validate, and certify artisan heritage through a human-in-the-loop workflow.

The prototype includes:

1. A UiPath Apps intake form where an artisan submits metadata and uploads an image of a costume, mask, embroidery piece, or design sketch.
2. A UiPath AI Agent using Analyze Files to analyze the uploaded image and extract visible cultural, material, and design elements.
3. A human validation step through UiPath Action Apps.
4. A Maestro BPMN workflow that coordinates submission, AI analysis, human review, and final certificate/hash generation.

The goal is not to replace artisans or cultural experts. The AI prepares a structured cultural record, but humans validate it before certification.

## How it works

The modeled workflow is:

1. Artisan piece submitted.
2. AI Agent analyzes the artisan piece.
3. Human reviewer validates the cultural record.
4. System generates certificate and hash.
5. Artisan piece becomes certified.

## UiPath components used

- UiPath Apps
- UiPath AI Agents
- Analyze Files
- UiPath Action Apps
- UiPath Maestro BPMN

## Prototype status

This hackathon prototype demonstrates the core components and orchestration of the ArtesanIA workflow:

- Artisan intake interface
- AI image/document analysis agent
- Human validation step
- Maestro BPMN process model
- Certificate/hash generation step as part of the modeled workflow

The next implementation step is to fully wire the form submission, uploaded file, AI output, human validation result, and certificate/hash generation into one executable end-to-end production workflow.

## Why Maestro BPMN matters

Maestro BPMN makes the solution understandable as one governed process.

Without Maestro, the project would feel like disconnected parts: a form, an AI agent, a human review screen, and a certification idea. With Maestro, these parts become a coordinated workflow involving agents, humans, files, decisions, and validation.

## Cultural responsibility

ArtesanIA treats AI as an assistant, not as the final cultural authority.

The AI can help extract visible elements, identify possible inconsistencies, and prepare structured documentation. However, cultural validation should remain in the hands of artisans, associations, researchers, and human reviewers.

## What's next

The next step is to present ArtesanIA to artisan and embroidery associations in Bolivia, validate the workflow with real users, and continue developing the certificate and blockchain timestamping layer.

Future improvements include:

- Full integration between UiPath Apps and Maestro BPMN
- Automatic passing of uploaded files to the AI Agent
- Human reviewer interface with structured AI output
- PDF certificate generation
- Hash generation and timestamping
- Optional blockchain anchoring
- Artisan digital portfolio pages

## Sources

- UNESCO Intangible Cultural Heritage — Carnival of Oruro  
  https://ich.unesco.org/es/RL/el-carnaval-de-oruro-00003

- UNESCO Intangible Cultural Heritage — Gran Poder Festival, La Paz  
  https://ich.unesco.org/es/RL/festividad-del-senor-jesus-del-gran-poder-en-la-ciudad-de-la-paz-el-dia-de-la-santisima-trinidad-01389

- ABI — Gran Poder 2026: 76 fraternities and 95,000 participants  
  https://abi.bo/la-asociacion-de-conjuntos-folkloricos-del-gran-poder-exhorta-a-la-pacificacion-del-pais/

- ABI — Gran Poder 2026: economic movement of at least USD 80 million  
  https://abi.bo/el-gran-poder-en-riesgo-por-conflictos-sociales/

- El Deber — Carnaval de Oruro 2026: 52 folkloric groups and 18 dance specialties  
  https://eldeber.com.bo/pais/carnaval-oruro-52-conjuntos-recorreran-tres-kilometros-medio-peregrinacion_1770990391

- La Paz Municipality / AMUN — Gran Poder economic estimate of up to USD 160 million including preparation cycle  
  https://lapaz.bo/el-gran-poder-generara-us-160-millones-desde-los-preparativos-hasta-la-entrada-del-3-de-junio/

## Note on figures

Cultural and economic figures vary by year and context. UNESCO sources are used to support the heritage recognition of Oruro Carnival and Gran Poder. Bolivian institutional and media sources are used to support recent scale indicators such as fraternities, participants, dance groups, and economic movement.
