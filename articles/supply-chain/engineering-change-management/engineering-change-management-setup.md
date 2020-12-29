---
title: Stanovení společných hodnot pro správu technických změn
description: Toto téma popisuje, jak stanovit běžné hodnoty, které se používají pro parametry v různých částech správy technických změn.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductParameters, EngChgEcmSeverityTable, EngChgEcmSeverityRuleSet, EngChgEcmSeverityLookup,EngChgEcmSeverityChart,EngChgEcmRequestSeverityChart,EngChgEcmPriorityTable, EngChgEcmPriorityLookup, EngChgEcmPriorityChart, EngChgEcmMaterialDisposition, EngChgEcmEH
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 86de050ef4110e3485a77099440f3402e46cc498
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/29/2020
ms.locfileid: "4424267"
---
# <a name="establish-common-values-for-engineering-change-management"></a>Stanovení společných hodnot pro správu technických změn

[!include [banner](../includes/banner.md)]

Když nastavíte správu technických změn, musíte vytvořit několik kolekcí hodnot, které se použijí k vyplnění rozevíracích seznamů v jiných částech uživatelského rozhraní (UI). Tyto hodnoty byste měli specifikovat podle typů produktů, které vyrábíte, a podle vašich konkrétních obchodních potřeb.

## <a name="engineering-change-categories"></a>Kategorie technických změn

Pomocí kategorií technických změn organizujete své objednávky technických změn, takže je lze snáze spravovat a kontrolovat. Například pro vás může být užitečné nastavit pracovní postup, kde v závislosti na kategorii musí konkrétní oddělení zkontrolovat navrhované změny. Pořadí technické změny proto zahrnuje pole **Kategorie**.

Chcete-li vytvořit kolekci kategorií technických změn, která se používá ve vaší společnosti, přejděte na **Řízení technických změn \> Nastavení \> Řízení technických změn \> Kategorie technických změn**. Potom můžete pomocí tlačítek v podokně akcí přidávat, odebírat a upravovat hodnoty a uspořádat je do pořadí, v jakém by se měly zobrazovat v rozevíracích seznamech, kde jsou zobrazeny.

## <a name="engineering-change-priorities"></a>Priority technických změn

Priority technických změn používáte k označení důležitosti nebo naléhavosti objednávky technických změn. Mohou vám pomoci sledovat důležitost objednávky technické změny, abyste mohli snadno určit, které objednávky by měly být zpracovány jako první a jak rychle.

Chcete-li vytvořit kolekci priorit technických změn, která se používá ve vaší společnosti, přejděte na **Řízení technických změn \> Nastavení \> Řízení technických změn \> Priority technických změn**. Potom můžete pomocí tlačítek v podokně akcí přidávat, odebírat a upravovat hodnoty a uspořádat je do pořadí, v jakém by se měly zobrazovat v rozevíracích seznamech, kde jsou zobrazeny.

## <a name="engineering-change-reasons"></a>Důvody technických změn

Důvody technických změn označují příčinu nebo povahu změny v pořadí změn.

Chcete-li vytvořit kolekci důvodů technických změn, která se používá ve vaší společnosti, přejděte na **Řízení technických změn \> Nastavení \> Řízení technických změn \> Důvody technických změn**. Potom můžete pomocí tlačítek v podokně akcí přidávat, odebírat a upravovat hodnoty a uspořádat je do pořadí, v jakém by se měly zobrazovat v rozevíracích seznamech, kde jsou zobrazeny.

## <a name="material-disposal-codes"></a>Kódy pro likvidaci materiálu

Kódy pro likvidaci materiálu používáte ke kategorizaci materiálů, které se používají ve vašich hotových výrobcích, nebo komponent, které musí být zlikvidovány konkrétním způsobem nebo vyžadují určité zacházení, než mohou být přidány do vašeho běžného koše. Když přidáte relevantní produkt do příkazu technické změny, můžete v rámci podrobností o změně přiřadit kód pro likvidaci.

Chcete-li vytvořit kolekci kódů pro likvidaci materiálu, která se používá ve vaší společnosti, přejděte na **Řízení technických změn \> Nastavení \> Řízení technických změn \> Kódy pro likvidaci materiálu**. Potom můžete pomocí tlačítek v podokně akcí přidávat, odebírat a upravovat hodnoty a uspořádat je do pořadí, v jakém by se měly zobrazovat v rozevíracích seznamech, kde jsou zobrazeny.

## <a name="received-customer-approval"></a>Přijatý souhlas zákazníka

Když navrhujete produkty pro konkrétního zákazníka, musí být design a specifikace často ověřovány, než bude možné produkt nastavit jako připravený. Pole **Obdržel souhlas zákazníka** umožňuje určit, jak daleko v procesu schválení zákazníkem je produkt a/nebo zda bylo schválení přijato.

