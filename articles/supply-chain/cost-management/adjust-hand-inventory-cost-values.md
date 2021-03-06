---
title: Úprava nákladové ceny množství na skladě
description: Stránku Úprava zásob na skladě použijte pro úpravu hodnoty nákladů na množství zásob na skladě po spuštění procesu uzávěrky skladu.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9ddb2962926e78fda80a9db7b9e5915550bc5965
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842194"
---
# <a name="adjust-on-hand-inventory-cost-values"></a>Úprava nákladové ceny množství na skladě

[!include [banner](../includes/banner.md)]

Stránku Úprava zásob na skladě použijte pro úpravu hodnoty nákladů na množství zásob na skladě po spuštění procesu uzávěrky skladu.

Stránku **Úprava zásob na skladě** můžete použít pro úpravu hodnoty nákladů na množství zásob na skladě po spuštění procesu uzávěrky skladu. **Poznámka:** Stránku **Úprava zásob na skladě** otevřete tak, že na stránce **Závěrka a oprava** vyberete záznam dokončeného procesu uzávěrky skladu a zvolíte možnost **Úprava** &gt; **Na skladě**. **Příklad:** V únoru dojde k následujícím transakcím:

-   1. únor: Finanční příjem zásob v množství 2 kusů v hodnotě 10,00 USD.
-   5. únor: Finanční příjem zásob v množství 1 kus v hodnotě 13,00 USD.
-   19. únor: Finanční výdej zásob v množství 1 kus a s průběžnou průměrnou cenou 11,00 USD.

Pro tuto položku byl nastaven skladový model podle metody FIFO a uzávěrka skladu byla provedena k 28. únoru. Finanční transakce výdeje v hodnotě 11,00 USD bude vyrovnána s finančním příjmem datovaným k 1. únoru a dále bude provedena úprava v hodnotě 1,00 USD. Následující skladové příjmy pak budou obsahovat otevřená skladová množství:

-   1. února: Množství 1 s náklady 10,00 USD
-   5. února: Množství 1 s náklady 13,00 USD

Chcete-li nastavit náklady těchto dvou položek na 15,00 USD, upravte pomocí možnosti úpravy množství na skladě k poslední uzávěrce skladu otevřené množství na skladě. **Poznámka:** Datem zaúčtování transakce úpravy množství na skladě bude datum poslední uzávěrky skladu. Toto datum nelze změnit.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]