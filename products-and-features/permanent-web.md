# Permanent Web

<figure><img src="../.gitbook/assets/Permanent Web icon.png" alt="" width="375"><figcaption></figcaption></figure>

The **permanent web**, or **permaweb**, is a decentralized layer of the internet where data, applications, and websites are stored permanently and remain accessible through a global network of gateways.

Unlike traditional websites (Web2) that rely on centralized servers and can disappear at any time if the hosting goes down, the Permaweb ensures that all content — from uploaded files to frontend code — remains permanently online as long as the blockchain network is alive.

## Comparison: Traditional Website vs. Decoy Phrase

| Aspect                             | Traditional Website (Web2)                                      | Decoy Phrase Website                                                       |
| ---------------------------------- | --------------------------------------------------------------- | -------------------------------------------------------------------------- |
| **Hosting**                        | Hosted on centralized servers (VPS, cloud hosting)              | Permanently stored on Arweave (decentralized storage)                      |
| **Cost**                           | Requires recurring payments (monthly/yearly)                    | One-time payment at upload, permanent afterward                            |
| **Offline Risk**                   | Can go offline if the server is down, not renewed, or hacked    | Cannot be deleted, shut down, or modified by third parties                 |
| **HTTP Error Pages**               | Needs to handle errors like 404/500 via backend logic           | Errors handled at static app level; content always accessible via TxID     |
| **CDN (Content Delivery Network)** | Often depends on services like Cloudflare for caching & routing | Uses AR.IO decentralized gateways (many nodes, no single point of failure) |
| **Data Ownership**                 | Controlled by hosting provider                                  | Fully owned, immutable, and controlled by the wallet                       |
| **File Storage**                   | Depends on cloud services or backend infrastructure             | Files are stored permanently and publicly on the Arweave blockchain        |
| **Transparency**                   | Server activity is not always visible                           | All files and transactions are verifiable on-chain (e.g., via ViewBlock)   |
| **Domain**                         | Uses traditional DNS                                            | Uses Arweave Name System (ArNS) — cannot expire or be taken down           |
| **Encryption**                     | Typically server-side encryption                                | End-to-end encryption in the user’s browser (Web Crypto API)               |

## Why Is the Decoy Phrase Website Permanent?

Decoy Phrase leverages [**Arweave**](https://www.arweave.org/) and [**AR.IO**](https://ar.io/) technologies, allowing all critical components of the application to be:

* [x] Stored as permanent data on the blockchain
* [x] Accessible forever through the decentralized AR.IO gateway network
* [x] Deployed once and remain live indefinitely — with no recurring hosting fees

Deployment is handled using tools like **ArLink**, which upload the final static version of the website to Arweave and bind it to a permanent **Arweave Name System (ArNS)** domain.

## Decoy Phrase Architecture

```
[ User ]
   ↓
Frontend (Next.js + Tailwind)
   ↓
Web Crypto API (In-Browser Encryption)
   ↓
Turbo SDK
   ↓
Bundling (ANS-104 Format)
   ↓
Arweave Network (Permanent Storage)
   ↓
AR.IO Gateways (Public Access)
   ↓
ArNS Domain (Permanent Web Address)
```

#### Core Components:

* **Frontend:** Static Next.js app hosted on Arweave
* **Crypto:** End-to-end encryption in the user’s browser using Web Crypto API
* **Storage:** Files and metadata are bundled with [Turbo](https://turbo.ar.io/) and uploaded to [Arweave](https://ao.arweave.net/)
* **Deployment:** Performed via [ArLink](https://arlink.ar.io/)
* **Domain:** Uses [**Arweave Name System (ArNS)**](https://arns.app/#/) as a permanent web address (non-expiring DNS alternative)
