---
title: Konfigurace zásilky
description: Toto téma vysvětluje, jak nakonfigurovat operace příchozí skladové zásilky.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 00102f5c7a043c5ca22458a53b1445c57c61957c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209556"
---
# <a name="set-up-consignment"></a>Konfigurace zásilky

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak nakonfigurovat operace příchozí skladové zásilky.

Zásoby dodávky jsou zásoby, které vlastní dodavatel, ale jsou uloženy ve vaší společnosti. Až budete připraveni spotřebovat nebo použít zásoby, převezmete vlastnictví zásob. Toto téma popisuje potřebné nastavení pro umožnění procesy dodávky. Další informace o procesech dodávek naleznete v tématu [Nastavení zásilky](consignment.md).

## <a name="inventory-owners"></a>Vlastníci zásob
Aby bylo možné zaznamenat fyzickou zásilku zásob, je třeba definovat dodavatele vlastníka. To se provádí na stránce **Vlastník zásob**. Při výběru **Účet dodavatele** se generují výchozí hodnoty pro pole **Název** a **Vlastník**. Hodnota v poli **Vlastník** se zobrazí dodavateli, takže ji můžete změnit v případě, že název účtu dodavatele se špatně rozpoznává externím uživatelům. Je možné upravit pole **Vlastník**, ale pouze do okamžiku, když ukládáte záznam **Vlastník zásob**. Pole **Název** se vyplňuje s názvem strany, k níž je přidružen účet dodavatele, a nemůže být změněno.

[![vlastníci-zásob](./media/inventory-owners.png)](./media/inventory-owners.png)

## <a name="tracking-dimension-group"></a>Skupina sledovací dimenze
Položky, které chcete použít v procesech dodávky, musí být přidruženy k **Skupina sledovací dimenze** kde dimenze **Vlastník** je nastavena na **Aktivní**. Dimenze vlastníka má vždy vybrané možnosti **Fyzické zásoby** a **Finanční zásoby**. Nikdy není vybrána možnost **Plán disponibility podle dimenzí**.

[![skupina-sledovací-dimenze](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)

## <a name="inventory-ownership-change-journal"></a>Deník změn vlastnictví zásob
Deník **Změny vlastnictví zásob** se používá k zaznamenání k přesunu vlastnictví dodávek zásob od dodavatele na stávající právnickou osobu, která ho využívá. Stejně jako jakýkoliv deník zásob musí být označen názvem deníku zásob. Tyto názvy jsou vytvářeny na stránce **Názvy deníků zásob**, kde **Typ deníku** musí být nastaven na **Změny vlastnictví**.

[![Deník-změn-vlastnictví-zásob](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Dodavatelská spolupráce v procesech zásilky
Pokud vaši dodavatelé využívají rozhraní dodavatelské spolupráce, mohou ho využívat ke sledování spotřeby zásob vaší společnosti. Další informace o nastavení dodavatelů pro použití dodavatelské spolupráce naleznete v tématu [Zabezpečení uživatele dodavatelského portálu](../procurement/configure-security-vendor-portal-users.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]