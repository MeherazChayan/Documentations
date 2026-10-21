Routes and implementation reference
===================================

Main application routes
-----------------------

``/``
   Student dashboard and portal assistant.

``/advising``
   Course discovery and advising preferences.

``/schedule``
   Class and examination schedules.

``/scholarships``
   Scholarship eligibility and improvement projections.

``/delegation``
   Agent permission and approval controls.

``/agent``
   A Phase 2 agent placeholder, not a completed connected AI service.

``/services/[slug]``
   Simulated service pages including ``course-drop``, ``semester-drop``,
   ``grade-sheet``, ``probation``, ``attendance``, ``payslip`` and ``requests``.

Implementation structure
------------------------

``src/app/``
   Next.js application routes.

``src/components/PortalAssistant.tsx``
   Shared assistant interface component, as identified by the README.

``src/lib/``
   Shared application utilities.

Configuration
-------------

The example environment file names ``DATABASE_URL`` and ``SESSION_SECRET``,
which the upstream README describes as reserved for future persistence and
authentication work. They should **not** be interpreted as evidence of an
operational database-backed authentication system in this prototype.

The upstream README does not specify a project license. Do not assume it is
licensed for redistribution merely because the repository is public.
