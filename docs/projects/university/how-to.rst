Run the research prototype
==========================

Prerequisites
-------------

- Node.js 20 or later
- npm

Installation
------------

.. code-block:: console

   git clone https://github.com/MeherazChayan/My-University-Portal.git
   cd My-University-Portal
   npm install

Copy the sample environment file. In Windows PowerShell:

.. code-block:: powershell

   Copy-Item .env.example .env

On a shell that supports ``cp``:

.. code-block:: console

   cp .env.example .env

Start the development server:

.. code-block:: console

   npm run dev

Open ``http://localhost:3000``.

Inspect the demonstration
-------------------------

1. Begin at the dashboard at ``/`` and inspect the profile and service navigation.
2. Open ``/advising`` to explore course discovery and comparison.
3. Open ``/scholarships`` to view eligibility and projection interfaces.
4. Open ``/delegation`` to examine proposed assistant authority boundaries.
5. Review a simulated service page via ``/services/[slug]``.

These actions demonstrate UI flows on fictional data and do not trigger real
university transactions.

Available project scripts
-------------------------

.. code-block:: console

   npm run build
   npm run lint
   npm run typecheck

The commands are published in the project's README. Their successful execution
has not been verified in this documentation workspace.
