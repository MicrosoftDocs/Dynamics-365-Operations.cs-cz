---
title: Přehled plánování vytížení pomocí konsolidace centra
description: Tento článek popisuje funkci konsolidace dodávky v centru, pokud doručujete zboží z různých skladů ke stejnému zákazníkovi, nebo při příjmu zboží od více dodavatelů ve stejném skladu.
author: MarkusFogelberg
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, TMSParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 92273
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87b599c953244109b56958c0fe02deedfa252973
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205195"
---
# <a name="plan-loads-using-hub-consolidation-overview"></a>Přehled plánování vytížení pomocí konsolidace centra

[!include [banner](../includes/banner.md)]

Tento článek popisuje funkci konsolidace dodávky v centru, pokud doručujete zboží z různých skladů ke stejnému zákazníkovi, nebo při příjmu zboží od více dodavatelů ve stejném skladu.

Může být užitečné sloučit dodávky v centru, pokud doručujete zboží z různých skladů ke stejnému zákazníkovi, nebo při doručování zboží od více dodavatelů do stejného skladu.

## <a name="building-loads"></a>Sestavení nákladů
Před použitím konsolidace centra je třeba povolit možnost **Plánování tranzitu** na stránce **Parametry správy přepravy**. Musíte také vytvořit centra, kde bude konsolidace provedena. Následující diagram znázorňuje příklad konsolidace centra. V tomto případě jsou prodejní objednávky z různých skladů směrovány ke stejnému zákazníkovi. Základní zatížení jsou vytvářeny na základě prodejních objednávek obvyklým způsobem pomocí stránky **Pracovní plocha plánování vytížení**. Ke sloučení dvou nákladů v centru před doručením zákazníkovi vyberte na stránce **Pracovní plocha plánování vytížení** v poli **Přeprava** možnost **Konsolidace centra**. Při výběru správného centra pro každý náklad budou náklady využívat centrum jako cíl vyložení. Vytvoří se také dva „řádky požadavku na přepravu" v části **Nabídka a poptávka** na stránce **Pracovní plocha plánování vytížení**. Poté můžete přidat tyto dva řádky do nového nákladu. Toto nové vytížení bude mít oba řádky prodejní objednávky, a bude mít také centrum nastaveno jako jako výdejní adresu a zákazníka A jako cíl vyložení. Tři náklady jsou pak připraveny k hodnocení a směrování jako každý jiný náklad. Pro každý náklad můžete vybrat jakéhokoli dopravce, kterého systém navrhne. [![Konsolidace centra](./media/hubconsol.jpg)](./media/hubconsol.jpg) Stejným způsobem můžete také sloučit náklady pro více převodních příkazů. V takovém případě působí zákazník A na předchozím obrázku jako sklad. Případně můžete konsolidovat náklady pro více nákupních objednávek, kde jsou náklady dodávány od různých dodavatelů do stejného skladu. Můžete mít více než jedno centrum konsolidace a konsolidovat ve více centrech více nákladů, které přichází z různých skladů. Po sestavení základního nákladu a použití možnosti konsolidace centra vytvoříte nové náklady pomocí řádků požadavku na konsolidovanou přepravu. Náklady poté můžete ohodnotit a dále směrovat.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]