---
title: Kombinovaný režim plánování – Kombinování zdrojů samostatné výroby, zpracování a štíhlé výroby
description: Toto téma obsahuje informace o plánování ve smíšeném režimu.
author: cvocph
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 52931
ms.assetid: 2e8b5fd1-cee9-45da-a3ae-6961fb020b89
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6d3febb420637c95e05e58444d0e2a67e5fa2b87
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260496"
---
# <a name="mixed-mode-planning---combine-discrete-process-and-lean-sourcing"></a>Kombinovaný režim plánování – Kombinování zdrojů samostatné výroby, zpracování a štíhlé výroby

[!include [banner](../includes/banner.md)]

Toto téma obsahuje informace o plánování ve smíšeném režimu. Při plánování ve smíšeném režimu můžete modelovat svůj dodavatelsko-odběratelský řetězec podle toku materiálu. Dynamics 365 Supply Chain Management zajišťuje, že tok materiálu bude probíhat podle vašich modelů bez ohledu na vybrané zásady dodávek (kanbany, výrobní zakázky, nákupní objednávky, dávkové objednávky nebo převodní příkazy). 

Můžete vybrat celkové strategie pro dodávání produktu bez ohledu na strukturu výrobku.  

Například máte ovládací prvek kanbanu ve shromáždění, kde jsou odebírány materiály pro oblasti sestavení podle výrobních zakázek, kanbanů, přenosů, dávkových objednávek, nebo libovolných kombinaci, které odpovídají vlastnostem vašeho dodavatelsko-odběratelského řetězce, ale stále můžete mít úplný přehled v dodávkách. Tato schopnost vede k optimalizaci a rozšířenou viditelnost do dodavatelsko-odběratelského řetězce.  

Rozlišovací schopnost zásad dodávek, které jsou použity při hlavním plánování závisí na dimenzích uskladnění, které jsou povoleny jako dimenze disponibility. K povolení hlavního plánování za účelem řízení doplňování a dodávání z různých typů skladových míst, (například oddělením dílenské výroby pro jiné výrobní jednotky, nebo rozdělením různých typů skladů materiálu a hotových výrobků) doporučujeme, abyste povolili pracoviště a sklad jako dimenze disponibility. Případně lze jako dimenzi disponibility vynechat sklad. V takovém případě při použití rozšířené správy skladu budou všechny přesuny ve skladu řízeny prací ve skladu, zatímco všech přesuny mezi sklady budou řízeny příslušnými kanbany.

## <a name="supply-policies"></a>Zásady zásobování
Smíšený způsob plánování řídí způsob dodávání výrobku na základě toho, jak jsou vydávány odvozené požadavky (spotřeba položek z kusovníku \[BOM\]). Podle typu objednávky systém automaticky kontroluje prostředky materiálů, které odpovídají požadavkům.  

Zásady dodávek lze definovat na úrovni produktu nebo na libovolné rozlišovací schopnosti, která podporuje vaše požadavky. Rozlišovací schopnost zásady dodávek jsou definovány na stránce **Výchozí nastavení objednávky**.  

Zásady dodávek mohou být řízeny produktem, dimenzemi položek (konfigurace, barva a velikost), pracovištěm a skladem. Toto nastavení se provádí na stránce **Disponibilita položky**.  

Výchozí typ objednávky určuje, jaké objednávky vygeneruje hlavní plánování.  

Bez ohledu na to, jak je modelován dodavatelsko-odběratelského řetězec, aplikace Supply Chain Management podporuje vaši kompilaci zásad dodávek. Můžete mít výrobních zakázky, které byly vytvořeny z kanbanů. Případně lze nastavit dávkovou objednávku, která vyžaduje produkt, který se dodává převodem nebo kanbanem.  

Aplikace Supply Chain Management zajišťuje, že tok materiálu se řídí modelem.  

Sklad pro výdej materiálu je dynamicky přidělován za běhu po definování zásad dodávky.  

Obvykle nejsou vytvořeny kanbany pro budoucí data, protože kanban má krátký životní cyklus. Pro udržování úplného přehledu o dodavatelsko-odběratelském řetězci, jsme zavedli nový koncept plánování "plánovaný kanban", který se používá k výpočtu odvozených požadavků a pomáhá zajistit, budou požadavky založené na stejné logice, která se používá při vytváření současného kanbanu.  

Stejný postup je k dispozici pro všechny ostatní typy zásad zásobování. Proto je dlouhodobé plánování materiálu založeno na stejném postupu, jaký očekáváte pro spuštění skutečných objednávek po schválení výroby a dodávek.

## <a name="materials-allocation-cross-supply-policy--resource-consumption-on-boms"></a>Zásady přidělení materiálu napříč dodávkami – Spotřeba prostředků v kusovnících
Spotřeba prostředků je důležitá funkce. Spotřeba prostředků umožňuje skladu dynamický výběr materiálu k výdeji na základě zásad zásobování (typu objednávky), a také usnadňuje údržbu základních dat.  

Spotřeba prostředků vyžaduje, aby sklad, jehož materiály se vybírají ze skladu, byly přiřazeny na základě způsobu,jakým je produkt dodáván. Jinak řečeno systém za běhu najde prostředky, které by měly být použity pro výrobu. Na základě těchto prostředků, systém poté vyhledá výdejní sklad.  

Pro práci, která je nezávislá na zásadách zásobování, není nutné změnit informace v Kusovníku, pokud dojde ke změně dodávky. Pro změny ad hoc se aplikace Supply Chain Management ujistí, že materiály pocházejí ze správného skladu.

## <a name="process-manufacturing--the-production-type"></a>Procesní výroba – typ výroby
Pro zajištění plné flexibility v kombinovaném režimu doporučujeme použít kusovníky výrobního typu pro všechny produkty. Potom můžete použít výrobní zakázky, kanbany, objednávky přenosu nebo nákupní objednávky k dodání produktu. Pro výrobní proces je nutné použít typ výroby **vzorce**, **souběžného produktu**, **vedlejšího produktu** nebo **položky plánování**. Kanbany a výrobní zakázky nelze použít pro tyto typy výroby.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]