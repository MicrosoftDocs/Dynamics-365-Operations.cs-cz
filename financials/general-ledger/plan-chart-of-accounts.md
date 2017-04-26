---
title: "Plánování účtové osnovy"
description: "V tomto článku jsou informace, které vám pomohou naplánovat účtové osnovy pro vaši organizaci."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: 34425ecd4b78a134c92a2282576d0d7967d870b3
ms.lasthandoff: 03/31/2017


---

# <a name="plan-your-chart-of-accounts"></a>Plánování účtové osnovy

[!include[banner](../includes/banner.md)]


V tomto článku jsou informace, které vám pomohou naplánovat účtové osnovy pro vaši organizaci.

Pro sledování a správu finančních informací v organizaci můžete nastavit účtovou osnovu. Účtová osnova je sada účtů, které definují finanční rámec. Pokud chcete dále sledovat transakce v těchto účtech, můžete přidat segmenty označované jako finanční dimenze. Účet výdajů může například zahrnovat finanční dimenze s názvem Oddělení, Nákladové středisko a Účel. Pravidla definovaná uživatelem, která se označují jako účetní struktury a rozšířená pravidla, určují způsob, jakým se finanční dimenze přiřazují k hlavním účtům a ostatním finančním dimenzím a jakým se zadávají transakce pro účetní strukturu. 

Účtová osnova představuje strukturovaný seznam účtů hlavní knihy právnické osoby. Tento seznam se používá pro přípravu finančního vykazování pro úřady a majitele. Účty se seskupují do typů účtů a obecných kategorií. Nejobecnější úroveň účty třídí jako výnosy a náklady (účty provozních nákladů) a aktiva a pasiva (rozvahový účet). 

Účtovou osnovu mohou sdílet a používat všechny právnické osoby v rámci organizace. Účtové osnovy, který používá právní subjekt je definováno na **knihy** stránky. 

Zde je několik faktorů, které je třeba brát v potaz při plánování struktury účtové osnovy ve vaší organizaci:

-   požadavky na výkazy v zemi nebo oblasti, ve které má společnost sídlo,
-   požadavky na výkazy vaší právnické osoby,
-   úroveň podrobností, kterou požadují jak externí organizace, tak i vaše společnost.

Na stránce **Účtová osnova** vytvořte účtovou osnovu. Hlavní účty lze vytvořit na stránce **Účtové osnovy** nebo **Hlavní účty**. V hlavních účtech nepoužívejte zvláštní znaky, které se používají jako oddělovače účtové osnovy. Pokud použijete zvláštní znak, který se shoduje s oddělovačem účtové osnovy, můžete zaznamenat nestabilitu nebo nutnost používat vyhledávání či plovoucí panel pokaždé, když zadáváte kombinací účtů a dimenzí. 

Je vhodné propojit hlavní účty s kategoriemi hlavních účtů, abyste mohli využít výhody výchozích finančních sestav bez nutnosti provádět změny. Můžete proto rychleji a snáze navrhovat a spravovat sestavy. 

Pomocí stránky **Konfigurovat účetní struktury** vytvořte účetní struktury. Účetní struktury definují platné kombinace. Kombinace, společně s hlavními účty, tvoří účtové osnovy. 

**Legal entity overrides** 

Všechny hlavní účty, které jsou platné pro všechny právnické osoby a některé může být pouze relevantní pro určité časové období. V tomto případě lze část Přepisy právnických osob použít k určení, u kterých společností by mělo být použití hlavního účtu pozastaveno, kdo je vlastníkem a časové období aktivity dimenze. Přepisy na sdílené úrovni nemohou být více omezující než přepisy na úrovni právnické osoby.

Další informace naleznete v tématu [finanční dimenze](financial-dimensions.md).




