---
title: Synchronizace kontaktů přímo z aplikace Sales na kontakty nebo odběratele v aplikaci Finance and Operations
description: Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci entit Kontakt (Kontakty) a Kontakty (Odběratelé) z Microsoft Dynamics 365 for Sales do Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: fbc75702c9db1e877addc4605dcb444c344dfa5c
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742440"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-finance-and-operations"></a>Synchronizace kontaktů přímo z aplikace Sales na kontakty nebo odběratele v aplikaci Finance and Operations

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Než budete moci použít řešení Zpeněžnění potenciálního zákazníka, měli byste se seznámit s modulem [Integrace dat do služby Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).

Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci entit Kontakt (Kontakty) a Kontakty (Odběratelé) přímo z Microsoft Dynamics 365 for Sales do Microsoft Dynamics 365 for Finance and Operations.

## <a name="data-flow-in-prospect-to-cash"></a>Tok dat ve zpeněžení potenciálního zákazníka

Řešení Zpeněžení potenciálního zákazníka používá funkci Integrace dat k synchronizaci dat mezi instancemi aplikací Finance and Operations a Sales. Šablony zpeněžení potenciálního zákazníka dostupné v rámci funkce integrace dat umožňují tok dat účtů, kontaktů, produktů, prodejních kvót, prodejních objednávek a prodejních faktur mezi aplikacemi Finance and Operations a Sales. Následující obrázek znázorňuje, jak jsou data synchronizována mezi aplikacemi Finance and Operations a Sales.

