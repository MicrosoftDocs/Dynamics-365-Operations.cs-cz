---
title: "Rozpad verze kusovníku"
description: "Tento článek popisuje scénář hlavního plánování, který zahrnuje rozpad verze kusovníku."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 6461a07f8c8f02f584e5ef70b21ebaf04f29b57b
ms.lasthandoff: 03/31/2017


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



