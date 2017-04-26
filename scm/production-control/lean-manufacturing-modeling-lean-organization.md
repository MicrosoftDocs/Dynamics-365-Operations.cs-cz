---
title: "Modelování štíhlé organizace"
description: "Tento článek obsahuje informace o klíčových konceptech pro modelování úsporné organizace."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-02-24 15 - 08 - 43
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LeanProductionFlow, PlanActivity
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53141
ms.assetid: 4f272f2f-ec2c-4b0d-a652-00a63b719b9e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 536b20d5c4c2030800df25d0d227deaac386aee5
ms.lasthandoff: 03/29/2017


---

# <a name="modeling-a-lean-organization"></a>Modelování štíhlé organizace

Tento článek obsahuje informace o klíčových konceptech pro modelování úsporné organizace. 

Obvykle je scénář lean manufacturingu více než kolekce nesouvisejících kanbanových pravidel nebo zásad dodávek materiálu. Tok materiálu a produktů v rámci pracovních buněk a umístění pro určitou výrobu nebo scénář dodávky lze popsat jako sekvenci nebo malou síť aktivit procesu nebo převodu. Tato sekvence nebo na síti je označována jako výrobní tok.

## <a name="production-flows-in-lean-manufacturing"></a>Výrobní toky v lean manufacturingu
Ve scénářích výroby založených na výrobních zakázkách je materiálu vydáván konkrétní výrobní zakázce. Během sekvence operací založených na kusovníku (BOM) a postupech, jsou produkty vytvořeny a nakonec přijímány v zadaném umístění. Doba propustnosti výrobních zakázek se liší od minut po týdny. Všechny související náklady, materiál a práce jsou shromážděny ve výrobní zakázce. Ke snížení doby realizace dodávky a nadbytečných zásob mezi pracovními středisky, které jsou způsobené výrobními dávkami, zavádí lean manufacturing doplnění kanbanu a supermarkety ve výrobě a doplnění skladu. Tyto prvky obvykle naruší výrobu částečně nezávislých kanbanových cyklů. Doplnění kanbanu pro polotovar již není aktivováno objednávkou hotového výrobku. Chcete-li znovu vytvořit kontext výroby a nákladů pro různé scénáře kanbanu navržených v aplikaci Microsoft Dynamics AX, výrobní toky na základě aktivity jsou vkládány jako základní stavební prvky lean manufacturingu. Všechna kanbanová pravidla naleznete v této předdefinované struktuře. Model založený na aktivitách podporuje širší škálu scénářů, než tomu bylo v předchozích verzích Lean manufacturingu aplikace Dynamics AX. Avšak tento model nezvyšuje náročnost pro dílenské pracovníky, protože všechny scénáře používají stejné uživatelské rozhraní založené na aktivitách.

## <a name="semifinished-products-nonbom-levels"></a>Semifinished produkty (nonBOM úrovní)
Lean manufacturing pro aplikaci Dynamics AX integruje kanbany pro produkty na skladě a polotovary v jednom rámci, tudíž nabízí ve všech případech sjednocené uživatelské prostředí. Díky této architektuře není třeba zavádět další úrovně kusovníku, aby bylo možné použít kanbany pro polotovary. Tato architektura také umožňuje omezit skladové transakce na minimum.

## <a name="products-and-material-in-work-in-progress"></a>Produkty a materiál u nedokončené výroby
Omezení velikosti dávky na ideální stav jednoho kusu toku lean manufacturingu může způsobit dramatické zvýšení skladových transakcí, pokud každý proces výdeje nebo registrace kanban způsobí transakce pro spotřebované položky. Architektura výrobního toku umožňuje přenos materiálu na výrobní tok společně s kanbany odběru ve velikostech manipulační jednotky pro skladování nebo přepravu. Hodnota vydaného materiálu je přičtena k účtu NV souvisejícímu s výrobním tokem. Toto chování je podobné chování pro materiál vydaný pro výrobní zakázku. Totéž lze použít pro polotovary a produkty. Pokud tyto produkty nejsou vytvořeny, převedeny nebo spotřebovány v rámci výrobního toku, skladové transakce jsou volitelné. Jakmile jsou produkty zaúčtovány do zásob, účet NV pro výrobní tok se sníží odečtením souvisejících standardních nákladů.

## <a name="value-streams-and-value-stream-mapping"></a>Hodnotové proudy a mapování hodnotových proudů
Architektura lean manufacturingu pro aplikaci Dynamics AX je inspirovaná pěti štíhlými zásadami formulovanými autory Womack a Jones: hodnota pro odběratele, hodnotový proud, tok, vyžádání a jakost. Jednou schválenou metodou pro implementaci řešení lean manufacturingu ve fyzickém světě výroby je mapování hodnotových proudů. Tato metoda byl představena Rotherem a Shookem v jejich publikaci "Learning to See" v institutu Lean Manufacturing. Hodnotový proud budoucího stavu může být modelován v aplikaci Dynamics AX jako verze výrobního toku. Všechny procesy hodnotového proudu jsou modelovány jako aktivity procesu. Pohyby nebo převody umožňují modelování jako aktivity převodu, pokud stav převodu musí být registrován nebo pokud je požadována integrace do výdeje zásob nebo konsolidovaných dodávek. Samotný hodnotový proud je modelován jako provozní jednotka v aplikaci Dynamics AX. Proto lze hodnotový proud použít jako finanční dimenzi.

## <a name="costing-for-lean-manufacturing-based-on-the-production-flow"></a>Výpočet nákladů pro lean manufacturing podle výrobního toku
Periodická konsolidace nákladů pro výrobní tok vyrovnává související účet NV a umožňuje určení odchylky pro produkty poskytnuté výrobním tokem.

## <a name="continuous-improvement"></a>Souvislá zlepšování
Pro lepší podporu souvislého zlepšování, jsou implementovány výrobní toky v aktuálně platné verzi. Proto stávající verzi výrobního toku společně se všemi souvisejícími kanbanovými pravidly lze zkopírovat do budoucí verze výrobního toku. Navíc výrobní tok budoucího stavu lze modelovat předtím, než bude ověřen a aktivován pro výrobu. Existující kanbany ze starších verzí výrobního toku jsou automaticky přiřazeny k nové verzi, což zajišťuje bezproblémový tok materiálu k datu převodu i po něm.

## <a name="simplicity"></a>Jednoduchost
K provedení pro Dynamics AX Lean manufacturing jsme volba výrobní tok a aktivity přístupu umožňující výrobu jednoduché i složité scénáře v jednom škálovatelná architektura modelovat. Bližší pohled na koncept aktivity odhalí nové jednoduché pro uživatele, kteří ji potřebují: dílny a pracovníky logistiky. Vykazování prací na základě neaktivity namísto skladových transakcí, přesune sjednocené uživatelské rozhraní pro všechny varianty lean manufacturingu složitost obchodu z uživatelského rozhraní tam, kam patří: výrobní tok jako základní stavební prvek lean manufacturingu..


