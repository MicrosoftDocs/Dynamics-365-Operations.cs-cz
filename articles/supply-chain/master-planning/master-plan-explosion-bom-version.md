---
title: "Rozpad verze kusovníku"
description: "Tento článek popisuje scénář hlavního plánování, který zahrnuje rozpad verze kusovníku."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f8c633e09103c45aff5614270a94a3bfe4fc5e20
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="explosion-of-a-bom-version"></a>Rozpad verze kusovníku

[!include[banner](../includes/banner.md)]


Tento článek popisuje scénář hlavního plánování, který zahrnuje rozpad verze kusovníku.

Rozpad poptávky verze kusovníku vytvoří poptávku pro každou řádkovou položku kusovníku na konkrétním pracovišti a v určitém skladu (pokud taková možnost existuje). Kusovník určitého pracoviště může mít pro každý řádek definovaný konkrétní sklad. Nastavení dimenzí položky na každém řádku kusovníku dále určuje, zda je zadání skladu povinné. Výsledná poptávka pro každý řádek kusovníku se potom stane výchozím bodem pro další rozpad poptávky. Pro tento scénář hlavního plánování platí následující podmínky:

-   Dimenze pracoviště je povinná a v případě transakce poptávky musí být zadaná.
-   Dimenze pracoviště je konzistentní. To znamená, že pracoviště v poptávce nižší úrovně je stejné, jako pracoviště v původní transakci poptávky.

Následující obrázek ilustruje, jakým způsobem postupuje rozpad poptávky při hlavním plánování. ![Rozpad poptávky pomocí verze kusovníku](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="see-also"></a>Viz také
--------

[Hlavní plánování – jak se určuje verze kusovníku](master-plan-bom-version-determined.md)

[Hlavní plánování a funkce více pracovišť](master-plan-multisite-functionality.md)




