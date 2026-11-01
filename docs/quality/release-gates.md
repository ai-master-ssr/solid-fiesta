# Quality and Release Gates

A release is eligible only when all applicable gates have evidence.

## Gate 1 — Functional correctness

- All required routes render and resolve correctly.
- Navigation, forms, search, and interactive controls behave as specified.
- Empty, loading, error, and success states are implemented.
- No placeholder links, dead controls, or fabricated content remain.

## Gate 2 — Responsive behavior

Verify supported viewport classes: narrow mobile, large mobile, tablet, laptop, and wide desktop. Check overflow, text wrapping, navigation, touch targets, image cropping, and layout stability.

## Gate 3 — Accessibility

- Semantic landmarks and heading hierarchy.
- Keyboard-operable interactions and visible focus.
- Accessible names and labels for controls.
- Sufficient text and non-text contrast.
- Reduced-motion support where motion is present.
- Form errors announced and associated with inputs.
- Automated checks supplemented by keyboard/manual review.

Target WCAG 2.2 AA unless the project specifies a stricter standard.

## Gate 4 — Performance

- Responsive, correctly sized images and modern formats where supported.
- Minimize render-blocking resources and unnecessary client-side JavaScript.
- Lazy-load below-the-fold media where appropriate.
- Avoid layout shifts and unnecessary third-party scripts.
- Measure real build output and representative pages; do not report assumed Lighthouse scores.

Use Core Web Vitals as operational targets: LCP <= 2.5 s, INP <= 200 ms, CLS <= 0.1 at the 75th percentile when field data is available.

## Gate 5 — Security and privacy

- Validate and normalize untrusted input.
- Protect forms and server actions against abuse.
- Apply least-privilege credentials and secret handling.
- Set appropriate security headers and content-security policy.
- Avoid exposing private keys, tokens, internal errors, or personal data.
- Document data collection, retention, consent, and third-party processors.

## Gate 6 — Search and content quality

- Unique title and description per indexable page.
- Canonical URLs and correct robots directives.
- Sitemap and structured data where appropriate.
- Social sharing metadata and descriptive image alt text.
- Content reviewed for accuracy, consistency, and legal claims.

## Gate 7 — Release readiness

- Production build succeeds.
- Required unit, integration, end-to-end, and accessibility checks pass.
- Independent review is complete.
- Environment variables and secrets are configured in the target environment.
- Preview/staging acceptance is recorded.
- Rollback procedure is known and tested or explicitly documented as untested.
- Deployment URL, build identifier, timestamp, and smoke-test results are recorded.

A missing check must be marked **not run** or **not applicable with rationale**; never silently treated as passed.
