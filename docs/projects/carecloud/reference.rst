System inventory and boundaries
===============================

Published technologies
----------------------

- MERN stack: MongoDB, Express, React and Node.js, as described by the project.
- ``frontend/``: user-facing application directory.
- ``backend/``: server application directory.
- Root ``package.json`` and ``package-lock.json``: Node project manifests.

Published feature areas
-----------------------

- Doctor discovery and available appointment times.
- Online and in-person consultation booking.
- Medical-record related functionality.
- Payments.
- Community and health-awareness functions.

The README does not publish an endpoint-by-endpoint API specification, a
verified database schema or tested production-deployment instructions.
Those details are intentionally not inferred here.

Privacy considerations
----------------------

Medical-record and payment features require additional care when preparing
screenshots and tests. Use synthetic data; avoid disclosing account tokens,
personally identifying patient information or payment credentials.
