---
title: Konfigurace a správa protokolování databáze
description: Můžete sledovat změny tabulek a polí v Dynamics 365 Human Resources s protokolováním databáze.
author: twheeloc
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3cbe4c105b14935db6803e4bded0d891c564fb81
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066433"
---
# <a name="configure-and-manage-database-logging"></a>Konfigurace a správa protokolování databáze


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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
2. Zvolte **Další**. 
3. Na stránce **Tabulky a pole** průvodce vyberte tabulky a pole, u kterých chcete povolit protokolování databáze, a vyberte možnost **Další**.

   > [!Note]
   > Protokolování databáze není k dispozici u všech tabulek v databázi aplikace Human Resources. Výběrem možnosti **Zobrazit všechny tabulky** pod seznamem rozbalíte seznam tabulek a polí, aby se zobrazily všechny databázové tabulky, u kterých je k dispozici protokolování databáze, ale toto bude jen podmnožina úplného seznamu databázových tabulek.

4. Na stránce **Typy změn** průvodce vyberte datové operace, u kterých chcete sledovat změny pro každou z tabulek a polí, a vyberte možnost **Další**. V následující tabulce najdete popis datových operací, které jsou k dispozici u protokolování.
5. Na stránce **Dokončit** zkontrolujte provedené změny a vyberte možnost **Dokončit**.

| Operace | popis |
| -- | -- |
| Sledovat nové transakce | Vytvořte protokol pro nové záznamy, které jsou vytvořeny v tabulce. |
| Aktualizace | Vytvořte protokol pro aktualizace záznamů tabulky nebo aktualizace jednotlivě vybraných polí v tabulce. Pokud se rozhodnete protokolovat aktualizace pro tabulku, vytvoří se záznam protokolu pokaždé, když se provede aktualizace jakéhokoli pole libovolného záznamu v tabulce. Pokud se rozhodnete protokolovat aktualizace pro konkrétní pole, záznam protokolu se vytvoří, pouze když se provedou aktualizace těchto polí záznamů tabulky. |
| Odstranit | Vytvořte protokol pro záznamy odstraněné z tabulky. |
| Přejmenovat klíč | Vytvořte záznam protokolu při přejmenování klíče tabulky. |


## <a name="clean-up-database-logs"></a>Vyčištění protokolů databáze

Můžete odstranit všechny nebo část protokolů databáze pomocí následujících možností:

- Vyberte všechny protokoly pro konkrétní tabulku.
- Vyberte konkrétní typy protokolu databáze.
- Vyberte datum a čas vytvoření protokolu.

Chcete-li nastavit čištění protokolu databáze, postupujte následujícím způsobem: 

1. Přejděte na **Správa systému > Odkazy > Databáze > Protokol databáze**. Vyberte **Vyčistit protokol**.
2. V záhlaví **Záznamy k zahrnutí** vyberte **Filtr**.
3. Vyberte metodu, která bude použita pro výběr protokolů k odstranění. Zadejte některou z následujících možností:

   - ID tabulky
   - Typ protokolu
   - Datum a čas vytvoření

4. Pomocí karty **Vyčištění protokolu databáze** zjistěte, kdy spustit úlohu vyčištění protokolu. Ve výchozím nastavení jsou protokoly databáze k dispozici po dobu 30 dnů.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
