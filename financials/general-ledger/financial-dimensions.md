---
title: "Finanční dimenze"
description: "Tento článek popisuje různé typy finančních dimenzí a způsob jejich nastavení."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25871
ms.assetid: af54621c-c8be-4b72-b6df-dcf886c40ce4
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 01f189b8de3f0cc707dcc54f4cde75aed95b8e3f
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="financial-dimensions"></a>Finanční dimenze

[!include[banner](../includes/banner.md)]


Tento článek popisuje různé typy finančních dimenzí a způsob jejich nastavení.

Použijte stránku Finanční dimenze pro vytváření finančních dimenzí, které lze použít jako segmenty účtu pro účtové osnovy. Existují dva typy finančních dimenzí – vlastní dimenze a dimenze zálohované entitou. Vlastní dimenze jsou společné pro více právnických osob a hodnoty se zadávají a spravují uživatelem. Dimenze zálohované entitou jsou dimenze, u kterých jsou hodnoty definovány jinde v systému, jako jsou například Odběratelé nebo Obchody. Některé dimenze zálohované entitami jsou společné pro více právnických osob a některé dimenze zálohované entitami jsou konkrétní pro společnost. 

Po vytvoření finančních dimenzí použijte stránku Hodnoty finanční dimenze k přiřazení dalších vlastností ke každé finanční dimenzi. 

Ačkoliv lze finanční dimenze použít k reprezentaci právnických osob bez vytvoření právnických osob v aplikaci Microsoft Dynamics 365 for Operations, finanční dimenze nejsou určeny řešení provozních ani obchodních potřeb právnických osob. Funkce mezijednotkového účetnictví v aplikaci Microsoft Dynamics 365 for Operations umožňuje pracovat pouze s účetními položkami vytvořenými jednotlivými transakcemi. 

Předtím než nastavíte finanční dimenze jako právnické osoby, ohodnoťte obchodní procesy v následujících oblastech pro určení, zda toto nastavení bude fungovat ve vaší organizaci:

-   Zásoby
-   Nákup a prodej mezi finančními dimenzemi a právnickými osobami
-   Výpočet a vykazování DPH
-   Operační vykazování

Níže jsou uvedeny některé příklady omezení:

-   Funkci DPH lze používat pouze s právnickými osobami, ale ne s finančními dimenzemi.
-   Některé sestavy nezahrnují finanční dimenze, takže nemůžete vždy vykazovat podle finančních dimenzí není-li tato sestava změněna.

**Vlastní dimenze** 

Pokud chcete vytvořit hodnoty definované uživatelem, vyberte v poli Použít formulář hodnot možnost &lt; Vlastní dimenze &gt;. Můžete také učit účetní masku pro omezení množství a typů informací, které můžete zadat pro hodnoty dimenze. Můžete zadat znaky, které zůstávají pro každou hodnotu dimenze stejné, například písmena nebo pomlčky. Můžete také zadat znaky čísel (\#) a znak ampersand (&) jako zástupné symboly pro písmena a čísla, která se změní pokaždé, když je hodnota dimenze vytvořena. Použijte znak čísla (\#) jako zástupný symbol pro číslo a ampersand (&) jako zástupný symbol pro písmeno. 

**Příklad** 

K omezení hodnoty dimenze na písmena CC a tři čísla zadejte jako masku formátu CC-\#\#\#. Toto pole je k dispozici pouze tehdy, pokud vyberete možnost &lt; Vlastní dimenze &gt; v poli Použít hodnoty od. 

**Dimenze zálohované entitou** 

Pokud chcete použít dimenze zálohované entitami, v poli Použít hodnoty od vyberte systémem definovanou entitu, která bude základ pro finanční dimenze. Hodnoty finanční dimenze jsou vytvořené z tohoto výběru. Chcete-li například vytvořit hodnoty dimenze pro projekty, vyberte Projekty. Hodnota dimenze se vytvoří pro každý název projektu. Stránka s hodnotami dimenzí zobrazuje hodnoty pro entitu, a když jsou konkrétní pro společnost, tak také hodnoty společnosti. 

**Aktivační dimenze** 

Aktivace finanční dimenze aktualizuje tabulku s názvem finanční dimenze a odstraněné dimenze odebere. Dříve než aktivujete finanční dimenzi, můžete zadat hodnoty dimenze, ale finanční dimenzi lze použít až po aktivaci. Například tuto finanční dimenzi nelze přidat do účetní struktury, dokud se neaktivuje finanční dimenze. Klepnutím na tlačítko Aktivovat budou u všech dimenzí aktualizovány změny stavu. 

**Překlady** 

Stránka Překlad textu umožňuje zadat text zobrazený v různých jazycích pro vybranou finanční dimenzi. Stránka Převod hlavního účtu je místo, kde můžete zadat text zobrazený v různých jazycích pro hlavní účet. 

**Přepisy právnických osob** 

Ne všechny dimenze platí pro všechny právnické osoby a některé mohou být relevantní pouze pro určité časové období. V tomto případě lze část Přepisy právnických osob použít k určení, u kterých společností by mělo být použití dimenze pozastaveno, kdo je vlastníkem a časové období aktivity dimenze.






