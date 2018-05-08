---
title: "Omezení nákladových verzí pro standardní náklady"
description: "Toto téma popisuje omezení, která se vztahují na nákladové verze pro standardní náklady."
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e14d5d11e987d2dbc841f86c39fc7e94864144d3
ms.openlocfilehash: 658575492597eed91509561f4710f07e271c53c8
ms.contentlocale: cs-cz
ms.lasthandoff: 01/17/2018

---


#  <a name="restrictions-on-costing-versions-for-standard-costs"></a>Omezení nákladových verzí pro standardní náklady

[!include [banner](../includes/banner.md)]

Toto téma popisuje omezení, která se vztahují na nákladové verze pro standardní náklady. 

Následující omezení pomáhají zajistit zachování principů pro standardní náklady:

-  Do nákladů na položku musí být zahrnuty náklady. Náklady pro vyráběnou položku reprezentují amortizované konstantní náklady v informaci o kusovníku a údaji o postupu. Náklady musí být tedy zahrnuty do jednotkových nákladů. Náklady pro zakoupenou položku budou také zahrnuty do jednotkových nákladů položky.

-  Výpočet standardních nákladů pro vyráběné položky musí být založen na záznamech nákladů v nákladové verzi pro standardní náklady. Alternativní zdroje dat nákladů lze použít pouze s nákladovou verzí pro plánované náklady, jako jsou například obchodní smlouvy s nákupní cenou pro zakoupené položky. Alternativní zdroje dat nákladů jsou definované podle skupiny výpočtu kusovníku.

-  Výpočty kusovníku musí být prováděny v režimu rozpadu s jedinou úrovní.

Data nákladů na položku pro standardní náklady mohou být zkopírována do jiné nákladové verze, která obsahuje standardní náklady nebo plánované náklady. Data nákladů na položku pro plánované náklady však nelze zkopírovat do nákladové verze, která obsahuje standardní náklady, protože by pro plánované náklady nebyla použita omezení uvedená výše v tomto tématu.

<a name="related-topics"></a>Související témata
--------

[Nákladové verze](costing-versions.md)

[Aktualizace standardních nákladů v nevýrobním prostředí](update-standard-costs-non-manufacturing-environment.md)

[Postup přípravy na správu standardních nákladů pro vyráběné položky](update-standard-costs-manufacturing-environment.md)


