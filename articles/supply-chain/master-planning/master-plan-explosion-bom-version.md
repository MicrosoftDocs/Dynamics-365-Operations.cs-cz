---
title: Rozpad verze kusovníku
description: Tento článek popisuje scénář hlavního plánování, který zahrnuje rozpad verze kusovníku.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 380f8069a726e53084164a5ac1fc0a0a99c83590
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213738"
---
# <a name="explosion-of-a-bom-version"></a>Rozpad verze kusovníku

[!include [banner](../includes/banner.md)]

Tento článek popisuje scénář hlavního plánování, který zahrnuje rozpad verze kusovníku.

Rozpad poptávky verze kusovníku vytvoří poptávku pro každou řádkovou položku kusovníku na konkrétním pracovišti a v určitém skladu (pokud taková možnost existuje). Kusovník určitého pracoviště může mít pro každý řádek definovaný konkrétní sklad. Nastavení dimenzí položky na každém řádku kusovníku dále určuje, zda je zadání skladu povinné. Výsledná poptávka pro každý řádek kusovníku se potom stane výchozím bodem pro další rozpad poptávky. Pro tento scénář hlavního plánování platí následující podmínky:

-   Dimenze pracoviště je povinná a v případě transakce poptávky musí být zadaná.
-   Dimenze pracoviště je konzistentní. To znamená, že pracoviště v poptávce nižší úrovně je stejné, jako pracoviště v původní transakci poptávky.

Následující obrázek ilustruje, jakým způsobem postupuje rozpad poptávky při hlavním plánování. ![Rozpad poptávky pomocí verze kusovníku](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="additional-resources"></a>Další zdroje
--------

[Určení verze kusovníku](master-plan-bom-version-determined.md)

[Přehled hlavního plánování a funkce více pracovišť](master-plan-multisite-functionality.md)



