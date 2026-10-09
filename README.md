
# Google Workspace APAC Customer Engineering Accelerators


Sample code that Google Workspace Customer Engineers in Asia Pacific use with
customers and partners during proofs of concept, pilots, and deployments.

NOTE: This project is intended for demonstration purposes only. It is not
intended for use in a production environment.

NOTE: This is not an officially supported Google product.

Eligibility for the
[Google Open Source Software Vulnerability Rewards Program](https://bughunters.google.com/open-source-security)
is determined by the
[Google Open Source Software Vulnerability Reward Program Rules](https://bughunters.google.com/about/rules/open-source/google-open-source-software-vulnerability-reward-program-rules).

## Security

To report a security issue, see [SECURITY.md](SECURITY.md).

## Samples

| Folder                                                                                          | Stage      | What it shows  |
| ----------------------------------------------------------------------------------------------- | ---------- | -------------- |
| [`presales/gemini-workspace-studio-poc-starter`](presales/gemini-workspace-studio-poc-starter/) | Pre-sales  | Apps Script    |
:                                                                                                 :            : that posts a   :
:                                                                                                 :            : notification   :
:                                                                                                 :            : card to a      :
:                                                                                                 :            : Google Chat    :
:                                                                                                 :            : space during a :
:                                                                                                 :            : PoC.           :
| [`postsales/admin-sdk-ou-dlp-onboarding`](postsales/admin-sdk-ou-dlp-onboarding/)               | Post-sales | Python dry-run |
:                                                                                                 :            : check of       :
:                                                                                                 :            : organizational :
:                                                                                                 :            : units before a :
:                                                                                                 :            : migration      :
:                                                                                                 :            : wave.          :

## Before You Run a Sample

*   Use a test or pilot Google Workspace domain, not production.
*   Read the sample's `README.md` for prerequisites, scopes, and setup.
*   Store secrets such as webhook URLs or keys in a secret store or script
    properties, never in code.
*   Review the code and the requested OAuth scopes with your administrator.

## Terms

*   The samples use Google Workspace and Google Cloud APIs, which are subject to
    the [Google Workspace Terms of Service](https://workspace.google.com/terms/)
    and the [Google APIs Terms of Service](https://developers.google.com/terms).
*   Licensed under the [Apache License 2.0](LICENSE).

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).
