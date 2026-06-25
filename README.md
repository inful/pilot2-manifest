# Manifest for Nasjonalt Genomsenter - Pilot 2

Vi er bioinformatikkmiljøene i Norge.
Vi arbeider for det samme målet: trygge, robuste og likeverdige helsetjenester for alle pasienter.

I dag er miljøene våre spredt, små og ofte alene om drift av kritisk infrastruktur.
Dette gir ulik praksis, ulik modenhet og ulikt pasienttjenestetilbud avhengig av geografi.

Denne fragmenteringen skal vi avvikle.

## Utfordring

Når hver region bygger alt selv:

- blir verktøy, metoder og kompetanse vanskelig å dele
- blir drift en ressurstyv for fagmiljøer som skal levere analyse og utvikling
- blir kvalitet, tilgjengelighet og beredskap mer sårbar enn nødvendig

## Retning

Vi bygger en nasjonal, samarbeidsdrevet plattformmodell der regionene kan:

- dele metoder, kompetanse, data og verktøy
- utvikle og forbedre tjenester sammen
- fungere som backup for hverandre når det er nødvendig
- dele data kontrollert mellom helseregioner og fagmiljøer

## Prinsipper

- Likeverdighet: Helsetilbud skal ikke avhenge av bosted.
- Samarbeid: Vi er sterkere og bedre sammen enn hver for oss.
- Standardisering: Felles grensesnitt gjør tjenester flyttbare og robuste.
- Bærekraft: Riktig kompetanse brukes på riktig oppgave.
- Åpenhet: Metoder og løsninger skal kunne forstås, deles og forbedres.

## Vårt felles minimum

Vi forplikter oss til en felles grunnmur av basistjenester.
Dette minimumet skal finnes i alle deltakende miljøer.

### Utvikling og samarbeid

- Forge med:
  - versjonskontroll (Git)
  - issue- og prosjektstyring
- CI/CD
- artefaktregister (docker, tarballs og tilsvarende)
- meldingstjeneste for samhandling (for eksempel Zulip)
- utviklingsmiljø (VM eller devcontainerbasert)

### Deployment og drift

- Kubernetes
- container-register
- metrikk, logging og tracing (OpenTelemetry-kompatibelt)
- block storage (predefinerte storage classes)
- object storage (S3-kompatibelt)
- databaser (PostgreSQL, MySQL, NoSQL-alternativ)
- message broker (NATS, RabbitMQ eller Kafka)
- secrets management (for eksempel Kubeseal/SOPS)
- authentication/authorization med felles prinsipper
- ingress/egress med automatisert sertifikathåndtering for HTTPS
- backup og gjenoppretting
- IAC (Ansible/Terraform)

### Beregning og analyse

- HPC for bearbeiding av sekvenseringsdata (somatisk, germline, humant og mikrobiologisk)
- SLURM-basert arbeidsflyt og støtte for etablerte orkestreringsverktøy som NextFlow, snakemake o.l. 

## Vår forpliktelse

Vi tar i bruk de-facto-standarder for utvikling, distribusjon og ressursforvaltning.
Med felles standarder kan tjenester flyttes mellom private skyplattformer i helseforetakene,
og ved behov videre til eksterne skytjenester.

## Vår ambisjon

- fra lokale særordninger til nasjonal samhandling
- fra sårbar drift til robust felleskapasitet
- fra fragmenterte løsninger til delte byggesteiner

Dette er ikke bare et teknisk initiativ - det er et felles løfte om kvalitet, beredskap og rettferdighet i norsk presisjonsmedisin.
