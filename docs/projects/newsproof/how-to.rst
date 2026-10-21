Local installation and browser extension
========================================

Start the application with Docker Compose
-----------------------------------------

The upstream README documents Docker Compose as the integrated local setup.
Install Docker Desktop, then run the following commands in a terminal:

.. code-block:: console

   git clone https://github.com/MeherazChayan/NewsProof.git
   cd NewsProof
   docker compose up --build

Review ``.env.example`` before starting the stack and configure required
values in ``.env`` as appropriate. Do not commit credentials.

The documented local service endpoints are:

- Frontend: ``http://localhost:3000``
- Backend: ``http://localhost:8000``
- PostgreSQL: ``localhost:5432``
- Redis: ``localhost:6379``

The backend container executes ``alembic upgrade head`` before serving the API.
These commands are transcribed from the upstream project documentation;
installation has not been independently executed in this documentation workspace.

Run application tests
---------------------

For the backend, with its dependencies installed:

.. code-block:: console

   cd backend
   pytest

For the frontend, with its npm dependencies installed:

.. code-block:: console

   cd frontend
   npm test

These are the project's published test commands, not a claim that tests passed.

Load the Chrome extension
-------------------------

1. Start the NewsProof stack.
2. Open ``chrome://extensions`` in Chrome.
3. Enable **Developer mode**.
4. Select **Load unpacked** and choose the ``extension/`` directory.
5. Use the popup on an article tab to request a URL verification preview.

The popup reports a label, a short explanation and a link to the full report.
Its default local targets are ``http://127.0.0.1:8000/api/v1`` for the API
and ``http://127.0.0.1:3000`` for the web app.

For temporary external testing, consult the upstream ``LOCAL_TUNNEL_SETUP.md``.
