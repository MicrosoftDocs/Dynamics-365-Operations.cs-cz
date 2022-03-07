---
title: Použití nákupní smlouvy při tvorbě nákupní objednávky
description: Tento postup popisuje použití nákupní smlouvy při vytváření nákupní objednávky.
author: Henrikan
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 130524dc8e0c8724e35bf13c6b250ab721383711
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570362"
---
# <a name="apply-a-purchase-agreement-when-creating-a-purchase-order"></a>Použití nákupní smlouvy při tvorbě nákupní objednávky

[!include [banner](../../includes/banner.md)]

Tento postup popisuje použití nákupní smlouvy při vytváření nákupní objednávky. Nákupní smlouva musí být použita při vytvoření nákupní objednávky, protože jsou v ní obecné podmínky, které musí být zkopírovány do záhlaví nákupní objednávky. Tento úkol obvykle provádí nákupčí. Nezbytným předpokladem pro tohoto průvodce je platná nákupní smlouva se závazkem na množství produktu pro dodavatele a položky. Stejný postup lze použít, máte-li nákupní smlouvou s jinými typy závazků.

## <a name="create-a-purchase-order"></a>Vytvoření nákupní objednávky

1. Přejděte na **Výroba a zdroje \> Pracovní prostory \> Příprava nákupní objednávky**.
1. V podokně akcí zvolte **Nová nákupní objednávka**.
1. Otevře se dialogové okno **Vytvořit nákupní objednávku**. Vyberte **Účet dodavatele**. Podle potřeby zkontrolujte a upravte další pole adresy.
1. Rozbalte pevnou záložku **Obecné**.
1. V poli **Kupní smlouva**, vyhledejte a vyberte platnou dohodu, kterou chcete použít. Zde jsou uvedeny všechny dostupné smlouvy pro daného dodavatele.  
1. Vyberte **Ano**.
1. Vyberte **OK**.

## <a name="add-a-line"></a>Přidat řádek

1. Zadejte hodnotu do pole **Číslo zboží**. Pokud jsou u závazku konkrétní dimenze zásob nebo místa, je nutné zadat stejné hodnoty na řádku nákupní objednávky, aby bylo možné smlouvu použít.
1. V poli **Lokalita** výběrem tlačítka rozevíracího seznamu otevřete vyhledávání. Site již může být vyplněn výchozí hodnotou z objednávky a od dodavatele. Pokud je vyplněn, tento krok vynechejte.  
1. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
1. Vyberte odkaz na vybraném řádku v seznamu.
1. Zadejte číslo do pole **Množství**. Ověřte, že se cena zkopírovala ze závazku.  

## <a name="look-up-the-commitment"></a>Vyhledání závazku

1. Vyberte **Aktualizovat řádek**.
1. Vyberte **Připojeno**. Zde můžete zjistit podrobnosti nákupní smlouvy. Například zde je cena a údaj, zda jsou cena a sleva pevné, což znamená, že při změně ceny nebo slevy na nákupní objednávce na jinou hodnotu, než která je v závazku, systém propojení odebere, aby řádek nákupní objednávky nesplňoval závazek. Můžete také vidět, zda je vybrána možnost Max je vynuceno, což znamená, že množství v závazku nelze překročit v součtu všech nákupů, které splňují daný závazek.  
1. Zavřete stránku.

## <a name="look-up-the-purchase-agreement"></a>Vyhledání nákupní smlouvy

1. V **podokně akcí** klikněte na možnost **Obecné**.
1. Vyberte **Nákupní smlouvu**.
1. Zavřete stránku.
1. Zavřete stránku.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]