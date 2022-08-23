---
title: Přidání kanálu do organizační hierarchie
description: Tento článek popisuje, jak přidat kanál do organizační hierarchie v řešení Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 9def2d7c3cf17ecd9b74ce41f56bc3220a754597
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278590"
---
# <a name="add-a-channel-to-an-organizational-hierarchy"></a>Přidání kanálu do organizační hierarchie


[!include [banner](includes/banner.md)]

Tento článek popisuje, jak přidat kanál do organizační hierarchie v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Kanály je nutné přidružit k jedné nebo více organizačním hierarchiím. Před vytvořením kanálů je nutné potvrdit, že byly nastaveny vaše organizační hierarchie.  

Viz [Organizční hierarchie](channels-org-hierarchies.md) pro další podrobnosti o vytváření organizačních hierarchií.

## <a name="select-a-hierarchy"></a>Vyberte hierarchii

Chcete-li vybrat hierarchii, postupujte podle následujících kroků.

1. V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Organizační hierarchie**.
1. Ze seznamu vyberte organizační hierarchii, do které chcete přidat kanál.
1. Výběrem možnosti **Zobrazit** v podokně akcí zobrazíte podrobnosti hierarchie.

Následující obrázek zobrazuje podrobnosti organizační hierarchie pro vybranou hierarchii.

![Podrobnosti organizační hierarchie pro vybranou hierarchii.](media/channel-add-to-org-hierarchy-1.png)

## <a name="add-a-channel-to-a-hierachy-node"></a>Přidání kanálu do uzlu hierachie

Chcete-li přidat kanál do uzlu hierachie, postupujte takto.

1. V podokně akcí vyberte **Upravit**.
1. Vyberte uzel hierachie, do kterého chcete přidat kanál, a poté v rozevíracím seznamu **Vložit** vyberte položku **Maloobchodní kanál**. 
1. Vyberte kanál, který chcete přidat, a poté vyberte tlačítko **OK**.
1. V podokně akcí vyberte **Uložit**.
1. V podokně akcí vyberte **Publikovat** a zadejte **Datum platnosti** v minulosti, má-li být tato akce provedena okamžitě.

Následující obrázek ukazuje, jak vybrat kanál, který má být přidán do uzlu hierarchie.

![Výběr kanálu pro přidání do uzlu hierarchie.](media/channel-add-to-org-hierarchy-2.png)

Na následujícím obrázku je znázorněna hierarchie s různými kanály.

![Hierarchie s různými přidanými kanály.](media/channel-add-to-org-hierarchy-3.png)

## <a name="additional-resources"></a>Další prostředky

[Přehled kanálů](channels-overview.md)

[Předpoklady nastavení kanálu](channels-prerequisites.md)

[Přehled organizací a organizačních hierarchií](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Plánování organizační hierarchie](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Organizační hierarchie](channels-org-hierarchies.md)

[Nastavení maloobchodního kanálu](channel-setup-retail.md)
    
[Nastavení online kanálu](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
