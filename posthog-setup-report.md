<wizard-report>
# PostHog post-wizard report

The wizard has completed a deep integration of your project. PostHog analytics has been added to this Next.js 16 App Router application. The integration uses `instrumentation-client.ts` for client-side initialization (the recommended approach for Next.js 15.3+), a reverse proxy via `next.config.ts` rewrites to keep ingestion traffic first-party, and inline `posthog.capture()` calls on every homepage CTA. Error tracking is enabled via `capture_exceptions: true`.

| Event | Description | File |
|-------|-------------|------|
| `deploy_now_clicked` | User clicks the "Deploy Now" CTA button on the homepage | `app/page.tsx` |
| `documentation_clicked` | User clicks the "Documentation" link on the homepage | `app/page.tsx` |
| `templates_link_clicked` | User clicks the "Templates" inline link in the homepage description | `app/page.tsx` |
| `learning_center_clicked` | User clicks the "Learning" center inline link in the homepage description | `app/page.tsx` |

## Next steps

We've built some insights and a dashboard for you to keep an eye on user behavior, based on the events we just instrumented:

- **Dashboard – Analytics basics**: https://eu.posthog.com/project/161464/dashboard/628843
- **CTA clicks over time** (line chart, 30d): https://eu.posthog.com/project/161464/insights/Tn4iUqzT
- **Most clicked CTA** (bar chart, 30d): https://eu.posthog.com/project/161464/insights/RbMWAjHH
- **Deploy Now conversion funnel**: https://eu.posthog.com/project/161464/insights/E0T8Egtg
- **Unique users clicking any CTA** (DAU, 30d): https://eu.posthog.com/project/161464/insights/xPh7Rdac
- **Documentation vs Deploy engagement ratio** (stacked, 60d): https://eu.posthog.com/project/161464/insights/H73wXN9j

### Agent skill

We've left an agent skill folder in your project. You can use this context for further agent development when using Claude Code. This will help ensure the model provides the most up-to-date approaches for integrating PostHog.

</wizard-report>
