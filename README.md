# -# Chest Drain Position Safety Agent Skill

## 1. Overview

This repository contains a prototype nursing Agent Skill for identifying potential position-related safety risks in patients with a chest drainage system.

The Skill is designed to transform relevant nursing safety knowledge into a structured, checkable workflow that an AI agent can follow.

The focus is not autonomous clinical decision-making, but information organization, risk identification, safety reminders, and human verification.

## 2. Clinical Scenario

Chest drainage systems are used in clinical care for patients who require drainage from the pleural or thoracic space.

Patient repositioning, movement of the drainage system, or changes in tubing configuration may introduce potential mechanical safety risks.

This Skill focuses on the relationship between:

- Patient position
- Chest tube and tubing configuration
- Drainage collection system position
- System integrity
- Relevant clinical changes

## 3. Agent Goal

The Agent should be able to:

1. Identify the patient's current position.
2. Detect whether the patient has recently changed position.
3. Organize information about the chest drainage system.
4. Identify potential tubing or positioning problems.
5. Identify missing or contradictory information.
6. Classify the potential safety risk.
7. Generate a structured safety reminder.
8. Determine whether bedside human verification is required.

## 4. Input

The Skill may use the following information:

### Patient

- Current body position
- Recent repositioning
- Relevant respiratory observations
- Relevant clinical changes

### Chest drainage system

- Presence of a chest tube
- Documented tube location
- Drainage collection system
- Drainage system position
- Connection status

### Tubing

- Kinking
- Compression
- Occlusion
- Excessive dependent loops
- Disconnection
- Displacement

### Reference information

- Institutional protocol
- Device instructions
- Physician or nursing orders

If essential information is unavailable, the Agent should identify the missing information rather than infer it.

## 5. Core Workflow

The Skill follows a structured workflow:

Patient position
↓
Recent repositioning?
↓
Drainage system position
↓
Tubing configuration
↓
System integrity
↓
Clinical warning information
↓
Risk classification
↓
Human verification

The workflow is intended to support consistent and reproducible safety assessment.

## 6. Risk Categories

The Agent classifies the available information into four categories:

### No identified position-related risk

No relevant position-related abnormality is identified from the available information.

### Potential position-related risk

A possible problem involving system positioning or tubing configuration is identified.

### Urgent human verification required

The available information suggests a potentially significant device-related safety concern or concerning clinical change.

### Insufficient information

Important information required for assessment is unavailable or contradictory.

## 7. Output

The Agent produces a structured assessment containing:

- Patient position
- Recent repositioning
- Drainage system position
- Tubing configuration
- System integrity
- Clinical warning information
- Risk classification
- Reason for classification
- Human verification requirement

This structure makes the Agent's output easier to inspect and evaluate.

## 8. Safety Boundaries

This Skill is a decision-support component.

The Agent must not independently:

- Diagnose a clinical complication
- Reposition a chest tube
- Clamp or unclamp a chest tube
- Disconnect or reconnect the drainage system
- Change suction settings
- Modify physician orders

When a potential high-risk situation is identified, the Agent should prompt qualified healthcare professionals to perform bedside assessment.

## 9. Human Oversight

The Agent is responsible for:

- Organizing information
- Detecting potential safety risks
- Explaining why a risk was identified
- Identifying missing information
- Prompting human verification

Qualified healthcare professionals remain responsible for bedside assessment and clinical decisions.

## 10. Intended Use

This Skill is intended for:

- Nursing informatics research
- Nursing education
- Clinical simulation
- Prototype nursing Agents
- Human-AI collaboration research
- Structured clinical reasoning research

It is not intended to function as an independent clinical decision-making system.

## 11. Repository Structure

nursing-agent-chest-drain-safety/
│
├── README.md
└── SKILL.md

## 12. Version

Version: v1.0

Status: Prototype

This repository is intended for research and educational development.
