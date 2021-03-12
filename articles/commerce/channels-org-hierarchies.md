---
title: Nastavení organizačních hierarchií
description: Toto téma popisuje, jak nastavit orhanizační hierarchie v aplikaci Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b887616ef29396ba99ca0c7428ab89df01b3008c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997768"
---
# <a name="set-up-organization-hierarchies"></a>Nastavení organizačních hierarchií


[!include [banner](includes/banner.md)]

Toto téma popisuje, jak nastavit orhanizační hierarchie v aplikaci Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Před vytvořením kanálů je nutné zajistit, že byly nastaveny organizační hierarchie.

Organizační hierarchii můžete použít k zobrazení a tvorbě sestav vašeho podnikání z různých perspektiv. Můžete například nastavit jednu hierarchii pro daňové, právní nebo statutární vykazování. Potom můžete nastavit jinou hierarchii pro finanční informace sestavy, které nejsou vyžadovány zákonem, ale které se používají pro interní výkaznictví.

Dříve než vytvoříte organizační hierarchií, musíte vytvořit organizace. Další informace naleznete v [Vytvoření právnické osoby](channels-legal-entities.md) nebo [Vytvoření provozní jednotky](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).


Další informace naleznete v následujících tématech.
- [Přehled organizací a organizačních hierarchií](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [Plánování organizační hierarchie](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [Vytvoření organizační hierarchie](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a>Vytvoření organizační hierarchie

Následující postup použijte k vytvoření organizační hierarchie.

1. V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Organizační hierarchie**.
1. V podokně akcí zvolte **Nový**.
1. Zadejte hodnotu do pole **Název**.
1. V sekci **Účel** vyberte **Přiřadit účel**.
1. Vyhledejte na seznamu požadovaný záznam a vyberte ho. Vyberte účel, který chcete přiřadit k hierarchii organizace.
1. V sekci **Přiřazené hierarchie** vyberte **Přidat**.
1. Označte na seznamu vybraný řádek. Vyhledejte hierarchii, kterou jste právě vytvořili.
1. Vyberte **OK**.

Následující obrázek znázorňuje ukázkovou organizační hierarchii vytvořenou pro fiktivní sadu obchodů "Adventure Works".

![Příklad organizační hierarchie](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a>Přidání organizací do hierarchie

Chcete-li přidat organizace do hierachie, postupujte takto.

1. Vyhledejte na seznamu požadovaný záznam a vyberte ho. Vyberte svoji hierarchii.
1. V podokně akcí vyberte **Zobrazit**.
1. Podle potřeby přidejte organizace.
1. Chcete-li přidat organizaci, vyberte **Upravit** a pak vyberte **Vložit**. Po dokončení provádění změn můžete uložit návrh a publikovat změny.

Na následujícím obrázku je znázorněna právnická osoba přidaná v kořenové složce hierarchie se čtyřmi nákladovými středisky přidanými pro kanály "Obchodní centrum", "Outlet", "Online" a "Kontaktní středisko". Do každé z nich lze přidat různé maloobchodní a online kanály.

![Příklad návrháře hierarchie](media/hierarchy-designer.png)

## <a name="additional-resources"></a>Další zdroje

[Přehled organizací a organizačních hierarchií](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Plánování organizační hierarchie](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Vytvořit právnické osoby](channels-legal-entities.md)

[Vytvoření provozních jednotek](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[Přehled kanálů](channels-overview.md)

[Předpoklady nastavení kanálu](channels-prerequisites.md)
