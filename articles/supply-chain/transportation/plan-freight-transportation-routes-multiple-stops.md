---
title: Plánování tras nákladní dopravy s více zastávkami
description: Tento článek popisuje různé prvky, které slouží k plánování tras přepravy v aplikaci Dynamics 365 Supply Chain Management.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSHubMaster, TMSLoadBuildTemplates, TMSRateRouteWorkbench, TMSRouteGuide, TMSRoutePlan, TMSRouteWorkbench, WHSLoadTemplate, TMSRouteSchedule, TMSRouteRateDetail
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 90013
ms.assetid: 50d6f58c-f1c8-4321-9e83-8445cec57a85
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 04346363070fff4dc3110a620c3d9bc9b1016d1e
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424208"
---
# <a name="plan-freight-transportation-routes-with-multiple-stops"></a>Plánování tras nákladní dopravy s více zastávkami

[!include [banner](../includes/banner.md)]

Tento článek popisuje různé prvky, které slouží k plánování tras přepravy v aplikaci Dynamics 365 Supply Chain Management.

Pro komplexní přepravní trasy, které mají více zastávek, můžete použít plány trasy a vodítka trasy. Pokud stejnou trasu používáte pravidelně, můžete nastavit plánované trasy.

## <a name="route-plans"></a>Plány trasy
Plán cesty obsahuje segmenty trasy, které poskytují informace o zastávkách, které jste navštívili na trase, a o dopravcích, kteří jsou použiti pro každý segment. Zastávky na trase je třeba definovat jako centra. Centrum může být dodavatel, sklad, zákazník nebo jenom překladní místo, kde měníte dopravce. Pro každý segment můžete definovat „místní sazby“ pro různé poplatky. Několik příkladů:

-   Náklady na dopravu na daném segmentu
-   Poplatky za vyskladnění zboží
-   Poplatky za složení zboží

Každý plán trasy musí být přidružen k průvodci trasy.

## <a name="route-guides"></a>Průvodce trasou
Průvodci trasy definují kritéria pro párování nákladu s konkrétním plánem trasy. Můžete například zadat původní centrum a cílové centrum, omezení pro objem hmotnost kontejneru a dopravce, službu nebo skupinu. Průvodci trasy jsou k dispozici na stránce **Pracovní plocha sazeb trasy**, kde lze náklady přiřadit k trasám, a to buď ručně nebo automaticky. Pokud je průvodce trasy určen pro naplánovanou trasu, je také k dispozici na stránce **Pracovní plocha sestavení vytížení**.

## <a name="scheduled-routes"></a>Plánované trasy
Naplánovaná trasa je předdefinovaný plán cesty, který obsahuje plán pro data expedice. Plánované trasy a neplánované trasy se liší způsobem, kterým jsou k nim náklady přiřazeny. Pokud přiřadíte neplánovanou trasu pomocí stránky Pracovní plocha sazeb trasy, jsou ověřeny pouze náklady a průvodce trasy. Pokud přiřadíte naplánovanou trasu, data a adresy z objednávky a center a datum pro plán trasy jsou také zohledněny. Není potřeba použít stránku Pracovní plocha sazeb trasy pro ruční přiřazení nákladů o naplánované trase. Místo toho můžete použít stránku Pracovní plocha sestavení vytížení a navrhnout tak sestavení nákladů na základě adres odběratele a datech dodání z prodejních objednávek pro danou plánovanou trasu. Pro plánované trasy bude plán trasy mít pevné původní a cílové centrum. Obvykle bude dopravce a služba stejná pro všechny segmenty, ale může se také lišit. Cílová centra jsou vytvářena pomocí PSČ odběratelů, kteří jsou po trase navštíveni. Několik schémat trasy lze definovat pro jeden plán trasy. Plán trasy musí být přidružen k průvodci trasy. Pro plánované trasy však může lze přidružit plán pouze k jednomu průvodci trasy. Plán trasy se používá pouze k vytvoření samotných tras na stránce **Plán trasy**. Při návrhu nákladů na stránce Pracovní plocha sestavení vytížení můžete použít výchozí šablonu nákladu.

## <a name="load-building-workbench"></a>Pracovní plocha sestavení vytížení
Pracovní plocha sestavení vytížení používá pro navržení nákladu adresy zákazníka a data dodání z prodejních objednávek a plánované trasy, které jsou k dispozici. Ve výchozím nastavení jsou hodnoty z trasy zadány v rámci pracovní plochy. Můžete však vybrat datum "od", které je dřívější, než datum "od" z trasy. Po navržení nákladu se zkontroluje adresa dodání a datum dodání pro všechny otevřené prodejní objednávky. Pokud PSČ dodací adresy odpovídá PSČ centra v plánu trasy, a pokud je datum dodání v rozsahu, který je vybrán v rámci kritérií, bude prodejní objednávka navržena pro náklad. Je třeba zvážit také kapacitu šablony nákladu. Najednou je nabízen pouze jeden náklad. Pokud máte prodejní objednávky, které nejsou zahrnuty, bude pravděpodobně nutné použít jinou šablonu nákladu (například šablonu nákladu pro větší nákladní vůz nebo kontejner), nebo naplánovat další dodávky.



