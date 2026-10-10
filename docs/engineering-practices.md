# Engineering practices

## Security by design

- Validate permissions and intent before administrative actions.
- Use nonces for state-changing WordPress requests.
- Sanitize external input and escape output for its destination context.
- Keep credentials outside source control.
- Minimise stored data and apply explicit retention rules.
- Treat third-party callbacks and webhooks as untrusted input.

## Maintainability

- Isolate integrations behind adapters.
- Keep analysis results independent from their visual presentation.
- Use lock files for reproducible dependencies.
- Prefer custom, purpose-built modules where third-party plugin combinations would introduce unnecessary coupling.
- Document release and rollback steps for production changes.

## Verification

- Automated PHP regression tests for platform behaviour and request guards.
- Browser-based checks for customer workflows and responsive presentation.
- Before-and-after review in a sandbox or staging environment.
- Production smoke checks after an approved deployment.

