---
title: Standardní uložená zobrazení pro Supply Chain Management
description: Tento článek popisuje standardní uložené pohledy, které jsou k dispozici, a vysvětluje, jak je povolit.
author: kamaybac
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 92ff2dfc9cd8b742a7b086e540bd2c527833254d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887551"
---
# <a name="standard-saved-views-for-supply-chain-management"></a>Standardní uložená zobrazení pro Supply Chain Management

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management obsahuje několik uložených zobrazení, která můžete podle potřeby povolit a použít. Některé z těchto standardních uložených zobrazení jsou optimalizovány a pojmenovány pro konkrétní roli nebo úkol (například „Kontrola kvality“ nebo „Příjem“). Jiné jsou optimalizovány tak, aby zahrnovaly pouze pole a nastavení, která podle statistik používání společnosti Microsoft zákazníci nejčastěji používají. Tato uložená zobrazení se obvykle označují jako *zjednodušená* zobrazení. Tento článek popisuje standardní uložené pohledy, které jsou k dispozici, a vysvětluje, jak je povolit a přizpůsobit.

Úplné podrobnosti o tom, jak pracovat s uloženými zobrazeními, včetně standardních uložených zobrazení, po jejich povolení najdete v části [Uložená zobrazení](../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json).

## <a name="customizing-the-standard-saved-views"></a>Přizpůsobení standardních uložených zobrazení

Můžete si přizpůsobit standardní uložená zobrazení, stejně jako si můžete přizpůsobit svá vlastní uložená zobrazení. Když však přizpůsobíte standardní uložené zobrazení, důrazně doporučujeme uložit vlastní verzi pod novým názvem. Jinak by vaše přizpůsobení mohlo být přepsáno při aktualizaci Supply Chain Management.

Další informace o tom, jak přizpůsobit a přejmenovat uložená zobrazení, najdete v části [Uložená zobrazení](../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json).

## <a name="available-saved-views-and-how-to-enable-them"></a>Dostupná uložená zobrazení a způsob jejich povolení

Chcete-li použít libovolné uložené zobrazení, musíte bez ohledu na to, zda použijete standardní uložené pohledy, zapnout funkci *Uložená zobrazení* ve [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (od verze 10.0.21 je tato funkce ve výchozím nastavení povolena).

Zbývající části tohoto článku obsahují tabulky, které popisují standardní uložená zobrazení, která jsou aktuálně k dispozici pro každý příslušný modul. Každá tabulka zobrazuje název každého uloženého zobrazení, stránku, kde ho najdete, a popis. Každá tabulka také zobrazuje název funkce, která zahrnuje uložené zobrazení. Chcete-li ve svém systému zobrazit standardní uložené zobrazení, musíte zapnout určenou funkci v okně [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Od verze 10.0.25 jsou všechna uvedená zobrazení ve výchozím nastavení zapnuta.

## <a name="saved-views-for-the-inventory-management-module"></a>Uložená zobrazení pro modul řízení zásob

Následující tabulka popisuje uložená zobrazení dostupná pro modul Řízení zásob.

| Strana | Název zobrazení | Zobrazení popisu | Název funkce |
|---|---|---|---|
| Seznam skladu | Finance | Toto zjednodušené zobrazení vám umožní soustředit se na finanční informace, zatímco budete spravovat zásoby na skladě. | Uložená zobrazení pro řízení zásob<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.21) |
| Seznam skladu | Řízení kvality | Toto zjednodušené zobrazení vám umožní soustředit se na kontrolu kvality, zatímco budete spravovat zásoby na skladě. | Uložená zobrazení pro řízení zásob<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.21) |
| Seznam skladu | Příjem | Toto zjednodušené zobrazení vám umožní soustředit se na operace příjmu, zatímco budete spravovat zásoby na skladě. | Uložená zobrazení pro řízení zásob<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.21) |
| Seznam skladu | Expedice | Toto zjednodušené zobrazení vám umožní soustředit se na operace expedování, zatímco budete spravovat zásoby na skladě. | Uložená zobrazení pro řízení zásob<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.21) |
| Transakce | Zjednodušený | Toto zjednodušené zobrazení umožňuje kontrolovat stav zásob, aniž by vás rozptylovaly finanční informace a další pole, která se používají méně často. | Uložená zobrazení pro řízení zásob<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.21) |
| Převodní příkazy | Expedice | Toto zjednodušené zobrazení vám umožní soustředit se na operace expedování, zatímco budete spravovat objednávky převodu. | Uložená zobrazení pro řízení zásob<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.21) |
| Převodní příkazy | Příjem | Toto zjednodušené zobrazení vám umožní soustředit se na operace příjmu, zatímco budete spravovat objednávky převodu. | Uložená zobrazení pro řízení zásob<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.21) |
| Převodní příkazy | Řízení kvality | Toto zjednodušené zobrazení vám umožní soustředit se na operace kontroly kvality, zatímco budete spravovat objednávky převodu. | Uložená zobrazení pro řízení zásob<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.21) |
| Převodní příkazy | Finance | Toto zjednodušené zobrazení vám umožní soustředit se na finanční údaje, zatímco budete spravovat objednávky převodu. | Uložená zobrazení pro řízení zásob<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.21) |

