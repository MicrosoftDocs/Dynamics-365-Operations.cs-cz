---
title: Plánování účetní osnovy
description: V tomto tématu jsou informace, které vám pomohou naplánovat účtové osnovy pro vaši organizaci.
author: aprilolson
ms.date: 04/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0734276a736cfdb91ec3a129c83dae1c0a6d3955
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722457"
---
# <a name="plan-your-chart-of-accounts"></a>Plánování účetní osnovy

[!include [banner](../includes/banner.md)]

V tomto tématu jsou informace, které vám pomohou naplánovat účtové osnovy pro vaši organizaci.

Pro sledování a správu finančních informací v organizaci můžete nastavit účtovou osnovu. Účtová osnova je sada účtů, které definují finanční rámec. Pokud chcete dále sledovat transakce na těchto účtech, můžete přidat segmenty. Tyto segmenty se označují jako finanční dimenze. Účet výdajů může například zahrnovat finanční dimenze s názvem Oddělení, Nákladové středisko a Účel. Pravidla definovaná uživatelem určují způsob, jakým se finanční dimenze přiřazují k hlavním účtům a ostatním finančním dimenzím a jakým se zadávají transakce pro účetní strukturu. Tato pravidla definovaná uživatelem se nazývají účetní struktury a pokročilá pravidla.

Účtová osnova představuje strukturovaný seznam účtů hlavní knihy právnické osoby. Tento seznam se používá pro přípravu finančního vykazování pro úřady a majitele. Účty se nejprve seskupují do typů účtů a obecných kategorií. Nejobecnější úroveň účty třídí jako výnosy a náklady (účty provozních nákladů) a aktiva a pasiva (rozvahový účet).

Účtovou osnovu mohou sdílet a používat všechny právnické osoby v rámci organizace. Účtové osnovy, které používá právnická osoba, jsou definovány na stránce **Kniha**.

Zde je několik faktorů, které je třeba brát v potaz při plánování struktury účtové osnovy ve vaší organizaci:

- požadavky na výkazy v zemi nebo oblasti, ve které má společnost sídlo,
- požadavky na výkazy vaší právnické osoby,
- úroveň podrobností, kterou požadují jak externí organizace, tak i vaše společnost.

Na stránce **Účtová osnova** vytvořte účtovou osnovu. Hlavní účty lze vytvořit na stránce **Účtové osnovy** nebo **Hlavní účty**. V hlavních účtech nepoužívejte zvláštní znaky, které se používají jako oddělovače účtové osnovy. V opačném případě může dojít k nestabilitě nebo je třeba vždy použít vyhledávání, resp. při zadávání kombinací účtů a dimenzí. Další informace naleznete v tématu [Vytvoření hlavního účtu](tasks/create-main-account.md).

> [!NOTE]
> V aplikaci Dynamics 365 for Finance and Operations verze 8.0 (duben 2018) můžete změnit oddělovač účtové osnovy ze stránky **Parametry hlavní knihy**.

Je vhodné propojit hlavní účty s kategoriemi hlavních účtů, abyste mohli využít výhody výchozích finančních sestav bez nutnosti provádět změny. Můžete proto rychleji a snáze navrhovat a spravovat sestavy.

Pomocí stránky **Konfigurovat účetní struktury** vytvořte účetní struktury. Účetní struktury definují platné kombinace. Tyto kombinace, společně s hlavními účty, tvoří účtové osnovy. Další informace naleznete v tématu [Vytvoření struktur účtu](tasks/create-account-structures.md).

**Přepisy právnických osob**

Ne všechny hlavní účty platí pro všechny právnické osoby a některé mohou být relevantní pouze pro určité časové období. V tomto případě lze pomocí části **Přepisy právnických osob** určit společnosti, u kterých má být použití hlavního účtu pozastaveno, kdo je vlastníkem a období aktivity dimenze. Přepisy na sdílené úrovni nemohou být více omezující než přepisy na úrovni právnické osoby.

Další informace naleznete v následujících tématech:

- [Finanční dimenze](financial-dimensions.md)
- [Vytvoření a přiřazení struktur rozšířeného pravidla](tasks/create-assign-advanced-rule-structures.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
