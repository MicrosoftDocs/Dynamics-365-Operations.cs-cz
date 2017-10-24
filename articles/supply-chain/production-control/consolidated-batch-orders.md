---
title: "Konsolidované dávkové objednávky"
description: "Tento článek popisuje koncept konsolidované dávkové objednávky."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3ca9c920ea333bd21defebc29b40243d3a618a3d
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="consolidated-batch-orders"></a>Konsolidované dávkové objednávky

[!include[banner](../includes/banner.md)]


Tento článek popisuje koncept konsolidované dávkové objednávky.

Vyrobená nebalená položka je považována za nadřazenou položku, zatímco zabalená položka je považována za podřízenou položku. Vztah mezi nebalenou položkou a zabalenou položkou je vyjádřen v převodu nebalené položky. Tento převod nebalené položky je definován pro nebalenou položku samotnou.  

Zabalené položky lze balit do kontejnerů jedné nebo více velikostí, které jsou považovány za jednu jednotku. Při konsolidaci objednávek nebalené položky můžete zobrazit všechny související dávkové objednávky v jednom zobrazení, abyste zjistili, zda musí být dokončena nějaká zbývající práce.  

Konsolidovaná dávková objednávka může obsahovat kombince následujících objednávek:

-   Jedna objednávka nebaleného zboží a více objednávek baleného zboží
-   Více objednávek nebaleného zboží a více objednávek baleného zboží
-   Více objednávek nebaleného zboží a jedna objednávka baleného zboží
-   Pouze objednávky baleného zboží





