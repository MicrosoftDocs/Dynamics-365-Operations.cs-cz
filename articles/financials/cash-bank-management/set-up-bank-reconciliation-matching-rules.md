---
title: "Nastavení pravidel párování pro odsouhlasení banky"
description: "Toto téma vysvětluje, jak lze nastavit odpovídající pravidla vyrovnání a sady odpovídajících pravidel vyrovnání pro usnadnění procesu bankovního odsouhlasení. Odpovídající pravidla odsouhlasení představují sadu kritérií, které se používají k filtru řádků bankovního výpisu a řádků dokladu banky během odsouhlasení."
author: twheeloc
manager: AnnBe
ms.date: 10/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: b48accdc7aaaa65b4c620777546b20056038905b
ms.contentlocale: cs-cz
ms.lasthandoff: 03/26/2018

---

# <a name="set-up-bank-reconciliation-matching-rules"></a>Nastavení pravidel párování pro odsouhlasení banky

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak lze nastavit odpovídající pravidla vyrovnání a sady odpovídajících pravidel vyrovnání pro usnadnění procesu bankovního odsouhlasení. Odpovídající pravidla odsouhlasení představují sadu kritérií, které se používají k filtru řádků bankovního výpisu a řádků dokladu banky během odsouhlasení.

Můžete nastavit odpovídající pravidla vyrovnání a sady odpovídajících pravidel vyrovnání pro usnadnění procesu bankovního odsouhlasení. Odpovídající pravidlo odsouhlasení představuje sadu kritérií, které se používají k filtru řádků bankovního výpisu a řádků bankovních transakcí aplikace Microsoft Dynamics 365 for Finance and Operations během odsouhlasení. Použijte stránku **Pravidla párování pro odsouhlasení** k nastavení pravidel párování odsouhlasení. Můžete nastavit více než jedno pravidlo párování a potom vytvořit sadu pravidel párování pro odsouhlasení na stránce **Sady pravidel párování pro odsouhlasení**. 

> [!NOTE] 
> Pravidla pro bankovní odsouhlasení se používají, pokud provádíte odsouhlasení elektronického bankovního výpisu pomocí předběžného bankovního odsouhlasení. 

Na stránce **Pravidla párování pro odsouhlasení** můžete vybrat, které akce a kritéria výběru jsou použity při spuštění pravidla pro porovnání. Ve skupině polí **Akce** vyberte akci, která bude provedena při spuštění pravidla porovnání během odsouhlasení.  

> [!NOTE] 
> Možnost, kterou vyberete, určuje pole, které se zobrazí.

|                                    |                                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Akce**                         |                                                                                                                                                                                                                                                                                                               | **Kritéria výběru, která jsou k dispozici, když je vybrána akce**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Spárovat s bankovním dokumentem**       | Vytvořte kritéria k určení, jak se bankovní doklady a řádky výkazu banky shodují při spuštění pravidla porovnání ze stránky **List odsouhlasení banky**. Řádky transakce se volí podle dalších kritérií nastavených na pevných záložkách.                                | **Krok 1: Definujte pravidlo párování** – vyberte kritéria v k určení, které bankovních výpisy mají být spárovány s bankovními transakcemi aplikace Finance and Operations. **Krok 2 (volitelný): vyberte řádky výkazu, na které se mají pravidla párování spustit:** Použijte filtr k určení, na které řádky výkazu se mají pravidla spustit.                                                                                                                                                                                                                                                                                                               |
| **Vymažte řádky výpisu s položkou storno** | Vytvořte kritéria k určení, jak se řádky výpisu s položkou storno mají odebrat ze stránky **List odsouhlasení banky** při spuštění pravidla porovnání. Tato možnost se používá, když chyba banky způsobí, že dva řádky bankovního výpisu jsou uvedené v importovaném bankovním výpisu a řádky musí být odsouhlaseny. | **Krok 1**:**Najděte řádky výpisu s položkou storno**– Přidejte výběr kritérií pro výběr řádků bankovního výpisu s položkou storno. Například chcete-li vybrat pouze šeky, vyberte možnost **Kód bankovní transakce** v poli Pole, vyberte symbol plus (+) v poli **Operátor** a zapište **Šeky** do pole Hodnota. **Krok 2: nalezení původních řádků výpisu** – Můžete přidat kritéria výběru odpovídajících řádkům dokladu banky do řádků bankovního výpisu. **Krok 3: nalezení bankovních transakcí aplikace Finance and Operations** – Můžete přidat kritéria výběru odpovídajících bankovním transakcím aplikace Finance and Operations do řádků bankovního výpisu. |
| **Označit nové transakce**          | Vytvořte kritéria k určení, jak se nové transakce mají označit na stránce **List odsouhlasení banky** při spuštění pravidla porovnání.                                                                                                                                                                 | **Krok 1: nalezení řádků výpisu**– přidejte pole výběru, abyste upřesnili, které řádky bankovního výpisu se mají vybrat na stránce **List odsouhlasení banky**. **Krok 2: nalezení bankovních transakcí aplikace Finance and Operations** – Můžete přidat kritéria výběru pro hledání řádků dokumentů. Není-li nalezen žádný bankovní dokument, bude označen řádek výpisu jako nová transakce.                                                                                                                                                                                                                                             |









