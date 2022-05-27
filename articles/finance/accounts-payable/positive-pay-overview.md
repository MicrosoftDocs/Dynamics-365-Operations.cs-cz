---
title: Přehled kladných plateb
description: Tento článek poskytuje informace o kladné platbě, kterou můžete použít pro generování elektronických seznamů šeků, které jsou dodávány bance.
author: panolte
ms.date: 08/22/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePaySummary
audience: Application User
ms.reviewer: kfend
ms.custom:
- "88463"
- intro-internal
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 25e1831e031860ec87a3984688e1b93f3a069657
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722401"
---
# <a name="positive-pay-overview"></a>Přehled kladných plateb

[!include [banner](../includes/banner.md)]

Tento článek poskytuje informace o kladné platbě, kterou můžete použít pro generování elektronických seznamů šeků, které jsou dodávány bance. 

Kladné platby můžete použít pro generování elektronických seznamů šeků, které jsou dodávány bance. Soubory kladných plateb pomáhají bankám zabránit podvodným šekům. Nastavte kladné platby pro generování elektronického seznamu šeků při každém tisku šeků. Potom při předložení šeku bance ho banka srovná se seznamem šeků, který byl předložen dříve. Pokud šek odpovídá tomu, co má banka má v záznamech v seznamu, banka jej zúčtuje. Pokud šek neodpovídá šeku v seznamu, banka předloží šek ke kontrole.

Kladné platby se také označují jako SafePay. 

Soubory kladných plateb mohou obsahovat citlivé informace o příjemcích plateb a šekových částkách. Nezapomeňte tedy použít dostatečná opatření od doby vytvoření souborů do jejich přijetí do banky. Soubory kladných plateb budou staženy podle pokynů pro stažení ve webovém prohlížeči. 

Soubory kladných plateb jsou vytvořeny pomocí datových entit. Před generováním souboru kladných plateb nastavte formáty transformace pro XML, který převádí data do formátu, který může banka používat. 

Pro každý bankovní účet, pro který chcete generovat informace o souborech kladných plateb, musíte přiřadit formát kladných plateb. Po vygenerování plateb lze vygenerovat soubor kladných plateb pro jednu právnickou osobu a jeden bankovní účet. Případně můžete vygenerovat soubory kladných plateb pro více právnických osob a bankovních účtů současně. 

Po zaplacení šeků, které jsou uvedeny v souboru kladných plateb, obdržíte číslo potvrzení od banky. Poté můžete potvrdit soubor kladných plateb v systému. 

Pokud je nutné změnit soubor kladných plateb, můžete jej odvolat. Pro každý šek v souboru kladných plateb se resetuje pole, které označuje, zda byl šek zahrnut do souboru kladných plateb.

Další informace naleznete v tématu [Nastavení a generování souborů kladných plateb](set-up-generate-positive-pay-files.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
