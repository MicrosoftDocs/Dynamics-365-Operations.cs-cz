---
title: "Úprava nákladové ceny množství na skladě"
description: "Stránku Úprava zásob na skladě použijte pro úpravu hodnoty nákladů na množství zásob na skladě po spuštění procesu uzávěrky skladu."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d1ef775c9783b975fd0f852dc7112506d3897605
ms.lasthandoff: 03/31/2017


---

# <a name="adjust-on-hand-inventory-cost-values"></a>Úprava nákladové ceny množství na skladě

[!include[banner](../includes/banner.md)]


Stránku Úprava zásob na skladě použijte pro úpravu hodnoty nákladů na množství zásob na skladě po spuštění procesu uzávěrky skladu.

Stránku **Úprava zásob na skladě** můžete použít pro úpravu hodnoty nákladů na množství zásob na skladě po spuštění procesu uzávěrky skladu. **Poznámka:** otevřete **úprava zásob na skladě** na stránky **závěrka a oprava** stránky, vyberte záznam dokončené soupisu zavřít a potom klepněte na tlačítko **úprava**&gt;**na skladě**. **Příklad:** V únoru dojde k následujícím transakcím:

-   1. únor: Finanční příjem zásob v množství 2 kusů v hodnotě 10,00 USD.
-   5. únor: Finanční příjem zásob v množství 1 kus v hodnotě 13,00 USD.
-   19. únor: Finanční výdej zásob v množství 1 kus a s průběžnou průměrnou cenou 11,00 USD.

Tato položka byla vytvořena s prvním v první ze skladu (FIFO) skladový model a od 28. února byla provedena uzávěrka skladu. Problém finanční transakce USD 11.00 budou vyrovnány proti finanční příjem, který je datován dne 1 a bude provedena úprava z USD 1.00. Následující skladové příjmy pak budou obsahovat otevřená skladová množství:

-   1. února: Množství 1 s náklady 10,00 USD
-   5. února: Množství 1 s náklady 13,00 USD

Chcete-li nastavit náklady těchto dvou položek na 15,00 USD, upravte pomocí možnosti úpravy množství na skladě k poslední uzávěrce skladu otevřené množství na skladě. **Poznámka:** Datem zaúčtování transakce úpravy množství na skladě bude datum poslední uzávěrky skladu. Toto datum nelze změnit.




