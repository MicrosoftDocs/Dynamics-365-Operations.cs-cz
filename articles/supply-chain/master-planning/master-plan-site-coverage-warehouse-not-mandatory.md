---
title: Hlavní plánování pro disponibilitu pracoviště, sklad není povinný
description: Toto téma popisuje, jak je plánována položka, která pro pokrytí nastavenou dimenzí pracoviště.
author: roxanadiaconu
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
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3650eaf11ecf75c39bfaa5ce4cce7fe03b861c60df72a898cfd7dfc57f062470
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768112"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a>Hlavní plánování pro disponibilitu pracoviště, sklad není povinný

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak je plánována položka, která má pro pokrytí nastavenou dimenzi pracoviště.

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

[Přehled hlavního plánování a funkce více pracovišť](master-plan-multisite-functionality.md)

[Hlavní plánování pro disponibilitu pracoviště a skladu, sklad je povinný](master-plan-site-coverage-warehouse-mandatory.md)

[Hlavní plánování pro disponibilitu pracoviště, povinný sklad](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Hlavní plánování pro disponibilitu pracoviště, sklad není povinný](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Určení verze kusovníku](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]