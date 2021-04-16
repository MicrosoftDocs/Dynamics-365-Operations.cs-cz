---
title: Nastavení dělení zodpovědnosti
description: Můžete nastavit pravidla k oddělení úkolů, které musí být prováděny různými uživateli.
author: peakerbl
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e25fee324ce95cd04b86ee0e4e6a56cfacb61a53
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745734"
---
# <a name="set-up-segregation-of-duties"></a>Nastavení dělení zodpovědnosti

[!include [banner](../../includes/banner.md)]

Můžete nastavit pravidla k oddělení úkolů, které musí být prováděny různými uživateli. Tento koncept se nazývá dělení zodpovědnosti. Nemusí být vhodné například, aby stejná osoba prováděla potvrzení příjmu zboží a zpracování platby dodavateli. Dělení zodpovědnosti pomáhá snížit riziko podvodu a rovněž pomáhá zjistit chyby a nesrovnalosti. Můžete také dělení zodpovědnosti použít k vynucení zásad interních kontrol. Chcete-li vytvořit pravidlo, proveďte následující postup. K dokončení postupu musíte být správce systému.

1. Přejděte do nabídky **Správa systému** > **Zabezpečení** > **Dělení zodpovědnosti** > **Pravidla dělení zodpovědnosti**.
2. Klepněte na možnost **Nový**.
3. Do pole **Název** zadejte hodnotu pravidla.
4. V poli **První funkční oprávnění** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. Vyhledejte na seznamu požadovaný záznam a vyberte ho. Vyberte první zodpovědnost, která se řídí pravidlem.
6. V poli **Druhé funkční oprávnění** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání. 
7. Vyhledejte na seznamu požadovaný záznam a vyberte ho. Vyberte druhou zodpovědnost, která se řídí pravidlem.
10. Vyberte možnost v poli **Závažnost**. Vyberte závažnost rizika, ke kterému dochází, když stejný uživatel nebo role provádí obě zodpovědnosti.  
11. Zadejte hodnotu do pole **Riziko zabezpečení**. Zadejte popis rizika zabezpečení.  
12. Zadejte hodnotu do pole **Snížení rizika zabezpečení**. Zadejte popis akcí, které budete provádět pro snížení rizika zabezpečení. Můžete například snížit riziko provedením podrobnějších kontrol procesu, prováděním měsíčních manažerských kontrol nebo sdílením prostředků se jinými odděleními.     
13. Klikněte na možnost **Uložit**.

> [!IMPORTANT] 
> Při vytváření pravidla není ověřeno dodržování pravidel pro oddělení povinností. Můžete vytvořit pravidlo, které vytvoří konflikt pro existující role. Stávající přiřazení rolí uživatelů může být také v konfliktu s novým pravidlem. Po vytvoření nebo úpravě pravidla musíte ověřit dodržování předpisů. Další informace získáte v části [Identifikace a vyřešení konfliktů v dělení zodpovědnosti](identify-resolve-conflicts-segregation-duties.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]