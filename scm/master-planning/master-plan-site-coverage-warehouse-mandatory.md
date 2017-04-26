---
title: "Hlavní plánování pro pokrytí serveru povinný sklad"
description: "Toto téma popisuje, jak je plánována položka, která má pracoviště jako dimenzi disponibility. Sklad je povinná dimenze."
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
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 4c595aa9809e37ba752b76f559ef909c071eb303
ms.lasthandoff: 03/31/2017


---

# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a>Hlavní plánování pro pokrytí serveru povinný sklad

[!include[banner](../includes/banner.md)]


Toto téma popisuje, jak je plánována položka, která má pracoviště jako dimenzi disponibility. Sklad je povinná dimenze.

Pro tento scénář hlavního plánování platí následující podmínky:

-   Dimenze pracoviště je nastavena jako povinná a musí být zadána v transakci poptávky. Toto nastavení nelze změnit.
-   Skladová dimenze je nastavena jako povinná a musí být zadána v transakci poptávky.
-   Dimenze pracovišť je nastavená pro plánování disponibility. Pro disponibilitu lze nastavit také další dimenze. Ty však nejsou ovlivněny funkcí více pracovišť.
-   Skladová dimenze není nastavena pro plánování disponibility. Nabídka a poptávka se tedy vyhodnocuje souhrnně podle pracovišť a případně podle dalších dimenzí nastavených pro plánování disponibility.

Následující obrázek ilustruje postup hlavního plánování. V obrázku jsou odkazy na následující parametry (v popisu je informace, kde je najdete):
-   Je definovaná disponibilita položky. Klepněte na tlačítko **řízení informací o produktech &gt;produkty&gt; uvolněných produktů**. Vyberte položku a potom klepněte na tlačítko **plán &gt;Disponibilita položky**.
-   Pro sklad jsou definovány vztahy doplnění. Klepněte na tlačítko **řízení zásob &gt;nastavení &gt;rozdělení zásob &gt;sklady**. Na kartě **Hlavní plánování** se podívejte do skupiny polí **Hlavní sklad**.
-   Výchozí typ objednávky je nastaven na možnost Výroba, Nákupní objednávka nebo Kanban. Klepněte na tlačítko **řízení informací o produktech &gt;produkty&gt; uvolněných produktů**. Vyberte položku a potom klepněte na tlačítko **plán &gt;výchozí nastavení objednávky**. Ve formuláři **Výchozí nastavení objednávky** zkontrolujte pole **Výchozí typ objednávky**.

![Požadavek na disponibilitu skladu pracoviště je povinný](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="see-also"></a>Viz také
--------

[Master planning and multisite functionality](master-plan-multisite-functionality.md)

[Hlavní plánování – disponibilita pracoviště a skladu, sklad povinný](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Hlavní plánování - webu disponibility. povinný sklad](master-plan-site-coverage-warehouse-mandatory.md)

[Hlavní plánování – disponibilita pracoviště a skladu, sklad není povinný](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Hlavní plánování – jak se určuje verze kusovníku](master-plan-bom-version-determined.md)




