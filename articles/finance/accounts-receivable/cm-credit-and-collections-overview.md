---
title: Přehled kreditu a inkas
description: V tomto tématu je uveden přehled funkcí pro kredit a inkaso.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: ade76b822904f49135e07dfe0a39d2227dd1dd77
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992979"
---
# <a name="credit-and-collections-overview"></a>Přehled kreditu a inkas

[!include [banner](../includes/banner.md)]

Můžete spravovat úvěrový limit pro vaše zákazníky a provádět Inkasní aktivity, když se stanou nezbytnými.

## <a name="credit-management"></a>Správa úvěrů

Správa úvěru odběratele vám umožňuje spravovat limity úvěru a řídit tok prodejních objednávek prostřednictvím procesu zaúčtování na základě pravidel úvěru, která vytvoříte.

Proces správy úvěru může zahrnovat libovolné z následujících kroků:

- Aktualizaci atributů úvěru pro odběratele, které poskytují dodatečné informace o jejich úvěrové způsobilosti.
- Vytvoření limitů úvěru pro odběratele pomocí úprav limitu úvěru.
- Vytvoření dočasných limitů úvěru pro odběratele pomocí úprav limitu úvěru. Tímto způsobem můžete dočasně zvýšit nebo snížit úvěrové limity odběratelů na základě obchodních požadavků.
- Přidání dalších informací, které mohou ovlivnit limit úvěru, jako jsou informace o pojištění a zárukách.
- Vytvoření skupin úvěrů odběratelů, které propojují odběratele, takže mohou sdílet jeden limit úvěru.
- Přiřazení hodnocení rizik k odběratelům a následné použití těchto hodnocení k automatickému generování limitů úvěrů pro odběratele pomocí úprav limitu úvěru.
- Vytvoření pravidel blokování, která blokují objednávku v jednom nebo více procesech zaúčtování na základě faktorů, jako jsou například rizika, platební podmínky, limity úvěrů, částky po splatnosti a použitá procentní hodnota limitu úvěru.
- Správu seznamu prodejních objednávek, které jsou blokovány, kontolu důvodů blokování a zmírňování problémů.
- Uvolnění prodejních objednávek, aby mohly pokračovat v procesu zaúčtování.
- Nastavení workflow pro správu schválení změn limitu úvěru a uvolnění prodejních objednávek.

## <a name="collections-management"></a>Správa inkasa

Stránka **Inkasa** poskytuje jedno ústřední zobrazení, kde jsou spravovány informace o inkasech pohledávek. Vedoucí inkasa mohou používat toto centrálizované zobrazení ke správě inkas. Inkasní agenti mohou zahájit proces kolekce ze seznamů odběratelů, které jsou generovány pomocí použitím předem definované kolekce kritérií nebo stránky **Odběratelé**.

Dříve než začnete s nastavením nebo práci s inkasem, měli byste se seznámit s následujícími koncepty:

- Snímky pro sledování splatnosti odběratele obsahují informace o splatném zůstatku v určitém okamžiku.
- Fondy zákazníků kolekce pomáhají v uspořádání vaší práce.
- Inkasní agenti mohou mít své vlastní fondy zákazníků.
- Stránky seznamů umožňují uspořádat odběratele inkasa, aktivity a případy.
- Všechny informace o inkasu odběratele jsou na jedné stránku, která umožňuje provádět další akce.
- Odpuštění, obnovení nebo stornování úroků a poplatků je možné provést v jednom kroku.
- Vytvoření transakcí odpisů je možné provést v jednom kroku.
- Zpracování plateb s nedostatečnými finančními prostředky je možné provést v jednom kroku.

Popis těchto pojmů naleznete v tématu [Koncepty správy inkasa](./cm-collections-concepts.md).

## <a name="additional-resources"></a>Další zdroje

[Nastavení parametrů správy úvěru odběratelů](./cm-credit-mgmt-setup.md)

[Informace o nastavení správy kreditu odběratelů](./cm-setup-information.md)

[Přidání informací o správě kreditu pro zákazníka](./cm-add-credit-mgmt-information-customer.md)

[Úvěrové skupiny odběratele](./cm-customer-credit-groups.md)

[Úpravy úvěrového limitu odběratele](./cm-credit-limit-adjustments.md)

[Blokování úvěru pro prodejní objednávky](./cm-sales-order-credit-holds.md)

[Periodické úkoly správy úvěru odběratelů](./cm-periodic-tasks.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]