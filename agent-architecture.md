flowchart TB
    subgraph TOP[" "]
        direction LR
        TR["TRIGGERS<br/>New transaction claim"]
        CH["CHANNELS<br/>Internal staff interface"]
        HO["HANDOFF<br/>Escalation · Human approval · Named owner"]
    end

    subgraph HARNESS["THE HARNESS"]
        direction TB
        subgraph UPPER[" "]
            direction LR
            INS["INSTRUCTIONS<br/>Complaint-handling rules<br/>Scope · Permissions · Escalation"]
            LOOP["MODEL REASONING<br/>Perceive → Plan and decide<br/>Act → Observe<br/>Repeat as needed"]
            KNOW["KNOWLEDGE AND GROUNDING<br/>Approved procedures<br/>Transaction-status rules"]
        end

        subgraph LOWER[" "]
            direction LR
            MEM["MEMORY AND CONTEXT<br/>Claim ID · Checks completed<br/>Case status · Missing evidence"]
            TOOLS["TOOLS AND ACTIONS<br/>Retrieve authorised records<br/>Reconcile data · Summarise evidence<br/>Update case · Route claim"]
        end
    end

    DATA["SYSTEMS OF RECORD AND DATA<br/>Authorised transaction records · Case-management system<br/>Bank or service-provider confirmations where access is approved"]

    GOV["HUMAN OVERSIGHT · EVALUATION · OBSERVABILITY<br/>Human approval for refunds and complex disputes · Action logs · Accuracy monitoring"]

    TOP --> HARNESS
    HARNESS --> DATA
    DATA --> GOV

    style TOP fill:#ffffff,stroke:#ffffff
    style HARNESS fill:#f8f7f4,stroke:#e60023,stroke-width:2px
    style UPPER fill:#ffffff,stroke:#ffffff
    style LOWER fill:#ffffff,stroke:#ffffff
    style TR fill:#20205e,color:#ffffff,stroke:#20205e
    style CH fill:#20205e,color:#ffffff,stroke:#20205e
    style HO fill:#20205e,color:#ffffff,stroke:#20205e
    style INS fill:#ffffff,color:#171747,stroke:#b8b8cc
    style LOOP fill:#ffffff,color:#171747,stroke:#e60023,stroke-width:2px
    style KNOW fill:#ffffff,color:#171747,stroke:#b8b8cc
    style MEM fill:#ffffff,color:#171747,stroke:#b8b8cc
    style TOOLS fill:#ffffff,color:#171747,stroke:#b8b8cc
    style DATA fill:#20205e,color:#ffffff,stroke:#20205e
    style GOV fill:#fff0b3,color:#171747,stroke:#e0ad00,stroke-width:2px
