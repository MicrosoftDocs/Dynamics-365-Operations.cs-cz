---
title: Průzkumník zdroje účetnictví
description: Tento článek obsahuje informace o nástroji Průzkumník zdroje účetnictví, který slouží pro podrobnou analýzu informace zdroje za účetními položkami hlavní knihy.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingSourceExplorer
audience: Application User
ms.reviewer: roschlom
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d98ab6c4bc1d6f98a863a36bd35c19696ccd7b3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972198"
---
# <a name="accounting-source-explorer"></a>Průzkumník zdroje účetnictví

[!include [banner](../includes/banner.md)]

Tento článek obsahuje informace o nástroji Průzkumník zdroje účetnictví, který slouží pro podrobnou analýzu informace zdroje za účetními položkami hlavní knihy.

Průzkumník zdroje účetnictví je nová stránka, která zobrazuje informace o zdroji. Můžete použít Průzkumníka zdroje účetnictví buď jako samostatný nástroj nebo k analýze podrobností za účetními položkami hlavní knihy. Průzkumníka zdroje účetnictví můžete například použít k získání podrobných informací o zdroji u zůstatku v předvaze nebo u transakce dokladu. Poté můžete použít funkci Exportovat do aplikace MS Excel a informace dále rozebírat v aplikaci Microsoft Excel (například v kontingenční tabulce nebo sestavě kontingenční tabulky).

Průzkumník zdroje účetnictví vždy zobrazuje stejnou celkovou částku pro účet hlavní knihy, jakou zobrazuje hlavní kniha (například v Předvaze). Stejně jako v předvaze můžete zobrazit segmenty v samostatných sloupcích. Stačí vybrat odpovídající sadu finančních dimenzí. 

Parametry slouží k definování časového intervalu pro analýzu. Tato funkce se také podobá fungování předvahy.

Pro všechny dokumenty používající architekturu zdrojového dokumentu, zobrazí průzkumník zdroje účetnictví další informace, které jsou založené na rozúčtování a v odpovídajících případech rozúčtování projektu. Tyto informace zahrnují typ peněžní částky, projekt, aktivitu, kategorii a vlastnost řádku. Zde je několik příkladů analýzy, kterou lze provést:

-   Odchylky mezi nákupními objednávkami a fakturami dodavatele, protože každou odchylku zastupuje typ peněžní částky, například odchylka ceny
-   Fakturovatelné a nefakturovatelné hodiny a výdaje na projekt, obchodní jednotku a hlavní účet

Pro zdrojové dokumenty, které používají koncept identit odkazu na zdrojový dokument, zobrazí Průzkumník zdroje účetnictví další podrobnosti, například odběratele, dodavatele, pracovníka, produkt, množství, text jednotky a popisy. Zde je několik příkladů analýzy, kterou lze provést:

-   Výdaje za hotel pro obchodní jednotku a značku hotelu pro fiskální období, založené na sestavách výdajů
-   Slevy na dodavatele, produkt, oddělení

Pro tyto dokumenty můžete také z Průzkumníka zdroje účetnictví přejít na samotný zdrojový dokument.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]