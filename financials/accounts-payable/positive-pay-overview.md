---
title: "Přehled kladných plateb"
description: "Tento článek poskytuje informace o kladné platbě, kterou můžete použít pro generování elektronických seznamů šeků, které jsou dodávány bance."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c5a9f3f2a5c456b4ec515b912bb7470b549684a5
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="positive-pay-overview"></a>Přehled kladných plateb

[!include[banner](../includes/banner.md)]


Tento článek poskytuje informace o kladné platbě, kterou můžete použít pro generování elektronických seznamů šeků, které jsou dodávány bance. 

Kladné platby můžete použít pro generování elektronických seznamů šeků, které jsou dodávány bance. Soubory kladných plateb pomáhají bankám zabránit podvodným šekům. Nastavte kladné platby pro generování elektronického seznamu šeků při každém tisku šeků. Potom při předložení šeku bance ho banka srovná se seznamem šeků, který byl předložen dříve. Pokud šek odpovídá tomu, co má banka má v záznamech v seznamu, banka jej zúčtuje. Pokud šek neodpovídá šeku v seznamu, banka předloží šek ke kontrole.

Kladné platby se také označují jako SafePay. 

Soubory kladných plateb mohou obsahovat citlivé informace o příjemcích plateb a šekových částkách. Nezapomeňte tedy použít dostatečná opatření od doby vytvoření souborů do jejich přijetí do banky. Soubory kladných plateb budou staženy podle pokynů pro stažení ve webovém prohlížeči. 

Soubory kladných plateb jsou vytvořeny pomocí datových entit. Před generováním souboru kladných plateb nastavte formáty transformace pro XML, který převádí data do formátu, který může banka používat. 

Pro každý bankovní účet, pro který chcete generovat informace o souborech kladných plateb, musíte přiřadit formát kladných plateb. Po vygenerování plateb lze vygenerovat soubor kladných plateb pro jednu právnickou osobu a jeden bankovní účet. Případně můžete vygenerovat soubory kladných plateb pro více právnických osob a bankovních účtů současně. 

Po zaplacení šeků, které jsou uvedeny v souboru kladných plateb, obdržíte číslo potvrzení od banky. Poté můžete potvrdit soubor kladných plateb v aplikaci Microsoft Dynamics 365 for Operations. 

Pokud je nutné změnit soubor kladných plateb, můžete jej odvolat. Pro každý šek v souboru kladných plateb se resetuje pole, které označuje, zda byl šek zahrnut do souboru kladných plateb.

Další informace naleznete v tématu [Nastavení a generování souborů kladných plateb](set-up-generate-positive-pay-files.md).




