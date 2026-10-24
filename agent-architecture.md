# MoMo Transaction Claims Resolution Agent
## Proposed Agent Architecture

### 1. Triggers
- A new transaction claim is submitted by a MoMo user.
- The claim is recorded in MoMo's authorised case-management system.

### 2. Channels
- Internal case-management interface for MoMo support and operations staff.
- Staff review and escalation interface.

### 3. Handoff
- Escalate conflicting transaction records, suspected fraud, and complex disputes to authorised staff.
- Human approval is required for refunds, compensation, and financial-liability decisions.
- Each escalated case must have a clearly assigned responsible team or staff member.

---

## The Harness

### Instructions
- Investigate transaction claims within the agent's approved scope.
- Follow MoMo's authorised complaint-handling procedures.
- Do not invent missing transaction information or promise unverified outcomes.
- Do not independently approve or execute refunds or compensation.
- Escalate cases that require human judgement or exceed the agent's permissions.

### Memory and Context
- Maintain the current claim ID and relevant transaction details during investigation.
- Track which checks have been completed and what information remains missing.
- Record the current case status and previous investigation actions.
- Retain only necessary information under approved data-retention policies.

### Knowledge and Grounding
- MoMo's approved complaint-handling procedures.
- Official transaction-status definitions and investigation rules.
- Approved guidance for common transaction discrepancies.
- Authorised transaction records and relevant case history, subject to access permissions.

### Tools and Actions
- Retrieve permitted transaction records through approved APIs.
- Compare available transaction references, timestamps, amounts, and statuses.
- Classify claims and prepare evidence summaries.
- Update case status where authorised.
- Route unresolved or complex cases to the responsible staff team.
- Draft user updates based on verified information.

### Agent Loop — Model Reasoning
1. **Perceive:** Interpret the claim and available transaction evidence.
2. **Plan and decide:** Identify the next investigation step and whether more evidence is needed.
3. **Act:** Use authorised tools to retrieve or compare records and update the case.
4. **Observe:** Check the outcome and determine whether to continue investigating, complete the permitted task, or escalate to a human.

The loop may repeat until the claim is sufficiently investigated or requires human intervention.

---

### Systems of Record and Data
- Authorised transaction records.
- Complaint and case-management records.
- Approved case-status history.
- Relevant bank or service-provider confirmations, only where authorised integrations are available.

### Human Oversight, Evaluation and Observability
- Human review for complex disputes, suspected fraud, and refund or compensation decisions.
- Logging of data access, tool calls, case updates, and escalation reasons.
- Evaluation of evidence accuracy, classification quality, escalation appropriateness, and processing time.
- Access controls, privacy safeguards, and monitoring for errors or unauthorised actions.

---

## Proposed Scope and Limitations
This architecture is a proposed design, not a claim that all required integrations currently exist at MoMo. Implementation depends on approved system access, data availability, and agreements with relevant third parties.
