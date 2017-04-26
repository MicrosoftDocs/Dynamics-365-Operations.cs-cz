---
title: "Správa zásob na obchodě"
description: "Tento článek popisuje typy dokumentů, které můžete použít ke správě skladových zásob."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fbe9945799f1e65ed6ad624a3df270fa4eb72b88
ms.lasthandoff: 03/31/2017


---

# <a name="manage-store-inventory"></a>Správa zásob na obchodě

[!include[banner](includes/banner.md)]


Tento článek popisuje typy dokumentů, které můžete použít ke správě skladových zásob.

Typy následující dokumentů slouží ke správě skladových zásob v organizaci.

## <a name="purchase-orders"></a>Nákupní objednávky
Nákupní objednávky se vytvářejí v ústředí. Pokud maloobchodní sklad je zahrnuta v záhlaví nákupní objednávky, objednávky přijaty v obchodě pomocí moderní POS (MPOS) nebo shluk POS v Microsoft Dynamics 365 pro operace - maloobchodní. Po zadání množství, které jsou přijímány v obchodě mohou být místně uloženy pro další úpravy. Množství lze také potvrdit a odeslat do ústředí. V ústředí, množství, které byly přijaty v obchodě jsou zobrazeny v 365 Dynamics pro operace v **nyní přijmout** pole na nákupní objednávce.

## <a name="transfer-orders"></a>Převodní příkazy
Převodní příkaz může stanovit, že určitý obchod je místo, ze kterého mohou být položky expedovány. V tomto případě převodního příkazu se zobrazí v obchodě jako požadavek vyskladnění MPOS nebo shluk Retail POS. Poté, co jsou vyskladněné množství, které jsou požadovány, jsou potvrzena a odeslány ústředí. Ústředí, množství, které byly vydány v obchodě jsou zobrazeny v 365 Dynamics pro operace v **Expedovat nyní** pole v objednávce transferu. Převodní příkaz může stanovit, že určitý obchod je místo, do kterého mohou být položky expedovány. V tomto případě převodního příkazu se zobrazí v obchodě jako přijímající žádost MPOS nebo shluk Retail POS. Po zadání množství, které jsou přijímány v obchodě mohou být místně uloženy pro další úpravy. Množství lze také potvrdit a odeslat do ústředí. V ústředí, množství, které byly přijaty v obchodě jsou zobrazeny v 365 Dynamics pro operace v **nyní přijmout** pole v objednávce transferu.

## <a name="stock-counts"></a>Počty na skladě
Inventury mohou být plánované nebo neplánované. Plánované inventury zahajuje ústředí, které také určuje, které položky musí být spočítány. Ústředí vytvoří dokument inventury, které lze přijmout v obchodě, kde jsou zadány skutečné množství na skladě množství MPOS nebo shluk Retail POS. Neplánované inventury jsou zahajovány v obchodě, a množství skutečné množství na skladě jsou aktualizovány v MPOS nebo shluk POS. Na rozdíl od plánované inventury neplánovanou inventuru nemají předdefinovaného seznamu položek. Po dokončení obou typů inventury budou potvrzeny a odeslány do ústředí. V ústředí bude inventura ověřena a zaúčtována.






