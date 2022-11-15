---
title: Hlavní plánování pro disponibilitu pracoviště a skladu, sklad není povinný
description: Tento článek popisuje, jak je plánována položka, která má pracoviště a sklad, jako dimenze disponibility. Dimenze skladu není povinná.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4989a05f4647ac836b78692da7f63396dbef788
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741005"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a>Hlavní plánování pro disponibilitu pracoviště a skladu, sklad není povinný

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak je plánována položka, která má pracoviště a sklad, jako dimenze disponibility. Dimenze skladu není povinná.

Pro tento scénář hlavního plánování platí následující podmínky:

-   Dimenze pracoviště je nastavena jako povinná a musí být zadána v transakci poptávky. Toto nastavení nelze změnit.
-   Dimenze skladu není povinná. Sklad může být znám, ale při výpočtu během hlavního plánování se nepoužije.
-   Dimenze pracoviště a skladová dimenze není nastavena pro plánování disponibility. Pro disponibilitu lze nastavit také další dimenze. Ty však nejsou ovlivněny funkcí více pracovišť.

Následující obrázek ilustruje postup hlavního plánování. V obrázku jsou odkazy na následující parametry (v popisu je informace, kde je najdete):
-   Sklad je nastaven na možnost Ruční. Klikněte postupně na možnosti **Řízení zásob &gt; Nastavení &gt; Rozdělení zásob &gt; Sklady**. Na pevné záložce **Hlavní plánování** zkontrolujte pole **Ruční**.
-   Je definovaná disponibilita položky. Klikněte na možnosti **Řízení informací o produktech &gt; Produkty&gt; Uvolněné produkty**. Zvolte položku a poté v podokně akcí na kartě **Plán** klikněte na **Disponibilita položky**.
-   Pro sklad jsou definovány vztahy doplnění. Klikněte postupně na možnosti **Řízení zásob &gt; Nastavení &gt; Rozdělení zásob &gt; Sklady**. Na pevné záložce **Hlavní plánování** zkontrolujte skupinu polí **Hlavní sklad**.
-   Výchozí typ objednávky je nastaven na možnost Výroba, Nákupní objednávka nebo Kanban. Klikněte na možnosti **Řízení informací o produktech &gt; Produkty&gt; Uvolněné produkty**. Zvolte položku a poté v podokně akcí na kartě **Plán** klikněte na možnost **Výchozí nastavení objednávky**. Ve formuláři **Výchozí nastavení objednávky** zkontrolujte pole **Výchozí typ objednávky**.

![Požadavek na pracoviště a sklad, sklad není.](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)



## <a name="additional-resources"></a>Další prostředky

- [Přehled hlavního plánování a funkce více pracovišť](master-plan-multisite-functionality.md)
- [Hlavní plánování pro disponibilitu pracoviště, povinný sklad](master-plan-site-warehouse-coverage-warehouse-mandatory.md)
- [Hlavní plánování pro disponibilitu pracoviště a skladu, sklad je povinný](master-plan-site-coverage-warehouse-mandatory.md)
- [Hlavní plánování pro disponibilitu pracoviště a skladu, sklad není povinný](master-plan-site-coverage-warehouse-not-mandatory.md)
- [Určení verze kusovníku](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]