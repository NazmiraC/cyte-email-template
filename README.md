# Cyte Notify - welcome and verification email

## Handover

- Template key: `welcome-verify`
- Subject: `Welcome to Cyte - verify your email address`
- Layout: `cyte-notify-layout.html`
- Body fragment: `welcome-verify-body.html`
- Merged QA preview: `welcome-verify-preview.html`

## Placeholder contract

| Placeholder | Used in | Example | Required |
| --- | --- | --- | --- |
| `verificationUrl` | Button link | `https://app.cyte.co.za/verify?token=sample` | Yes |

The layout contains `{{Body}}` exactly once. It intentionally contains no other placeholders because Cyte Notify only resolves `{{Body}}` in layouts. The preview uses a safe example URL and is not the file to load as the Notify template.

## Implementation notes

- Table-based layout, inline styles, web-safe fonts and live text throughout.
- 600px desktop container with fluid mobile width.
- Address and contact columns stack below 600px.
- The call-to-action remains visible with images disabled and provides a 48px-high tap target.
- Styling is translated from Figma node `1:22`: navy header/title band, green CTA and divider, 30px content padding, and the two-column navy footer.
- `assets/cyte-logo.png` is the exact 124 x 41 Figma logo export and is referenced through its permanent public GitHub raw URL, as required by Notify.
- Footer copy and contact presentation follow the referenced Figma design.
- Test the merged result at 375px and 600px, with dark mode and images disabled, before production use.
