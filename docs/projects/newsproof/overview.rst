Architecture and verification model
===================================

NewsProof combines a Next.js frontend and a FastAPI backend. PostgreSQL provides
persistent storage, Redis is included in the service stack, and Alembic
manages database migrations. A separate Chrome extension exposes a shorter
verification workflow for the active browser tab.

Input processing
----------------

The web application accepts a URL, pasted text or uploaded media. A URL is
extracted server-side; image processing uses Tesseract OCR. Video processing
attempts key-frame OCR before falling back to media metadata. Audio currently
uses metadata-based preprocessing; speech transcription is not yet part of
the documented implementation.

Verification and evidence
-------------------------

The pipeline separates provenance proof from supporting evidence. The
repository documents **Verified** only when strong first-layer proof exists;
a trusted proof mismatch results in **Verification Failed**. **Not
Verifiable** indicates that reliable provenance proof was not found; a
**Timeout** indicates incomplete extraction or verification. Other evidence
layers cannot independently produce Verified.

Cohere embedding/reranking is optional. Without the API key, the system uses
a lexical overlap fallback rather than requiring Cohere access.

Cryptographic provenance
------------------------

The provenance subsystem handles article snapshots, evidence bundles and
review events. It constructs canonical JSON, computes a SHA-256 digest and
signs it using an Ed25519 private key. Verification checks digests, signatures,
issuer status, timestamp data and version-chain continuity. This mechanism
provides a record integrity trail; it does not itself determine truthfulness.

Sources
-------

- `NewsProof README <https://github.com/MeherazChayan/NewsProof#readme>`_
- `Source architecture notes <https://github.com/MeherazChayan/NewsProof/tree/main/docs>`_
