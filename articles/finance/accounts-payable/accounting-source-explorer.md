---
title: Průzkumník zdroje účetnictví
description: Tento článek obsahuje informace o stránce Průzkumník zdroje účetnictví, který slouží pro podrobnou analýzu informace zdroje za účetními položkami hlavní knihy.
author: RyanCCarlson2
ms.date: 11/21/2022
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
ms.openlocfilehash: 5bd5580dc0be37ec89e6c7934b47c7d5593d8716
ms.sourcegitcommit: 5f8f042f3f7c3aee1a7303652ea66e40d34216e3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806426"
---
# <a name="accounting-source-explorer"></a>Průzkumník zdroje účetnictví

[!include [banner](../includes/banner.md)]

Tento článek obsahuje informace o stránce **Průzkumník zdroje účetnictví**, který slouží pro podrobnou analýzu informace zdroje za účetními položkami hlavní knihy.

Stránka **Průzkumník zdroje účetnictví** zobrazuje informace o zdroji. Můžete ji použít buď jako samostatný nástroj, nebo k analýze podrobností za účetními položkami hlavní knihy. Stránku můžete například použít k získání podrobných informací o zdroji u zůstatku v předvaze nebo u transakce dokladu. Poté můžete použít funkci **Exportovat do aplikace MS Excel** a informace dále rozebírat v aplikaci Microsoft Excel (například v kontingenční tabulce nebo sestavě kontingenční tabulky).

**Průzkumník zdroje účetnictví** vždy zobrazuje stejnou celkovou částku pro účet hlavní knihy, jakou zobrazuje hlavní kniha (například v Předvaze). Stejně jako v předvaze můžete zobrazit segmenty v samostatných sloupcích. Stačí vybrat odpovídající sadu finančních dimenzí. 

Parametry slouží k definování časového intervalu pro analýzu. Tato funkce se také podobá fungování předvahy.

Pro všechny dokumenty používající architekturu zdrojového dokumentu, zobrazí stránka **Průzkumník zdroje účetnictví** další informace, které jsou založené na rozúčtování a v odpovídajících případech rozúčtování projektu. Tyto informace zahrnují hodnotu **Typ peněžní částky**, **Projekt**, **Aktivita**, **Kategorie** a **Vlastnost řádku**. Zde je několik příkladů analýzy, kterou lze provést:

- Odchylky mezi nákupními objednávkami a fakturami dodavatele, protože každou odchylku zastupuje typ peněžní částky, například odchylka ceny
- Fakturovatelné a nefakturovatelné hodiny a výdaje na projekt, obchodní jednotku a hlavní účet

Pro zdrojové dokumenty, které používají koncept identit odkazu na zdrojový dokument, zobrazí stránku **Průzkumník zdroje účetnictví** další údaje, například hodnoty **Zákazník**, **Dodavatel**, **Pracovník**, **Produkt**, **Množství**, **Text jednotky** a **Popis**. Zde je několik příkladů analýzy, kterou lze provést:

- Výdaje za hotel pro obchodní jednotku a značku hotelu pro fiskální období, založené na sestavách výdajů
- Slevy na dodavatele, produkt, oddělení

Pro tyto dokumenty můžete také ze stránky **Průzkumník zdroje účetnictví** přejít na samotný zdrojový dokument.

> [!NOTE]
> Od verze 10.0.31 je ve správě funkcí k dispozici nová funkce **Pokročilé filtrování průzkumníka zdrojů účetnictví**. Tato funkce nahrazuje tlačítko **Aktualizovat** a poskytuje robustnější pokročilé možnosti dotazování, které se podobají tomu, co je k dispozici u stránky **Transakce dokladů**. Pokročilý filtr vám umožní filtrovat podle podobných polí, jaké najdete na stránce **Dotaz na transakce dokladu**, jako je **Účet hlavní knihy**, **Obchodní jednotka**, **Nákladové středisko** a **Oddělení**. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
