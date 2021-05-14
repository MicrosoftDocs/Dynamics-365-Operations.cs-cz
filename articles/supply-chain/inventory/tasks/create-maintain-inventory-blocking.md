---
title: Vytvoření a správa blokování zásob
description: Toto téma popisuje, jak použít blokování zásob k zabránění u fyzických zásob na skladě rezervaci jinými odchozími zdrojovými dokumenty.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9aa38ca52da577fff258bb330922ad7f4044330
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956151"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>Vytvoření a správa blokování zásob

[!include [banner](../../includes/banner.md)]

Toto téma popisuje, jak použít blokování zásob k zabránění u fyzických zásob na skladě rezervaci jinými odchozími zdrojovými dokumenty. Před zahájením tohoto postupu je třeba mít k dispozici položku s dostupnými fyzickými zásobami na skladě.

## <a name="block-inventory"></a>Blokovat zásoby

Chcete-li vytvořit záznam blokování zásob tak, aby byly blokované zásoby, postupujte takto.

1. Přejděte do možnosti **Řízení zásob \> Periodické úkoly \> Blokování zásob**.
1. V podokně akcí zvolte **Nový**.
1. V záhlaví nového blokujícího záznamu nastavte pole **Číslo položky** na položku, kterou chcete blokovat, a zadejte popis.
1. Na pevné záložce **Obecné** v poli **Množství** zadejte počet položek, které mají být zablokovány.
1. Na rychlé záložce **Dimenze zásob** určete místo a sklad, kde se aktuálně nacházejí položky, které chcete blokovat.
1. V podokně akcí vyberte **Uložit**.

## <a name="update-the-conditions-of-the-inventory-blocking"></a>Aktualizace podmínek pro blokování zásob

Chcete-li aktualizovat záznam blokování inventáře, postupujte takto.

1. Přejděte do možnosti **Řízení zásob \> Periodické úkoly \> Blokování zásob**.
1. V podokně seznamu vyberte příslušný záznam blokování.
1. Podle potřeby záznam upravte. Například můžete chtít změnit hodnotu **Očekávané datum** k určení, že se blokovaných zásob očekává uvolnění pro rezervaci. Pokud je vybrána **Očekávané příjmy**, datum se zobrazí u očekávané transakce. (Možnost **Očekávané příjmy** je při ručním vytvoření blokujícího záznamu vybrána ve výchozím nastavení.)
1. V podokně akcí vyberte **Uložit**.

## <a name="unblock-inventory"></a>Odblokování zásob

Chcete-li odstranit záznam blokování zásob tak, aby byly zásoby odblokovány, postupujte takto.

1. Přejděte do možnosti **Řízení zásob \> Periodické úkoly \> Blokování zásob**.
1. V podokně seznamu vyberte příslušný záznam blokování.
1. V podokně Akce zvolte **Odstranit**.
1. Budete vyzvání k potvrzení operace. Pokračujte výběrem tlačítka **Ano**.
1. Zavřete stránku.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
