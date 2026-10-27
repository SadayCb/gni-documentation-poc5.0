# LOAN_API — Workflows

[← Back to Overview](README.md) · [API Reference](api.md) · [Workflows](workflows.md) · [Data Model](data-model.md) · [Dependencies](dependencies.md) · [Error Handling](error-handling.md)

## Workflow index

- [Limit evaluation](#workflow-limit-evaluation)
- [Automatic payment](#workflow-automatic-payment)
- [Interest calculation](#workflow-interest-calculation)
- [Overdue transit](#workflow-overdue-transit)

<a id="workflow-limit-evaluation"></a>
### Limit evaluation

**Purpose:** Reconciles calculated limits with recorded limit accounts.

**Trigger / entry point:** [evaluate_limit_amount](api.md#evaluate-limit-amount)

```mermaid
flowchart TD
    A[Select eligible loan limits] --> B[Calculate available credit limit]
    B --> C[Compare recorded and calculated limits]
    C --> D[Create debit and credit amounts]
    D --> E[Post journal entries]
    E --> F[Finalize metadata and add history]

```

**Key business rules**

- Credit-line or card loan eligibility and active status are checked.
- Zero calculated limits apply to category 667 or elapsed loan end date.

**Result / side effects:** Processing may affect loan financial records or their history; see [Data Model](data-model.md) and [Error Handling](error-handling.md).

<a id="workflow-automatic-payment"></a>
### Automatic payment

**Purpose:** Processes payments for loans eligible in the selected run.

**Trigger / entry point:** [do_Auto_Payment](api.md#do-auto-payment)

```mermaid
flowchart TD
    A[Select loans for the requested run] --> B[Read plan and account data]
    B --> C[Prepare payment allocation]
    C --> D[Execute payment processing]
    D --> E[Record operational results]

```

**Key business rules**

- Processing is sensitive to the selected EOD/SOD phase and requested loan/range.

**Result / side effects:** Processing may affect loan financial records or their history; see [Data Model](data-model.md) and [Error Handling](error-handling.md).

<a id="workflow-interest-calculation"></a>
### Interest calculation

**Purpose:** Calculates loan interest for an eligible processing date.

**Trigger / entry point:** [do_int_calculation](api.md#do-int-calculation)

```mermaid
flowchart TD
    A[Select loans and processing phase] --> B[Read accounts and interest terms]
    B --> C[Determine calculation amounts]
    C --> D[Process calculated interest]
    D --> E[Record operation results]

```

**Key business rules**

- Inputs include processing date, loan identifier/range, and EOD/SOD phase.

**Result / side effects:** Processing may affect loan financial records or their history; see [Data Model](data-model.md) and [Error Handling](error-handling.md).

<a id="workflow-overdue-transit"></a>
### Overdue transit

**Purpose:** Applies overdue transition processing to qualifying loan accounts.

**Trigger / entry point:** [do_overdue_transit_operation](api.md#do-overdue-transit-operation)

```mermaid
flowchart TD
    A[Select overdue candidates] --> B[Evaluate grace and overdue conditions]
    B --> C[Resolve target overdue account]
    C --> D[Apply overdue transit operation]
    D --> E[Update related plan or records]

```

**Key business rules**

- Overdue eligibility depends on configured account categories and dates.

**Result / side effects:** Processing may affect loan financial records or their history; see [Data Model](data-model.md) and [Error Handling](error-handling.md).

