---
title: Transakce dlouhodobého majetku zaúčtované do účtovací vrstvy
description: V tomto článku naleznete přehled o funkci účtovací vrstvy pro transakce dlouhodobého majetku.
author: moaamer
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf35194badfa3c09758ad4dd9927af172a4ffdab
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990532"
---
# <a name="post-fixed-asset-transactions-to-posting-layers"></a>Transakce dlouhodobého majetku zaúčtované do účtovací vrstvy

[!include [banner](../includes/banner.md)]

V tomto článku naleznete přehled o funkci účtovací vrstvy pro transakce dlouhodobého majetku.

Dlouhodobý majetek se často odepisuje různými způsoby za různými účely. Odpisy pro daňové účely se vypočítávají pomocí platných daňových pravidel pro dosažení co nejvyšších odpisů před zdaněním, ale odpisy pro účely vykazování se vypočítávají podle účetních zákonů a pravidel. Různé druhy odpisů se vypočítávají a zaznamenávají odděleně v účtovacích vrstvách.

Každá kniha, která je připojena k dlouhodobému majetku, se vytváří pro určitou účtovací vrstvu, která má celkový cíl odpisu. Existuje deset účtovacích vrstev: Aktuální, Operace, Daň a sedm vlastních vrstev. Zaúčtování knihy do hlavní knihy také můžete zakázat nastavením hodnoty v poli Zaúčtovat do hlavní knihy na hodnotu Ne. Pole Účtovací vrstva se automaticky nastaví na Žádná. Knihy, které nebudou zaúčtovány do hlavní knihy, se obvykle používají pro účely vykazování daně. Tento přístup vám dává další flexibilitu k odstranění historických transakcí pro knihu majetku, protože nebyly potvrzeny do hlavní knihy.

Deníky dlouhodobého majetku jsou definovány na stránce Názvy deníků v části Hlavní kniha > Nastavení deníku > Názvy deníků. Každý deník, do kterého lze zaúčtovat odpisy, je určen svým názvem deníku platným jen pro jednu účtovací vrstvu. Účtovací vrstvu v deníku nelze změnit. Toto omezení pomáhá zajistit, že transakce pro každou účtovací vrstvu jsou udržovány odděleně. Je nutné vytvořit alespoň jeden název deníku pro každou účtovací vrstvu. Pokud používáte knihy, které nechcete zaúčtovat do hlavní knihy, je také nutné vytvořit deník, kde je účtovací vrstva nastavena na Žádná.

Na stránce Účetní profily dlouhodobého majetku lze označit účty hlavní knihy pro transakce dlouhodobého majetku. Pro každý účetní profil vyberte odpovídající typ transakce a knihy a potom označte účty hlavní knihy. Nastavte záznam účetního profilu pro každou knihu, která se zaúčtuje do hlavní knihy.

Dlouhodobý majetek lze zadat v dokumentech, které podporují pouze **Aktuální** účtovací vrstvu, jako je **Nákupní objednávka**, **Nevyřízená faktura dodavatele**, **Prodejní objednávka** nebo **Volná faktura**. Při výběru ID dlouhodobého majetku v kterémkoli z těchto dokumentů je kniha majetku filtrována do knihy s **Aktuální** účtovací vrstvou a bude vyplněna automaticky během účtování, když systém ověří, že účtovací vrstva dlouhodobého majetku je **Aktuální**. Pokud toto ověření nelze dokončit, proces účtování bude zastaven. 

> [!NOTE] 
> Používání odvozených knih umožňuje zároveň zaúčtovat transakce do jiných účtovacích vrstev. Transakce primární knihy se vytvoří v deníku nebo zdrojovém dokumentu s účtovací vrstvou, která odpovídá účtovací vrstvě knihy. Při účtování se odvozené transakce knihy zaúčtují do příslušných účtovacích vrstev. 


Další informace naleznete v části [Odvozené knihy](derived-books.md) a [Zaúčtování pomocí odvozených knih](post-derived-value-models.md).



