---
title: Omezení nákladových verzí pro standardní náklady
description: Toto téma popisuje omezení, která se vztahují na nákladové verze pro standardní náklady.
author: AndersGirke
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9d828e2413a20c4e61d162a31d3c2ed2b18718b
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187667"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a>Omezení nákladových verzí pro standardní náklady

[!include [banner](../includes/banner.md)]

Toto téma popisuje omezení, která se vztahují na nákladové verze pro standardní náklady. 

Následující omezení pomáhají zajistit zachování principů pro standardní náklady:

-  Do nákladů na položku musí být zahrnuty náklady. Náklady pro vyráběnou položku reprezentují amortizované konstantní náklady v informaci o kusovníku a údaji o postupu. Náklady musí být tedy zahrnuty do jednotkových nákladů. Náklady pro zakoupenou položku budou také zahrnuty do jednotkových nákladů položky.

-  Výpočet standardních nákladů pro vyráběné položky musí být založen na záznamech nákladů v nákladové verzi pro standardní náklady. Alternativní zdroje dat nákladů lze použít pouze s nákladovou verzí pro plánované náklady, jako jsou například obchodní smlouvy s nákupní cenou pro zakoupené položky. Alternativní zdroje dat nákladů jsou definované podle skupiny výpočtu kusovníku.

-  Výpočty kusovníku musí být prováděny v režimu rozpadu s jedinou úrovní.

Data nákladů na položku pro standardní náklady mohou být zkopírována do jiné nákladové verze, která obsahuje standardní náklady nebo plánované náklady. Data nákladů na položku pro plánované náklady však nelze zkopírovat do nákladové verze, která obsahuje standardní náklady, protože by pro plánované náklady nebyla použita omezení uvedená výše v tomto tématu.

## <a name="related-topics"></a>Související témata

[Přehled verzí výpočtu nákladů](costing-versions.md)

[Aktualizace standardních nákladů v nevýrobním prostředí](update-standard-costs-non-manufacturing-environment.md)

[Postup přípravy na správu standardních nákladů pro vyráběné položky](update-standard-costs-manufacturing-environment.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]