API and configuration reference
===============================

Verification endpoints
----------------------

.. code-block:: text

   POST /api/v1/verify/url
   POST /api/v1/verify/text
   POST /api/v1/verify/image
   POST /api/v1/verify/audio
   POST /api/v1/verify/video
   GET  /api/v1/results/{job_id}
   GET  /api/v1/history
   GET  /api/v1/audit/{job_id}

Publisher management
--------------------

.. code-block:: text

   GET    /api/v1/publishers
   POST   /api/v1/publishers
   PUT    /api/v1/publishers/{id}
   DELETE /api/v1/publishers/{id}

Provenance record operations
----------------------------

.. code-block:: text

   GET  /api/v1/crypto/issuers
   GET  /api/v1/crypto/issuers/{id}
   POST /api/v1/crypto/issuers
   POST /api/v1/crypto/issuers/{id}/revoke
   POST /api/v1/crypto/article-snapshots
   POST /api/v1/crypto/evidence-bundles
   POST /api/v1/crypto/review-events
   POST /api/v1/crypto/manifests/sign
   POST /api/v1/crypto/manifests/verify
   GET  /api/v1/crypto/manifests/{id}
   GET  /api/v1/crypto/records/{object_type}/{record_id}/history
   GET  /api/v1/crypto/records/{object_type}/{record_id}/compare

The upstream README lists routes but does not supply a complete request/response
schema for each endpoint; this reference deliberately omits inferred payloads.

Selected environment variables
------------------------------

``DATABASE_URL``
   PostgreSQL connection string.

``REDIS_URL``
   Redis connection string.

``COHERE_API_KEY``
   Optional reranking API key; lexical fallback is documented without it.

``NEXT_PUBLIC_API_BASE_URL``
   Client-visible API base URL.

``INTERNAL_API_BASE_URL``
   Frontend-to-backend service URL within Docker.

``BACKEND_CORS_ORIGINS_RAW``
   Comma-separated frontend origins allowed by the API.

``UPLOAD_DIR``
   Local uploaded-file storage directory.

``REQUEST_TIMEOUT_SECONDS``
   URL extraction timeout setting.

``PLATFORM_SIGNING_PRIVATE_KEY_B64``
   Optional development signing-key setting. In production, configure stable,
   protected signing material rather than relying on the documented ephemeral key.

``TIMESTAMP_MODE``
   Timestamp mode, ``internal`` by default or ``rfc3161`` for the stated
   production integration point.

Refer to the upstream ``.env.example`` for the authoritative current list.
