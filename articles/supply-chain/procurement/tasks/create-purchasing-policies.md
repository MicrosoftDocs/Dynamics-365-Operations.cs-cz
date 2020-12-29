---
title: Vytvoření zásad nákupu
description: Totot téma popisuje, jak vytvořit zásady nákupu a srovnat tak obchodní procesy pro nákup.
author: mkirknel
manager: tfehr
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicyParameters, SysPolicy, RequisitionPurposeRule
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d4ba2a23f84972391283eaf01cef70a161c75226
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423753"
---
# <a name="create-purchasing-policies"></a>Vytvoření zásad nákupu

[!include [banner](../../includes/banner.md)]

Totot téma popisuje, jak vytvořit zásady nákupu a srovnat tak obchodní procesy pro nákup. Před vytvořením zásady nakupování nastavte parametry zásady nákupu. Je možné vytvořit, upravit a vyřadit zásady nákupu, ale zásady nákupu nelze odstranit. Tento proces obvykle provádí manažer nákupu. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.


## <a name="set-up-policy-parameters"></a>Nastavení parametrů zásad
1. V navigačním podokně přejděte na **Moduly > Zásobování a nákup > Nastavení > Zásady > Zásady nákupu**.
2. V podokně akcí zvolte **Parametry**.
- Pravidla priorit zásad se aplikují na různých úrovních ve vaší organizaci. Organizační jednotky, které jsou zobrazeny, závisí na hierarchii v organizaci a na jakých úrovních v hierarchii byl přiřazena účel interní kontroly zásobování. Například vaše organizace může používat právnické osoby, nákladová střediska, oblasti a oddělení, ale je možné, že jen některé z nich mají účel hierarchie Interní kontrola zásobování. Ve výchozím stavu je k dispozici organizace typu Společnost.  
3. Vyberte kartu **Parametry typu pravidla zásad**.
4. Ve stromové struktuře přejděte na **Zásady nákupu >Pravidlo kontroly pro nákupní žádanku**.
- Pořadí zpracování zásad se definuje na úrovni zásad. U některých typů zásad však můžete přepsat pořadí zpracování jednotlivých typů pravidel zásad. Například můžete definovat pořadí zpracování zásad nákupu v tomto pořadí: nákladové centrum, oddělení, společnost. V případě pravidla zásad katalogu můžete chtít upravit pořadí zpracování takto: oddělení, nákladové středisko, společnost. Pořadí zpracování zásad změníte pro pravidlo zásad katalogu. Jakmile zaměstnanec vytvoří požadavek, je určen katalog, který je zobrazen, podle zásad, které jsou přiřazeny k oddělení pracovníka a jeho nákladovému středisku a jeho společnosti.  
- Pokud je na výběr více organizačních úrovní, pomocí šipky nahoru nebo dolů můžete nastavit pořadí priorit pro pravidlo kontroly nákupní žádanky.  
5. Zavřete stránku.

## <a name="create-a-new-policy"></a>Vytvořit nové zásady
1. Zvolte **Nové**.
2. Zadejte hodnotu do pole **Název**.
3. Zadejte hodnotu do pole **Popis**.
- Jednu zásadu nákupu lze použít pouze pro jednu organizační hierarchii. Například může mít jednu hierarchii nazývanou „Geografické“ a jednu „Oddělení“, a používat pro každou jiné zásady nákupu.  
- Vyberte organizaci, pro kterou chcete použít zásady.  
4. Výběrem šipky přidejte vybranou organizaci.
- Tento proces je možné zopakovat a přidat tak další organizace.  

## <a name="add-a-policy-rule"></a>Přidání pravidla zásad
1. V seznamu **Typ pravidla zásad** vyberte **pravidlo Účel žádanky**.
- Vytvoříte pravidlo, které nastaví výchozí účel žádanky jako Spotřeba, ale umožní výběr možnosti Doplnění.  
2. Vyberte **Vytvořit pravidlo zásad**.
3. Vyberte možnost **Ano** v poli **Povolit ruční přepsání**.
4. Vyberte **Zavřít**.
- Nyní můžete nastavit jiná pravidla zásad pro zásady nákupu. Všimněte si, že typ pravidel zásad nemůže mít překrývající se pravidla, která jsou aktivní současně v rámci jedné zásady zásobování.  

