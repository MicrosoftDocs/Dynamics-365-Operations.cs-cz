---
title: "Plánování vytížení pomocí konsolidace center"
description: "Tento článek popisuje funkci konsolidace dodávky v centru, pokud doručujete zboží z různých skladů ke stejnému zákazníkovi, nebo při příjmu zboží od více dodavatelů ve stejném skladu."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 92273
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3145febe40108e50b263514de1ca541dd914b7c5
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="plan-loads-using-hub-consolidation"></a>Plánování vytížení pomocí konsolidace center

[!include[banner](../includes/banner.md)]


Tento článek popisuje funkci konsolidace dodávky v centru, pokud doručujete zboží z různých skladů ke stejnému zákazníkovi, nebo při příjmu zboží od více dodavatelů ve stejném skladu.

Může být užitečné sloučit dodávky v centru, pokud doručujete zboží z různých skladů ke stejnému zákazníkovi, nebo při doručování zboží od více dodavatelů do stejného skladu.

## <a name="building-loads"></a>Sestavení nákladů
Před použitím konsolidace centra je třeba povolit možnost **Plánování tranzitu**na stránce **Parametry správy přepravy**. Musíte také vytvořit centra, kde bude konsolidace provedena. Následující diagram znázorňuje příklad konsolidace centra. V tomto případě jsou prodejní objednávky z různých skladů směrovány ke stejnému zákazníkovi. Základní zatížení jsou vytvářeny na základě prodejních objednávek obvyklým způsobem pomocí stránky **Pracovní plocha plánování vytížení**. Ke sloučení dvou nákladů v centru před doručením zákazníkovi vyberte na stránce **Pracovní plocha plánování vytížení** v poli **Přeprava** možnost **Konsolidace centra**. Při výběru správného centra pro každý náklad budou náklady využívat centrum jako cíl vyložení. Vytvoří se také dva „řádky požadavku na přepravu" v části **Nabídka a poptávka** na stránce **Pracovní plocha plánování vytížení**. Poté můžete přidat tyto dva řádky do nového nákladu. Toto nové vytížení bude mít oba řádky prodejní objednávky, a bude mít také centrum nastaveno jako jako výdejní adresu a zákazníka A jako cíl vyložení. Tři náklady jsou pak připraveny k hodnocení a směrování jako každý jiný náklad. Pro každý náklad můžete vybrat jakéhokoli dopravce, kterého systém navrhne. [![Konsolidace centra](./media/hubconsol.jpg)](./media/hubconsol.jpg) Stejným způsobem můžete také sloučit náklady pro více převodních příkazů. V takovém případě působí zákazník A na předchozím obrázku jako sklad. Případně můžete konsolidovat náklady pro více nákupních objednávek, kde jsou náklady dodávány od různých dodavatelů do stejného skladu. Můžete mít více než jedno centrum konsolidace a konsolidovat ve více centrech více nákladů, které přichází z různých skladů. Po sestavení základního nákladu a použití možnosti konsolidace centra vytvoříte nové náklady pomocí řádků požadavku na konsolidovanou přepravu. Náklady poté můžete ohodnotit a dále směrovat.




