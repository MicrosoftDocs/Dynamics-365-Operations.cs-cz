---
title: "Průzkumník zdroje účetnictví"
description: "Tento článek obsahuje informace o nástroji Průzkumník zdroje účetnictví, který slouží pro podrobnou analýzu informace zdroje za účetními položkami hlavní knihy."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: 8913e61285d5d180883471991b659ddcb260afe3
ms.lasthandoff: 03/31/2017


---

# <a name="accounting-source-explorer"></a>Průzkumník zdroje účetnictví

[!include[banner](../includes/banner.md)]


Tento článek obsahuje informace o nástroji Průzkumník zdroje účetnictví, který slouží pro podrobnou analýzu informace zdroje za účetními položkami hlavní knihy.

Průzkumník zdroje účetnictví je nová stránka, která zobrazuje informace o zdroji. Můžete použít Průzkumník zdroje účetní buď jako samostatný nástroj nebo analyzovat podrobnosti za účetní položky hlavní knihy. Například můžete použít explorer zdroj účetnictví získat nejpodrobnější informace o zdroji pro rovnováhu v rovnováze Trail nebo transakci dokladu. Poté můžete použít funkci Exportovat do aplikace Microsoft Excel a informace dále rozebírat v Microsoft Excelu (například v kontingenční tabulce nebo sestavě kontingenční tabulky).

Průzkumník zdroje účetnictví vždy zobrazuje stejnou celkovou částku pro účet hlavní knihy, jakou zobrazuje hlavní kniha (například v Předvaze). Stejně jako v předvaze můžete zobrazit segmenty v samostatných sloupcích. Stačí vybrat odpovídající sadu finančních dimenzí. 

Parametry slouží k definování časového intervalu pro analýzu. Tato funkce se také podobá fungování předvahy.

Pro všechny dokumenty, které používají framework zdrojových dokumentů, účetních zdroj explorer zobrazí další informace, které jsou založeny na rozúčtování a v případě potřeby projektu rozúčtování. Tyto informace zahrnují typ peněžní částku, projektu, aktivity, kategorie a vlastnost řádku. Zde je několik příkladů analýzy, kterou lze provést:

-   Odchylky mezi nákupními objednávkami a fakturami dodavatele, protože každou odchylku zastupuje typ peněžní částky, například odchylka ceny
-   Fakturovatelné a nefakturovatelné hodiny a výdaje na projekt, obchodní jednotku a hlavní účet

Pro zdrojové dokumenty, které používají koncept identit odkazu na zdrojový dokument, zobrazí Průzkumník zdroje účetnictví další podrobnosti, například odběratele, dodavatele, pracovníka, produkt, množství, text jednotky a popisy. Zde je několik příkladů analýzy, kterou lze provést:

-   Výdaje za hotel pro obchodní jednotku a značku hotelu pro fiskální období, založené na sestavách výdajů
-   Slevy na dodavatele, produkt, oddělení

Pro tyto dokumenty můžete také z Průzkumníka zdroje účetnictví přejít na samotný zdrojový dokument.




