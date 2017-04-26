---
title: "Hlavní plánování pro pokrytí serveru, sklad není povinný"
description: "Toto téma popisuje, jak je plánována položka, která pro pokrytí nastavenou dimenzí pracoviště."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 28607f0fc8db99c9fc8e96b4514763b8cf589dd8
ms.lasthandoff: 03/31/2017


---

# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a>Hlavní plánování pro pokrytí serveru, sklad není povinný

[!include[banner](../includes/banner.md)]


Toto téma popisuje, jak je plánována položka, která pro pokrytí nastavenou dimenzí pracoviště.

Pro tento scénář hlavního plánování platí následující podmínky:

-   Dimenze pracoviště je nastavena jako povinná a musí být zadána v transakci poptávky.
-   Dimenze skladu není povinná. Sklad může být znám, ale při výpočtu během hlavního plánování se nepoužije.
-   Dimenze pracovišť je nastavená pro plánování disponibility.
-   Skladová dimenze není nastavena pro plánování disponibility. Nabídka a poptávka se tedy vyhodnocuje souhrnně podle pracovišť a případně podle dalších dimenzí nastavených pro plánování disponibility.

Následující obrázek ilustruje postup hlavního plánování. V obrázku jsou odkazy na následující parametry (v popisu je informace, kde je najdete):
-   Je definovaná disponibilita položky. Klepněte na tlačítko **řízení informací o produktech &gt;produkty&gt; uvolněných produktů**. Vyberte položku a potom klepněte na tlačítko **plán &gt;Disponibilita položky**.
-   Pro sklad jsou definovány vztahy doplnění. Klepněte na tlačítko **řízení zásob &gt;nastavení &gt;rozdělení zásob &gt;sklady**. Na kartě **Hlavní plánování** se podívejte do skupiny polí **Hlavní sklad**.
-   Výchozí typ objednávky je nastaven na výrobu, nákupní objednávky nebo kanban. Klepněte na tlačítko **řízení informací o produktech &gt;produkty&gt; uvolněných produktů**. Vyberte položku a potom klepněte na tlačítko **plán &gt;výchozí nastavení objednávky**. Ve formuláři **nastavení výchozí objednávky**, viz pole **typ výchozí objednávky**.

![Poptávka po webu disponibilní sklad není povinný](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="see-also"></a>Viz také
--------

[Master planning and multisite functionality](master-plan-multisite-functionality.md)

[Hlavní plánování – disponibilita pracoviště, sklad povinný](master-plan-site-coverage-warehouse-mandatory.md)

[Hlavní plánování – disponibilita pracoviště a skladu, sklad není povinný](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Hlavní plánování – disponibilita pracoviště a skladu, sklad povinný](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Hlavní plánování - jak je určena verze Kusovníku](master-plan-bom-version-determined.md)




