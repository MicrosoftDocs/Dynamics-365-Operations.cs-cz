---
title: "Transakce dlouhodobého majetku zaúčtované do účtovací vrstvy"
description: "V tomto článku naleznete přehled o funkci účtovací vrstvy pro transakce dlouhodobého majetku."
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 2d65dca16cf4ead60c8664066828240c82e58a4f
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="post-fixed-asset-transactions-to-posting-layers"></a>Transakce dlouhodobého majetku zaúčtované do účtovací vrstvy

[!include[banner](../includes/banner.md)]


V tomto článku naleznete přehled o funkci účtovací vrstvy pro transakce dlouhodobého majetku.

Dlouhodobý majetek se často odepisuje různými způsoby za různými účely. Odpisy pro daňové účely se vypočítávají pomocí platných daňových pravidel pro dosažení co nejvyšších odpisů před zdaněním, ale odpisy pro účely vykazování se vypočítávají podle účetních zákonů a pravidel. Různé druhy odpisů se vypočítávají a zaznamenávají odděleně v účtovacích vrstvách.

Každá kniha, která je připojena k dlouhodobému majetku, se vytváří pro určitou účtovací vrstvu, která má celkový cíl odpisu. Existuje deset účtovacích vrstev: Aktuální, Operace, Daň a sedm vlastních vrstev. Zaúčtování knihy do hlavní knihy také můžete zakázat nastavením hodnoty v poli Zaúčtovat do hlavní knihy na hodnotu Ne. Pole Účtovací vrstva se automaticky nastaví na Žádná. Knihy, které nebudou zaúčtovány do hlavní knihy, se obvykle používají pro účely vykazování daně. Tento přístup vám dává další flexibilitu k odstranění historických transakcí pro knihu majetku, protože nebyly potvrzeny do hlavní knihy.

Deníky dlouhodobého majetku jsou definovány na stránce Názvy deníků v části Hlavní kniha > Nastavení deníku > Názvy deníků. Každý deník, do kterého lze zaúčtovat odpisy, je určen svým názvem deníku platným jen pro jednu účtovací vrstvu. Účtovací vrstvu v deníku nelze změnit. Toto omezení pomáhá zajistit, že transakce pro každou účtovací vrstvu jsou udržovány odděleně. Je nutné vytvořit alespoň jeden název deníku pro každou účtovací vrstvu. Pokud používáte knihy, které nechcete zaúčtovat do hlavní knihy, je také nutné vytvořit deník, kde je účtovací vrstva nastavena na Žádná.

Na stránce Účetní profily dlouhodobého majetku lze označit účty hlavní knihy pro transakce dlouhodobého majetku. Pro každý účetní profil vyberte odpovídající typ transakce a knihy a potom označte účty hlavní knihy. Nastavte záznam účetního profilu pro každou knihu, která se zaúčtuje do hlavní knihy.

> [!NOTE] 
> Používání odvozených knih umožňuje zároveň zaúčtovat transakce do jiných účtovacích vrstev. Vytvoříte transakce primární knihy v deníku s účtovací vrstvou, která odpovídá účtovací vrstvě knihy. Při účtování se odvozené transakce knihy zaúčtují do příslušných účtovacích vrstev.

Další informace naleznete v části [Odvozené knihy](derived-books.md) a [Zaúčtování pomocí odvozených knih](post-derived-value-models.md).




