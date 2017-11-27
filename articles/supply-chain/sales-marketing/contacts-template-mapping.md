---
title: "Synchronizace kontaktů z aplikace Sales s kontakty nebo odběrateli v aplikaci Finance and Operations"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci kontaktu (Kontakty) a kontaktu (odběratelé) z aplikace Microsoft Dynamics 365 for Sales do aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c838fef502f643c764fade9cd79ae770ffc36974
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a>Synchronizace kontaktů z aplikace Sales s kontakty nebo odběrateli v aplikaci Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Než budete moci použít řešení Zpeněžnění potenciálního zákazníka, seznamte se s modulem [Integrace dat Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration). 

Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci entit Kontakt (Kontakty) a Kontakt (Odběratelé) z aplikace Microsoft Dynamics 365 for Sales (Sales) do aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (Finance and Operations).

## <a name="templates-and-tasks"></a>Šablony a úkoly

K synchronizaci entit Kontakt (Kontakty) v aplikaci Sales a Kontakt (Odběratelé) v aplikaci Finance and Operations slouží následující šablony a základní úkoly:

- **Názvy šablon:**

    - Kontakty (Sales do Fin and Ops)
    - Kontakty s entitou Odběratel (prodej do modulů Fin a Ops)

- **Názvy úkolů v projektu:**

    - Kontakty
    - ContactToCustomer

Následující úkol synchronizace je požadován před synchronizací kontaktu: Účty (Prodej do modulů Fin a Ops)

## <a name="entity-sets"></a>Sady entit

| Prodej.    | CDS     | Finance and Operations |
|----------|---------|------------------------|
| Kontakty | Kontakt | CDS kontakty           |
| Kontakty | Účet | Zákazníci V2           |

## <a name="entity-flow"></a>Tok entity

Kontakty jsou spravovány v modulu Sales a jsou synchronizovány pro Common Data Service (CDS) a Finance and Operations.

Kontakt v aplikaci Sales se může stát kontaktem v CDS a Finance and Operations. Případně to může být účet v CDS a odběratel v modulu Finance and Operations. K určení, zda kontakt má být vydán v aplikaci Sales pro synchronizaci s aplikací CDS a Finance and Operations (například kontakty v aplikaci Sales &gt; kontakt v CDS &gt; Kontakty v aplikaci Finance and Operations), systém vyhledá následující vlastnosti kontaktu v aplikaci Sales:

- **Synchronizace s účtem v aplikaci CDS a zákazníkem v aplikaci Finance and Operations:** Kontakty, u nichž je možnost **Je aktivní zákazník** nastavena na **Ano**
- **Synchronizace s kontaktem v aplikaci CDS a kontaktem v aplikaci Finance and Operations:** Kontakty, kde je možnost **Je aktivní zákazník** nastavena na **Ne** a **Společnost** (Nadřazený účet/Kontakt) odkazuje na účet (ne na kontakt)

## <a name="prospect-to-cash-solution-for-sales"></a>Řešení Potenciální zákazník pro hotovost v aplikaci Sales 

Do kontaktu bylo přidáno nové pole **Je aktivní odběratel**. Toto pole slouží k rozlišení kontaktů, které mají prodejní aktivitu, a kontaktů, které nemají prodejní aktivitu. Hodnota **Je aktivní odběratel** je nastavena na **Ano** pouze pro kontakty, které obsahují odpovídající nabídky, objednávky nebo faktury. V aplikaci Finance and Operations jsou jako zákazníci synchronizovány pouze tyto kontakty.

Do kontaktu bylo přidáno nové pole **IsCompanyAnAccount**. Toto pole se používá k označení, zda je kontakt propojen se společností (nadřazený účet/kontakt) typu **Účet**. Tyto informace slouží k identifikaci kontaktů, které mají být synchronizovány s aplikací Finance and Operations jako kontakty.

Do kontaktu bylo přidáno nové pole **Číslo kontaktu** na pomoc se zaručení přirozeného a jedinečného klíče pro integraci. Po vytvoření nového kontaktu je automaticky generována hodnota **číslo kontaktu** pomocí číselné řady. Hodnota se skládá z údaje **CON** a následně dalšího čísla číselné řady, a pak přípony šest znaků. Tady je příklad: **CON-01000-BVRCPS**

Když je do aplikace Sales přidáno integrační řešení pro aplikaci Sales, skript pro upgrade nastaví pole **Číslo kontaktu** pro existující kontakty pomocí číselné řady, o které jsme diskutovali dříve. Skript pro upgrade nastaví také hodnotu v poli **Je aktivní zákazník** na **Ano** u všech kontaktů, které mají aktivitu prodeje.

## <a name="in-finance-and-operations"></a>V aplikaci Finance and Operations 

Kontakty jsou označeny pomocí vlastnosti **IsContactPersonExternallyMaintained**. Tato vlastnost označuje, že je daný kontakt spravován externě. V takovém případě jsou externě spravované kontakty evidovány v prodeji.

