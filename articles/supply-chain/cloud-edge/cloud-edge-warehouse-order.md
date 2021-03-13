---
title: Skladové objednávky pro jednotky škálování cloudu a hraniční sítě
description: Toto téma poskytuje informace o schopnosti objednávky skladu, která se používá jako součást pracovního vytížení jednotky měřítka skladu.
author: perlynne
manager: tfeyr
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: c04127b9fe621d962be2d7fe06358b3bd1b78916
ms.sourcegitcommit: 289e9183d908825f4c8dcf85d9affd4119238d0c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/02/2021
ms.locfileid: "5105696"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a>Skladové objednávky pro jednotky škálování cloudu a hraniční sítě

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> Ne všechny obchodní funkce jsou ve veřejném náhledu plně podporovány, když se používají jednotky škálování pracovní zátěže. Pokud používáte jednotky škálování, používejte pouze takové procesy, které toto téma výslovně popisuje jako podporované.

## <a name="what-are-warehouse-orders"></a>Co jsou to skladové objednávky?

*Skladové objednávky* jsou typem objednávky, která byla vytvořena k podpoře nasazení centra podpory a škálování jednotek skladu. Umožní vám přijímat zásoby, když pracujete se zatížením skladu na jednotce škálování. Aktuálně se používají pouze u objednávek.

Objednávky skladu se používají jako součást zpracování správy skladu, například když se skladová aplikace používá k registraci fyzických zásob na skladě během zpracování příchozí nákupní objednávky. Skladové objednávky jsou vytvářeny jako součást procesu *Vydání do skladu*, který je k dispozici pro nákupní objednávky, které určují sklad jednotek měřítka a položky, které mají povoleno používat procesy správy skladu.

> [!IMPORTANT]
> Objednávky skladu jsou k dispozici pouze v nasazeních, která používají [úlohy správy skladu pro cloudové a okrajové jednotky škálování](cloud-edge-workload-warehousing.md).

## <a name="create-a-warehouse-order"></a>Vytvoření skladové objednávky

Chcete-li vytvořit skladovou objednávku, postupujte následujícím způsobem.

1. Přihlaste se k instanci aplikace Microsoft Dynamics 365 Supply Chain Management, která běží v centru. (Musíte zahájit proces *Vydání do skladu*, když jste přihlášeni v centru.)
1. Přejděte na **Zásobování a zdroje \> Nákupní objednávky \> Všechny nákupní objednávky**.
1. V podokně akcí na kartě **Sklad** ve skupině **Akce** vyberte možnost **Uvolnit do skladu.**
1. Chcete-li zobrazit související řádky skladové objednávky, otevřete příslušnou nákupní objednávku a vyberte řádek v části **Řádky nákupní objednávky** a poté na panelu nástrojů vyberte **Sklad \> Skladové řádky**. Chcete-li zobrazit všechny řádky, přejděte na **Řízení skladu \> Dotazy a zprávy \> Skladové řádky**.

## <a name="cancel-a-warehouse-order"></a>Zrušení skladové objednávky

V rámci procesu *Vydání do skladu* jsou skladové transakce nákupních objednávek propojeny se skladovými objednávkami a zablokovány před aktualizací v centru. Pokud jste vydali zboží do skladu omylem nebo pokud máte jiný důvod pro zrušení vytváření řádků skladových objednávek, můžete požádat o zrušení řádků skladových objednávek.

Chcete-li zrušit řádky skladové objednávky, postupujte následujícím způsobem.

1. Přihlaste se k instanci Supply Chain Management, která běží v centru.
1. Přejděte na **Řízení skladu \> Dotazy a zprávy \> Skladové řádky**.
1. Vyberte příslušný řádek.
1. V podokně akcí vyberte **Zrušit řádky skladové objednávky**.

> [!NOTE]
> Žádost o zrušení řádků bude zamítnuta pro všechny řádky, které již čekají na zrušení nebo které se aktivně zpracovávají ve skladu, na kterém běží jeho pracovní zátěž na jednotce měřítka.

## <a name="monitor-a-warehouse-order"></a>Sledování skladové objednávky

V zobrazení **Skladové řádky** můžete sledovat průběh příchozího příjmu kontrolou hodnot ve sloupci **Zbývající množství k přijetí**. Chcete-li zobrazit podrobnosti, které souvisejí s prací prováděnou pomocí aplikace Sklad, postupujte podle jednoho z těchto kroků.

- Jděte na **Řízení skladu \> Dotazy a sestavy \> Řádky skladové objednávky** a pomocí filtru najděte řádky, které hledáte.
- Jděte na **Zásobování a zdroje \> Nákupní objednávky \> Všechny nákupní objednávky** a otevřete příslušnou nákupní objednávku. V části **Řádky nákupní objednávky** vyberte jeden nebo více řádků a poté na panelu nástrojů vyberte **Sklad \> Záznamy o přijetí do skladu**.
