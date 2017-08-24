--- 
title: "Vytvoření zásad nákupu"
description: "Tento postup popisuje, jak vytvořit zásady nákupu a srovnat tak obchodní procesy pro nákup."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 51486712d732bba064fd6c9b64dbccb730603877
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="create-purchasing-policies"></a>Vytvoření zásad nákupu

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje, jak vytvořit zásady nákupu a srovnat tak obchodní procesy pro nákup. Před vytvořením zásady nakupování nastavte parametry zásady nákupu. Je možné vytvořit, upravit a vyřadit zásady nákupu, ale zásady nákupu nelze odstranit. Tento proces obvykle provádí manažer nákupu. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.


## <a name="set-up-policy-parameters"></a>Nastavení parametrů zásad
1. Přejděte na zásady nákupu.
2. Klikněte na Parametry.
    * Pravidla priorit zásad se aplikují na různých úrovních ve vaší organizaci. Organizační jednotky, které jsou zobrazeny, závisí na hierarchii v organizaci a na jakých úrovních v hierarchii byl přiřazena účel interní kontroly zásobování. Například vaše organizace může používat právnické osoby, nákladová střediska, oblasti a oddělení, ale je možné, že jen některé z nich mají účel hierarchie Interní kontrola zásobování. Ve výchozím stavu je k dispozici organizace typu Společnost.  
3. Klikněte na kartu Parametry typu pravidla zásad.
4. Ve stromové struktuře vyberte Pravidlo kontroly pro zásady nákupu/nákupní žádanku.
    * Pořadí zpracování zásad se definuje na úrovni zásad. U některých typů zásad však můžete přepsat pořadí zpracování jednotlivých typů pravidel zásad. Například můžete definovat pořadí zpracování zásad nákupu v tomto pořadí: nákladové centrum, oddělení, společnost. V případě pravidla zásad katalogu můžete chtít upravit pořadí zpracování takto: oddělení, nákladové středisko, společnost. Pořadí zpracování zásad změníte pro pravidlo zásad katalogu. Jakmile zaměstnanec vytvoří požadavek, je určen katalog, který je zobrazen, podle zásad, které jsou přiřazeny k oddělení pracovníka a jeho nákladovému středisku a jeho společnosti.  
    * Pokud je na výběr více organizačních úrovní, pomocí šipky nahoru nebo dolů můžete nastavit pořadí priorit pro pravidlo kontroly nákupní žádanky.  
5. Zavřete stránku.

## <a name="create-a-new-policy"></a>Vytvořit nové zásady
1. Klikněte na položku Nová.
2. Zadejte hodnotu do pole Název.
3. Zadejte nějakou hodnotu do pole Popis.
    * Jednu zásadu nákupu lze použít pouze pro jednu organizační hierarchii. Například může mít jednu hierarchii nazývanou „Geografické“ a jednu „Oddělení“, a používat pro každou jiné zásady nákupu.  
    * Vyberte organizaci, pro kterou chcete použít zásady.  
4. Klepnutím na šipku přidejte vybranou organizaci.
    * Tento proces je možné zopakovat a přidat tak další organizace.  

## <a name="add-a-policy-rule"></a>Přidání pravidla zásad
1. V seznamu Typ pravidla zásad vyberte pravidlo Účel žádanky.
    * Vytvoříte pravidlo, které nastaví výchozí účel žádanky jako Spotřeba, ale umožní výběr možnosti Doplnění.  
2. Klikněte na Vytvořit pravidlo zásad.
3. Vyberte možnost Ano v poli Povolit ruční přepsání.
4. Klikněte na tlačítko Zavřít.
    * Nyní můžete nastavit jiná pravidla zásad pro zásady nákupu.   Všimněte si, že typ pravidel zásad nemůže mít překrývající se pravidla, která jsou aktivní současně v rámci jedné zásady zásobování.  
5. Zavřete stránku.
6. Zavřete stránku.


