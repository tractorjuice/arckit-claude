# G-Cloud Submission Pack Guide

> **Guide Origin**: Community | **ArcKit Version**: [VERSION]

`/arckit-uk-gcloud:submission-pack` bundles all approved documents for a G-Cloud service into a submission
folder and writes a manifest. It is an export action: it copies existing artefacts and does not
create a new ArcKit document type.

---

## Command

```bash
/arckit-uk-gcloud:submission-pack <service project or service name>
```

Output:

```text
projects/<NNN>-<service-name>/submission/
projects/<NNN>-<service-name>/submission/manifest.md
```

---

## When to Use

- After `/arckit-uk-gcloud:review` shows the service is ready or close to ready.
- When supplier-wide and per-service documents need to be assembled for CCS upload.
- When evidence files, pricing, SDD, security, supplier profile, and declaration need one manifest.

---

## Required Artefacts

| Artefact | Source command |
|----------|----------------|
| `ARC-000-SUPP` | `/arckit-uk-gcloud:supplier-profile` |
| `ARC-000-DECL` | `/arckit-uk-gcloud:declaration` |
| `ARC-<NNN>-SVCD` | `/arckit-uk-gcloud:service-design` |
| `ARC-<NNN>-SDD` | `/arckit-uk-gcloud:sdd-lot1`, `/arckit-uk-gcloud:sdd-lot2`, or `/arckit-uk-gcloud:sdd-lot3` |
| `ARC-<NNN>-PRIC` | `/arckit-uk-gcloud:pricing` |
| `ARC-<NNN>-SECA` | `/arckit-uk-gcloud:security` |

---

## Manifest Contents

The generated `submission/manifest.md` should include:

- Service name, lot, project number, framework number, and assembly date.
- The copied file list with source ARC IDs.
- Evidence still to upload to the Digital Marketplace.
- A pre-submission checklist.
- Submission steps and clarification-response reminders.

---

## Guardrails

- Do not create a service project here; run `/arckit-uk-gcloud:service-design` first.
- Do not rewrite approved source documents while assembling the pack.
- Treat the pack as an internal aid, not a guarantee of CCS acceptance.
- Confirm live framework deadlines and upload requirements before submission.

---

## Related Commands

- `/arckit-uk-gcloud:review` - Readiness check before packing.
- `/arckit-uk-gcloud:declaration` - Supplier-wide declaration input.
- `/arckit-uk-gcloud:security` - Security evidence input.