## <a name="saved-views-for-the-master-planning-module"></a>Uložená zobrazení pro modul hlavního plánování

Následující tabulka popisuje uložená zobrazení dostupná pro modul Hlavní plánování.

| Strana | Název zobrazení | Zobrazení popisu | Název funkce |
|---|---|---|---|
| Plánované objednávky: Stránka s podrobnostmi o plánované objednávce | Zjednodušené | Toto zjednodušené zobrazení zahrnuje pouze pole, která se nejčastěji používají pro práci s podrobnostmi jedné plánované objednávky. Tímto způsobem poskytuje rychlejší přehled a efektivní pracovní proces. | Uložená zobrazení pro plánované objednávky<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.25) |
| Plánované objednávky: Stránka se seznamem plánovaných objednávek | Zjednodušený | Toto zjednodušené zobrazení zahrnuje pouze pole, která se nejčastěji používají pro práci se seznamy plánovaných objednávek. Tímto způsobem poskytuje rychlejší přehled a efektivní pracovní proces. | Uložená zobrazení pro plánované objednávky<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.25) |

## <a name="saved-views-for-the-procurement-and-sourcing-module"></a>Uložená zobrazení pro modul Zásobování a zdroje

Následující tabulka popisuje uložená zobrazení dostupná pro modul Zásobování a zdroje.

| Strana | Název zobrazení | Zobrazení popisu | Název funkce |
|---|---|---|---|
| Podrobnosti nákupní objednávky | Vytvoření objednávky | Toto zjednodušené zobrazení je optimalizováno pro vytváření nových objednávek. | Uložená zobrazení pro nákupní objednávky<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.25) |
| Podrobnosti nákupní objednávky | Řízení zásob | Toto zjednodušené zobrazení je optimalizováno pro provádění činností souvisejících s inventářem, jako je sledování zásob, které byly přijaty, příjem inventáře, kontrola požadavků na síť a úprava množství objednávky. | Uložená zobrazení pro nákupní objednávky<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.25) |
| Podrobnosti nákupní objednávky | Správa financí | Toto zjednodušené zobrazení je optimalizováno pro provádění činností souvisejících s financemi, jako je fakturace a kontrola cen, součtů a poplatků. | Uložená zobrazení pro nákupní objednávky<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.25) |
| Podrobnosti nákupní objednávky | Schválení objednávky | Toto zjednodušené zobrazení je optimalizováno pro schvalování nákupních objednávek. | Uložená zobrazení pro nákupní objednávky<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.25) |

## <a name="saved-views-for-the-product-information-management-module"></a>Uložená zobrazení pro modul správy Informace o produktu

Následující tabulka popisuje uložená zobrazení dostupná pro modul správy Informace o produktu.

| Strana | Název zobrazení | Zobrazení popisu | Název funkce |
|---|---|---|---|
| Seznam uvolněných produktů | Vytvoření produktu | Zjednodušené zobrazení stránky, které obsahuje pouze nejčastěji používaná pole při tvorbě produktů. | Uložená zobrazení pro uvolněné produkty<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.21) |
| Podrobnosti o uvolněném produktu | Vytvoření produktu | Zjednodušené zobrazení stránky, které obsahuje pouze nejčastěji používaná pole při tvorbě produktů. | Uložená zobrazení pro uvolněné produkty<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.21) |
| Podrobnosti o uvolněném produktu | Správa logistických informací | Zjednodušené zobrazení stránky, které obsahuje pouze nejčastěji používaná pole při správě logistických informací o produktech. | Uložená zobrazení pro uvolněné produkty<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.21) |
| Podrobnosti o uvolněném produktu | Správa informací o nákupu | Zjednodušené zobrazení stránky, které obsahuje pouze nejčastěji používaná pole při správě informací o nákupech produktů. | Uložená zobrazení pro uvolněné produkty<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.21) |
| Podrobnosti o uvolněném produktu | Správa informací o prodeji | Zjednodušené zobrazení stránky, které obsahuje pouze nejčastěji používaná pole při správě informací o produktech souvisejících s prodejem. | Uložená zobrazení pro uvolněné produkty<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.21) |

## <a name="saved-views-for-the-production-control-module"></a>Uložená zobrazení pro modul řízení výroby

Následující tabulka popisuje uložená zobrazení dostupná pro modul Řízení výroby.

