---
title: Domovská stránka Správa organizace
description: Toto téma odkazuje na zdroje, které vám pomůžou ve vaší organizaci.
author: sericks007
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 20421
ms.assetid: 7aa24a03-d172-47e9-81f8-ebd39e80bc60
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 53a2abad03ab9349834aaafbec572d17d96df9c1
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693995"
---
# <a name="organization-administration-home-page"></a>Domovská stránka Správa organizace

[!include [banner](../includes/banner.md)]

Toto téma odkazuje na obsah, který uživatelům s oprávněním power user a správcům pomůže nakonfigurovat systém tak, aby fungoval pro vaši organizaci a obchod hladce a efektivně.

Většina zde uvedeného obsahu se použije k funkcím v modulu **Správa organizace**. Existuje však několik úlohy, jako je vytváření a používání šablony záznamu, které lze provést v kterémkoli modulu, aby vaše organizace mohla pracovat efektivněji.

## <a name="number-sequences"></a>Číselné řady

Číselné řady v aplikaci slouží ke generování čitelných, jedinečných identifikátorů pro hlavní datové záznamy a záznamy transakcí, které požadují identifikátory. Hlavní záznam dat nebo záznam transakce, která vyžaduje identifikátor, je označován jako *odkaz*. Než bude možné vytvořit nové záznamy pro odkaz, musíte nastavit číselné řady a spojit je s odkazem.

- [Přehled číselných řad](number-sequence-overview.md)
- [Nastavení číselných řad pomocí průvodce](tasks/set-up-number-sequences-wizard.md) (Průvodce záznamem úloh)
- [Nastavení jednotlivých číselných řad](tasks/set-up-number-sequences-individual-basis.md) (Průvodce záznamem úloh)

## <a name="organizations"></a>Organizace

Organizace představuje skupinu lidí, kteří spolupracují na provádění obchodního procesu nebo dosažení cíle. Organizační hierarchie představuje vztahy mezi organizacemi, které tvoří váš podnik.

Před nastavením organizací a organizačních hierarchií se ujistěte, že máte plán, jak bude vaše společnost modelována. Organizační model má podstatný vliv na implementaci a obchodní procesy.

- [Přehled organizací a organizačních hierarchií](organizations-organizational-hierarchies.md)
- [Plánování organizační hierarchie](plan-organizational-hierarchy.md)
- [Vytvoření organizační hierarchie](tasks/create-organization-hierarchy.md) (Průvodce záznamem úloh)
- [Vytvoření právnické osoby](tasks/create-legal-entity.md) (Průvodce záznamem úloh)
- [Vytvoření provozní jednotky](tasks/create-operating-unit.md) (Průvodce záznamem úloh)

## <a name="address-books"></a>Adresáře

Globální adresář je centralizovaným úložištěm pro hlavní data, která musí být uložena pro všechny interní a externí osoby a organizace, se kterými společnost přichází do styku. Data přidružená k záznamům strany zahrnují název strany, adresu a kontaktní informace.

Po vytvoření globálního adresáře můžete vytvořit další adresáře podle potřeby, například samostatný adresář pro každou společnost v organizaci a pro každé odvětví obchodu.

- [Přehled globálního adresáře](overview-global-address-book.md)
- [Plán pro globální adresář a další adresáře](plan-configuration-global-address-book-additional-address-books.md)
- [Konfigurace globálního adresáře](tasks/configure-global-address-book.md)
- [Často kladené dotazy o adresáři](qa-address-books.md)

## <a name="workflow"></a>Workflow

Workflow je systém, který nabízí funkce, pomocí kterých lze vytvářet individuální workflowy nebo obchodní procesy. Když vytváříte workflow, určete tok dokumentu nebo jeho procházení systémem pomocí zobrazení toho, kdo musí splnit úkol, provádět rozhodování nebo schválení dokumentu.

- [Přehled systému workflow](overview-workflow-system.md)
- [Prvky workflow](workflow-elements.md)
- [Akce v procesech schválení workflow](workflow-actions.md)
- [Přehled vytvoření workflow](create-workflow.md)

## <a name="electronic-signatures"></a>Elektronické podpisy

Elektronický podpis potvrzuje identitu osoby, která spouští nebo schvaluje určitý proces využívající výpočetní techniku. V některých průmyslových odvětvích má elektronický podpis stejnou právní hodnotu jako ruční podpis. Elektronické podpisy jsou vyžadovány předpisy v několika průmyslových odvětvích, například ve farmaceutickém, potravinářském, leteckém a zbrojním průmyslu.

Můžete používat elektronické podpisy pro důležité obchodní procesy. Některé procesy obsahují vestavěné prvky pro práci s elektronickými podpisy. Kromě toho můžete vytvářet vlastní požadavky na podpisy, připojené k libovolné databázové tabulce a poli.

- [Přehled elektronických podpisů](electronic-signature-overview.md)
- [Nastavení parametrů elektronického podpisu](tasks/set-up-electronic-signatures.md) (Průvodce záznamem úloh)

## <a name="case-management"></a>Správa případů

Plánováním, sledováním a analýzou případů můžete vytvořit efektivní řešení, která lze použít pro podobné případy. Například když zástupci servisu zákazníka nebo pracovníci lidských zdrojů vytváří případy, mohou najít informace v článcích znalostní databáze o tom, jak pracovat nebo vyřešit případy efektivněji.

- [Přehled správy případů](cases.md)
- [Plánování bezpečnosti kategorie případu, procesů případu a kategorií případu](plan-case-management.md)

## <a name="record-templates"></a>Šablony záznamu

Šablony záznamu vám mohou pomoci vytvořit záznamy rychleji. Můžete vytvořit šablonu záznamu tak, že hodnoty pole, které jsou často používány, nemusí být zadány explicitně pro každý nový záznam.

- [Přehled šablon záznamu](record-templates.md)
- [Vytvoření šablony záznamu pro usnadnění zadávání dat](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (Průvodce záznamem úloh)
- [Vytvoření nového záznamu s použitím šablony záznamu](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (Průvodce záznamem úloh)

## <a name="general-organization-administration"></a>Obecná správa organizace

- [Změna nápisu nebo loga](../get-started/tasks/change-banner-or-logo.md) (Průvodce záznamem úloh)
- [Konfigurace správy dokumentů](configure-document-management.md)
- [Konfigurace a odeslání e-mailu](configure-email.md)
- [Údaje data a času a časové pásmo](date-time-zones.md)
