# SKACH Repository Policy

## Purpose and scope

The intention is for all code, data pipelines, notebooks and documentation produced for the project live in, are registered with, or are findable from the consortium GitHub organization **chsrc**. This keeps project outputs findable after people move on, lets us report them to funders, and makes them citable.

The policy covers any repository created or substantially developed with project funding, by any partner, from the project start date onwards.

## Where repositories live

1. **New repositories** are created directly in the organization, not in personal accounts.
2. **Existing personal repositories** are transferred into the organization (Settings → Danger Zone → Transfer ownership). Ask the org admins to add you as a member first. Old URLs will keep redirecting.
3. **Special case: Forks** are transferred the same way and stay linked to their upstream. If two people forked the same upstream, only one fork can move in; talk to the admins. Forks that have become independent projects can be detached via GitHub Support.
4. **Repositories that must stay elsewhere** (e.g. they mix project and non-project work, or belong to an institution) are listed in [`PROJECT_OUTPUTS.md`](PROJECT_OUTPUTS.md) with owner, purpose and work package if relevant. Please make sure the project work stays public or accessible to the consortium.

## Naming and tagging

The sections from here on are recommended practice, not requirements. They make repositories easier to find, cite and report on, so please follow them where you can and adapt them where they don't fit.

- **Suggested name:** `wpN-short-description`, lowercase with hyphens, e.g. `wp2-flood-model`, or `general-` for cross-cutting repos. A clear, descriptive name matters more than the prefix.
- **Description:** a one-line summary of what the repo does.

## Recommended files in each repository

| File | What it contains |
| --- | --- |
| `README.md` | What the repo is, how to run it, a contact person, and a funding line such as: "This work was funded by the State Secretariat for Education, Research and Innovation (SERI) under the SKACH consortium." |
| `LICENSE` | An open licence, default **\[MIT / Apache-2.0\]** for code and **CC-BY-4.0** for documents and data, unless a partner agreement says otherwise. |
| `CITATION.cff` | Authors, title, version and DOI once one exists, so others can cite the work. |

Templates for all three are available in the chsrc `.github` repo.

## Access and roles

- **Org owners:** Owners include people from across the consortium's institutes so requests are not waiting on one specific person. 
- **Repo creators** keep admin rights on repos they bring in.
- **External collaborators** can be added as outside collaborators on specific repos by default, can be added as org members if needed.
- We strongly encourage enabling two-factor authentication for github. When someone leaves the project, admins remove them from the org; their repos stay.
- Please reach out to the existing org owners if you would like access, or should be an owner yourself. 

## Releases and archiving

- Consider making a GitHub **release** whenever a version is used in a paper, deliverable or demo.
- Consider connecting a repo to **Zenodo** archives each release and gives it a DOI automatically. Adding the DOI to the README and `CITATION.cff` makes it easy to cite.
- Where possible, cite the DOI rather than the GitHub URL in deliverables and publications.
- At project end, a final release and a note on maintenance status in the README are good practice.

## AI-assisted code

Using AI coding tools (e.g. GitHub Copilot, ChatGPT, Claude) is fine. The person who commits the code stays responsible for it.

- **Review it like your own work:** read, understand and test AI-generated code before committing it.
- **Check what you share:** don't paste credentials, personal data or unpublished partner code into AI tools unless your institution has approved that tool for such data.
- **Watch licensing:** AI tools can reproduce existing code verbatim. Where available, turn on filters that block suggestions matching public code (e.g. in Copilot settings).
- **Be transparent:** if a substantial part of a repo was AI-generated, say so briefly in the README or commit messages. Some journals and funders ask for this.
- **Authorship:** list people, not AI tools, as authors in `CITATION.cff`.
- **AI agents with repo access** (bots that open pull requests) should go through the same review as any other contributor, with no access to secrets.

## What to keep out of repositories

- Passwords, API keys, tokens or other credentials. GitHub secrets or environment variables work better.
- Personal data, or data covered by a data-sharing agreement. Linking to where it is stored is safer.
- Large raw data files. Zenodo or an institutional repository suits these better; link to them from the repo.

If something sensitive is committed by mistake, please tell the chsrc org admins quickly. Deleting the file is not enough, because it stays in the history.

## Suggested checklist for members

- [ ] Accept the invitation to join chsrc
- [ ] Transfer your project repositories into the org, or register them in [`PROJECT_OUTPUTS.md`](PROJECT_OUTPUTS.md)
- [ ] Consider a clear name (e.g. with a `wpN-` prefix) and add a description
- [ ] Add a README funding line, LICENSE and CITATION.cff
- [ ] Make a release for any version used in a deliverable

Questions: **\[Rohini Joshi, rohini.joshi@fhnw.ch\]**.
