---
title: "Amortizace konstantních nákladů na vyráběné zboží"
description: "Konstantní náklady na vyráběné zboží reflektují doby nastavení operace a komponenty s konstantní kvalitou nebo s konstantní odpadovostí."
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcDialog, BOMCalcTable, BOMCalcTrans
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 274503
ms.assetid: 535ab25d-a031-4e8c-84ec-478f2987a1ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: AndersGirke
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: b5345fde8e77b75fd160d08153b19a9be01f18ab
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="amortize-constant-costs-for-a-manufactured-item"></a>Amortizace konstantních nákladů na vyráběné zboží

[!include[banner](../includes/banner.md)]


Konstantní náklady na vyráběné zboží reflektují doby nastavení operace a komponenty s konstantní kvalitou nebo s konstantní odpadovostí. 

Koncept velikosti nákladové šarže slouží k amortizaci těchto konstantních nákladů ve vypočteném nákladu na vyráběnou položku. Tento koncept má několik synonym, z nichž jedním je velikost účetní šarže. Koncept amortizace konstantních nákladů má také několik synonym, z nichž jedním jsou proporční konstantní náklady.

Množství velikosti nákladové šarže pro vyráběnou položku je používáno ve výpočtu ceny kusovníku (BOM). Množství závisí na způsobu zahájení a provedení výpočtu ceny kusovníku, jak je uvedeno dále:

-   Výchozí množství pro výpočet ve výpočtu ceny kusovníku položky − Standardní množství objednávky této položky (pro sklad) se chová jako výchozí možnost velikosti nákladové šarže, ale výchozí možnost by mohla být větší, aby reflektovala násobek množství objednávky položky. Standardní množství objednávky této položky a jeho násobek lze definovat ve výchozím nastavení objednávky nebo v nastaveních objednávky specifických pro pracoviště.
-   Zadané množství pro výpočet ve výpočtu ceny kusovníku položky − Zadané množství pro výpočet se chová jako velikost nákladové šarže této položky. Na počátku vypočtené množství používá standardní množství objednávky tohoto zboží, ale tuto výchozí hodnotu lze ručně přepsat. Zadané množství pro výpočet reprezentuje velikost nákladové šarže dané položky a vyráběných komponent, které mají typ výroby Řádek kusovníku. Důvodem je předpoklad, že součást bude vyráběna v přesném množství. Velikost nákladové šarže vyráběných součástí s produkcí typu kusovník bude odpovídat standardnímu množství objednávky.
-   Zadané množství pro výpočet pro objednávku ve výpočtu ceny kusovníku položky − Zadané množství pro výpočet se v případě, že výpočet ceny kusovníku používá režim rozpadu pro objednávku, chová jako velikost nákladové šarže položky a jejích vyráběných součástí. Předpokládá se, že vyráběné součásti budou vyráběny ve stejném množství, stejně jako vyráběná součást s produkcí typu kusovník.
-   Zadané množství pro výpočet ve výpočtu ceny kusovníku specifickém pro objednávku − Výpočet ceny kusovníku specifický pro objednávku lze provést pro položku řádku kusovníku na prodejní objednávce, na prodejní nabídce nebo na servisní zakázce. Určené množství pro výpočet využívá množství původní položky řádku, ale toto výchozí množství lze přepsat. Můžete vybrat, zda bude výpočet ceny kusovníku specifický pro objednávku používat režim rozpadu pro objednávku nebo režim rozpadu na více úrovních.

Vypočtené množství amortizovaných konstantních nákladů na vyráběnou položku je označeno jako termínované náklady.





