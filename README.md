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

The site is published from the `main` branch root through GitHub Pages at `https://github.com/mynameismilindm-design/shivashankarandco-website`. `.nojekyll` prevents Jekyll processing. The custom domain `shivashankarandco.com` is configured in GitHub Pages and the `CNAME` file. The four GitHub apex A records and the `www` CNAME are saved at Squarespace; Google Workspace MX, SPF and DKIM records are preserved. Form activation and email delivery are verified. HTTPS provisioning remains pending before the secure launch can be marked complete.

The domain registration and Google Workspace subscription remain separate from hosting. This repository contains only public website content and assets; it does not contain mailbox credentials, private API keys or customer submissions.

## Enquiry form activation

The contact form uses FormSubmit's standard form POST endpoint for `proprietor@shivashankarandco.com`. It includes an email field for replies, the selected services, a honeypot and the provider's default CAPTCHA. CAPTCHA has not been disabled.

The recipient confirmed FormSubmit activation on 20 November 2026. An authorized setup test with Registration and Book-keeping selected passed the provider's CAPTCHA and redirected to the configured thank-you URL. The recipient confirmed that the test email arrived correctly, including both selected services. End-to-end email delivery is verified. The thank-you page is temporarily blocked by the custom domain's pending HTTPS certificate; no security warning was bypassed. A successful redirect alone does not prove email delivery.

The success redirect is `https://shivashankarandco.com/thank-you/`, so it is intended for the connected custom domain. During temporary GitHub Pages testing, use care before submitting: that redirect will still use the final domain. The thank-you page does not claim that an email has been delivered.

FormSubmit may provide an opaque form endpoint after activation; that endpoint can replace the email URL in the form action. Do not put SMTP passwords or private API keys into the HTML or JavaScript.

## Design and assets

- Background: teal `#126B62` and white sections.
- Heading font: Gloock, regular; body font: Inter. Both load through Google Fonts.
- The supplied edited proprietor portrait is bundled locally at `assets/m-r-shivashankar.png`.
- The contact recipient is `proprietor@shivashankarandco.com`; the additional email is `shivashankarandco@yahoo.com`.
- Phone links use international dialling format, while their displayed text matches the approved content.

The website is a static implementation and does not include Squarespace's visual editor or hosted form service.
