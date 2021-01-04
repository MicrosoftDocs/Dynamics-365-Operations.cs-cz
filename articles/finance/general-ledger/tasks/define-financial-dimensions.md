---
title: Definování finančních dimenzí
description: Tento průvodce úkoly ukazuje přidávání finančních dimenzí zálohovaných entitami a vlastní finanční dimenzi.
author: aprilolson
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6fbe739eec0cfa1e7b0276872640bd4f82be3ef7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440987"
---
# <a name="define-financial-dimensions"></a>Definování finančních dimenzí

[!include [banner](../../includes/banner.md)]

Tento průvodce úkoly ukazuje přidávání finančních dimenzí zálohovaných entitami a vlastní finanční dimenzi.  Průvodce používá ukázkovou společnost USMF.


## <a name="create-an-entity-backed-financial-dimension"></a>Vytvoření finanční dimenze zálohované entitou
1. Přejděte do části **Navigační podokno > Moduly > Hlavní kniha > Účtová osnova > Dimenze > Finanční dimenze**.
2. Klepněte na možnost **Nový**.
3. V poli **Formulář hodnot uživatele** vyberte systémem definovanou entitu jako základ finanční dimenze. 
4. V poli **Název dimenze** zadejte hodnotu pro popis finanční dimenze. Název může být jiný než entita definovaná systémem, nesmí však obsahovat mezery ani speciální znaky.
5. Klepněte na tlačítko **Aktivovat**. Aktivace finanční dimenze aktualizuje tabulku s názvem finanční dimenze a odstraněné dimenze odebere. Dříve než aktivujete finanční dimenzi, můžete zadat hodnoty dimenze, ale finanční dimenzi lze použít až po aktivaci.  
6. Klikněte na **Zavřít** na aktivační zprávě.
7. Klepněte na tlačítko **Aktivovat**. Aktivace dimenzí může být naplánována po dávkách ke konkrétnímu datu a času.  
8. V **Podokně akcí** klikněte na možnost **Hodnoty dimenze**. Některé hodnoty dimenze jsou konkrétní pro společnosti. Zda jsou konkrétní pro společnost můžete ověřit, bude-li název společnosti zobrazen v seznamu hodnot dimenzí.  

## <a name="create-a-custom-financial-dimension"></a>Vytvoření vlastní finanční dimenze
1. Zavřete stránku.
2. Klepněte na možnost **Nový**.
3. V poli **Použít hodnoty od** vyberte **Vlastní dimenze**.
4. V poli **Název dimenze** zadejte hodnotu pro popis finanční dimenze.
    - Název nemůže obsahovat mezery ani speciální znaky.  
    - Můžete také učit účetní masku pro omezení množství a typů informací, které můžete zadat pro hodnoty dimenze.   
    - Můžete zadat znaky, které zůstávají pro každou hodnotu dimenze stejné, například písmena nebo pomlčky. Můžete také zadat znaky čísel (#) a znak ampersand (&) jako zástupné symboly pro písmena a čísla, která se změní pokaždé, když je hodnota dimenze vytvořena. Použijte znak čísla (#) jako zástupný symbol pro číslo a ampersand (&) jako zástupný symbol pro písmeno.  Příklad: K omezení hodnoty dimenze na písmena CC a tři čísla zadejte jako masku formátu CC-###.  
5. Klepněte na tlačítko **Aktivovat**. Aktivace finanční dimenze aktualizuje tabulku s názvem finanční dimenze a odstraněné dimenze odebere. Dříve než aktivujete finanční dimenzi, můžete zadat hodnoty dimenze, ale finanční dimenzi lze použít až po aktivaci.     
6. Klepněte na tlačítko **Aktivovat**. Aktivace dimenzí může být naplánována po dávkách ke konkrétnímu datu a času.      
7. V **Podokně akcí** klikněte na možnost **Hodnoty dimenze**.
8. Klepněte na možnost **Nový**.
9. V poli **Hodnota dimenze** zadejte název pro popis vaší finanční hodnoty.
10. V poli **Popis** zadejte popis, který popisuje vaši hodnotu finanční dimenze.

