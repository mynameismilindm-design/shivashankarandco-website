# Shivashankar & Co website

Static recreation of the approved Squarespace design for GitHub Pages. No package installation or build step is needed.

## Pages

- `index.html`: homepage
- `about/index.html`: firm and proprietor portrait
- `areas-of-practice/index.html`: seven services, including Registration
- `contact-us/index.html`: office contact details and enquiry form
- `thank-you/index.html`: form return page
- `404.html`: missing-page message

The header, navigation, page content and footer are present in the HTML. JavaScript only controls the mobile navigation. Links use relative paths so the site can be previewed under the repository's GitHub Pages path before the custom domain is connected.

## Local preview

From this directory, run `python3 -m http.server 8765`, then open `http://localhost:8765/`. Stop the server with Ctrl+C.

## Hosting

Publish the `main` branch root through GitHub Pages. `.nojekyll` prevents Jekyll processing. The intended custom domain is `shivashankarandco.com`. Add the `CNAME` file and GitHub Pages custom-domain setting only when ready to connect the domain. Preserve all Google Workspace MX and email verification/security records when changing website DNS.

The domain registration and Google Workspace subscription remain separate from hosting. This repository contains only public website content and assets; it does not contain mailbox credentials, private API keys or customer submissions.

## Enquiry form activation

The contact form uses FormSubmit's standard form POST endpoint for `proprietor@shivashankarandco.com`. It includes an email field for replies, the selected services, a honeypot and the provider's default CAPTCHA. CAPTCHA has not been disabled.

FormSubmit requires the recipient to activate the form through its confirmation email before enquiries are delivered. The first submission triggers that email. The proprietor should confirm it, then complete an agreed test enquiry and verify receipt. Website code alone cannot prove delivery. No activation or delivery test was performed while building these files.

The success redirect is `https://shivashankarandco.com/thank-you/`, so it is intended for the connected custom domain. During temporary GitHub Pages testing, use care before submitting: that redirect will still use the final domain. The thank-you page does not claim that an email has been delivered.

FormSubmit may provide an opaque form endpoint after activation; that endpoint can replace the email URL in the form action. Do not put SMTP passwords or private API keys into the HTML or JavaScript.

## Design and assets

- Background: teal `#126B62` and white sections.
- Heading font: Gloock, regular; body font: Inter. Both load through Google Fonts.
- The supplied edited proprietor portrait is bundled locally at `assets/m-r-shivashankar.png`.
- The contact recipient is `proprietor@shivashankarandco.com`; the additional email is `shivashankarandco@yahoo.com`.
- Phone links use international dialling format, while their displayed text matches the approved content.

The website is a static implementation and does not include Squarespace's visual editor or hosted form service.
