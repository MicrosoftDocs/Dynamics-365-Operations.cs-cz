---
title: Snadný offline přepínač pro operace dárkového poukazu a dobropisu
description: V tomto tématu je uveden přehled vylepšení, která poskytují jednoduchý offline přepínač pro určité typy plateb.
author: rubendel
ms.date: 02/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 20120-02-28
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 47867447e6d16a0fb4542c17ab184068300b2c1c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019950"
---
# <a name="seamless-offline-switch-for-gift-card-and-credit-memo-operations"></a>Snadný offline přepínač pro operace dárkového poukazu a dobropisu

[!include [banner](../includes/banner.md)]

Pokud zařízení pokladního místa (POS) ztratí spojení s databází kanálu, většina operací a transakcí POS, které probíhaly, mohou pokračovat poté, co pokladník obdrží varovnou zprávu o ztrátě připojení. V některých případech však transakce obsahují prvky, které vyžadují službu v reálném čase, a tyto prvky nejsou podporovány v případě, že je POS offline. V tomto tématu jsou popsány některé funkce, které v takových případech pomáhají snižovat dopad ztraceného připojení.

## <a name="completing-gift-card-transactions-in-offline-mode"></a>Provedení transakcí dárkového poukazu v offline režimu

Interní dárkové poukazy vyžadují službu v reálném čase, protože zůstatek pro dárkové poukazy musí být centrálně udržován v Microsoft Dynamics 365 Commerce Headquarters. Aby se zabránilo podvodům nebo jiným problémům se synchronizací, dárkové poukazy jsou uzamčeny okamžitě po přidání do transakce. Funkce uzamknutí zajišťuje, že dárkový poukaz nelze použít na více terminálech současně. Po dokončení transakce je dárkový poukaz automaticky aktualizován a odemknut.

Pokud však POS ztratí spojení po přidání dárkového poukazu do transakce, může být dárkový poukaz nepoužitelný. Chcete-li předejít této situaci, Dynamics 365 Commerce obsahuje parametr, který umožňuje dokončit transakce zahrnující řádek dárkového poukazu v době, kdy je POS v režimu offline. Je-li tento parametr zapnut, budou transakce dárkových poukazů, které jsou vynuceny offline, uloženy společně s offline transakcemi a budou synchronizovány s Commerce Headquarters při synchronizaci offline transakcí. Synchronizace také odemkne dárkový poukaz, takže jej bude možné použít na jiném terminálu.

Chcete-li povolit funkci uzavření transakcí dárkového poukazu po přepnutí do režimu offline, přejděte na kartu **Zaúčtování** na stránce **Parametry Commerce**. Na dané kartě vyhledejte pevnou záložku **Dárkový poukaz** a nastavte možnost **Povolit uzavření transakcí dárkového poukazu v offline režimu** na hodnotu **Ano**.

![Nastavení dárkového poukazu offline](../media/gift.png)

Parametry Commerce jsou obvykle uloženy v mezipaměti. Z toho vyplývá, že po aktualizaci nastavení tohoto parametru a při zahájení plánu distribuce dojde k synchronizaci změny v kanálu, takže se tato změna může uskutečnit až 24 hodin. Chcete-li provést okamžitou efektivní změnu, obnovte službu IIS (Microsoft Internet Information Services).

## <a name="completing-credit-memo-transactions-in-offline-mode"></a>Provedení transakcí dobropisu v offline režimu

Stejně jako u interních dárkových poukazů jsou dobropisy centrálně udržovány v Commerce Headquarters. Comerce má parametr, který umožňuje dokončení transakcí dobropisu v době, kdy je POS v režimu offline. Tento parametr funguje podobně jako parametr dárkového poukazu uvedený v předchozí sekci. Je-li parametr zapnutý, budou transakce dobropisu, které jsou vynuceny offline, synchronizovány zpět s databází kanálů spolu s ostatními transakcemi, které byly provedeny v době, kdy byl POS v režimu offline.

Chcete-li povolit funkci uzavření transakcí dobropisu po přepnutí do režimu offline, přejděte na kartu **Zaúčtování** na stránce **Parametry Commerce**. Na dané kartě vyhledejte pevnou záložku **Dobropis** a nastavte možnost **Povolit uzavření transakcí dobropisu v offline režimu** na hodnotu **Ano**.

![Nastavení dobropisu offline](../media/creditmemo.png)

Parametry Commerce jsou obvykle uloženy v mezipaměti. Z toho vyplývá, že po aktualizaci nastavení tohoto parametru a při zahájení plánu distribuce dojde k synchronizaci změny v kanálu, takže se tato změna může uskutečnit až 24 hodin. Chcete-li provést změny okamžitě, obnovte službu IIS.

## <a name="related-topics"></a>Související témata

- [Offline funkce pokladního místa (POS)](../pos-offline-functionality.md)
- [Online a offline operace pokladního místa (POS)](../pos-operations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]