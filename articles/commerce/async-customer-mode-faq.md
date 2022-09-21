---
title: Časté otázky k asynchronnímu režim vytváření zákazníka
description: V tomto článku jsou odpovědi na časté otázky týkající se režimu asynchronního vytváření zákazníků v Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 08/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: bd5741aeb3278f1d40d63bb02ca57571a907dc21
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/13/2022
ms.locfileid: "9474062"
---
# <a name="asynchronous-customer-creation-mode-faq"></a>Časté otázky k asynchronnímu režim vytváření zákazníka

[!include [banner](includes/banner.md)]

V tomto článku jsou odpovědi na časté otázky týkající se režimu asynchronního vytváření zákazníků v Microsoft Dynamics 365 Commerce.

### <a name="why-cant-i-enable-the-enable-editing-customers-in-asynchronous-mode-feature"></a>Proč nemohu aktivovat funkci „Povolit úpravy zákazníků v asynchronním režimu“?

Než aktivujete funkci **Povolit úpravy zákazníků v asynchronním režimu**, musíte aktivovat následující funkce:

- Vylepšení výkonu pro objednávky a transakce zákazníků
- Aktivovat vylepšené vytváření asynchronního zákazníka
- Povolit asynchronní vytváření pro adresy zákazníků

### <a name="why-do-i-still-see-real-time-service-calls-made-to-commerce-headquarters-after-the-enable-editing-customers-in-asynchronous-mode-feature-is-enabled"></a>Proč se po aktivaci funkce „Povolit úpravy zákazníků v asynchronním režimu“ stále zobrazují volání služeb v reálném čase do Commerce headquarters?

K tomuto problému dochází, když úlohy Commerce Data Exchange (CDX) nebyly spuštěny, aby bylo zajištěno, že stav funkce a další metadata kanálu jsou synchronizována s kanálem. Než scénář zopakujete, ujistěte se, že jsou v Commerce headquarters spuštěny následující úlohy CDX:

- 1110 (Globální konfigurace)
- 1010 (Zákazníci)
- 1070 (Konfigurace kanálu)

Data uložená v mezipaměti v Commerce Scale Unit (CSU) se nemusí po spuštění úloh CDX okamžitě projevit v Commerce headquarters.

### <a name="why-doesnt-commerce-headquarters-show-customer-creation-or-updates-from-the-point-of-sale-pos-or-e-commerce-channel"></a>Proč Commerce headquarters neukazuje vytvoření nebo aktualizace zákazníků z pokladního místa (POS) nebo kanálu elektronického obchodu?

Ujistěte se, že následující akce byly provedeny v pořadí, ve kterém jsou zde uvedeny.

1. Spusťte P-úlohu CDX v Commerce headquarters, abyste zajistili, že asynchronní zákaznická data, která jsou uložena v tabulkách **RETAILASYNCCUSTOMERV2**, **RETAILASYNCADDRESSV2**, **RETAILASYNCCUSTOMERCONTACT**, **RETAILASYNCCUSTOMERAFFILIATION** a **RETAILASYNCCUSTOMERATTRIBUTEV2** jsou k dispozici v Commerce headquarters.
1. Spusťte dávkovou úlohu **Synchronizovat požadavky zákazníků a kanálů** v Commerce headquarters. Po úspěšném provedení dávkové úlohy budou mít všechny záznamy, které byly úspěšně zpracovány z výše uvedených tabulek, pole **OnlineOperationCompleted** nastaveno na **1**.
