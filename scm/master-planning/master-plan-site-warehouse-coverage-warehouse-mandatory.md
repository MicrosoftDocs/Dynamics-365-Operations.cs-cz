---
title: "Hlavní plánování disponibility pracoviště a sklad, sklad povinné"
description: "Toto téma popisuje, jak je plánována položka, která má pracoviště a sklad, jako dimenze disponibility. Dimenze skladu je povinná."
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
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: a0931d88f84544160803e42466575c02f47588a4
ms.lasthandoff: 03/31/2017


---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a>Hlavní plánování disponibility pracoviště a sklad, sklad povinné

[!include[banner](../includes/banner.md)]


Toto téma popisuje, jak je plánována položka, která má pracoviště a sklad, jako dimenze disponibility. Dimenze skladu je povinná.

Pro tento scénář hlavního plánování platí následující podmínky:

-   Dimenze pracoviště je nastavena jako povinná a musí být zadána v transakci poptávky.
-   Skladová dimenze je nastavena jako povinná a musí být zadána v transakci poptávky.
-   Dimenze pracoviště a skladová dimenze není nastavena pro plánování disponibility. Pro disponibilitu lze nastavit také další dimenze. Ty však nejsou ovlivněny funkcí více pracovišť.

Následující obrázek ilustruje postup hlavního plánování. V obrázku jsou odkazy na následující parametry (v popisu je informace, kde je najdete):
-   The warehouse is set to **Manual**. Klepněte na tlačítko **řízení zásob &gt;nastavení &gt;rozdělení zásob &gt;sklady**. Na pevné záložce **Hlavní plánování** zkontrolujte pole **Ruční**.
-   Je definovaná disponibilita položky. Klepněte na tlačítko **řízení informací o produktech &gt;produkty&gt; uvolněných produktů**. Vyberte položku a pak v podokně akcí na **plán** karta, klepněte na tlačítko **Disponibilita položky**.
-   Pro sklad jsou definovány vztahy doplnění. Klepněte na tlačítko **řízení zásob &gt;nastavení &gt;rozdělení zásob &gt;sklady**. Na pevné záložce **Hlavní plánování** zkontrolujte skupinu polí **Hlavní sklad**.
-   Výchozí typ objednávky je nastaven na možnost Výroba, Nákupní objednávka nebo Kanban. Klepněte na tlačítko **řízení informací o produktech &gt;produkty&gt; uvolněných produktů**. Vyberte položku a pak v podokně akcí na **plán** karta, klepněte na tlačítko **výchozí nastavení objednávky**. Ve formuláři **Výchozí nastavení objednávky** zkontrolujte pole **Výchozí typ objednávky**.

![Poptávka krytí pracoviště a sklad, co je povinné](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="see-also"></a>Viz také
--------

[Master planning and multisite functionality](master-plan-multisite-functionality.md)

[Hlavní plánování – disponibilita pracoviště, sklad povinný](master-plan-site-coverage-warehouse-mandatory.md)

[Hlavní plánování – disponibilita pracoviště, sklad není povinný](master-plan-site-coverage-warehouse-not-mandatory.md)

[Hlavní plánování – disponibilita pracoviště a skladu, sklad není povinný](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Hlavní plánování – jak se určuje verze kusovníku](master-plan-bom-version-determined.md)