| Strana | Název zobrazení | Zobrazení popisu | Název funkce |
|---|---|---|---|
| Stránka kusovníku výrobního příkazu | Zjednodušené | Toto zjednodušené zobrazení zahrnuje pouze pole, která se nejčastěji používají. Tímto způsobem poskytuje rychlejší přehled a efektivní pracovní proces. | Uložená zobrazení pro řízení výroby<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.21) |
| Stránka podrobností výrobního příkazu | Zjednodušený | Toto zjednodušené zobrazení zahrnuje pouze pole, která se nejčastěji používají. Tímto způsobem poskytuje rychlejší přehled a efektivní pracovní proces. | Uložená zobrazení pro řízení výroby<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.21) |
| Stránka výdejky výrobního příkazu | Zjednodušený | Toto zjednodušené zobrazení zahrnuje pouze pole, která se nejčastěji používají. Tímto způsobem poskytuje rychlejší přehled a efektivní pracovní proces. | Uložená zobrazení pro řízení výroby<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.21) |
| Stránka výdejky výrobních příkazů | Zjednodušený | Toto zjednodušené zobrazení zahrnuje pouze pole, která se nejčastěji používají. Tímto způsobem poskytuje rychlejší přehled a efektivní pracovní proces. | Uložená zobrazení pro řízení výroby<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.21) |

## <a name="saved-views-for-the-sales-and-marketing-module"></a>Uložená zobrazení pro modul Prodej a marketing

Následující tabulka popisuje uložená zobrazení dostupná pro modul Prodej a marketing.

| Strana | Název zobrazení | Zobrazení popisu | Název funkce |
|---|---|---|---|
| Deník dodacích listů | Recenze deníku | Toto zjednodušené zobrazení zahrnuje pouze pole, která se nejčastěji používají ke kontrole deníků dodacích listů. | Uložená zobrazení pro prodej a marketing<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.25) |
| Prodejní objednávka | Tvorba objednávky | Toto zjednodušené zobrazení zahrnuje pouze pole, která se nejčastěji používají k vytvoření prodejních objednávek. | Uložená zobrazení pro prodej a marketing<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.25) |
| Prodejní objednávka | Kontrola objednávky | Toto zjednodušené zobrazení zahrnuje pouze pole, která se nejčastěji používají ke kontrole prodejních objednávek. | Uložená zobrazení pro prodej a marketing<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.25) |
| Prodejní nabídka | Tvorba nabídky | Toto zjednodušené zobrazení zahrnuje pouze pole, která se nejčastěji používají k vytvoření prodejních nabídek. | Uložená zobrazení pro prodej a marketing<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.25) |

## <a name="saved-views-for-the-warehouse-management-module"></a>Uložená zobrazení pro modul řízení skladu

Následující tabulka popisuje uložená zobrazení dostupná pro modul Řízení skladu.

| Strana | Název zobrazení | Zobrazení popisu | Název funkce |
|---|---|---|---|
| Všechny náklady | Příchozí zpracování | Toto zjednodušené zobrazení zahrnuje pouze pole, která se nejčastěji používají ke zpracování příchozích nákladů. | Uložená zobrazení pro zpracování vytížení<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.25) |
| Všechny náklady | Odchozí zpracování | Toto zjednodušené zobrazení zahrnuje pouze pole, která se nejčastěji používají ke zpracování odchozích nákladů. | Uložená zobrazení pro zpracování vytížení<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.25) |
| Všechny dodávky | Příchozí zpracování | Toto zjednodušené zobrazení zahrnuje pouze pole, která se nejčastěji používají ke zpracování příchozích zásilek. | Uložená zobrazení pro zpracování dodávky<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.25) |
| Všechny dodávky | Odchozí zpracování | Toto zjednodušené zobrazení zahrnuje pouze pole, která se nejčastěji používají ke zpracování odchozích zásilek. | Uložená zobrazení pro zpracování dodávky<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.25) |
| Všechny vlny | Zjednodušený | Toto zjednodušené zobrazení zahrnuje pouze pole, která se nejčastěji používají. Tímto způsobem poskytuje rychlejší přehled a efektivní pracovní proces. | Uložené zobrazení pro zpracování vlny<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.25) |
| Pracovní plocha plánování vytížení | Zjednodušený | Toto zjednodušené zobrazení zahrnuje pouze pole, která se nejčastěji používají. Tímto způsobem poskytuje rychlejší přehled a efektivní pracovní proces. | Uložené zobrazení pro pracovní plochu plánování vytížení<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.25) |
| Podrobnosti o práci | Zjednodušený | Toto zjednodušené zobrazení zahrnuje pouze pole, která se nejčastěji používají. Tímto způsobem poskytuje rychlejší přehled a efektivní pracovní proces. | Uložené zobrazení stránky s podrobnostmi o práci<br><br>(Ve výchozím nastavení zapnuto od verze 10.0.25) |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]