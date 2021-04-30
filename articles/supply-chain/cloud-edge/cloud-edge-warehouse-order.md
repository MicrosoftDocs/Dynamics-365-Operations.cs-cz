---
title: Skladové objednávky pro jednotky škálování cloudu a hraniční sítě
description: Toto téma poskytuje informace o schopnosti objednávky skladu, která se používá jako součást pracovního vytížení jednotky měřítka skladu.
author: perlynne
ms.date: 04/13/2021
ms.topic: article
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c24c08771c83453bb65312700cf994c7a800b7fd
ms.sourcegitcommit: 639175a39da38edd13e21eeb5a1a5ca62fa44d99
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/15/2021
ms.locfileid: "5899112"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a>Skladové objednávky pro jednotky škálování cloudu a hraniční sítě

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> Ne všechny obchodní funkce jsou ve veřejném náhledu plně podporovány, když se používají jednotky škálování pracovní zátěže. Pokud používáte jednotky škálování, používejte pouze takové procesy, které toto téma výslovně popisuje jako podporované.

## <a name="what-are-warehouse-orders"></a>Co jsou to skladové objednávky?

*Skladové objednávky* jsou typem objednávky, která byla vytvořena k podpoře nasazení centra podpory a škálování jednotek skladu. Umožní vám přijímat zásoby, když pracujete se zatížením skladu na jednotce škálování. Aktuálně se používají pouze u objednávek.

Objednávky skladu se používají jako součást zpracování správy skladu, například když se mobilní aplikace Řízení skladu používá k registraci fyzických zásob na skladě během zpracování příchozí nákupní objednávky. Skladové objednávky jsou vytvářeny jako součást procesu *Vydání do skladu*, který je k dispozici pro nákupní objednávky, které určují sklad jednotek měřítka a položky, které mají povoleno používat procesy správy skladu.

> [!IMPORTANT]
> Objednávky skladu jsou k dispozici pouze v nasazeních, která používají [úlohy správy skladu pro cloudové a okrajové jednotky škálování](cloud-edge-workload-warehousing.md).

## <a name="create-a-warehouse-order"></a>Vytvoření skladové objednávky

Chcete-li vytvořit skladovou objednávku, postupujte následujícím způsobem.

1. Přihlaste se k instanci aplikace Microsoft Dynamics 365 Supply Chain Management, která běží v centru. (Musíte zahájit proces *Vydání do skladu*, když jste přihlášeni v centru.)
1. Přejděte na **Zásobování a zdroje \> Nákupní objednávky \> Všechny nákupní objednávky**.
1. V podokně akcí na kartě **Sklad** ve skupině **Akce** vyberte možnost **Uvolnit do skladu.**
1. Chcete-li zobrazit související řádky skladové objednávky, otevřete příslušnou nákupní objednávku a vyberte řádek v části **Řádky nákupní objednávky** a poté na panelu nástrojů vyberte **Sklad \> Skladové řádky**. Chcete-li zobrazit všechny řádky, přejděte na **Řízení skladu \> Dotazy a zprávy \> Skladové řádky**.

Proces *Uvolnění do skladu* můžete také spustit z dávkové úlohy, a to přechodem do nabídky **Správa skladu > Uvolnění do skladu > Automatické uvolnění nákupních objednávek**. Při nastavování dávkové úlohy můžete vybrat konkrétní řádky nákupní objednávky na základě dotazu. Typickým scénářem by bylo nastavení opakované dávkové úlohy, která uvolní všechny potvrzené řádky nákupní objednávky, které se očekávají příští den.

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

V zobrazení **Skladové řádky** můžete sledovat průběh příchozího příjmu kontrolou hodnot ve sloupci **Zbývající množství k přijetí**. Chcete-li zobrazit podrobnosti, které souvisejí s prací prováděnou pomocí mobilní aplikace Řízení skladu, postupujte podle jednoho z těchto kroků.

- Jděte na **Řízení skladu \> Dotazy a sestavy \> Řádky skladové objednávky** a pomocí filtru najděte řádky, které hledáte.
- Jděte na **Zásobování a zdroje \> Nákupní objednávky \> Všechny nákupní objednávky** a otevřete příslušnou nákupní objednávku. V části **Řádky nákupní objednávky** vyberte jeden nebo více řádků a poté na panelu nástrojů vyberte **Sklad \> Záznamy o přijetí do skladu**.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