Chcete-li vytvořit kolekci přijatých hodnot schválení zákazníkem, která se používá ve vaší společnosti, přejděte na **Řízení technických změn \> Nastavení \> Řízení technických změn \> Přijaté schválení zákazníka**. Potom můžete pomocí tlačítek v podokně akcí přidávat, odebírat a upravovat hodnoty a uspořádat je do pořadí, v jakém by se měly zobrazovat v rozevíracích seznamech, kde jsou zobrazeny.

## <a name="engineering-change--environmental-health-and-safety-codes"></a>Technické změny - Předpisy o ochraně zdraví a bezpečnosti životního prostředí

Pokud je při výrobě produktu nutné zohlednit některá standardní nařízení o ochraně zdraví a bezpečnosti při práci nebo předpisy nebo postupy specifické pro společnost, můžete je definovat pomocí předpisů o ochraně zdraví a bezpečnosti při práci. V pořadí technických změn můžete určit, které kódy se vztahují na výrobu produktu, zatímco upravujete podrobnosti dotčeného produktu.

Chcete-li vytvořit kolekci hodnot zdraví a bezpečnosti, která se používá ve vaší společnosti, přejděte na **Řízení technických změn \> Nastavení \> Řízení technických změn \> Změna technického zpracování - kódy zdraví a bezpečnosti pro životní prostředí**. Potom můžete pomocí tlačítek v podokně akcí přidávat, odebírat a upravovat hodnoty a uspořádat je do pořadí, v jakém by se měly zobrazovat v rozevíracích seznamech, kde jsou zobrazeny.

## <a name="engineering-change-severities"></a>Závažnosti technických změn

Pomocí závažnosti technických změn označujete úroveň dopadu, která se vztahuje na produkty v pořadí technických změn.

Chcete-li vytvořit kolekci závažností technických změn, která se používá ve vaší společnosti, přejděte na **Řízení technických změn \> Nastavení \> Řízení technických změn \> Závažnosti technických změn**. Potom můžete pomocí tlačítek v podokně akcí přidávat, odebírat a upravovat hodnoty a uspořádat je do pořadí, v jakém by se měly zobrazovat v rozevíracích seznamech, kde jsou zobrazeny.

Můžete vytvořit pravidla, která se vztahují na každou úroveň závažnosti, kterou vytvoříte. Další informace o tom, jak přiřadit tato pravidla, najdete v další části.

## <a name="engineering-change-severity-rule-sets"></a>Sady pravidel závažnosti technických změn

Sady pravidel závažnosti technické změny použijete k vytvoření skupiny pravidel, kterou můžete použít k automatickému výpočtu závažnosti pořadí změn na základě typu změn v ovlivněných produktech. Chcete-li použít pravidla závažnosti, otevřete stránku **Parametry řízení technických změn** a nastavte hodnotu v poli **Pravidlo závažnosti** na *Vypočítat* nebo *Vypočítat automaticky*.

Když systém vyhodnotí závažnost, zpracuje pravidla v pořadí, v jakém se zobrazí na stránce, shora dolů. Aby bylo možné pravidlo vybrat a nastavit jeho prioritu, musí být splněna všechna pravidla v sadě pravidel.

Chcete-li nastavit pravidla, která platí pro každou úroveň závažnosti změny, kterou jste definovali, přejděte na **Řízení technických změn \> Založit \> Řízení technických změn \> Sady pravidel závažnosti technické změny**. Potom proveďte jeden z následujících kroků.

- Chcete-li vytvořit novou sadu pravidel, vyberte **Nová** v podokně akcí a poté nastavte pole, jak je popsáno dále v této části.
- Chcete-li upravit existující sadu pravidel, vyberte ji v podokně seznamu, zvolte **Upravit** v podokně akcí a poté nastavte pole, jak je popsáno dále v této části.
- Chcete-li odstranit existující sadu pravidel, vyberte ji v podokně seznamu a poté v podokně akcí vyberte **Odstranit**.
- Chcete-li změnit uspořádání seznamu sady pravidel, vyberte sadu pravidel v podokně seznamu a poté použijte tlačítka **Nahoru** a **Dolů** v podokně akcí pro její přemístění.

U každé sady pravidel je třeba nastavit následující pole:

- **Závažnost** - Vyberte úroveň závažnosti pro nastavení pravidel. Stránku **Závažnosti technických změn** použijete k vytvoření a pojmenování úrovní. (Další informace naleznete v předchozí části.)

Použijte tlačítka na pevné záložce **Pravidla** pro přidání nebo odebrání pravidla pro aktuální nastavení závažnosti. Každé pravidlo má pole **Pravidlo** a pole **Název**. Pravidla stanoví systém a označují typy změn, které produkt může mít. Název indikuje typ změny.
