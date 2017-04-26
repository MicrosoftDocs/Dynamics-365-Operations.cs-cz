---
title: "Konsolidované dávkové objednávky"
description: "Tento článek popisuje koncept konsolidované dávkové objednávky."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 3359f1cd5c3f1ecf25c3f28a366c022826cf895e
ms.lasthandoff: 03/31/2017


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





