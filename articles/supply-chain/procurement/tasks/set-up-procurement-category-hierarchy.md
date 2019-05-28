---
title: Nastavení hierarchie kategorií zásobování
description: Tento postup popisuje vytvoření nových uzlů v hierarchii kategorií zásobování a konfiguraci kategorie zásobování pro použití v procesu zásobování.
author: mkirknel
manager: AnnBe
ms.date: 11/06/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 01809a8a3256342682d8a9cfb296a355310fe4ed
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569884"
---
# <a name="set-up-a-procurement-category-hierarchy"></a>Nastavení hierarchie kategorií zásobování

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje vytvoření nových uzlů v hierarchii kategorií zásobování a konfiguraci kategorie zásobování pro použití v procesu zásobování. Tyto úkoly obvykle provádějí vedoucí nákupu. Před zahájením tohoto postupu musí existovat hierarchie kategorií typu Zásobování. Používáte-li ukázková data společnosti, můžete tento postup provést se společností USMF.


## <a name="add-a-new-procurement-category"></a>Přidání nové kategorie zásobování
1. Přejděte do nabídky Zásobování a zdroje > Kategorie zásobování.
2. Klikněte na možnost Upravit hierarchii kategorií.
    * Aktuální hierarchie kategorií zásobování se zobrazí v levé části stránky. Chystáte se upravit hierarchii.  
3. Klikněte na možnost Nový uzel kategorie.
    * Systém vybere ve výchozím nastavení nejvyšší uzel. Používáte-li tento postup jako úkol průvodce, lze kliknout na tlačítko Odemknout a vybrat jiný nadřazený uzel pro vložení nového uzlu. Po skončení znovu zamkněte průvodce úkolem a pak klikněte na uzel Nová kategorie.  
4. Zadejte hodnotu do pole Název.
5. Zadejte nějakou hodnotu do pole Popis.
6. Do pole Popisný název zadejte hodnotu.
    * Popisný název je volitelný. Zobrazí se ve vyhledávání kategorií společně s názvem kategorie.  
7. Klikněte na položku Uložit.

## <a name="add-products-to-your-new-procurement-category"></a>Přidání produktů do nové kategorie zásobování
1. Přejděte do nabídky Zásobování a zdroje > Kategorie zásobování.
    * Vyberte uzel, který jste právě přidali. Pokud tento postup používáte jako průvodce úkolem, možná bude třeba průvodce odemknout, aby bylo možné uzel vybrat.  
2. Rozbalte oddíl Produkty.
3. Kliknutím na tlačítko Přidat přidružte produkty ke kategorii zásobování.
4. Vyberte produkt, který chcete přidat do kategorie zásobování.
5. Kliknutím na šipku vyberte produkt.
6. Vyberte další produkt, který chcete přidat do kategorie zásobování.
7. Kliknutím na šipku vyberte produkt.
8. Klikněte na tlačítko OK.

## <a name="add-approved-and-preferred-vendors"></a>Přidání schválených a upřednostňovaných dodavatelů
1. Přepněte rozšíření oddílu Dodavatelé.
2. Klepněte na možnost Přidat.
    * Můžete přidat dodavatele do kategorie zásobování a určit, zda se jedná o upřednostňovaného dodavatele nebo jen schváleného dodavatele pro danou kategorii. Při odstraňování dodavatele z kategorie, nebudou odstraněny historické transakce s dodavatelem v kategorii.   
3. Vyhledejte dodavatele, kterého chcete do kategorie přidat.
4. Kliknutím na šipku vyberte dodavatele.
5. Klepněte na tlačítko OK.
6. Vyberte řádek dodavatele, který chcete upravit.
7. Vyberte možnost v poli Stav dodavatele.
    * Nastavení volby dodavatele v pravidle zásad kategorie určí, zda jsou upřednostňovaní, schválení nebo všichni dodavatelé k dispozici na nákupních žádankách.   

## <a name="add-additional-information-to-the-category"></a>Přidání dalších informací do kategorie
1. Rozbalte oddíl Skupiny kritérií hodnocení dodavatelů.
    * Na této kartě můžete definovat kritéria pro hodnocení dodavatelů v kategorii zásobování. Tento krok lze provést by kliknutím na tlačítko Přidat a poté zvolením skupiny hodnocení dodavatelů, která obsahuje požadovaná kritéria.  
2. Rozbalte oddíl Dotazníky.
    * Na této kartě lze přidat dotazníky, které se objeví na žádance, pokud nastavíte typ aktivity „Žádanka“. Žadatel potom musí vyplnit dotazník, aby mohl odeslat žádanku pro konkrétní produkt nebo produkty v kategorii zásobování.  
3. Rozbalte oddíl Skupiny prodejní daně položky.
4. V poli Skupina DPH zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. Vyberte skupinu DPH.
6. Rozbalte oddíl Stránka kategorie.
    * Stránky kategorie jsou vytvořeny na stránce Hierarchie kategorií. Obsahují informace o kategorii zásobování, jako jsou informace o typu produktů v kategorii, obrázky produktů v kategorii a oznámení, jako např. prodej nebo sleva, které jsou v kategorii k dispozici. Informace na stránce kategorie budou zobrazeny na nákupní žádance.  
7. Zavřete stránku.

