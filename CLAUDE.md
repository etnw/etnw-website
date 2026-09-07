# CLAUDE.md — etnw.eu Website Rebuild

## Project overview

Rebuilding etnw.eu, Etienne Winkelmuller's personal professional website, replacing an expired Squarespace site. Static site, plain HTML/CSS preferred, no framework or build step unless there's a real reason for one. Deploy target: Cloudflare Pages. Legal entity behind the site: ETNW Consulting (Einzelunternehmen, Munich).

## Content source

`content/old-site-copy.md` is the previous site's content and is the primary source of truth for substance and tone. Treat it as the base to work from, not a rough draft to reinvent. `images/` contains the profile photo and service artwork, match images to the sections they were created for, ask if placement is ambiguous rather than guessing.

## What to keep vs adapt

**Keep:** the overall content and tone of the old site. Don't rewrite the voice or restructure sections that already work just for the sake of change.

**Adapt:** the services section. The offering has moved on since the old copy was written, current focus is senior semiconductor commercial operator work (embedded commercial leadership, retainer engagements) and building The Engine Factory (TEF), a separate consulting brand at theenginefactory.com. Reflect the current direction here rather than porting the old service descriptions over unchanged.

**Non-negotiable:** the semiconductor product and business unit executive background stays front and center regardless of how the services section evolves. 25+ years, full P&L ownership, product lines built from zero to $10M+ revenue, this is the core credibility anchor, not a detail to compress or bury under newer consulting positioning.

**Open question, don't decide silently:** how much this site should read as "available for full-time operator roles" versus "consulting and TEF-adjacent." If the old copy leaned a particular way, preserve that lean. If it's genuinely unclear, ask rather than picking a direction. Same applies to overlap with theenginefactory.com, this site should not duplicate TEF's website copy wholesale; a link over to TEF is fine, a rewritten version of TEF's own pitch is not.

## Accuracy guardrails

- No overclaiming. State gaps plainly rather than soft-framing them.
- Etienne owned the foundry migration strategy and program management (IHP to GlobalFoundries, at indie), not hands-on engineering. Never describe him as a "foundry migration specialist" or claim hands-on industrialization work.
- Don't invent metrics, dates, or claims that aren't in `old-site-copy.md`, the CV, or content Etienne provides directly. If something needed is missing, flag it and ask rather than filling the gap with something plausible-sounding.

## Impressum and legal page

German law requires a compliant Impressum for a site tied to a German business. Model it on the existing TEF Impressum, same legal entity:

- Etienne Winkelmuller, ETNW Consulting (Einzelunternehmen), Sendlinger Strasse 29, 80331 München, Deutschland
- Umsatzsteuer-ID: DE461952429
- Steuernummer: 148/203/21503
- Verantwortlich für den Inhalt nach § 18 Abs. 2 MStV: Etienne Winkelmuller, same address
- Standard Haftung für Inhalte, Haftung für Links, and Urheberrecht sections, generic boilerplate, reusable near-verbatim from the TEF site since it's the same entity

Contact details, confirmed by Etienne on 2026-09-07: e-mail contact@etnw.eu (etnw.eu's own, different from TEF's), phone +49 89 55273295 (deliberately the same number TEF uses). These are settled, no need to re-ask.

Add a Datenschutzerklärung (privacy policy) as well if the site has a contact form, analytics, or any embedded third-party scripts or fonts, standard requirement for German sites regardless of business size.

## Writing style, applies to all copy on this site

- No em dashes, anywhere, ever. Use a comma, a period, or restructure the sentence instead. Regular hyphens are fine for compound words, used sparingly.
- Direct and evidence-based. Lead with what he actually did, not a framing sentence about the problem first.
- No corporate buzzwords, no vague value-speak.
- Humble register, not braggy. Let the numbers and specifics carry the weight rather than telling the reader how impressive something is.
- Short, mostly parallel sentences over long compound ones.
- Don't narrate the reader's own situation back to them.

## Working style with Etienne

- Terse instructions. Don't restate the request back before acting on it.
- For content changes, propose the actual text, not a plan to write text.
- For non-trivial or structural decisions (what belongs on this site vs. TEF's site, how to frame the services section), analyze first, then recommend, rather than picking a direction unprompted.
- When real trade-offs exist, present them concisely, a short table is fine, rather than long prose.
- Ask before assuming when something is ambiguous (current services wording, Impressum contact details) rather than inventing something plausible to fill the gap.

## Technical notes

- Deploy target: Cloudflare Pages, plain static HTML/CSS.
- Domain: etnw.eu. DNS is being migrated to Cloudflare. Email runs through Microsoft 365 on this domain, if any change touches MX, TXT, or CNAME records, confirm the current record values with Etienne first rather than assuming, mail must not break.
- Git repo tracked from project start. Commit incrementally, not as one giant commit at the end.
