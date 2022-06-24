---
title: Skladové objednávky pro jednotky škálování cloudu a hraniční sítě
description: Tento článek poskytuje informace o schopnosti objednávky skladu, která se používá jako součást pracovního vytížení jednotky měřítka skladu.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: db254216e6c34b81f83c87a8fda454d0aeb1cece
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893519"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a>Skladové objednávky pro jednotky škálování cloudu a hraniční sítě

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Ne všechny obchodní funkce jsou ve veřejném náhledu plně podporovány, když se používají jednotky škálování pracovní zátěže. Pokud používáte jednotky škálování, používejte pouze takové procesy, které tento článek výslovně popisuje jako podporované.

## <a name="what-are-warehouse-orders"></a>Co jsou to skladové objednávky?

*Skladové objednávky* jsou typem objednávky používané k podpoře nasazení centra podpory a škálování jednotek skladu. Umožní vám přijímat a dodávat zásoby, když pracujete se zatížením skladu na jednotce škálování.

Skladové objednávky se používají jako součást zpracování správy příchozích i odchozích skladů. Jsou vytvořeny jako součást procesu *Uvolněte do skladu*, který se inicializuje na rozbočovači.
Pro příchozí zpracování slouží mobilní aplikace skladu k registraci fyzického skladového inventáře během zpracování příchozích objednávek, což je k dispozici u nákupních a výrobních objednávek, které specifikují skladovou jednotku škálování a položky, u kterých je povoleno používat procesy správy skladu.
Odchozí skladové objednávky se používají jako součást procesu mávání zásilky pro převodní a prodejní objednávky.

> [!IMPORTANT]
> Objednávky skladu jsou k dispozici pouze v nasazeních, která používají [úlohy správy skladu pro cloudové a okrajové jednotky škálování](cloud-edge-workload-warehousing.md).

## <a name="create-an-inbound-warehouse-order"></a>Vytvoření příchozího skladového příkazu

Chcete-li vytvořit příchozí skladovou objednávku pro proces nákupní objednávky, postupujte takto.

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
