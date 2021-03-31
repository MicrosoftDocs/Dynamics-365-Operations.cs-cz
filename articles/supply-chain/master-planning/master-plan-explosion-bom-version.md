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
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 617d9c3f05f2db30ec075a07b54c4827e668c20e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220841"
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





[!INCLUDE[footer-include](../../includes/footer-banner.md)]