---
title: Konfigurace a správa protokolování databáze
description: Můžete sledovat změny tabulek a polí v Dynamics 365 Human Resources s protokolováním databáze.
author: Darinkramer
manager: AnnBe
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3dc4658a0a13af95978c66f5aab882902f754a2d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417630"
---
# <a name="configure-and-manage-database-logging"></a>Konfigurace a správa protokolování databáze

Můžete sledovat změny tabulek a polí v Dynamics 365 Human Resources s protokolováním databáze. Toto téma popisuje následující postupy:

- Správa zabezpečení a výkonu pro protokolování databáze
- Nastavit protokolování databáze
- Vyčištění protokolů databáze

## <a name="overview-of-database-logging"></a>Přehled protokolování databáze

Protokolování databáze sleduje konkrétní změny tabulek a polí Microsoft Dynamics 365 Human Resources. Tyto změny zahrnují vkládání, aktualizaci nebo odstraňování. Protokolování databáze ukládá záznam změn do tabulek nebo polí v tabulce protokolu databáze.

Obchodní využití protokolování databáze zahrnuje:

- Vytvoření záznamu auditu změn konkrétních tabulek, které obsahují citlivé informace.
- Sledování jednotlivých transakcí. Protokolování databáze není určeno ke sledování automatických transakcí, které probíhají v dávkových úlohách.

## <a name="security-for-database-logging"></a>Zabezpečení pro protokolování databáze

Protokoly databází mohou obsahovat citlivá data. Omezte přístup tak, aby zahrnoval pouze role zabezpečení, které vyžadují přístup k datům protokolu.

## <a name="database-logging-and-performance"></a>Protokolování databáze a výkon

Ačkoli je to hodnotné z obchodního hlediska, protokolování databáze může být nákladné z hlediska používání a správy zdrojů. Dopady výkonu protokolování databáze zahrnuje:

- Tabulka databázového protokolu se může rychle rozšiřovat a způsobit nárůst velikosti databáze. Rozrůstání tabulky závisí na množství zaprotokolovaných dat, která se rozhodnete zachovat. Ve výchozím nastavení tabulka protokolu databáze uchovává data protokolu pouze za 30 dní. 

- Protokolování databáze může nepříznivě ovlivnit dlouhodobé automatizované procesy, například dlouhodobý import dat.

### <a name="best-practices"></a>Doporučené postupy

Chcete-li vylepšit výkon, omezte položky protokolu výběrem konkrétních polí k zaprotokolování místo celých tabulek. Z důvodu udržení celkového výkonu je protokolování databáze omezeno na 20 tabulek.

> [!NOTE]
> Pro jednotlivá pole lze protokolovat pouze aktualizace.

## <a name="set-up-database-logging"></a>Nastavit protokolování databáze

Můžete použít průvodce **Protokolováním změn databáze** k nastavení protokolování databáze. Průvodce poskytuje flexibilní způsob nastavení protokolování tabulek nebo polí.

1. Přejděte na **Správa systému > Odkazy > Databáze > Nastavení protokolu databáze**. Výběrem tlačítka **Nový** spusťte průvodce **změnami protokolování databáze**.
2. Průvodce dokončete.

## <a name="clean-up-database-logs"></a>Vyčištění protokolů databáze

Můžete odstranit všechny nebo část protokolů databáze pomocí následujících možností:

- Vyberte všechny protokoly pro konkrétní tabulku.
- Vyberte konkrétní typy protokolu databáze.
- Vyberte datum a čas vytvoření protokolu.

Chcete-li nastavit čištění protokolu databáze, postupujte následujícím způsobem: 

1. Přejděte na **Správa systému > Odkazy > Databáze > Protokol databáze**. Vyberte **Vyčistit protokol**.

2. Vyberte metodu výběru protokolů k odstranění zadáním jedné z následujících možností:

   - ID tabulky
   - Typ protokolu
   - Datum a čas vytvoření

3. Pomocí karty **Vyčištění protokolu databáze** zjistěte, kdy spustit úlohu vyčištění protokolu. Ve výchozím nastavení jsou protokoly databáze k dispozici po dobu 30 dnů.


[!INCLUDE[footer-include](../includes/footer-banner.md)]