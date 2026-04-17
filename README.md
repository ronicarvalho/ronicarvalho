<div align="center">

# `RONI-CARVALHO.CBL`

</div>

```cobol
       IDENTIFICATION DIVISION.
       PROGRAM-ID.        RONI-CARVALHO-PROFILE.
       AUTHOR.            RONI CARVALHO.
       DATE-COMPILED.     CURRENT-SYSTEM-DATE.
       REMARKS.           SENIOR SOFTWARE ENGINEER & SOFTWARE ARCHITECT.

       ENVIRONMENT DIVISION.
       CONFIGURATION SECTION.
       SOURCE-COMPUTER.   DISTRIBUTED-CLOUD-MAINFRAME.
       OBJECT-COMPUTER.   KUBERNETES-CLUSTER-NODE.

       INPUT-OUTPUT SECTION.
       FILE-CONTROL.
           SELECT COM-PORTS ASSIGN TO "NETWORK-LINKS".

       DATA DIVISION.
       FILE SECTION.
       FD  COM-PORTS.
       01  LINK-RECORD             PIC X(100).

       WORKING-STORAGE SECTION.
       01  WS-PROFILE-DATA.
           05 WS-NAME              PIC X(30) VALUE 'Roni Carvalho'.
           05 WS-TITLE             PIC X(50) VALUE 'Sr. Software Engineer & Architect'.
           05 WS-EXPERIENCE        PIC X(20) VALUE '20+ Years Uptime'.
           05 WS-LOCATION          PIC X(20) VALUE 'Global (Remote)'.

       01  WS-CORE-ARCHITECTURE.
           05 WS-PROCESSOR         PIC X(50) VALUE '.NET C# / Spring Java / Python / Node.js'.
           05 WS-MEMORY            PIC X(50) VALUE 'Cloud / Kubernetes / Docker / Distributed'.
           05 WS-BASE-OS           PIC X(50) VALUE 'Event-Driven / Clean Architecture'.
           05 WS-CAPABILITY        PIC X(60) VALUE 'High Scalability, Resilience, Complex Integrations'.

       01  WS-COMPETENCIES.
           05 WS-COMP-1            PIC X(40) VALUE '[X] Cloud & Distributed Systems'.
           05 WS-COMP-2            PIC X(40) VALUE '[X] Software Arch & Design Patterns'.
           05 WS-COMP-3            PIC X(40) VALUE '[X] Event-Driven Architectures'.
           05 WS-COMP-4            PIC X(40) VALUE '[X] DevOps & Platform Engineering'.
           05 WS-COMP-5            PIC X(40) VALUE '[X] Domain-Driven & Clean Architecture'.
           05 WS-COMP-6            PIC X(40) VALUE '[X] Software Quality (TDD / BDD)'.
           05 WS-COMP-7            PIC X(40) VALUE '[X] Microservices & Choreography'.
           05 WS-COMP-8            PIC X(40) VALUE '[X] CI/CD Pipelines & GitOps'.

       01  WS-TECH-STACK.
           05 WS-BACKEND           PIC X(60) VALUE '.NET, Java, Spring, Python, Node, Go'.
           05 WS-FRONTEND          PIC X(60) VALUE 'React, Vue, JavaScript (ES6+)'.
           05 WS-CLOUD             PIC X(60) VALUE 'Azure, AWS, GCP, K8s, Docker'.
           05 WS-DATABASES         PIC X(60) VALUE 'SQL Server, Oracle, PostgreSQL, MongoDB'.
           05 WS-MESSAGING         PIC X(60) VALUE 'Kafka, REST, gRPC, WCF, BizTalk'.

       01  WS-PROFESSIONAL-HISTORY.
           05 WS-JOB-1-YEARS       PIC X(15) VALUE '2023 - CURR'.
           05 WS-JOB-1-COMPANY     PIC X(30) VALUE 'Capitani Group / Lojas Renner'.
           05 WS-JOB-1-ROLE        PIC X(40) VALUE 'Sr. Software Eng (MarTech/Loyalty)'.
           05 WS-JOB-2-YEARS       PIC X(15) VALUE '2021 - 2023'.
           05 WS-JOB-2-COMPANY     PIC X(30) VALUE 'XP Investimentos'.
           05 WS-JOB-2-ROLE        PIC X(40) VALUE 'Sr. Software Engineer (Private Bank)'.
           05 WS-JOB-3-YEARS       PIC X(15) VALUE '2021 - 2025'.
           05 WS-JOB-3-COMPANY     PIC X(30) VALUE 'TSCO Angola'.
           05 WS-JOB-3-ROLE        PIC X(40) VALUE 'DevOps Engineer Consultant'.
           05 WS-JOB-4-YEARS       PIC X(15) VALUE '2013 - 2021'.
           05 WS-JOB-4-COMPANY     PIC X(30) VALUE 'Angola Prev'.
           05 WS-JOB-4-ROLE        PIC X(40) VALUE 'Sr. Software Consultant'.
           05 WS-JOB-5-YEARS       PIC X(15) VALUE '1998 - 2013'.
           05 WS-JOB-5-COMPANY     PIC X(30) VALUE 'Multiple Enterprises'.
           05 WS-JOB-5-ROLE        PIC X(40) VALUE 'Software Engineer / Developer'.

       01  WS-EDUCATION.
           05 WS-EDU-1             PIC X(60) VALUE 'MBA in Project Management (AIEC) - In Progress'.
           05 WS-EDU-2             PIC X(60) VALUE 'Extension in Financial Mathematics (AIEC)'.
           05 WS-EDU-3             PIC X(60) VALUE 'Systems Analysis and Development (AIEC)'.

       01  WS-LANGUAGES.
           05 WS-LANG-PT           PIC X(30) VALUE 'Portuguese [||||||||||] 100%'.
           05 WS-LANG-EN           PIC X(30) VALUE 'English    [||||||    ]  65%'.

       PROCEDURE DIVISION.
       0000-MAIN-PROCESSING.
           DISPLAY '**************************************************************'.
           DISPLAY '* SYSTEM INITIALIZATION............................ STATUS: OK'.
           DISPLAY '* LOADING PROFILE_DATA.SYS......................... STATUS: OK'.
           DISPLAY '**************************************************************'.
           DISPLAY ' '.
           
           PERFORM 1000-DISPLAY-PROFILE.
           PERFORM 2000-DISPLAY-ARCHITECTURE.
           PERFORM 3000-DISPLAY-COMPETENCIES.
           PERFORM 4000-DISPLAY-HISTORY.
           PERFORM 5000-DISPLAY-EDUCATION.
           PERFORM 6000-DISPLAY-LINKS.
           
           DISPLAY '**************************************************************'.
           DISPLAY '* END OF EXECUTION. RETURN CODE 00000.                       *'.
           DISPLAY '**************************************************************'.
           STOP RUN.

       1000-DISPLAY-PROFILE.
           DISPLAY '>>> 010. USER_PROFILE'.
           DISPLAY '    NAME.......: ' WS-NAME.
           DISPLAY '    TITLE......: ' WS-TITLE.
           DISPLAY '    UPTIME.....: ' WS-EXPERIENCE.
           DISPLAY '    LOCATION...: ' WS-LOCATION.
           DISPLAY ' '.

       2000-DISPLAY-ARCHITECTURE.
           DISPLAY '>>> 020. CORE_ARCHITECTURE'.
           DISPLAY '    PROCESSOR..: ' WS-PROCESSOR.
           DISPLAY '    MEMORY.....: ' WS-MEMORY.
           DISPLAY '    BASE OS....: ' WS-BASE-OS.
           DISPLAY '    CAPABILITY.: ' WS-CAPABILITY.
           DISPLAY ' '.

       3000-DISPLAY-COMPETENCIES.
           DISPLAY '>>> 030. COMPETENCIES_AND_STACK'.
           DISPLAY '    ' WS-COMP-1 ' | ' WS-COMP-2.
           DISPLAY '    ' WS-COMP-3 ' | ' WS-COMP-4.
           DISPLAY '    ' WS-COMP-5 ' | ' WS-COMP-6.
           DISPLAY '    ' WS-COMP-7 ' | ' WS-COMP-8.
           DISPLAY ' '.
           DISPLAY '    --- TECH STACK DRIVERS ---'.
           DISPLAY '    BACKEND....: ' WS-BACKEND.
           DISPLAY '    FRONTEND...: ' WS-FRONTEND.
           DISPLAY '    CLOUD......: ' WS-CLOUD.
           DISPLAY '    DATABASES..: ' WS-DATABASES.
           DISPLAY '    MESSAGING..: ' WS-MESSAGING.
           DISPLAY ' '.

       4000-DISPLAY-HISTORY.
           DISPLAY '>>> 040. EXECUTION_LOG (PROFESSIONAL HISTORY)'.
           DISPLAY '    [' WS-JOB-1-YEARS '] ' WS-JOB-1-COMPANY.
           DISPLAY '      > ROLE: ' WS-JOB-1-ROLE.
           DISPLAY '    [' WS-JOB-2-YEARS '] ' WS-JOB-2-COMPANY.
           DISPLAY '      > ROLE: ' WS-JOB-2-ROLE.
           DISPLAY '    [' WS-JOB-3-YEARS '] ' WS-JOB-3-COMPANY.
           DISPLAY '      > ROLE: ' WS-JOB-3-ROLE.
           DISPLAY '    [' WS-JOB-4-YEARS '] ' WS-JOB-4-COMPANY.
           DISPLAY '      > ROLE: ' WS-JOB-4-ROLE.
           DISPLAY '    [' WS-JOB-5-YEARS '] ' WS-JOB-5-COMPANY.
           DISPLAY '      > ROLE: ' WS-JOB-5-ROLE.
           DISPLAY '    ... (EARLIER LOGS ARCHIVED / DUMPED) ...'.
           DISPLAY ' '.

       5000-DISPLAY-EDUCATION.
           DISPLAY '>>> 050. SYSTEM_VARIABLES'.
           DISPLAY '    EDUCATION_01: ' WS-EDU-1.
           DISPLAY '    EDUCATION_02: ' WS-EDU-2.
           DISPLAY '    EDUCATION_03: ' WS-EDU-3.
           DISPLAY ' '.
           DISPLAY '    LANGUAGES: ' WS-LANG-PT ' | ' WS-LANG-EN.
           DISPLAY ' '.

       6000-DISPLAY-LINKS.
           DISPLAY '>>> 060. OPEN_COM_PORTS (CONTACT_NETWORKS)'.
           DISPLAY '    LINKEDIN...: <a href="https://www.linkedin.com/in/roni-peterson-carvalho-roni-b75385281">CONNECT 0x01</a>'.
           DISPLAY '    GITHUB.....: <a href="https://github.com/ronicarvalho">CONNECT 0x02</a>'.
           DISPLAY '    EMAIL......: <a href="mailto:roni.carvalho@protonmail.com">SEND_MAIL 0x03</a>'.
           DISPLAY ' '.
```

<div align="center">
  <i>"Writing code with the precision of a mainframe, running it with the speed of the cloud."</i>
</div>
