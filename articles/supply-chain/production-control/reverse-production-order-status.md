---
title: "Vrácení stavu výrobní zakázky"
description: "Toto téma popisuje způsob stornování stavu výrobní zakázky."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParmStatusDecrease
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 70131
ms.assetid: b1e0df43-b388-4326-8fb7-501f30c89776
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4761e44b6bbc93ebf4a395948f42c2a73013ecb9
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="reverse-the-production-order-status"></a>Vrácení stavu výrobní zakázky

[!include [banner](../includes/banner.md)]

Toto téma popisuje způsob stornování stavu výrobní zakázky. 

Při stornování stavu výrobní zakázky se vrátí zakázku včetně všech operací připojených k postupům do předchozího kroku výrobního cyklu. Například výrobní zakázka má stav **Plánováno**, a vy změníte stav zpět na **Vytvořeno**. V tomto případě musí systém nejprve stav změnit na **Odhad**, což je stav, který okamžitě předchází stavu **Plánováno**. Stav pak můžete změnit na stav, který chcete, **Vytvořeno**. **Poznámka:** Pokud vaše zakázka dosáhla stavu **Hlášeno jako dokončené**, můžete ji stále vrátit do dřívějšího stavu. Je třeba znovu spustit odhad a plánování operací, plánování úlohy, nebo oba typy plánování a aktualizovat informace na zakázce. Důvodem nutnosti tohoto kroku je, že veškeré rezervace spotřeby zbývajících položek a spotřeby provozních prostředků musí být rovněž vynulovány. Zbývající část tohoto článku vysvětluje, co se děje po stornování stavu výrobní zakázky následujícími způsoby:

-   Ze stavu **Odhadnuto** do stavu **Vytvořeno**
-   Ze stavu **Plánováno** do stavu **Odhadnuto**
-   Ze stavu **Uvolněno** do stavu **Plánováno**
-   Ze stavu **Zahájeno** do stavu **Uvolněno**

## <a name="from-estimated-to-created"></a>Ze stavu Odhadnuto do stavu Vytvořeno
Když vrátíte stav výrobní zakázky ze stavu **Odhadnuto** na **Vytvořeno**, spotřeba položky, která byla vypočtena pro položky v kusovnících, je odstraněna. Skladové transakce v řádku výroby jsou odstraněny a pole **Následný stav** na řádcích kusovníku výrobní zakázky je nastaven zpět na **Ukončeno**. Pokud vyberete možnost **Odvozené nákupy** a **Odvozené výroby**, veškeré podřízené nákupní objednávky nebo výrobní zakázky budou odstraněny. Pokud jste odhadovali náklady výrobní zakázky, nebo ručně rezervovali položky, takže je lze použít ve výrobě, tyto transakce budou odebrány.

## <a name="from-scheduled-to-estimated"></a>Ze stavu Plánováno do stavu Odhadnuto
Když stav vrátíte výrobní zakázky ze stavu **Plánováno** na **odhadnuto**, budou odstraněny plánovaná počáteční a koncová data a časy. Odstraní se rezervace kapacity provedené během plánování a úlohy, jež byly vytvořeny během plánování úlohy. Všechny informace, které jsou zaznamenány o plánování operací a plánování práce na stránce **Podrobnosti výrobní zakázky** budou obnoveny.

## <a name="from-released-to-scheduled"></a>Ze stavu Uvolněno do stavu Plánováno
Když vrátíte stav výrobní zakázky ze stavu **Uvolněno** do stavu **Plánováno**, jedinou změnou bude změna hodnoty ve stavovém poli.

## <a name="from-started-to-released"></a>Ze stavu Zahájeno do stavu Uvolněno
Když vrátíte stav výrobní zakázky ze stavu **Zahájeno** zpět do stavu **Uvolněno**, budou všechny položky hlášené jako dokončené vráceny zpět. Jestliže došlo k vydání materiálu nebo k provedení vstupních a výstupních dodávek do výroby, budou tato nastavení stornována. Pole **Následný stav** na řádcích kusovníku výrobní zakázky se změní z **Ukončeno** na **Spotřeba materiálu**. Pokud nebyl zaregistrován čas, nebo množství bylo hlášeno jako dokončené u operací ve výrobním postupu, budou tato nastavení stornována. Pole **Následný stav** se změní z **Ukončeno** na **Spotřeba postupu** ve výrobním postupu. Nastavení pro všechny položky, které jsou zaúčtovány jako procesu nebo nedokončená výroba, budou stornovány. Na stránce **Podrobnosti výrobní zakázky** se vynulují pole, která zobrazí množství, které bylo zahájeno nebo ohlášeno jako dokončené. Data pro tyto transakce jsou rovněž vynulovány.




