---
title: Synchronizace kontaktů přímo z aplikace Sales na kontakty nebo odběratele v aplikaci Supply Chain Management
description: Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci entit Kontakt (Kontakty) a Kontakty (Odběratelé) z Dynamics 365 Sales do Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 8cbc2909c3f4533b4ea68e522f0874873989f3ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994037"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-supply-chain-management"></a>Synchronizace kontaktů přímo z aplikace Sales na kontakty nebo odběratele v aplikaci Supply Chain Management

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> Než budete moci použít řešení Zpeněžnění potenciálního zákazníka, měli byste se seznámit s modulem [Integrace dat do služby Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).

Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci tabulek Kontakt (Kontakty) a Kontakty (Odběratelé) přímo z Dynamics 365 Sales do Dynamics 365 Supply Chain Management.

## <a name="data-flow-in-prospect-to-cash"></a>Tok dat ve zpeněžení potenciálního zákazníka

Řešení Zpeněžení potenciálního zákazníka používá funkci Integrace dat k synchronizaci dat mezi instancemi aplikací Supply Chain Management a Sales. Šablony zpeněžení potenciálního zákazníka dostupné v rámci funkce integrace dat umožňují tok dat účtů, kontaktů, produktů, prodejních kvót, prodejních objednávek a prodejních faktur mezi aplikacemi Supply Chain Management a Sales. Následující obrázek znázorňuje, jak jsou data synchronizována mezi aplikacemi Supply Chain Management a Sales.

