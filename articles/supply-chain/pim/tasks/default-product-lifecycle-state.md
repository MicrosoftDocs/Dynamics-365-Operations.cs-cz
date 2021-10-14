---
title: Vytvoření výchozího stavu životního cyklu produktu
description: Tento postup popisuje, jak vytvoříte výchozí stav životního cyklu produktu i jak přidružit výchozí stav uvolněným produktům.
author: t-benebo
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a628ed2b609f48c22076f409889c212e4d9463ac
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578193"
---
# <a name="create-a-default-product-lifecycle-state"></a>Vytvoření výchozího stavu životního cyklu produktu

[!include [banner](../../includes/banner.md)]

Tento postup popisuje, jak vytvoříte výchozí stav životního cyklu produktu i jak přidružit výchozí stav uvolněným produktům.


## <a name="create-a-default-lifecycle-state"></a>Vytvoření výchozího stavu životního cyklu
1. Přejděte na Řízení informací o produktech > Nastavení > Stav životnosti produktu.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Stav.
4. Vyberte možnost Ano výchozí pro uvolněné pole právnické osoby.
5. Zadejte nějakou hodnotu do pole Popis.
6. Vyberte možnost Ne v poli Je aktivní pro plánování.

> [!NOTE]
> Pokud nemá nový uvolněný produkt být zahrnut do hlavního plánování, vyberte Ne. Pokud má být zahrnutý do hlavního plánování, ponechte ovládací prvek na výchozí hodnotě Ano.  

## <a name="create-a-new-released-product"></a>Vytvoření nového uvolněného produktu
1. Zavřete stránku.
2. Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.
3. Klikněte na položku Nová.
4. Zadejte hodnotu do pole Číslo produktu.
5. Do pole Název produktu zadejte hodnotu.
6. Do pole Vyhledávání jména zadejte hodnotu.
7. V poli Skupina modelů zboží zadejte nebo vyberte hodnotu.
8. V poli Skupina zboží zadejte nebo vyberte hodnotu.
9. V poli Skupina dimenze úložiště zadejte nebo vyberte hodnotu.
10. V poli Skupina sledovací dimenze zadejte nebo vyberte hodnotu.
11. Klikněte na tlačítko OK.

> [!NOTE]
> Výchozí stav životního cyklu produktu je globální definice.  

## <a name="change-the-product-to-an-active-state"></a>Změna produktu na aktivní stav
1. V poli Stav cyklu životnosti produktu zadejte nebo vyberte hodnotu.

> [!NOTE]
> Předpokládejme, že jste nastavili aktivní stav, nyní můžete vybrat aktivní stav pro povolení použití produktu v hlavmím plánování a výpočtu na úrovni kusovníku. Samozřejmě to dává smysl, pouze pokud nejsou zadány všechny podrobnosti o produktu vyžadované pro konzistentní plánování.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]