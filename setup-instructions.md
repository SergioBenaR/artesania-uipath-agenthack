# Setup Instructions

This project was built as a UiPath AgentHack prototype using UiPath Automation Cloud.

## Prerequisites

- UiPath Automation Cloud account
- Access to UiPath Apps
- Access to UiPath AI Agents / Agent Builder
- Access to Analyze Files
- Access to Action Apps
- Access to Maestro BPMN
- An OpenAI-compatible model available inside UiPath AI Agents

## 1. Create the artisan intake form in UiPath Apps

Create a new UiPath App with the title:

**ArtesanIA — Registro de Obra Artesanal**

Add the following fields:

- Artisan name
- Piece name
- Dance
- Festival
- Image upload field
- Submit button

Example form values:

- Artisan name: Sara Mendoza
- Piece name: Boceto Traje Caporales
- Dance: Caporales
- Festival: Carnaval de Oruro

After submission, show a success message:

**Tu obra ha sido enviada a ArtesanIA para análisis y certificación. En breve recibirás tu ficha cultural.**

## 2. Create the AI Agent

Create a UiPath AI Agent named:

**ArtesanIA-Agente-Analisis**

Configure the agent with:

- A multimodal model
- Analyze Files tool
- Inputs:
  - artisan name
  - piece name
  - declared dance
  - festival
  - uploaded image/file

Use the agent prompt documented in:

`agent-prompt.md`

The agent should return structured JSON with fields such as:

- piece_type
- declared dance
- AI-suggested dance
- confidence level
- identifying elements
- dominant colors
- visible materials
- artisan technique
- cultural symbols
- review required

## 3. Create the human validation step

Create an Action App using a simple approval/review template.

The human reviewer should validate:

- Image quality
- Declared dance
- Visible cultural elements
- AI-generated cultural record
- Whether the piece should be approved or corrected before certification

Example task title:

**Validate ArtesanIA cultural record**

## 4. Create the Maestro BPMN workflow

Create a Maestro BPMN process with the following flow:

1. Artisan piece submitted
2. Analyze artisan piece with AI
3. Validate cultural record
4. Generate certificate and hash
5. Certified artisan piece

The workflow is documented in:

`maestro-workflow.md`

## 5. Certificate and hash step

For the hackathon prototype, the certificate/hash step is modeled as part of the workflow.

The intended production behavior is:

- Generate a digital certificate
- Create a hash from the validated cultural record
- Use the hash as tamper-evident proof of authorship and creation date
- Optionally anchor the hash to a blockchain or timestamping service

## Prototype status

This hackathon version demonstrates the core components:

- UiPath Apps intake form
- AI Agent with Analyze Files
- Human validation through Action Apps
- Maestro BPMN orchestration
- Certificate/hash step modeled in the process

The next implementation step is to fully connect the form submission, uploaded image, AI output, human validation result, and certificate/hash generation into one executable end-to-end workflow.
