# Joining flow – co-producers and producers

**Owner:** João Mata · **Updated on:** 13/11/2026 · **SRS section:** Appendix – Analysis models
**Sources:** FR-01 to FR-08 and FR-14 in [RF01_GestaoAMAPMembrosEN.md](../RF01_GestaoAMAPMembrosEN.md) · [3.1](../../srs/3.1_AMAPMemberManagementEN.md) · [E-8](../../interviews/10-11-2026/Entrevista10_11EN.md) §1.3, §2.1, §2.2

These activity diagrams show the path of a person from the first contact until they are an active member of an AMAP. They complement the use cases "Request to join" (FR-03) and "Apply to an AMAP" (FR-08) of section 3.1. The states reached in each flow are detailed in the [state diagrams](DiagramasEstadoEN.md).

## 1. Co-producer joining

**Image (for the SRS):** [imagens/FluxoAdesaoCoprodutorEN.png](imagens/FluxoAdesaoCoprodutorEN.png)

```mermaid
flowchart TD
    A([Start]) --> B[Prospective co-producer opens the AMAP's<br/>public page or searches the portal]
    B --> C[Selects 'I want to join', fills in name,<br/>email and phone and accepts the Terms]
    C --> D{Accepts the Terms?}
    D -- No --> X1([Request not submitted])
    D -- Yes --> E[System records the request and notifies<br/>whoever handles it: management or main producer]
    E --> G{Are there places in the AMAP?}
    G -- No --> H[System adds the person to the<br/>waiting list, ordered by arrival]
    H --> I[A place opens: the system notifies<br/>the first person on the list]
    I --> F
    G -- Yes --> F{Management approves?}
    F -- No --> X2([Person notified; request rejected])
    F -- Yes --> J[Status 'on trial': the system schedules<br/>the trial deliveries configured by the AMAP]
    J --> K[Trial deliveries take place]
    K --> L[System invites the person to subscribe<br/>to the current or next cycle]
    L --> M{Subscribes?}
    M -- No --> X3([Status 'left'])
    M -- Yes --> N[Subscription confirmed and<br/>first payment request]
    N --> O([Active co-producer])
```

**Notes**
- **Places exist at two levels:** the AMAP's maximum capacity and the number of co-producers each producer accepts per product (E-8 §2.2, FR-14).
- **The number of trial deliveries** is configured per AMAP (e.g. 1 or 2), which resolves the difference between E-4 and D-C (DV-01).
- **Management may change the order of the waiting list**, recording the reason (group decision of 21/10, FR-03).
- What happens when a person does not subscribe after the trial is a **group assumption**; it was not discussed with the client.

## 2. Producer joining

**Image (for the SRS):** [imagens/FluxoAdesaoProdutorEN.png](imagens/FluxoAdesaoProdutorEN.png)

```mermaid
flowchart TD
    A([Start]) --> B{How does it start?}
    B -- Application --> C[Producer selects 'Apply'<br/>on the AMAP's page]
    B -- Invitation --> D[Management invites the producer;<br/>the producer opens the invitation]
    C --> E
    D --> E[Producer fills in name, location, main products,<br/>farming method and uploads documents,<br/>e.g. organic certificate]
    E --> F[System records the application<br/>and notifies management]
    F --> G{Farm visit?}
    G -- Yes --> H[AMAP members visit the farm and record<br/>the visit: date, who went, notes]
    G -- No --> I
    H --> I{Management approves?}
    I -- No --> X1([Producer notified; application rejected])
    I -- Yes --> J{Does the AMAP have capacity?}
    J -- No --> K[Producer goes to the waiting list<br/>and is notified when a place opens]
    K --> L
    J -- Yes --> L[Producer becomes active in the AMAP;<br/>documents shown on the public profile]
    L --> M[Producer states the dates they can deliver<br/>and what they can deliver]
    M --> N([Active producer, ready for the next cycle])
```

**Notes**
- An **invited** producer is invited to apply, with the selection practically made (E-8 §2.1).
- The **farm visit** is typical but not mandatory; the process may vary between AMAPs, but there is always a producer registration (E-8 §2.1).
- A producer can be in **several AMAPs**; each application is separate (E-8 §2.1, NFR-22).

## 3. AMAP joining the platform (context)

The producer and co-producer flows assume the AMAP already exists. When it does not, the AMAP is registered first.

**Image (for the SRS):** [imagens/FluxoAdesaoAMAPEN.png](imagens/FluxoAdesaoAMAPEN.png)

```mermaid
flowchart TD
    A([Start]) --> B[A person registers a new AMAP]
    B --> C[FAIR administrator requests the documentation:<br/>AMAP name, location, representative, NIF]
    C --> D[The person submits the documents]
    D --> E{FAIR administrator authorises?}
    E -- No --> X1([Registration not authorised])
    E -- Yes --> F[AMAP created; the person becomes<br/>its first manager]
    F --> G{Was the AMAP started by a producer?}
    G -- Yes --> H[The producer applies to the AMAP as producer<br/>and accepts the application as manager]
    G -- No --> I
    H --> I[Management configures the AMAP's rules<br/>and opens the public page]
    I --> J([AMAP ready to receive producers and co-producers])
```

**Note:** an AMAP started by a producer holds both the management and producer roles (E-8 §2.1, FR-06).
