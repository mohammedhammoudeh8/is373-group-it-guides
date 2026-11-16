# IS373 Group Record · NJIT IT How-To Hub

Fall 2026 · Section 001 · Plan stage (Nov 17, 2026)

**Team:** Mohamad Hammoudeh · *partner not yet assigned* (this record will be updated when a partner joins).

## 3. Group content system + problem research

### Course problem and reader

**Reader:** an NJIT student (especially a new or commuter student) who hits a common campus tech problem, like connecting to campus Wi-Fi, setting up Duo two-factor, printing, or reaching the VPN, and needs short, trustworthy steps fast.

**Problem:** NJIT's IT help information is spread across many pages and is written for every case at once. Students end up asking friends or guessing. **Scope:** one collection of short how-to guides on a handful of common tasks, with one draft → review → publish flow.

### Permitted sources (planned manifest)

| ID | Source | Permission approach |
| --- | --- | --- |
| NJIT-IST-* | NJIT's public IT help pages (one row per page, with URL and date checked) | Public to read, **not** licensed for copying. We write our own short guides in our own words and link to the original page as the source; we do not republish NJIT text |
| TEAM-* | Guides written by team members | Our own work |

No private student data and no screenshots of personal accounts.

### Two approaches compared

| | A · Link directory | B · Reviewed short guides |
| --- | --- | --- |
| What it is | A page listing links to the right NJIT pages by topic | Members draft a short guide that cites the NJIT source page; a second member reviews it before it's published |
| Pros | Fast, no rewriting | Actually solves "too long, too scattered"; every guide is checked and sourced |
| Cons | Doesn't fix the core problem; student still reads the long page | More work; guides can go stale when NJIT changes a page |

**Chosen: B**, but only while every published guide keeps its source link and "date checked." A guide whose source changed goes back to draft.

### Chosen workflow (planned)

```text
source manifest (URL + date checked)
  → member drafts guide in the app (status: draft, private)
  → different member reviews: steps match the source? link works? (status: approved)
  → editor/admin publishes (status: published, visible to everyone)
  → readers search published guides by keyword (vector search optional later)
```

Built on the App Studio foundation (FastAPI with accounts and server-enforced member/admin roles): members draft, admins review/publish, visitors read published guides only. **Retrieval:** keyword search first, since guide titles use the same words students search ("Duo", "Wi-Fi", "print"). Graph adds little for a small set of independent how-tos; vector search is a possible later step for paraphrased searches.

### Stories / checks (all **planned**, none run yet)

1. A visitor sees only published guides; drafts stay private.
2. Every published guide shows its NJIT source link and date checked.
3. A member can draft, but cannot approve their own guide.
4. Importing the source manifest twice doesn't create duplicate entries.
5. A visitor searching "duo" finds the Duo setup guide.

### Owner / reviewer split (planned)

| Area | Owner | Reviewer |
| --- | --- | --- |
| Source manifest + import, draft workflow | Mohamad | Partner (TBD) |
| Review/publish behavior + permission checks | Partner (TBD) | Mohamad |
| Design, integration, final checks | Shared | Each reviews the other's PRs |

Assignments will be confirmed when the partner joins; no partner work is claimed here.

### Contribution notes

- **Mohamad Hammoudeh:** proposed the problem, reader and both approaches; drafted this record and the source/permission plan; will own the source manifest/import and draft workflow. Help received: Claude (AI) helped structure the record and the approach comparison.
- **Partner:** TBD.
