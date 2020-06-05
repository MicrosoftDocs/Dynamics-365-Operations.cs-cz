---
title: Mezipodnikové výdaje
description: Pracovník, který je zaměstnán jednou právnickou osobou v jedné organizaci, může provádět práci pro jinou právnickou osobu v rámci stejné organizace. V takové situaci můžete použít funkci mezipodnikových výdajů přiřazení pro přiřazení výdajů pracovníka k právnické osobě, pro kterou byla práce prováděna.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 07e425707eb20730f10246a27799f4deeef93f97
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/21/2020
ms.locfileid: "3390877"
---
# <a name="intercompany-expenses"></a>Mezipodnikové výdaje

[!include [banner](../includes/banner.md)]

Pracovník, který je zaměstnán jednou právnickou osobou v jedné organizaci, může provádět práci pro jinou právnickou osobu v rámci stejné organizace. V takové situaci můžete použít funkci mezipodnikových výdajů přiřazení pro přiřazení výdajů pracovníka k právnické osobě, pro kterou byla práce prováděna. Právnická osoba, která pracovníka zaměstnává, se nazývá půjčující právnická osoba. Právnická osoba, vůči které pracovník uplatňuje výdaje, se nazývá vypůjčující právnická osoba. 

Předtím, než pracovník může vytvářet a odesílat výdaje za práci pro jinou právnickou osobu, zvolte u půjčující právnické osoby na stránce **Parametry správy výdajů** možnost **Povolit řádky mezipodnikových výdajů**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Zaúčtování daně pro mezipodnikové výdaje

[!include [banner](../includes/banner.md)]

Pokud chcete ve své sestavě výdajů použít daňové skupiny, které jsou přidruženy k půjčující (zdrojové) právnické osobě, místo právnické osoby vypůjčující (cílové), budete to muset nakonfigurovat v nastavení DPH v hlavní knize. Když je parametr hlavní knihy **Právnická osoba pro zaúčtování mezipodnikové daně** nastaven na **Zdroj** a **Použít daňové předpisy pro DPH** je nastaveno na **Ne**, bude použita daňová kombinace pro půjčující právnickou osobu. Když je stejný parametr nastaven na **Cíl**, bude použita daňová kombinace pro vypůjčující právnickou osobu. U právnických osob ve Spojených státech, musí být pole **DPH na vstupu** nakonfigurováno na nové stránce **Účetní skupiny hlavní knihy**, když je parametr nastaven na **Zdroj**. Účetní modul použije informace z tohoto pole pro účetní záznam vztahující se k dani.   
Chování je konzistentní pro výdajové řádky zaúčtované s projektem nebo bez něj.  