[![Tok dat ve zpeněžení potenciálního zákazníka](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Šablony a úkoly

Chcete-li získat přístup k dostupným šablonám, otevřete [Centrum pro správu PowerApps](https://preview.admin.powerapps.com/dataintegration). Vyberte **Projekty**a v pravém horním rohu vyberte **Nový projekt**, abyste zvolili veřejné šablony.

K synchronizaci entit Kontakt (Kontakty) v aplikaci Sales a Kontakt (Odběratelé) v aplikaci Finance and Operations slouží následující šablony a základní úkoly:

- **Názvy šablon v integraci dat:**

    - Kontakty (Sales do Fin and Ops) - přímo
    - Kontakty na odběratele (Sales do Fin and Ops) - přímo

- **Názvy úkolů v projektu integrace dat:**

    - Kontakty
    - ContactToCustomer

Následující úkol synchronizace je požadován před tím, než může dojít k synchronizací kontaktů: Účty (Sales do Fin and Ops)

## <a name="entity-sets"></a>Sady entit

| Sales    | Finance and Operations |
|----------|------------------------|
| Kontakty | CDS kontakty           |
| Kontakty | Zákazníci V2           |

## <a name="entity-flow"></a>Tok entity

Kontakty se spravují v aplikaci Sales a synchronizují se do aplikace Finance and Operations.

Kontakt v aplikaci Sales se může stát buď kontaktem nebo odběratelem v aplikaci Finance and Operations. K určení toho, zda kontakt v aplikaci Sales má být synchronizován do aplikace Finance and Operations jako kontakt nebo odběratel, vyhledá systém následující vlastnosti kontaktu v aplikaci Sales:

- **Synchronizace na odběratele v aplikaci Finance and Operations:** Kontakty, u nichž je možnost **Je aktivní zákazník** nastavena na **Ano**
- **Synchronizace na kontakt v aplikaci Finance and Operations:** Kontakty, kde je možnost **Je aktivní zákazník** nastavena na **Ne** a **Společnost** (nadřazený účet/kontakt) odkazuje na účet (ne na kontakt)

## <a name="prospect-to-cash-solution-for-sales"></a>Řešení Potenciální zákazník pro hotovost v aplikaci Sales

Do kontaktu bylo přidáno nové pole **Je aktivní odběratel**. Toto pole slouží k rozlišení kontaktů, které mají prodejní aktivitu, a kontaktů, které nemají prodejní aktivitu. Hodnota **Je aktivní odběratel** je nastavena na **Ano** pouze pro kontakty, které obsahují odpovídající nabídky, objednávky nebo faktury. V aplikaci Finance and Operations jsou jako odběratelé synchronizováni pouze tyto kontakty.

Do kontaktu bylo přidáno nové pole **IsCompanyAnAccount**. Toto pole označuje, zda je kontakt propojen se společností (nadřazený účet/kontakt) typu **Účet**. Tyto informace slouží k identifikaci kontaktů, které mají být synchronizovány s aplikací Finance and Operations jako kontakty.

Do kontaktu bylo přidáno nové pole **Číslo kontaktu** pro pomoc se zaručením přirozeného a jedinečného klíče pro integraci. Po vytvoření nového kontaktu je automaticky generována hodnota **Číslo kontaktu** pomocí číselné řady. Hodnota se skládá z údaje **CON** a následně dalšího čísla číselné řady, a pak přípony šest znaků. Tady je příklad: **CON-01000-BVRCPS**

Když je pro aplikaci Sales použito integrační řešení, skript pro upgrade nastaví pole **Číslo kontaktu** pro existující kontakty pomocí číselné řady, o které jsme mluvili dříve. Skript pro upgrade nastaví také hodnotu v poli **Je aktivní zákazník** na **Ano** u všech kontaktů, které mají aktivitu prodeje.

## <a name="in-finance-and-operations"></a>V aplikaci Finance and Operations

Kontakty jsou označeny pomocí vlastnosti **IsContactPersonExternallyMaintained**. Tato vlastnost označuje, že je daný kontakt spravován externě. V takovém případě jsou externě spravované kontakty evidovány v aplikaci Sales.

## <a name="preconditions-and-mapping-setup"></a>Nastavení mapování a předpokladů

### <a name="contact-to-customer"></a>Kontakt na odběratele

- **CustomerGroup** je v aplikaci Finance and Operations povinná. Aby nedocházelo k chybám synchronizace, můžete zadat výchozí hodnotu v mapování. Tato výchozí hodnota se pak použije, pokud pole v aplikaci Sales zůstane prázdné.

    Výchozí hodnota šablony je **10**.

- Přidáním následujících mapování můžete snížit počet ručních aktualizací, které jsou potřebné v aplikaci Finance and Operations. Můžete použít výchozí hodnotu nebo mapu hodnot například z pole **Země/oblast** nebo **Město**.

    - **SiteId** - Pro produkty v aplikaci Finance and Operations je také možné definovat výchozí pracoviště. Pracoviště je nutné za účelem generování nabídky a řádky prodejní objednávky v aplikaci Finance and Operations.

        Hodnota šablony pro **SiteId** není definována.

    - **WarehouseId** - Pro produkty v aplikaci Finance and Operations je také možné definovat výchozí sklad. Sklad je nutné zadat za účelem generování nabídky a řádky prodejní objednávky v aplikaci Finance and Operations.

        Hodnota šablony pro **WarehouseId** není definována.

    - **LanguageId** – jazyk je nutný za účelem generování nabídek a prodejních objednávek v aplikaci Finance and Operations.
    
        Výchozí hodnota šablony je **en-us**.

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

Na následujícím obrázku je příklad mapování šablony v integraci dat. 

> [!NOTE]
> Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Sales do aplikace Finance and Operations.

### <a name="contact-to-contact"></a>Kontakt na kontakt

![Mapování šablony v integrátoru dat](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a>Kontakt na odběratele

![Mapování šablony v integrátoru dat](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a>Související témata

[zpeněžení potenciálního zákazníka](prospect-to-cash.md)

[Synchronizace účtů přímo z aplikace Sales na odběratele v aplikaci Finance and Operations](accounts-template-mapping-direct.md)

[Synchronizace produktů přímo z aplikace Finance and Operations na produkty v aplikaci Sales](products-template-mapping-direct.md)

[Synchronizace hlaviček a řádků prodejní objednávky přímo z aplikace Finance and Operations do aplikace Sales](sales-order-template-mapping-direct-two-ways.md)

[Synchronizace hlaviček a řádků prodejní faktury přímo z aplikace Finance and Operations do Sales](sales-invoice-template-mapping-direct.md)


