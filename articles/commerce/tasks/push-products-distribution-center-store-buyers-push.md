---
title: " Zadání produktů z distribučního centra do obchodu pomocí metody buyer's push"
description: Tato procedura vás provede postupem, jak vytvořit a zpracovat buyer´s push k distribuci produktů z jednoho skladové místa do jednoho nebo více obchodů.
author: rubencdelgado
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailBuyersPush, InventLocationIdLookup, InventItemIdLookupSimple, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bf5dc0320e16bb53dbebc9e0bea689e0125b9827
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232827"
---
# <a name="push-products-from-distribution-center-to-store-using-buyers-push"></a> Zadání produktů z distribučního centra do obchodu pomocí metody buyer's push

[!include [banner](../includes/banner.md)]

Tato procedura vás provede postupem, jak vytvořit a zpracovat buyer´s push k distribuci produktů z jednoho skladové místa do jednoho nebo více obchodů. Můžete definovat více konfigurací a nechat systém navrhovat, jak budou produkty distribuovány, nebo ručně zadat, kam budou produkty distribuovány a kolik jich bude distribuováno do jednotlivých obchodů. Tato procedura neobsahuje nastavení dat, která lze použít pro buyer´s push, jako jsou například pravidla doplnění, organizační hierarchie a skladovací hmotnosti. Tato procedura používá ukázkovou společnost USRT.

1. Přejděte na možnost Buyer's push.
2. Klikněte na položku Nová.
3. Zadejte nějakou hodnotu do pole Popis.
4. V poli Lokalita zadejte nebo vyberte hodnotu.
5. V poli Sklad zadejte nebo vyberte sklad, který obsahuje produkty s hodnotami množství na skladě.
6. Klepněte na možnost Přidat.
7. Označte na seznamu vybraný řádek.
8. V poli Číslo zboží zadejte nebo vyberte produkt.
9. Klepněte na možnost Přidat.
10. Označte na seznamu vybraný řádek.
11. V poli Číslo zboží zadejte nebo vyberte variantu produktu.
    * Při zadávání varianty produktu budou vytvořeny řádky pro každou variantu.  
12. Označte řádek na seznamu.
13. V poli Zadané množství zadejte počet vybraných produktů, které chcete distribuovat.
14. Do pole Další množství k zadání zadejte množství produktů, které mají dostupné množství pro distribuci.
15. V poli Distribuce zadejte „Váha místa“.
    * Můžete vybrat ostatní typy pro používání jiných pravidel pro distribuci.  
16. V poli Hierarchie doplnění zadejte nebo vyberte hodnotu.
17. Vyberte možnost Ano v poli Uznat sortimenty.
18. Klikněte na Vypočítat množství a zkontrolujte množství, která jsou přidána k řádkům v oddílu Sklad.
19. Klepněte na Vytvořit objednávku.
20. Klepněte na tlačítko Ano.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]