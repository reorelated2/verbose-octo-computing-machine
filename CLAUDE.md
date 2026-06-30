# Kyle Real Estate Agentic Operating System

## Mission

Build the most advanced Zapier Agents based real estate operating system possible for Kyle Kleinman, Miami real estate agent.

This is not a basic Zap system. This is an agentic operations layer.

Use:
- Zapier Agents as the primary agentic brain
- Zapier MCP as the tool execution layer
- Zapier Tables as memory, audit log, approval queue, and lead state database
- Zaps as deterministic trigger and execution rails
- Interfaces as Kyle’s mobile control panel
- Twilio/SMS as Kyle’s fastest approval channel

## Operating Principle

The agent prepares decisions. Kyle approves client facing action.

Never send client facing communication without Kyle approval unless explicitly configured as safe automation.

## Core Workflows

1. Lead intake
   - Watch new and updated leads
   - Classify urgency, seriousness, intent, lead source, stage, and risk
   - Detect whether the lead needs immediate response, follow up, consult booking, lender intro, showing setup, or nurture

2. AI analysis
   For each meaningful lead or client event, generate:
   - seriousness score
   - urgency score
   - lead stage
   - likely motivation
   - risk flags
   - KPI risk
   - next best action
   - recommended Kyle message
   - execution plan
   - audit summary

3. Approval gate
   Send Kyle an SMS approval request before client facing execution.

   Valid Kyle responses:
   - APPROVE
   - EDIT
   - NO
   - SNOOZE
   - DONE

4. Execution
   After approval:
   - send message
   - update CRM or Agent Tools
   - create task
   - create calendar event
   - update Zapier Table
   - log final outcome

5. Audit logging
   Every action must log:
   - lead_id
   - event_type
   - received_at
   - recommended_action
   - approval_status
   - approved_at
   - executed_at
   - response_time
   - final_outcome
   - error_state
   - notes

## Real Estate Rules

Kyle’s priorities:
- fast speed to lead
- clean follow up discipline
- short client ready messaging
- no generic AI tone
- no sloppy automation
- no unauthorized client communication
- protect time
- qualify hard
- move serious buyers and sellers quickly

Default tone for client text:
- short
- clear
- human
- confident
- Miami real estate agent tone
- no corporate language

Avoid:
- “circle back”
- “just checking in”
- “touch base”
- long explanations
- fake enthusiasm
- robotic phrasing

## Build Order

1. Confirm Zapier MCP tools available
2. Confirm Zapier Agents setup path
3. Create required Zapier Tables
4. Wire trigger sources
5. Build approval queue
6. Build SMS approval loop
7. Build LLM analysis step
8. Build execution rails
9. Build audit logging
10. Test end to end with fake lead

## Required End To End Test

A fake lead must flow through the full system:

1. Lead enters table
2. Agent analyzes lead
3. Agent creates recommendation
4. Kyle receives SMS
5. Kyle replies APPROVE
6. Approved action executes
7. Audit log updates
8. Final status is visible in table/interface

Until this works, do not build predictive scoring, voice, or competitive intelligence.

## Definition of Done

The system is done only when:
- live trigger works
- AI recommendation works
- Kyle approval SMS works
- approved execution works
- audit logging works
- failure states are logged
- Kyle can run it from mobile
