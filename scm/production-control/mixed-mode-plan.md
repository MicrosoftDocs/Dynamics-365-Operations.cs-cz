---
title: "Kombinovaný režim plánování - kombinují diskrétní, procesu a štíhlé původ"
description: "Tento článek obsahuje informace o plánování ve smíšeném režimu. Při plánování ve smíšeném režimu můžete modelovat svůj dodavatelsko-odběratelský řetězec podle toku materiálu. 365 Microsoft Dynamics pro operace zajišťuje, že následuje toku materiálu modely, bez ohledu na zásady dodávek, který je vybrán (kanbany, výrobní zakázky, nákupní objednávky, dávkové objednávky nebo objednávky transferu)."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 52931
ms.assetid: 2e8b5fd1-cee9-45da-a3ae-6961fb020b89
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d635421112f6d1e79a47090de3ffc4178b36b132
ms.lasthandoff: 03/31/2017


---

# <a name="mixed-mode-planning---combine-discrete-process-and-lean-sourcing"></a>Kombinovaný režim plánování - kombinují diskrétní, procesu a štíhlé původ

[!include[banner](../includes/banner.md)]


Tento článek obsahuje informace o plánování ve smíšeném režimu. Při plánování ve smíšeném režimu můžete modelovat svůj dodavatelsko-odběratelský řetězec podle toku materiálu. 365 Microsoft Dynamics pro operace zajišťuje, že následuje toku materiálu modely, bez ohledu na zásady dodávek, který je vybrán (kanbany, výrobní zakázky, nákupní objednávky, dávkové objednávky nebo objednávky transferu). 

Můžete vybrat celkové strategie pro dodávání produktu bez ohledu na strukturu výrobku.  

Například máte ovládací prvek kanbanu ve shromáždění, kde jsou odebírány materiály pro oblasti sestavení podle výrobních zakázek, kanbanů, přenosů, dávkových objednávek, nebo libovolných kombinaci, které odpovídají vlastnostem vašeho dodavatelsko-odběratelského řetězce, ale stále můžete mít úplný přehled v dodávkách. Tato schopnost vede k optimalizaci a rozšířenou viditelnost do dodavatelsko-odběratelského řetězce.  

Rozlišovací schopnost zásad dodávek, které jsou použity při hlavním plánování závisí na dimenzích uskladnění, které jsou povoleny jako dimenze disponibility. K povolení hlavního plánování za účelem řízení doplňování a dodávání z různých typů skladových míst, (například oddělením dílenské výroby pro jiné výrobní jednotky, nebo rozdělením různých typů skladů materiálu a hotových výrobků) doporučujeme, abyste povolili pracoviště a sklad jako dimenze disponibility. Případně lze jako dimenzi disponibility vynechat sklad. V takovém případě při použití rozšířené správy skladu budou všechny přesuny ve skladu řízeny prací ve skladu, zatímco všech přesuny mezi sklady budou řízeny příslušnými kanbany.

## <a name="supply-policies"></a>Zásady zásobování
Dynamics 365 pro plánování operací kombinovaný režim řídí, jak je produkt dodaný a, založené na tom, jak odvozené požadavky (spotřeba položky kusovníku materiálů \[Kusovníku\]) jsou vydávány. Podle typu objednávky systém automaticky kontroluje prostředky materiálů, které odpovídají požadavkům.  

Zásady dodávek lze definovat na úrovni produktu nebo na libovolné rozlišovací schopnosti, která podporuje vaše požadavky. Rozlišovací schopnost zásady dodávek jsou definovány na stránce **Výchozí nastavení objednávky**.  

Zásady dodávek mohou být řízeny produktem, dimenzemi položek (konfigurace, barva a velikost), pracovištěm a skladem. Toto nastavení se provádí na stránce **Disponibilita položky**.  

Výchozí typ objednávky určuje, jaké objednávky vygeneruje hlavní plánování.  

Bez ohledu na to, jak je modelována dodavatelského řetězce 365 Dynamics pro operace podporuje váš mix zásady dodávek. Můžete mít výrobních zakázky, které byly vytvořeny z kanbanů. Případně lze nastavit dávkovou objednávku, která vyžaduje produkt, který se dodává převodem nebo kanbanem.  

Dynamics 365 pro operace je zajištěno, že následuje toku materiálu v modelu.  

Sklad pro výdej materiálu je dynamicky přidělován za běhu po definování zásad dodávky.  

Obvykle nejsou vytvořeny kanbany pro budoucí data, protože kanban má krátký životní cyklus. Pro udržování úplného přehledu o dodavatelsko-odběratelském řetězci, jsme zavedli nový koncept plánování "plánovaný kanban", který se používá k výpočtu odvozených požadavků a pomáhá zajistit, budou požadavky založené na stejné logice, která se používá při vytváření současného kanbanu.  

Stejný postup je k dispozici pro všechny ostatní typy zásad zásobování. Proto je dlouhodobé plánování materiálu založeno na stejném postupu, jaký očekáváte pro spuštění skutečných objednávek po schválení výroby a dodávek.

## <a name="materials-allocation-crosssupply-policy--resource-consumption-on-boms"></a>Zásady přidělení materiálů – crosssupply-spotřeba zdrojů v kusovnících
Spotřebu zdrojů je důležité funkce. Spotřeba prostředků umožňuje skladu dynamický výběr materiálu k výdeji na základě zásad zásobování (typu objednávky), a také usnadňuje údržbu základních dat.  

Spotřeba prostředků vyžaduje, aby sklad, jehož materiály se vybírají ze skladu, byly přiřazeny na základě způsobu,jakým je produkt dodáván. Jinak řečeno systém za běhu najde prostředky, které by měly být použity pro výrobu. Na základě těchto prostředků, systém poté vyhledá výdejní sklad.  

Pro práci, která je nezávislá na zásadách zásobování, není nutné změnit informace v Kusovníku, pokud dojde ke změně dodávky. Ad-hoc změn 365 Dynamics pro operace zajišťuje, že se materiály pocházející z pravé skladu.

## <a name="process-manufacturing--the-production-type"></a>Procesní výroba – typ výroby
Úplná flexibilita v kombinovaném režimu doporučujeme použít typ výrobní kusovníky pro všechny produkty. Potom můžete výrobních zakázek, kanbany, objednávky transferu nebo objednávky nákupní dodávky produktu. Pro výrobní proces je nutné použít typ výroby **vzorce**, **souběžného produktu**, **vedlejšího produktu** nebo **položky plánování**. Kanbany a výrobní zakázky nelze použít pro tyto typy výroby.




