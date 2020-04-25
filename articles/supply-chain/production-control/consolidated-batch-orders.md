---
title: Konsolidované dávkové objednávky
description: Tento článek popisuje koncept konsolidované dávkové objednávky.
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e8b017455c0821d97f9039d4ebf00d2dfa28eaa
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211631"
---
# <a name="consolidated-batch-orders"></a>Konsolidované dávkové objednávky

[!include [banner](../includes/banner.md)]

Tento článek popisuje koncept konsolidované dávkové objednávky.

Vyrobená nebalená položka je považována za nadřazenou položku, zatímco zabalená položka je považována za podřízenou položku. Vztah mezi nebalenou položkou a zabalenou položkou je vyjádřen v převodu nebalené položky. Tento převod nebalené položky je definován pro nebalenou položku samotnou.  

Zabalené položky lze balit do kontejnerů jedné nebo více velikostí, které jsou považovány za jednu jednotku. Při konsolidaci objednávek nebalené položky můžete zobrazit všechny související dávkové objednávky v jednom zobrazení, abyste zjistili, zda musí být dokončena nějaká zbývající práce.  

Konsolidovaná dávková objednávka může obsahovat kombince následujících objednávek:

-   Jedna objednávka nebaleného zboží a více objednávek baleného zboží
-   Více objednávek nebaleného zboží a více objednávek baleného zboží
-   Více objednávek nebaleného zboží a jedna objednávka baleného zboží
-   Pouze objednávky baleného zboží




