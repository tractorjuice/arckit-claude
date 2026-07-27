# G-Cloud Submission Review Guide

> **Guide Origin**: Community | **ArcKit Version**: [VERSION]

`/arckit-uk-gcloud:review` checks a G-Cloud service submission for completeness and internal consistency
before CCS submission. It validates the supplier profile, declaration, service design, SDD,
pricing, and security evidence as a joined submission set.

---

## Command

```bash
/arckit-uk-gcloud:review <service project or service name>
```

Output:

```text
projects/<NNN>-<service-name>/ARC-<NNN>-GCRV-v1.0.md
```

---

## When to Use

- After supplier-wide and service-specific documents are drafted.
- Before `/arckit-uk-gcloud:submission-pack`.
- When there are multiple revisions and you need a single readiness view.
- Before copying answers into the Digital Marketplace submission form.

---

## Required Artefacts

| Artefact | Command |
|----------|---------|
| `ARC-000-SUPP` | `/arckit-uk-gcloud:supplier-profile` |
| `ARC-000-DECL` | `/arckit-uk-gcloud:declaration` |
| `ARC-<NNN>-SVCD` | `/arckit-uk-gcloud:service-design` |
| `ARC-<NNN>-SDD` | `/arckit-uk-gcloud:sdd-lot1`, `/arckit-uk-gcloud:sdd-lot2`, or `/arckit-uk-gcloud:sdd-lot3` |
| `ARC-<NNN>-PRIC` | `/arckit-uk-gcloud:pricing` |
| `ARC-<NNN>-SECA` | `/arckit-uk-gcloud:security` |

---

## Review Areas

- Document existence and version currency.
- Marketplace mandatory fields and limits.
- Cross-document consistency for service name, lot, support, pricing, and security claims.
- Evidence gaps for certifications, hosting, security, data, and support statements.
- Action plan with owners and commands to rerun.

---

## Related Commands

- `/arckit-uk-gcloud:gcloud-competitors` - Run benchmark analysis before final review.
- `/arckit-uk-gcloud:submission-pack` - Bundle approved artefacts after review.
- `/arckit:risk` - Track material submission or delivery risks.
