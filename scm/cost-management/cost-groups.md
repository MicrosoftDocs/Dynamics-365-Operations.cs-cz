---
title: "Nákl. skupiny"
description: "Nákladové skupiny poskytují základ pro segmentaci a analýzu nákladových příspěvků v rámci vypočtených nákladů na určitou vyráběnou položku (například nákladové příspěvky na materiál, práci a režii). Termín segmentace nákladových skupin má ve výrobním prostředí několik dalších synonym (například rozúčtování nákladů, dekompozice nákladů nebo klasifikace nákladů)."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCostGroup
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 50871
ms.assetid: 1855f744-f73f-4fa8-8290-a7ee126d368b
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: fb335a521a1a79ea7d978171d233364c58765a0b
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="cost-groups"></a>Nákl. skupiny

[!include[banner](../includes/banner.md)]


Nákladové skupiny poskytují základ pro segmentaci a analýzu nákladových příspěvků v rámci vypočtených nákladů na určitou vyráběnou položku (například nákladové příspěvky na materiál, práci a režii). Termín segmentace nákladových skupin má ve výrobním prostředí několik dalších synonym (například rozúčtování nákladů, dekompozice nákladů nebo klasifikace nákladů). 

Termín segmentace nákladových skupin má ve výrobním prostředí několik dalších synonym (například rozúčtování nákladů, dekompozice nákladů nebo klasifikace nákladů). Segmentace nákladových skupin může sloužit různým účelům. Několik příkladů:

-   Rozdělení nákladů do segmentů podle různých typů materiálů (například ingredience nebo obalový materiál pro konzervované výrobky) na základě nákladových skupin přiřazených k jednotlivým položkám.
-   Rozdělení nákladů do segmentů pro různé typy provozních prostředků (například různé typy práce nebo zařízení) na základě nákladových skupin přiřazených k nákladovým kategoriím souvisejícím s provozními prostředky a operacemi postupů.
-   Rozdělení nákladů do segmentů pro čas pro konfiguraci a pro operační čas v operacích postupu, na základě nákladových skupin přiřazených k nákladovým kategoriím souvisejícím s operacemi postupů.
-   Rozdělení nákladů do segmentů pro různé typy režijních nákladů (například režijní náklady související s prací či zařízeními), na základě nákladových skupin přiřazených v nastavení nákladového formuláře k nepřímým nákladům.
-   Použijte jako základ pro výpočet různých typů režijních nákladů na výrobu v nastavení nákladového formuláře. To může zahrnovat různé typy režijních náklady souvisejících s informacemi postupu o provozních prostředcích nebo o nastavení a operačním čase. Režijní náklady na výrobu mohou také souviset s nákladovými příspěvky na materiál součástí, a odrážet tak filosofii úsporné výroby, která eliminuje potřebu informací o postupu.

Rozdělení nákladových skupin do segmentů se týká vypočtených nákladů vyráběné položky bez ohledu na to, zda byly ceny založeny na standardních nebo na plánovaných nákladech. Stránka **Souhrn** obsahuje toto rozdělení podle nákladových skupin, podle úrovní nebo podle nákladové skupiny i úrovně. 

Tuto možnost zachování rozdělení nákladových skupin do segmentů přes více úrovní v produktové struktuře odráží termín *rozdělení*. Rozdělení se vztahuje pouze na vyráběné položky, které používají skladový model standardních nákladů. Bez použití rozdělení jsou náklady na vyráběnou součást zpracovávány jako nákladový příspěvek na materiál. Parametr zásob pro rozúčtování nákladů podle dílčí hlavní knihy indikuje, že rozdělení nákladových skupin do segmentů bude zachováno ve více úrovních ve standardních výpočtech nákladů. Zatímco zásady bez udané úrovně značí, že rozdělení skupiny nákladů do segmentu se bude vztahovat pouze na výpočty na jedné úrovni. Na stránce **Shrnutí nákladů podle skupiny nákladů** bude například zobrazeno rozdělení nákladových skupin do segmentů přes více úrovní pro standardní nákladové položky. 

Rozdělení nákladových skupin do segmentů může být použito také na odchylky od standardní nákladové položky. Druhý parametr zásob definuje, zda budou odchylky označeny podle nákladové skupiny nebo zda budou pouze shrnuty. 

Nákladové skupině může být přiřazen typ nákladové skupiny a chování pro účely doplňkového rozdělení do segmentů.

-   **Typ nákladové skupiny** − Ke každé nákladové skupině musí být přiřazen typ nákladové skupiny, který označuje nákladovou skupinu jako týkající se přímého materiálu, přímého outsorcingu nebo navržení jako nepřímé či nedefinované výroby. Nákladovou skupinu označenou jako týkající se přímého materiálu lze přiřadit k položkám. Nákladovou skupinu přímé výroby lze přiřadit k nákladovým kategoriím. Nákladová skupina přímého outsourcingu může být přiřazena k typu produktu služby, která umožňuje klasifikaci nákladů souvisejících s nákupem služby pro subdodavatelské aktivity. Nepřímou nákladovou skupinu lze přiřadit k nepřímým nákladům pro příplatky nebo sazby. Nákladovou skupinu, která je označena jako nedefinovaná, lze přiřadit k položkám, nákladovým kategoriím nebo nepřímým nákladům. Přiřazení typu nákladové skupiny slouží několika účelům. Zaprvé omezuje možnost přiřazení nákladové skupiny a zobrazení seznamu použitelných nákladových skupin. Za druhé poskytuje doplňkovou segmentaci pro účely vykazování. Za třetí jej lze použít pro přiřazení účtů hlavní knihy pro různé odchylky.
-   **Chování** − Ke každé nákladové skupině lze volitelně přiřadit určité chování, které označuje danou nákladovou skupinu jako týkající se pevných nebo variabilních nákladů. Nákladová skupina s chováním s hodnotou Null je zpracována jako skupina variabilních nákladů. Přiřazení chování slouží pouze k účelům vykazování. Náklady lze například zobrazit s rozdělením na segmenty pevných a variabilních nákladů v nákladovém formuláři nebo na**Shrnutí nákladů podle skupiny nákladů**. Pokud přiřadíte podíl nastavení zisku pro každou nákladovou skupinu, výpočet kusovníku lze použít pro návrh prodejní ceny na základě vzorce: náklady plus přirážka.





