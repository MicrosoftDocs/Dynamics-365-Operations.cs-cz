---
title: EUR-00015 Registrace DIČ dodavatele
description: Tato procedura ukazuje, jak přidat ID registrace DPH a číslo osvobození od daně k účtu dodavatele.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddress, RegNumTaxIdLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eb8e5ea8a7a8360155c9eb30eaa85004483950e2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4984756"
---
# <a name="eur-00015-registration-of-vendor-vat-id"></a>EUR-00015 Registrace DIČ dodavatele

[!include [banner](../../includes/banner.md)]

Tato procedura ukazuje, jak přidat ID registrace DPH a číslo osvobození od daně k účtu dodavatele. Tento proces je podobný pro právnické osoby a odběratele. 

Dokončení této procedury vyžaduje nastavení hodnot DIČ. Postup se vztahuje na všechny evropské země/oblasti. Procedura byla vytvořena za použití ukázkových dat společnosti DEMF s primární adresou právnické osoby v Německu. Tato procedura je určena pro správce správy dat, manažera závazků nebo manažera pohledávek. Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.

1. Přejděte do části Závazky > Dodavatelé > Všichni dodavatelé.
2. V seznamu vyhledejte a vyberte dodavatele DE-01001.
3. Klikněte na ID registrace.
4. Klepněte na možnost Přidat.
5. Vyberte DIČ.
6. Zadejte hodnotu do pole Číslo registrace.
    * Zadejte DIČ v Německu pro vybraného dodavatele. Identifikátor se musí shodovat se zadaným formátem typu registrace.  
7. Klikněte na záložku Obecné.
8. V poli Platnost zadejte datum.
9. Klikněte na položku Uložit.
10. Klikněte na položku Nová.
11. Zadejte hodnotu do pole Název nebo popis.
    * Zadejte například ITA.  
12. V poli Země/oblast zadejte nebo vyberte hodnotu.
    * Vyberte například ITA.  
13. Vyberte možnost Primární v poli Země.
14. Klikněte na položku Uložit.
15. Klikněte na záložku Přehled.
16. Klepněte na možnost Přidat.
17. V poli Typ registrace zadejte nebo vyberte hodnotu.
    * Vyberte například DIČ.  
18. Zadejte hodnotu do pole Číslo registrace.
    * Například zadejte DIČ v Itálii.  Identifikátor musí mít stejný formát jako typ registrace.  
19. Klikněte na položku Uložit.
20. Zavřete stránku.
21. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Vyberte například DE-01001.  
22. Klikněte na odkaz na vybraném řádku v seznamu.
23. Rozbalte oddíl Faktury a dodávky.
24. Klikněte na možnost Upravit.
25. V poli DIČ zadejte nebo vyberte hodnotu.
26. Klikněte na položku Uložit.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]