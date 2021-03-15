---
title: Schválení dodavatelů pro konkrétní produkty
description: Tento postup popisuje způsob schválení dodavatelů pro určité produkty.
author: RichardLuan
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, PdsApprovedVendorList, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cc7d8a93bdbdb5a1446fc34beff4b74aa9d11a0
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016646"
---
# <a name="approve-vendors-for-specific-products"></a>Schválení dodavatelů pro konkrétní produkty

[!include [banner](../../includes/banner.md)]

Tento postup popisuje způsob schválení dodavatelů pro určité produkty. Tímto způsobem lze určit, které dodavatele lze použít při přidání produktu do nákupní objednávky. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat. Tento úkol obvykle provádí manažer nákupu.

1. V navigačním podokně přejděte na **Moduly > Řízení informací o produktech > Produkty > Vydané produkty**.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. Rozbalte pevnou záložku **Nákup**. Pokud je v poli **Dodavatel** zobrazen primární dodavatel, je třeba přidat tohoto dodavatele jako schváleného dodavatele v následujících krocích. Poznamenejte si číslo dodavatele, pokud je uvedeno.  
5. V podokně akcí klikněte na možnost **Zakoupit**.
6. Klikněte na možnost **Nastavení**.
7. Klikněte na tlačítko **Přidat**.
8. V poli Dodavatel zadejte nebo vyberte hodnotu. Vyberte schváleného dodavatele. Alespoň jeden z řádků musí být hlavním dodavatelem, pokud existují dodavatelé v záznamu produktů. Pokud jste si dříve číslo dodavatele poznamenali, vyberte je zde.  
9. Do pole **Vypršení platnosti** zadejte datum. Vyberte datum, které je několik měsíců v budoucnu.  
10. Klikněte na tlačítko **Přidat**.
11. V poli **Dodavatel** zadejte nebo vyberte hodnotu.
12. Do pole **Vypršení platnosti** zadejte datum. Vyberte datum, které se liší od předchozího data vypršení platnosti.  
13. Zavřete stránku.
14. V podokně akcí klikněte na **Schválení dodavatelé**.
15. Do pole **Vypršení platnosti** zadejte datum. Toto datum se chová jako filtr, abyste viděli, kdo jsou schválení dodavatelé, a to až do určitého data.  
16. Zavřete stránku.
17. V podokně akcí klikněte na **Období platnosti**.
18. V poli **Zobrazit dodavatele s ukončenou platností k** zadejte datum. Tato stránka slouží k identifikaci dodavatelů, kde stav schválení vyprší po určitém datu.  
19. Zavřete stránku.
20. Klikněte na možnost **Upravit**.
21. Poté vyberte možnost v poli **Metoda kontroly schválených dodavatelů**. Toto pole umožňuje vybrat zásady pro situace, které nastanou při přidání produktu na řádek nákupní objednávky, pokud dodavatel není schváleným dodavatelem.  
22. Klikněte na možnost **Uložit**.
23. Zavřete stránku.
24. Zavřete stránku.
25. V navigačním podokně přejděte na **Moduly >Zásobování a zdroje > Dodavatelé > Vztahy dodavatel/položka > Seznam schválených dodavatelů podle položky**. Na této stránce je uveden přehled všech produktů a schválení dodavatelé.  
26. Zavřete stránku.
27. V navigačním podokně přejděte na **Moduly > Zásobování a zdroje > Dodavatelé > Všichni dodavatelé**. Můžete také začít od dodavatele a přejít na seznam schválených produktů pro tento účet dodavatele.  
28. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
29. V podokně akcí klikněte na možnost **Zásobování**.
30. Klikněte na **Seznam schválených dodavatelů podle dodavatele**.
31. Zavřete stránku.
32. Zavřete stránku.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]