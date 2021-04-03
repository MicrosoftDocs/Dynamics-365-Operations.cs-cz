---
title: Vytvoření výrobní zakázky
description: Tato procedura popisuje způsob vytváření výrobní zakázky.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdTable, ProdBOM, ProdRoute, ProdJournalCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dec447302da3a3bbca7d9c3e783af54bc77dfe70
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259811"
---
# <a name="create-a-production-order"></a>Vytvoření výrobní zakázky

[!include [banner](../../includes/banner.md)]

Tato procedura popisuje způsob vytváření výrobní zakázky. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Jedná se o první proceduru ze sedmi, která vysvětluje životního cyklus výrobní zakázky.


## <a name="create-a-production-order"></a>Vytvoření výrobní zakázky
1. Přejděte na Řízení výroby > Výrobní zakázky > Všechny výrobní zakázky.
2. Klikněte na možnost Nová výrobní zakázka.
3. Do pole Číslo položky zadejte D0001.
4. Do pole Dodání zadejte datum.
    * Datum dodání označuje, kdy by měla skončit výrobní zakázka pro provedení včas. Toto datum lze použít v procesu plánování. Můžete například naplánovat objednávku zpětně od data dodání.  
5. Nastavte množství na hodnotu 20.
    * Poznámka: V poli s číslem kusovníku se automaticky zobrazí počet aktivního kusovníku pro stávající položku, avšak kusovník můžete změnit z výrobní zakázky výběrem aktivního kusovníku ze seznamu schválených verzí kusovníku.    V poli s číslem postupu se automaticky zobrazí počet aktivního postupu pro stávající položku, avšak postup můžete změnit z výrobní zakázky výběrem aktivního postupu ze seznamu schválených verzí postupu.  
6. Klikněte na položku Vytvořit.

## <a name="validate-the-production-order"></a>Ověření výrobní zakázky
1. Klikněte na odkaz na vybraném řádku v seznamu.
    * Klepněte na odkaz na číslo výrobní zakázky, kterou jste právě vytvořili. To otevře stránku s podrobnostmi o objednávce.  
2. Klikněte na položku Upravit.
3. Do pole Dodání zadejte datum.
    * Můžete například změnit data dodání výrobní zakázky.  
4. Klikněte na položku Uložit.
5. Zavřete stránku.

## <a name="update-the-bom"></a>Aktualizace kusovníku
1. V podokně akcí klikněte na položku Výrobní zakázka.
2. Klikněte na položku Kusovník.
    * Otevřete stránku kusovníku a ověřte data kusovníku, která byla zkopírována z výchozích dat při vytvoření výrobní zakázky. V tomto postupu je nutné aktualizovat množství pro kusovník.  
3. Klikněte na položku Upravit.
4. Zadejte číslo do pole Množství.
    * Změna množství na řádku kusovníku má vliv na odhad nákladů spotřeby materiálu pro výrobní zakázku.  
5. Klikněte na položku Uložit.
6. Zavřete stránku.

## <a name="update-the-production-route"></a>Aktualizace výrobního postupu
1. V podokně akcí klikněte na položku Výrobní zakázka.
2. Klikněte na Postup.
    * Otevřete stránku Směrování a ověřte data výrobního postupu, která byla zkopírována z výchozích dat při vytvoření zakázky. V tomto postupu je nutné aktualizovat množství pro jednu operaci ve výrobním postupu.  
3. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
4. Klikněte na položku Upravit.
5. Do pole Množství procesu zadejte číslo.
    * Změna času zpracování se projeví na odhadované spotřebě a nákladech výrobní zakázky.  
6. Klikněte na položku Uložit.
7. Zavřete stránku.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]