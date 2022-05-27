---
title: Průzkumník zdroje účetnictví
description: Tento článek obsahuje informace o nástroji Průzkumník zdroje účetnictví, který slouží pro podrobnou analýzu informace zdroje za účetními položkami hlavní knihy.
author: RyanCCarlson2
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingSourceExplorer
audience: Application User
ms.reviewer: kfend
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1200092306c1848a2e705b868c2185362b5a3c89
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710462"
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

> [!NOTE]
> Od verze 10.0.20 tlačítko **Aktualizace** poskytuje dva další rozsahy k omezení počátečního dotazu, který je spuštěn pro zadávání dat na stránce. Tyto další rozsahy jsou také k dispozici ve verzi 10.0.19 jako aktualizace služby. Byla přidána následující pole:
>
> - Od dokladu, Po doklad
> - Z hlavního účtu, Na hlavní účet

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
