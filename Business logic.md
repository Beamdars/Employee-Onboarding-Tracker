## BUSINESS LOGIC

The  business logic this system seeks to implement includes: 

> The trigger logic; starting from the first event, which entering a new hire record into the HRIS system, which would trigger a flow, as long as it contains all the required fields to create a task bucket.

> The Task logic is next; the system assigns task templates by matching pre-defined attributes like Dept, Employment type(full-time, student contractor or part-time), location. After which it assigns each task to a named owner or team.

> Due Date calculation Logic: every assigned task has a due date calculated from the start date. Individual tasks assigned will be factored with internal dead lines to respect dependencies.

> Dependency enforcement logic: tasks are created and assigned with dependency in mind. The system must enforce an ordering where downstream tasks cannot be marked complete until their prerequisites are done. for example; Network account should be followed by email creation. Equipment ordering must be confirmed before preparation, and preparation before issuance. This will ensure that all steps in the onboarding process is taken. 

> Escalation Logic: The system is built to trigger an alert within 1 hour to the task owner if a task is not completed by its due date and an escalation alert to the manager if the case is still open after 4 business hours.

The business logic will follow this flow; validate entry → select template → generate & assign tasks → enforce deadlines → escalate on failure → propagate changes → log everything.

