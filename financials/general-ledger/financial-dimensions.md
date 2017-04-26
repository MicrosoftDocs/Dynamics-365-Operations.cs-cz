---
title: "Finanční dimenze"
description: "Tento článek popisuje různé typy finančních dimenzí a způsob jejich nastavení."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: f849b98cac88d182875aca88aaf04cd3575ed99f
ms.lasthandoff: 03/31/2017


---

# <a name="financial-dimensions"></a>Finanční dimenze

[!include[banner](../includes/banner.md)]


Tento článek popisuje různé typy finančních dimenzí a způsob jejich nastavení.

Použijte stránku Finanční dimenze pro vytváření finančních dimenzí, které lze použít jako segmenty účtu pro účtové osnovy. Existují dva typy finančních dimenzí – vlastní dimenze a dimenze zálohované entitou. Vlastní dimenze jsou společné pro více právnických osob a hodnoty se zadávají a spravují uživatelem. Dimenze zálohované entitou jsou dimenze, u kterých jsou hodnoty definovány jinde v systému, jako jsou například Odběratelé nebo Obchody. Některé dimenze zálohované entitami jsou společné pro více právnických osob a některé dimenze zálohované entitami jsou konkrétní pro společnost. 

Po vytvoření finančních dimenzí použijte stránku Hodnoty finanční dimenze k přiřazení dalších vlastností ke každé finanční dimenzi. 

Přestože finanční dimenze můžete použít k reprezentaci právnických osob bez vytvoření právnických osob v 365 Microsoft Dynamics pro operace, finanční dimenze nejsou určeny k provozním adresa nebo obchodních potřeb právnických osob. Mezijednotkové účetnictví funkce v Microsoft Dynamics 365 pro operace je určena adresovat pouze účetní položky vytvořené pro každou transakci. 

Předtím než nastavíte finanční dimenze jako právnické osoby, ohodnoťte obchodní procesy v následujících oblastech pro určení, zda toto nastavení bude fungovat ve vaší organizaci:

-   Zásoby
-   Nákup a prodej mezi finančními dimenzemi a právnickými osobami
-   Výpočet a vykazování DPH
-   Operační vykazování

Níže jsou uvedeny některé příklady omezení:

-   Funkci DPH lze používat pouze s právnickými osobami, ale ne s finančními dimenzemi.
-   Některé sestavy nezahrnují finanční dimenze, takže nemůžete vždy vykazovat podle finančních dimenzí není-li tato sestava změněna.

**Custom dimensions** 

Chcete-li vytvořit finanční dimenze definované uživatelem, použijte hodnoty z pole, vyberte &lt;vlastní dimenze&gt;. Můžete také učit účetní masku pro omezení množství a typů informací, které můžete zadat pro hodnoty dimenze. Můžete zadat znaky, které zůstávají pro každou hodnotu dimenze stejné, například písmena nebo pomlčky. Můžete také zadat znaky čísel (\#) a znaky ampersand (&) jako zástupné symboly pro písmena a čísla, která se změní pokaždé, když je vytvořena hodnota dimenze. Použijte znak čísla (\#) jako zástupný znak pro čísla a znak ampersand (&) jako zástupný symbol pro písmeno. 

**Příklad** 

Chcete-li omezit hodnoty dimenze na písmena CC a tři čísla, zadejte CC -\#\#\# jako masku formátu. Toto pole je dostupné pouze pokud vyberete &lt;vlastní dimenze &gt;v poli použít hodnoty z pole. 

**Dimenze entity zálohování** 

Vytvářet finanční dimenzi entity zálohy použít hodnoty z pole, vyberte entitu systémem definované na základě finančních dimenzí. Hodnoty finanční dimenze jsou vytvořené z tohoto výběru. Chcete-li například vytvořit hodnoty dimenze pro projekty, vyberte Projekty. Hodnota dimenze se vytvoří pro každý název projektu. Stránka s hodnotami dimenzí zobrazuje hodnoty pro entitu, a když jsou konkrétní pro společnost, tak také hodnoty společnosti. 

**Aktivace dimenzí** 

Aktivace finanční dimenze aktualizuje tabulku s názvem finanční dimenze a odstraněné dimenze odebere. Dříve než aktivujete finanční dimenzi, můžete zadat hodnoty dimenze, ale finanční dimenzi lze použít až po aktivaci. Například tuto finanční dimenzi nelze přidat do účetní struktury, dokud se neaktivuje finanční dimenze. Klepnutím na tlačítko Aktivovat budou u všech dimenzí aktualizovány změny stavu. 

**Translations** 

Stránka Překlad textu můžete zadat text zobrazený v různých jazycích pro vybranou finanční dimenzi. Stránka Převod hlavního účtu je místo, kde můžete zadat text zobrazený v různých jazycích pro hlavní účet. 

**Legal entity overrides** 

Všechny rozměry jsou platné pro všechny právnické osoby a některé může být pouze relevantní pro určité časové období. V tomto případě lze část Přepisy právnických osob použít k určení, u kterých společností by mělo být použití dimenze pozastaveno, kdo je vlastníkem a časové období aktivity dimenze.






