# Methodology and Scope Appendix

## 1. Assessment Context

This appendix documents the testing context, scope boundaries, and limitations of the assessment described in the main report. The assessment was intentionally narrow and limited to externally observable behaviors and non-destructive testing of public-facing systems.

## 2. Scope of Review

The assessment focused on the following areas:

- HTTP response headers and publicly exposed metadata;
- PHP runtime version disclosure and technology identification;
- public phpMyAdmin setup exposure;
- TLS protocol enforcement and connection behavior;
- cookie security attributes and session-related parameters;
- DNS wildcard behavior and arbitrary subdomain resolution;
- search functionality and input-handling validation for common injection patterns.

## 3. Testing Model

The testing model was black-box and non-destructive. It did not rely on internal system access, application source code, database access, or privilege escalation. The objective was to assess publicly observable security posture, not to prove full application safety across all internal logic and code paths.

## 4. Limitations

The following limitations should be considered:

- No source code or server-side configuration inspection was available.
- No authenticated application testing was performed.
- No database-level validation beyond public error behavior was conducted.
- No destructive exploitation or service disruption testing was performed.
- The absence of observed exploitation does not confirm complete absence of vulnerabilities.

## 5. Technical Notes

Where a finding was based on a public indicator rather than direct confirmation of an exploit, the report explicitly called for manual validation against the exact production environment. This applies particularly to:

- the specific PHP package revision and vendor patch state,
- the applicability of public CVEs to the live environment,
- the current live TLS policy and cipher configuration,
- the actual use and classification of affected cookies,
- the operational necessity of wildcard DNS records.

## 6. Reporting Standard

The assessment was drafted to align with professional expectations for external security review reporting, including:

- clear executive summaries,
- structured technical findings,
- severity rationale,
- evidence-based recommendations,
- implementation prioritization,
- clearly labeled limitations and reviewer follow-up items.
