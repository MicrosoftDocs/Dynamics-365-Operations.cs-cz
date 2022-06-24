---
title: Zobrazení výstupní plánované mezipodnikové poptávky
description: Tento článek obsahuje postup ukazující, jak zobrazit odchozí plánovanou mezipodnikovou poptávku.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqOutboundIntercompanyDemand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dcdea0af5cb522646bc63c7e5ef1d4e54e0a3547
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895634"
---
# <a name="view-outbound-planned-intercompany-demand"></a>Zobrazení výstupní plánované mezipodnikové poptávky

[!include [banner](../../includes/banner.md)]

Tato procedura ukazuje, jak zobrazit všechny plánované objednávky, které budou splněny mezipodnikovým dodavatelem. K vytvoření tohoto postupu jsou použita ukázková data společnosti DEMF.

1. Vyberte **Hlavní plánování**.
2. V poli **Plán** zadejte nebo vyberte hodnotu.
    * V poli **Plán** vyberte plán *10*.  
3. Vyberte *Spustit*.
4. Do pole **Počet vláken** zadejte číslo.
    * To představuje počet paralelních podprocesů použitých pro hlavní plánování.  
5. Vyberte **OK**.
    * Tato operace může chvíli trvat.  
6. Vyberte možnost **Plánovaná mezipodniková poptávka**.
7. Vyberte možnost **Výstupní plánované mezipodniková poptávka**.
    * Tato stránka obsahuje přehled plánované poptávky, kterou splní dodavatel interního zásobovacího řetězce.  
8. Rozbalte část **Podrobnosti nadřazené poptávky**.
    * V této části můžete zobrazit podrobnosti o tom, jak bude splněna poptávka. Než se zde zobrazí další informace, budete muset počkat na spuštění hlavního plánování v dodavatelské společnosti.  

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
