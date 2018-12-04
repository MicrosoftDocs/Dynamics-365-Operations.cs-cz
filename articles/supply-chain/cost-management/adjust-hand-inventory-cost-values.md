---
title: "Úprava nákladové ceny množství na skladě"
description: "Stránku Úprava zásob na skladě použijte pro úpravu hodnoty nákladů na množství zásob na skladě po spuštění procesu uzávěrky skladu."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 21942f7aa57d21f70e3014051c42328164b750a3
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

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

