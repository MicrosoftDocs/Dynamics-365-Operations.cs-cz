---
title: Definování finančních dimenzí
description: Tento průvodce úkoly ukazuje přidávání finančních dimenzí zálohovaných entitami a vlastní finanční dimenzi.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5cfe92b8733a0a6d76e074cc31eec3f3935b512
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1530861"
---
# <a name="define-financial-dimensions"></a>Definování finančních dimenzí

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento průvodce úkoly ukazuje přidávání finančních dimenzí zálohovaných entitami a vlastní finanční dimenzi.  Průvodce používá ukázkovou společnost USMF.


## <a name="create-an-entity-backed-financial-dimension"></a>Vytvoření finanční dimenze zálohované entitou
1. Přejděte do části Hlavní kniha > Účtová osnova > Dimenze > Finanční dimenze.
2. Klikněte na možnost Nový.
3. V poli formuláře Hodnoty uživatele vyberte systémem definovanou entitu jako základ finanční dimenze. 
4. V poli Název dimenze zadejte hodnotu pro popis finanční dimenze.
    * Název může být jiný než entita definovaná systémem, nesmí však obsahovat mezery ani speciální znaky.  
5. Klepněte na tlačítko Aktivovat.
    * Aktivace finanční dimenze aktualizuje tabulku s názvem finanční dimenze a odstraněné dimenze odebere. Dříve než aktivujete finanční dimenzi, můžete zadat hodnoty dimenze, ale finanční dimenzi lze použít až po aktivaci.  
6. Klepněte na Zavřít na aktivační zprávě.
7. Klepněte na tlačítko Aktivovat.
    * Aktivace dimenzí může být naplánována po dávkách ke konkrétnímu datu a času.  
8. Klepněte na Hodnoty dimenzí.
    * Některé hodnoty dimenze jsou konkrétní pro společnosti. Zda jsou konkrétní pro společnost můžete ověřit, bude-li název společnosti zobrazen v seznamu hodnot dimenzí.  

## <a name="create-a-custom-financial-dimension"></a>Vytvoření vlastní finanční dimenze
1. Zavřete stránku.
2. Klikněte na možnost Nový.
3. V poli Použít hodnoty od vyberte Vlastní dimenze.
4. V poli Název dimenze zadejte hodnotu pro popis finanční dimenze.
    * Název nemůže obsahovat mezery ani speciální znaky.  
    * Můžete také učit účetní masku pro omezení množství a typů informací, které můžete zadat pro hodnoty dimenze.   
    * Můžete zadat znaky, které zůstávají pro každou hodnotu dimenze stejné, například písmena nebo pomlčky. Můžete také zadat znaky čísel (#) a znak ampersand (&) jako zástupné symboly pro písmena a čísla, která se změní pokaždé, když je hodnota dimenze vytvořena. Použijte znak čísla (#) jako zástupný symbol pro číslo a ampersand (&) jako zástupný symbol pro písmeno.  Příklad: K omezení hodnoty dimenze na písmena CC a tři čísla zadejte jako masku formátu CC-###.  
5. Klepněte na tlačítko Aktivovat.
    * Aktivace finanční dimenze aktualizuje tabulku s názvem finanční dimenze a odstraněné dimenze odebere. Dříve než aktivujete finanční dimenzi, můžete zadat hodnoty dimenze, ale finanční dimenzi lze použít až po aktivaci.  
6. Klepněte na tlačítko Aktivovat.
    * Aktivace dimenzí může být naplánována po dávkách ke konkrétnímu datu a času.  
7. Klepněte na Hodnoty dimenzí.
8. Klikněte na položku Nová.
9. V poli hodnota dimenze zadejte název pro popis vaší finanční hodnoty.
10. V poli Popis zadejte popis, který popisuje vaši hodnotu finanční dimenze.

