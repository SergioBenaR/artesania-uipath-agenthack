# ArtesanIA

ArtesanIA is an agentic workflow for documenting, validating, and certifying Bolivian artisan heritage.

## Project description

The project helps artisans submit images of costumes, masks, embroidery, or design sketches through a simple UiPath Apps intake form. A UiPath AI Agent analyzes the uploaded file using Analyze Files, extracts visible cultural and design elements, and prepares a structured cultural record.

The record is then reviewed by a human through Action Apps before the certification step. The final workflow is orchestrated in UiPath Maestro BPMN and includes certificate/hash generation for tamper-evident authorship evidence.

## UiPath components used

- UiPath Apps
- UiPath AI Agents
- Analyze Files
- UiPath Action Apps
- UiPath Maestro BPMN

## Agent type

Low-code AI Agent using UiPath Agent Builder and Analyze Files.

## Workflow

1. Artisan submits metadata and image.
2. AI Agent analyzes the file.
3. Human reviewer validates the cultural record.
4. System generates certificate and hash.
5. Artisan piece becomes certified.

## Setup instructions

This hackathon prototype was built in UiPath Automation Cloud. To reproduce it, create a UiPath Apps form, configure a UiPath AI Agent with Analyze Files, add a human validation step with Action Apps, and orchestrate the workflow in Maestro BPMN.
