---
title: Modelování úsporné organizace
description: Tento článek obsahuje informace o klíčových konceptech pro modelování úsporné organizace.
author: cvocph
ms.date: 09/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, KanbanFlowSelection, KanbanFlow
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53141
ms.assetid: 4f272f2f-ec2c-4b0d-a652-00a63b719b9e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 476dfd6be55ce484cb9bc101ac27dc6181f3c010
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910370"
---
# <a name="modeling-a-lean-organization"></a>Modelování úsporné organizace

[!include [banner](../includes/banner.md)]

Tento článek obsahuje informace o klíčových konceptech pro modelování úsporné organizace. 

Obvykle je scénář lean manufacturingu více než kolekce nesouvisejících kanbanových pravidel nebo zásad dodávek materiálu. Tok materiálu a produktů v rámci pracovních buněk a umístění pro určitou výrobu nebo scénář dodávky lze popsat jako sekvenci nebo malou síť aktivit procesu nebo převodu. Tato sekvence nebo na síti je označována jako výrobní tok.

## <a name="production-flows-in-lean-manufacturing"></a>Výrobní toky v lean manufacturingu
Ve scénářích výroby založených na výrobních zakázkách je materiálu vydáván konkrétní výrobní zakázce. Během sekvence operací založených na kusovníku (BOM) a postupech, jsou produkty vytvořeny a nakonec přijímány v zadaném umístění. Doba propustnosti výrobních zakázek se liší od minut po týdny. Všechny související náklady, materiál a práce jsou shromážděny ve výrobní zakázce. 

Ke snížení doby realizace dodávky a nadbytečných zásob mezi pracovními středisky, které jsou způsobené výrobními dávkami, zavádí lean manufacturing doplnění kanbanu a supermarkety ve výrobě a doplnění skladu. Tyto prvky obvykle naruší výrobu částečně nezávislých kanbanových cyklů. Doplnění kanbanu pro polotovar již není aktivováno objednávkou hotového výrobku. 

Chcete-li znovu vytvořit kontext výroby a nákladů pro různé scénáře kanbanu navržených, výrobní toky na základě aktivity jsou vkládány jako základní stavební prvky lean manufacturingu. Všechna kanbanová pravidla naleznete v této předdefinované struktuře. Model založený na aktivitách podporuje nastavení široké škály scénářů. Avšak tento model nezvyšuje náročnost pro dílenské pracovníky, protože všechny scénáře používají stejné uživatelské rozhraní založené na aktivitách.

## <a name="semi-finished-products-non-bom-levels"></a>Polotovary (bez úrovní kusovníku)
Lean manufacturing integruje kanbany pro produkty na skladě a polotovary v jednom rámci, tudíž nabízí ve všech případech sjednocené uživatelské prostředí. Díky této architektuře není třeba zavádět další úrovně kusovníku, aby bylo možné použít kanbany pro polotovary. Tato architektura také umožňuje omezit skladové transakce na minimum.

## <a name="products-and-material-in-work-in-progress"></a>Produkty a materiál u nedokončené výroby
Omezení velikosti dávky na ideální stav jednoho kusu toku lean manufacturingu může způsobit dramatické zvýšení skladových transakcí, pokud každý proces výdeje nebo registrace kanban způsobí transakce pro spotřebované položky. Architektura výrobního toku umožňuje přenos materiálu na výrobní tok společně s kanbany odběru ve velikostech manipulační jednotky pro skladování nebo přepravu. Hodnota vydaného materiálu je přičtena k účtu NV souvisejícímu s výrobním tokem. Toto chování je podobné chování pro materiál vydaný pro výrobní zakázku. Totéž lze použít pro polotovary a produkty. Pokud tyto produkty nejsou vytvořeny, převedeny nebo spotřebovány v rámci výrobního toku, skladové transakce jsou volitelné. Jakmile jsou produkty zaúčtovány do zásob, účet NV pro výrobní tok se sníží odečtením souvisejících standardních nákladů.

## <a name="value-streams-and-value-stream-mapping"></a>Hodnotové proudy a mapování hodnotových proudů
Architektura lean manufacturingu je inspirovaná pěti štíhlými zásadami formulovanými autory Womack a Jones: hodnota pro odběratele, hodnotový proud, tok, vyžádání a jakost. Jednou schválenou metodou pro implementaci řešení lean manufacturingu ve fyzickém světě výroby je mapování hodnotových proudů. Tato metoda byl představena Rotherem a Shookem v jejich publikaci "Learning to See" v institutu Lean Manufacturing. 

Hodnotový proud budoucího stavu může být modelován v aplikaci Dynamics AX jako verze výrobního toku. Všechny procesy hodnotového proudu jsou modelovány jako aktivity procesu. Pohyby nebo převody umožňují modelování jako aktivity převodu, pokud stav převodu musí být registrován nebo pokud je požadována integrace do výdeje zásob nebo konsolidovaných dodávek. 

Samotný hodnotový proud je modelován jako provozní jednotka. Proto lze hodnotový proud použít jako finanční dimenzi.

Další informace o provozních jednotkách naleznete v tématu [Vytvoření provozní jednotky](../../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md).

## <a name="costing-for-lean-manufacturing-based-on-the-production-flow"></a>Výpočet nákladů pro lean manufacturing podle výrobního toku
Periodická konsolidace nákladů pro výrobní tok vyrovnává související účet NV a umožňuje určení odchylky pro produkty poskytnuté výrobním tokem.

## <a name="continuous-improvement"></a>Souvislá zlepšování
Pro lepší podporu souvislého zlepšování, jsou implementovány výrobní toky v aktuálně platné verzi. Proto stávající verzi výrobního toku společně se všemi souvisejícími kanbanovými pravidly lze zkopírovat do budoucí verze výrobního toku. Navíc výrobní tok budoucího stavu lze modelovat předtím, než bude ověřen a aktivován pro výrobu. Existující kanbany ze starších verzí výrobního toku jsou automaticky přiřazeny k nové verzi, což zajišťuje bezproblémový tok materiálu k datu převodu i po něm.

## <a name="simplicity"></a>Jednoduchost
K nasazení Lean Manufacturingu jsme zvolili přístup k výrobnímu toku a aktivitám, který umožňuje modelování jednoduchých a složitých scénářů výroby do jedné škálovatelné architektury. Podrobnější pohled na koncept aktivity odhaluje nové zjednodušení pro uživatele, kteří to opravdu potřebují: dílenské vedoucí a zaměstnance logistiky. Vykazování prací na základě neaktivity namísto skladových transakcí, přesune sjednocené uživatelské rozhraní pro všechny varianty lean manufacturingu složitost obchodu z uživatelského rozhraní tam, kam patří: výrobní tok jako základní stavební prvek lean manufacturingu..





[!INCLUDE[footer-include](../../includes/footer-banner.md)]