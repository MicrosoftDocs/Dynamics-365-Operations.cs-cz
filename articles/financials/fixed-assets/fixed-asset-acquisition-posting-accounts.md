---
title: "Účty pro zaúčtování pořízení dlouhodobého majetku"
description: "V tomto článku je vysvětleno nastavení účtů pro zaúčtování do hlavní knihy pro účely pořizování majetku."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a1a7da48b45566217399bc1d01a9c6e87ad56ec8
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="fixed-asset-acquisition-posting-accounts"></a>Účty pro zaúčtování pořízení dlouhodobého majetku

[!include [banner](../includes/banner.md)]

V tomto článku je vysvětleno nastavení účtů pro zaúčtování do hlavní knihy pro účely pořizování majetku.

Účty použité pro zaúčtování pořízení dlouhodobého majetku se mohou lišit v závislosti na způsobu pořízení majetku. Na stránce profilů zaúčtování dlouhodobého majetku na kartě Účty hlavní knihy vyberte možnost Pořízení a Oprava pořizovací ceny a nastavte účty dlouhodobého majetku pro zaúčtování do hlavní knihy. 

V denících a nákupních objednávkách je účet hlavní knihy obvykle rozvahovým účtem, ve kterém je hodnota pořizovací ceny nového dlouhodobého majetku zaúčtována na stranu Má dáti. Tento účet není v deníku zobrazen a nelze jej nahradit ani v průběhu transakcí. 

Protiúčet je také rozvahovým účtem. V hlavním deníku a v deníku dlouhodobého majetku bude tento účet často sloužit jako bankovní účet používaný pro platby za pořízení majetku. Protiúčet je výchozím účtem nabízeným v denících. Je možné jej změnit v deníku na jakýkoli jiný účet z účtové osnovy nebo na účet dodavatele, a to v případě, že byl dlouhodobý majetek zakoupen od dodavatele. 

Jsou-li položky Deník faktur nebo Nákupní objednávky v modulu Závazky určeny k pořízení dlouhodobého majetku, bude protiúčet pro transakci dlouhodobého majetku nahrazen účtem dodavatele vybraným pro tuto transakci.

Pro nabytí zaúčtované pomocí Skladového deníku dlouhodobého majetku v modulu Hlavní kniha není dlouhodobý majetek zakoupen z externích zdrojů, ale převeden z vlastních zásob společnosti. Z toho důvodu je protiúčet účtem skladového výdeje pro skladové položky v modulu Správa zásob.

Další informace naleznete v tématu [Pořízení majetku pomocí zásobování](acquire-assets-procurement.md).