## <a name="preconditions-and-mapping-setup"></a>Nastavení mapování a předpokladů

### <a name="contact-to-contact"></a>Kontakt do kontaktu

- Aktualizujte **ID organizace CDS** mapování **Zdroj &gt; CDS**.

    - Výchozí hodnota šablony pro **Organization_OrganizationId [Organization ID]** je **ORG001**.
    - Výchozí hodnota šablony pro **PrimaryAccount_Organization_OrganizationId [ID organizace]** je **ORG001**.

- **Kód země/oblasti pro adresu** je v aplikaci Finance and Operations vyžadován. Aby nedocházelo k chybám synchronizace, můžete zadat výchozí hodnotu v mapování **CDS &gt; Operace**. Tato výchozí hodnota se pak použije, pokud pole v aplikaci Sales zůstane prázdné. Výchozí hodnota šablony pro **PrimaryAddressCountryRegionISOCode** je **USA**.
- Zkontrolujte, že v aplikaci Finance and Operations existuje hodnota pro následující pole. Pokud tyto informace nejsou v aplikaci Finance and Operations požadovány, můžete odebrat mapování z mapování **CDS &gt; Cíl**.

    - **Název pole v aplikaci Finance and Operations:** Rozhodnutí
    - **Mapování:** PrimaryAccountRole = DecisionMakingRole

### <a name="contact-to-customer"></a>Kontakt na odběratele

- Aktualizujte **ID organizace CDS** mapování **Zdroj &gt; CDS**. Výchozí hodnota šablony pro **Organization_OrganizationId [Organization ID]** je **ORG001**.
- **Kód země/oblasti pro adresu** je v aplikaci Finance and Operations vyžadován. Aby nedocházelo k chybám synchronizace, můžete zadat výchozí hodnotu v mapování **CDS &gt; Cíl**. Tato výchozí hodnota se pak použije, pokud pole v aplikaci Sales zůstane prázdné. Výchozí hodnota šablony pro **PrimaryAddressCountryRegionISOCode** je **USA**.
- **CustomerGroup** je v aplikaci Finance and Operations povinná. Aby nedocházelo k chybám synchronizace, můžete zadat výchozí hodnotu v mapování **CDS &gt; Cíl**. Tato výchozí hodnota se pak použije, pokud pole v aplikaci Sales zůstane prázdné. Výchozí hodnota šablony pro **CustomerGroupId** je **10**.
- Přidáním následujících mapování z aplikace **CD &gt; Cíl** můžete snížit počet ručních aktualizací, které jsou povinné v aplikaci Finance and Operations. Můžete použít výchozí hodnotu nebo mapu hodnot například z pole **Země/oblast** nebo **Město**.

    - **SiteId** - pro produkty v aplikaci Finance and Operations je také možné definovat výchozí pracoviště. Pracoviště je nutné za účelem generování nabídky a řádky prodejní objednávky v aplikaci Finance and Operations. Hodnota šablony pro **SiteId** není definována.
    - **WarehouseId** - pro produkty v aplikaci Finance and Operations je také možné definovat výchozí sklad. Sklad je nutné zadat za účelem generování nabídky a řádky prodejní objednávky v aplikaci Finance and Operations. Hodnota šablony pro **WarehouseId** není definována.
    - **LanguageId** – jazyk je nutný za účelem generování nabídek a prodejních objednávek v aplikaci Finance and Operations. Výchozí hodnota šablony pro **LanguageId** je **en-us**.

## <a name="template-mapping-in-data-integrator"></a>Mapování šablony v integrátoru dat

Na následujícím obrázku je příklad mapování šablony v integrátoru dat.

### <a name="contact-to-contact"></a>Kontakt do kontaktu

![Mapování šablony v integrátoru dat](./media/contacts-template-mapping-data-integrator-1.png)

![Mapování šablony pro kontakty v integrátoru dat](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a>Kontakt na odběratele

![Mapování šablony v integrátoru dat](./media/contacts-template-mapping-data-integrator-3.png)

![Mapování šablony pro kontakty v integrátoru dat](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Související témata

[Synchronizace produktů z aplikace Finance and Operations na produkty v aplikaci Sales](products-template-mapping.md)

[Synchronizace obchodních vztahů z aplikace Sales na odběratele v aplikaci Finance and Operations](accounts-template-mapping.md)

[Synchronizace hlaviček a řádků prodejních nabídek z aplikace Sales do aplikace Finance and Operations](sales-quotation-template-mapping.md)

[Synchronizace hlaviček a řádků prodejní objednávky z aplikace Finance and Operations do Sales](sales-order-template-mapping.md)

[Synchronizace hlaviček a řádků prodejní faktury z aplikace Finance and Operations do Sales](sales-invoice-template-mapping.md)

