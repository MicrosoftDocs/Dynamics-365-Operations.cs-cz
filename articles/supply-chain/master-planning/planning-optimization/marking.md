---
title: Značení zásob s optimalizací plánování
description: Toto téma poskytuje informace o možnostech, které jsou k dispozici pro označení zásob v potvrzených objednávkách, když používáte optimalizaci plánování.
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 7813f570afb0260e6740507c9504320c3e87be93
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263343"
---
# <a name="inventory-marking-with-planning-optimization"></a>Značení zásob s optimalizací plánování

[!include [banner](../../includes/banner.md)]

Toto téma poskytuje informace o možnostech, které jsou k dispozici pro označení zásob v potvrzených objednávkách, když používáte optimalizaci plánování.

*Označení* slouží k propojení nabídky a poptávky. Připomíná to *doložení*, které označuje, jak hlavní plánování očekává pokrytí poptávky. Z hlediska plánování je hlavní rozdíl v tom, že značení je trvalejší než doložení.

Značení bylo zavedeno na podporu speciálních scénářů výpočtu nákladů pro metody FIFO a LIFO. Nyní se však také používá pro některé scénáře bez výpočtu nákladů. Označení mezi nabídkou a poptávkou je volitelné a téměř trvalé. Označení může uživatel odstranit ručně nebo ho lze odstranit spuštěním rozpadu řádku prodejní objednávky, kde je vybrána možnost **Odstranit označení**.

Doložení je řízeno hlavním plánováním během pokrytí, aby se propojila poptávka s požadovanou nabídkou. Doložení lze aktualizovat pro každé spuštění plánování, aby se optimalizovala nabídka, která je nutná k pokrytí poptávky. Když hlavní plánování aktualizuje informace o doložení, respektuje jakékoli stávající označení.

Doložení začíná zahrnutím příslušného značení, rezervací zásob na skladě a rezervací na objednávce v následujícím pořadí:

1. Značení mezi poptávkou a nabídkou
1. Rezervace zásob na skladě
1. Rezervace na objednávce

Když zpracujete plánovanou objednávku, dialogové okno **Potvrzení** poskytuje pole **Aktualizovat označení**, které používáte k nastavení možností značení pro objednávky, které jsou vytvářeny během potvrzování. Vyberte jednu z následujících hodnot:

- **Ne** - Není použito žádné označení zásob.
- **Standardní** – Označení zásob se aktualizuje podle doložení. Objednávka požadavku (poptávka) se označí podle objednávky splnění (nabídka). Pokud na objednávce plnění zůstane nějaké množství, není označeno a referenční informace zůstanou prázdné. Například pokud je prodejní objednávka na 100 ea doložena proti nákupní objednávce na 150 ea, referenční informace budou přiřazeny pouze k prodejní objednávce.
- **Rozšířený** – Označí se objednávka požadavku (poptávka) i objednávka splnění (nabídka) bez ohledu na to, zda v objednávce splnění zůstane nějaké množství nebo ne. Například pokud je prodejní objednávka na 100 ea doložena proti nákupní objednávce na 150 ea, referenční informace budou přiřazeny jak k prodejní objednávce, tak k nákupní objednávce.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]