[![Tok dat ve zpeněžení potenciálního zákazníka](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Šablony a úkoly

Chcete-li získat přístup k dostupným šablonám, otevřete [Centrum pro správu PowerApps](https://preview.admin.powerapps.com/dataintegration). Vyberte **Projekty** a v pravém horním rohu vyberte **Nový projekt**, abyste zvolili veřejné šablony.

K synchronizaci tabulek Kontakt (Kontakty) v aplikaci Sales a Kontakt (Odběratelé) v aplikaci Supply Chain Management slouží následující šablony a základní úkoly:

- **Názvy šablon v integraci dat**

    - Kontakty (Sales do Supply Chain Management) – Přímo
    - Kontakty do odběratele (Sales do Supply Chain Management) – Přímo

- **Názvy úkolů v projektu integrace dat**

    - Kontakty
    - ContactToCustomer

Následující úkol synchronizace je požadován před tím, než může dojít k synchronizací kontaktů: Účty (Sales do Supply Chain Management)

## <a name="entity-sets"></a>Sady entit

| Prodej.    | Správa dodavatelsko-odběratelského řetězce |
|----------|------------------------|
| Kontakty | Dataverse kontakty           |
| Kontakty | Zákazníci V2           |

## <a name="entity-flow"></a>Tok entity

Kontakty se spravují v aplikaci Sales a synchronizují se do aplikace Supply Chain Management.

Kontakt v aplikaci Sales se může stát buď kontaktem nebo odběratelem v aplikaci Supply Chain Management. K určení toho, zda kontakt v aplikaci Sales má být synchronizován do aplikace Supply Chain Management jako kontakt nebo odběratel, vyhledá systém následující vlastnosti kontaktu v aplikaci Sales:

- **Synchronizace na odběratele v aplikaci Supply Chain Management:** Kontakty, u nichž je možnost **Je aktivní zákazník** nastavena na **Ano**
- **Synchronizace na kontakt v aplikaci Supply Chain Management:** Kontakty, kde je možnost **Je aktivní zákazník** nastavena na **Ne** a **Společnost** (nadřazený účet/kontakt) odkazuje na účet (ne na kontakt)

## <a name="prospect-to-cash-solution-for-sales"></a>Řešení Potenciální zákazník pro hotovost v aplikaci Sales

Do kontaktu byl přidán nový sloupec **Je aktivní odběratel**. Tento sloupec slouží k rozlišení kontaktů, které mají prodejní aktivitu, a kontaktů, které nemají prodejní aktivitu. Hodnota **Je aktivní odběratel** je nastavena na **Ano** pouze pro kontakty, které obsahují odpovídající nabídky, objednávky nebo faktury. V aplikaci Supply Chain Management jsou jako odběratelé synchronizováni pouze tyto kontakty.

Do kontaktu byl přidán nový sloupec **IsCompanyAnAccount**. Tento sloupec označuje, zda je kontakt propojen se společností (nadřazený účet/kontakt) typu **Účet**. Tyto informace slouží k identifikaci kontaktů, které mají být synchronizovány s aplikací Supply Chain Management jako kontakty.

Do kontaktu byl přidán nový sloupec **Číslo kontaktu** pro pomoc se zaručením přirozeného a jedinečného klíče pro integraci. Po vytvoření nového kontaktu je automaticky generována hodnota **Číslo kontaktu** pomocí číselné řady. Hodnota se skládá z údaje **CON** a následně dalšího čísla číselné řady, a pak přípony šest znaků. Tady je příklad: **CON-01000-BVRCPS**

Když je pro aplikaci Sales použito integrační řešení, skript pro upgrade nastaví sloupec **Číslo kontaktu** pro existující kontakty pomocí číselné řady, o které jsme mluvili dříve. Skript pro upgrade nastaví také hodnotu ve sloupci **Je aktivní zákazník** na **Ano** u všech kontaktů, které mají aktivitu prodeje.

## <a name="in-supply-chain-management"></a>V Supply Chain Management

Kontakty jsou označeny pomocí vlastnosti **IsContactPersonExternallyMaintained**. Tato vlastnost označuje, že je daný kontakt spravován externě. V takovém případě jsou externě spravované kontakty evidovány v aplikaci Sales.

## <a name="preconditions-and-mapping-setup"></a>Nastavení mapování a předpokladů

### <a name="contact-to-customer"></a>Kontakt na odběratele

- **Skupina odběratelů** je požadována v Supply Chain Management. Aby nedocházelo k chybám synchronizace, můžete zadat výchozí hodnotu v mapování. Tato výchozí hodnota se pak použije, pokud sloupec v aplikaci Sales zůstane prázdný.

    Výchozí hodnota šablony je **10**.

- Přidáním následujících mapování můžete snížit počet ručních aktualizací, které jsou potřebné v aplikaci Supply Chain Management. Můžete použít výchozí hodnotu nebo mapu hodnot například z pole **Země/oblast** nebo **Město**.

    - **SiteId** - Pro produkty v aplikaci Supply Chain Management je také možné definovat výchozí pracoviště. Pracoviště je nutné za účelem generování nabídky a prodejních objednávek v aplikaci Supply Chain Management.

        Hodnota šablony pro **SiteId** není definována.

    - **WarehouseId** - Pro produkty v aplikaci Supply Chain Management je také možné definovat výchozí sklad. Sklad je nutný za účelem generování nabídky a prodejních objednávek v aplikaci Supply Chain Management.

        Hodnota šablony pro **WarehouseId** není definována.

    - **LanguageId** – jazyk je nutný za účelem generování nabídek a prodejních objednávek v aplikaci Supply Chain Management.
    
        Výchozí hodnota šablony je **en-us**.

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

Na následujícím obrázku je příklad mapování šablony v integraci dat. 

> [!NOTE]
> Mapování ukazuje, jaké informace o sloupci budou synchronizovány z aplikace Sales do aplikace Supply Chain Management.

### <a name="contact-to-contact"></a>Kontakt na kontakt

![Mapování šablony v integrátoru dat](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a>Kontakt na odběratele

![Mapování šablony v integrátoru dat](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a>Související témata

[Zpeněžení potenciálního zákazníka](prospect-to-cash.md)

[Synchronizace obchodních vztahů přímo z aplikace Sales na odběratele v Supply Chain Management.](accounts-template-mapping-direct.md)

[Synchronizace produktů přímo z aplikace Supply Chain Management do produktů v Sales](products-template-mapping-direct.md)

[Synchronizace prodejních objednávek přímo mezi aplikacemi Sales a Supply Chain Management](sales-order-template-mapping-direct-two-ways.md)

[Synchronizace hlaviček a řádků faktury přímo z aplikace Supply Chain Management do aplikace Sales](sales-invoice-template-mapping-direct.md)


