---
title: Chybějící počáteční zůstatky roční uzávěrky
description: Tento článek vysvětluje, proč mohou při uzavírání roku chybět počáteční zůstatky a jak tyto zůstatky znovu vytvořit, pokud chybí.
author: kweekley
ms.date: 05/12/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9b64118fc3ff368e21ea8935c1e706f2161c620f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894841"
---
# <a name="year-end-close-missing-opening-balances"></a>Chybějící počáteční zůstatky roční uzávěrky

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje, proč mohou při uzavírání roku chybět počáteční zůstatky a jak tyto zůstatky znovu vytvořit, pokud chybí.

### <a name="symptom"></a>Příznak

Proč po spuštění roční závěrky hlavní knihy nejsou žádné počáteční zůstatky? 

### <a name="resolution"></a>Řešení

Zde je třeba zkontrolovat, zda jste provedli roční uzávěrku v hlavní knize a poté vygenerovali předvahu, která nezobrazuje počáteční zůstatky pro příští fiskální rok.

Pokud je pole **Vrátit zpět předchozí uzávěrku** nastaveno na **Ano**, dojde ke stornování předchozí roční uzávěrky pro stejný fiskální rok. Při spuštění procesu stornování roční uzávěrky se odstraní všechny záznamy pro konečné a počáteční zůstatky, jako kdyby roční uzávěrka nikdy neproběhla. Odstraní se i doklady. Proces roční uzávěrky se znovu automaticky nespustí. Celý proces je třeba spustit znovu, ale tentokrát s aktualizovaným nastavením **Vrátit zpět předchozí uzávěrku** na **Ne**.

Tomuto scénáři se věnuje článek s častými dotazy na téma roční uzávěrky. Další informace viz [Časté dotazy k aktivitám na konci roku](faq-year-end-activities.md).

### <a name="symptom"></a>Příznak

Koncem roku byla spuštěna roční uzávěrka s možností **Vrátit zpět předchozí uzávěrku** nastavenou na **Ne**, ale počáteční zůstatky za fiskální rok stále nejsou.

### <a name="resolution"></a>Řešení

Nejprve zkontrolujte stav dávkové úlohy. Uzavření roku zahrnuje řadu samostatných úloh, ale nejdůležitějším krokem je dávková úloha s popisem úlohy **Krok 5.0.0**. Zaúčtování počátečních transakcí a volitelně uzávěrkových transakcí do hlavní knihy probíhá během tohoto kroku. 

[![Seznam historie dávek](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)

Pokud tento krok skončil úspěšně, ale na stránce **Dotaz na předvahu** (**Hlavní kniha > Dotazy a sestavy > Předvaha**) nevidíte počáteční zůstatky, zkontrolujte výsledky dávkové úlohy roční uzávěrky a zjistěte, zda byl krok Znovu sestavit zůstatky úspěšně dokončen.

[![Výsledky dávkové úlohy roční uzávěrky](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)

Pokud se tento krok z nějakého důvodu nepovedl, počáteční (a volitelně uzávěrkové) transakce byly pravděpodobně úspěšně zaúčtovány. Můžete ověřit, že transakce hlavní knihy byly úspěšně zaúčtovány, a to pomocí stránky **Dotaz na transakce dokladu** zadáním čísla a data dokladu poskytnutého v dialogu roční uzávěrky pro rok, který jste uzavřeli (**Hlavní kniha > Dotazy a sestavy > Transakce dokladu**).

[![Dotaz na transakce dokladu](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)

Pokud jsou k dispozici počáteční (a volitelně uzávěrkové) doklady, nemusíte roční uzávěrku spouštět znovu. Místo toho v další části vyhledejte informace o tom, jak postupovat dále.

### <a name="symptom"></a>Příznak

Krok „Znovu sestavit zůstatky“ v roční uzávěrce se nepovedl, musím spustit celý proces roční uzávěrky znovu?

### <a name="resolution"></a>Řešení

Krok Znovu sestavit zůstatky aktualizuje zůstatky hlavní knihy, které se používají při generování dotazu na předvahu.  Jde o poslední krok v procesu roční uzávěrky.  Pokud je tento krok jediným krokem, který se nepovedl, transakce hlavní knihy byly úspěšně zaúčtovány.  Roční uzávěrku nemusíte znovu spouštět. Proces můžete spustit, abyste ručně znovu sestavili zůstatky, a to pomocí stránky **Sady finanční dimenze** (**Hlavní kniha > Účtová osnova > Dimenze > Sady finančních dimenzí**).

[![Tlačítko Znovu sestavit zůstatky na stránce Sady finančních dimenzí](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)

Pokud zpracování tohoto kroku trvá dlouho, doporučujeme zkontrolovat doporučené postupy pro sady finančních dimenzí, jak je popsáno v části [Osvědčené postupy pro aktualizaci sad finančních dimenzí](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets). 

