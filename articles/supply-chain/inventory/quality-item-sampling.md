---
title: Vzorkování položek řízení kvality
description: Toto téma popisuje, jak nastavit vzorkování položek.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae8bfd329ca0d7c30adcd93a759ee6bea7b76278
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022221"
---
# <a name="quality-management-item-sampling"></a>Vzorkování položek řízení kvality

Vzorkování položek se používá jako součást přidružení kvality. Definuje množství aktuální fyzické zásoby, která musí být zkontrolována. Vzorkování může být založeno na pevném množství, procentuální hodnotě nebo celé licenční značky.

## <a name="set-up-item-sampling"></a>Nastavení vzorkování zboží

Pro nastavení vzorkování položek postupujte následujícím způsobem.

1. Přejděte na **Řízení zásob \> Nastavení \> Řízení kvality \> Vzorkování položek**.
1. Zvolte **Nové**.
1. Zadejte hodnotu do pole **Vzorkování položky**.
1. V poli **Popis** zadejte hodnotu.
1. Zadejte číslo do pole **Hodnota**. Tato hodnota se vztahuje k určení množství, které je vybráno v přilehlém poli.
1. V oddílu **Zpracování** vyberte zaškrtávací políčko **Úplné blokování**, pokud má být zablokováno celé množství šarže nebo množství objednávky, pokud test selže. Pokud toto políčko není zaškrtnuto, budou v případě neúspěchu testu blokovány pouze položky v objednávce kvality.
1. Zvolte **Uložit**.
1. Zavřete stránku.

> [!NOTE]
> Funkce *Správa kvality pro procesy skladu* poskytuje dodatečné možnosti vzorkování zboží. Přidá koncepci *rozsahu vzorkování položek* a možnost definovat plnou registrační značku jako specifikaci množství. Pokud jste tuto funkci povolili, další informace naleznete v tématu [Správa kvality pro procesy skladu](quality-management-for-warehouses-processes.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
