# Thiago Sommerfeld — Azure Cloud Resume Challenge

This repository contains the frontend for my Azure Cloud Resume Challenge. The focus of this project is deploying and validating a static website with Azure Storage Static Website hosting.

## Objective

Host the resume website using Azure Storage Static Website hosting, providing a simple and cost-effective way to serve static web content.

## Azure resources

| Setting | Configuration |
| --- | --- |
| Service | Azure Storage Account |
| Account kind | StorageV2 (general-purpose v2) |
| Performance tier | Standard |
| Access tier | Hot |
| Redundancy | Locally-redundant storage (LRS) |
| Static website container | `$web` |

## Implementation

1. Created a Storage Account in the Azure portal.
2. Enabled the **Static Website** feature.
3. Set `index.html` as the index document.
4. Uploaded the website files, including HTML, CSS, JavaScript, and image assets, to the `$web` container.
5. Opened the primary static website endpoint and verified that the site was available.
6. Troubleshot an HTML rendering issue by correcting the blob's `Content-Type` metadata to `text/html`.

## Validation

The website loads through the Azure Storage static website endpoint, and the browser renders the HTML page correctly.

## Lessons learned

- Azure Storage Static Website hosting serves static content without requiring a web server.
- The `$web` container stores the files published by the static website feature.
- Correct HTTP `Content-Type` metadata helps browsers interpret and render files as intended.
- The Azure-provided endpoint can be used to verify a deployment before configuring a custom domain.

## Current limitations and next steps

- The site currently consists of static frontend files.
- The visitor counter and backend API have not yet been implemented.
- Automated deployment through GitHub Actions is planned.
- A custom domain has not yet been configured.

## Website files

- `index.html` — resume website markup
- `assets/` — stylesheets, scripts, and web fonts
- `images/` — website images

---

Built by Thiago Sommerfeld as a personal portfolio and cloud learning project.
