---
title: Hlavní plánování pro disponibilitu pracoviště, sklad není povinný
description: Tento článek popisuje, jak je plánována položka, která pro pokrytí nastavenou dimenzí pracoviště.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b03bd1970aa7a2f3276186a0a9f8c2cd2880956
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741142"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a>Hlavní plánování pro disponibilitu pracoviště, sklad není povinný

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak je plánována položka, která pro pokrytí nastavenou dimenzí pracoviště.

Pro tento scénář hlavního plánování platí následující podmínky:

-   Dimenze pracoviště je nastavena jako povinná a musí být zadána v transakci poptávky.
-   Dimenze skladu není povinná. Sklad může být znám, ale při výpočtu během hlavního plánování se nepoužije.
-   Dimenze pracovišť je nastavená pro plánování disponibility.
-   Skladová dimenze není nastavena pro plánování disponibility. Nabídka a poptávka se tedy vyhodnocuje souhrnně podle pracovišť a případně podle dalších dimenzí nastavených pro plánování disponibility.

Následující obrázek ilustruje postup hlavního plánování. V obrázku jsou odkazy na následující parametry (v popisu je informace, kde je najdete):
-   Je definovaná disponibilita položky. Klikněte na možnosti **Řízení informací o produktech &gt; Produkty&gt; Uvolněné produkty**. Vyberte položku a poté klikněte na volbu **Plán &gt; Disponibilita položky**.
-   Pro sklad jsou definovány vztahy doplnění. Klikněte postupně na možnosti **Řízení zásob &gt; Nastavení &gt; Rozdělení zásob &gt; Sklady**. Na kartě **Hlavní plánování** se podívejte do skupiny polí **Hlavní sklad**.
-   Výchozí typ objednávky je nastaven na výrobu, nákupní objednávky nebo kanban. Klikněte na možnosti **Řízení informací o produktech &gt; Produkty&gt; Uvolněné produkty**. Vyberte položku a poté klikněte na volbu **Plán &gt; Výchozí nastavení objednávky**. Ve formuláři **nastavení výchozí objednávky**, viz pole **typ výchozí objednávky**.

![Požadavek na disponibilitu skladu pracoviště není povinný.](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



## <a name="additional-resources"></a>Další prostředky

- [Přehled hlavního plánování a funkce více pracovišť](master-plan-multisite-functionality.md)
- [Hlavní plánování pro disponibilitu pracoviště a skladu, sklad je povinný](master-plan-site-coverage-warehouse-mandatory.md)
- [Hlavní plánování pro disponibilitu pracoviště, povinný sklad](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)
- [Hlavní plánování pro disponibilitu pracoviště, sklad není povinný](master-plan-site-warehouse-coverage-warehouse-mandatory.md)
- [Určení verze kusovníku](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]