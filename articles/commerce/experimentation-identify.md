---
title: Identifikace hypotézy a určení metriky experimentu
description: Toto téma popisuje, jak identifikovat hypotézu a metriku úspěšnosti experimentu, který spouštíte na webu elektronického obchodu v Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 99642861d69b7545f03c6ed2c2650eadeb377534
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930154"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a>Identifikace hypotézy a určení metriky úspěšnosti experimentu
První fáze životního cyklu experimentování zahrnuje identifikování hypotézy experimentu a určení metriky, kterou budete sledovat k vyhodnocení úspěšnosti. Následující schéma znázorňuje všechny kroky, které zahrnuje [nastavení a spuštění experimentu](experimentation-overview.md) na webu elektronického obchodu v Dynamics 365 Commerce. Další kroky jsou popsány v samostatných tématech. 

[ ![Cesta uživatele experimentováním – identifikace](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)

Hypotéza je tvrzení, ve kterém predikujete výsledek experimentu. Do definování hypotézy vstupuje mnoho faktorů, například výzkum chování uživatelů a data webu, která jste shromáždili. Pomocí hypotézy definujete předpoklad nebo teorii, které chcete ověřit experimentem. Příkladem hypotézy pro váš experiment může být tvrzení, že „ *obrázek bílého trička na mé domovské stránce bude mít v letních měsících více kliknutí než tmavomodrý svetr, protože lidé chtějí v létě nosit něco lehkého a světlého.* ” V takovém případě vytvoříte varianty, které budou zahrnovat bílé tričko a tmavomodrý svetr, a publikujete obě najednou.

K ověření hypotézy by měl být úspěch nebo neúspěch experimentu přímo svázán s akcemi uživatelů – například jestli uživatel webu klikne na určitý odkaz nebo tlačítko. Tyto akce musí odpovídat událostem, které budou hlášeny službě třetí strany, která experiment sleduje. V průběhu času se bude procento uživatelů, kteří provedou danou akci, načítat jako metrika, kterou můžete použít ke generování sestav a provádění analýz. V článku [Události komponent Commerce pro diagnostiku a řešení potíží](dev-itpro/retail-component-events-diagnostics-troubleshooting.md) se můžete podívat na všechny dostupné události a atributy.

## <a name="previous-step"></a>Předchozí krok
[Experimentování v Dynamics 365 Commerce](experimentation-overview.md)


## <a name="next-step"></a>Další krok
[Nastavení experimentu](experimentation-setup.md)
