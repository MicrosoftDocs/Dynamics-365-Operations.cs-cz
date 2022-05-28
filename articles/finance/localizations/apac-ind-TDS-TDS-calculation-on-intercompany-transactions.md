---
title: Výpočet TDS u mezipodnikových transakcí
description: Toto téma popisuje proces, který se používá k výpočtu daně odečtené u zdroje (TDS) u mezipodnikových transakcí ve fázích.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 381b00c64e3e3a09a245c82cbe1f1599986a49aa
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726970"
---
# <a name="tds-calculation-on-intercompany-transactions"></a>Výpočet TDS u mezipodnikových transakcí

[!include [banner](../includes/banner.md)]

Toto téma popisuje proces, který se používá k výpočtu daně odečtené u zdroje (TDS) u mezipodnikových transakcí ve fázích.

Když je vytvořena mezipodniková nákupní objednávka nebo prodejní objednávka, použije se k výpočtu částky TDS výchozí skupina TDS, která je definována pro zákazníka nebo dodavatele. Po zaúčtování faktury se částka TDS zaúčtuje na vratné nebo splatné účty.

Mezipodniková prodejní objednávka nebo nákupní objednávka se automaticky vytvoří pro původní nákupní objednávku nebo prodejní objednávku. Výchozí skupina TDS se zobrazuje na mezipodnikové objednávce, takže lze vypočítat TDS. Skupinu TDS můžete změnit. Fakturu lze zaúčtovat pouze v případě, že čistá částka faktury na mezipodnikové objednávce, která je automaticky vytvořena, odpovídá čisté částce faktury na původní objednávce. (Čistá částka je částka faktury po odečtení TDS.)

Například je vytvořena prodejní faktura pro 50 000 a je k ní připojena skupina TDS **10 %**. Zaúčtovaná částka faktury je 45 000 a zaúčtovaná částka TDS prodejní faktury je 5 000. Nákupní objednávka se automaticky vytvoří pro mezipodnikovou prodejní objednávku a je k ní připojena skupina TDS **10 %**. Pokud změníte skupinu TDS na **15 %**, nemůžete zaúčtovat fakturu, protože čistá částka faktury mezipodnikové prodejní objednávky, která byla automaticky vytvořena, se neshoduje s čistou částkou faktury původní prodejní objednávky.

Deník plateb, který je vytvořen pro mezipodnikovou fakturu, je automaticky zaúčtován. Tento deník plateb lze zaúčtovat pouze v případě, že částka čisté platby v něm odpovídá částce čisté platby v původním deníku plateb.
