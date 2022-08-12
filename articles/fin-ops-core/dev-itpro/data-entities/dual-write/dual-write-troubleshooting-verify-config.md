---
title: Ověření konfigurace duálního zápisu ve finančních a provozních aplikacích a Dataverse
description: Tento článek vysvětluje, jak můžete určit, zda je dvojí zápis konfigurován v finančních a provozních aplikacích a v Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: d5191f5dd9c3a286abac622aede07d04fb72a8f7
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111385"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Ověření konfigurace duálního zápisu ve finančních a provozních aplikacích a Dataverse

[!include [banner](../../includes/banner.md)]





Tento článek obsahuje informace o odstraňování potíží pro integrací dvojitého zápisu mezi finančními a provozními aplikacemi a Dataverse. Konkrétně vysvětluje, jak můžete určit, zda je dvojí zápis konfigurován v finančních a provozních aplikacích a v Dataverse.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Ověření konfigurace duálního zápisu ve finanční a provozní aplikaci

Chcete-li zjistit, zda jsou chyby, které se zobrazí při pokusu o uložení řádků pro aktualizaci, pocházet z duálního zápisů, ověřte nejprve, zda je konfigurován dvojí zápis.

+ Máte-li ve finanční a provozní aplikaci oprávnění správce, přejděte na možnost **Pracovní prostory \> Správa dat** a vyberte dlaždici **Dvojí zápis**. Jsou-li zobrazeny podrobnosti o propojených prostředích a seznam spuštěných map tabulek, je nakonfigurován dvojí zápis.

    ![Ověřuje se připojení finanční a provozní aplikace, když nemáte oprávnění správce.](media/verify_fin_ops_1.png)

+ Nemáte-li oprávnění správce, zobrazí se chybová zpráva *Nelze zapsat data do entity \<entity name\>*. V příkladu na následujícím obrázku nelze vytvořit řádek odběratele ve finanční a provozní aplikaci, protože je nakonfigurován dvojí zápis, ale skupina odběratelů a referenční data platebních podmínek neexistují v Dataverse.

    ![Ověřuje se připojení finanční a provozní aplikace, když nemáte oprávnění správce.](media/verify_fin_ops_2.png)

Informace o tom, jak vyřešit problémy při vytváření dat v finančních a provozních aplikacích, naleznete v tématu [Poradce při potížích s synchronizací v ostrém provozu](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Ověření, zda je nakonfigurován duální zápis v Dataverse

Pokud se při vytváření dat nachází sloupec **Společnost** na stránkách v aplikaci Dataverse, je nakonfigurováno dvojí zapisování.

![Ověřování připojení Dataverse.](media/verify_cds.png)

Informace o tom, jak vyřešit problémy při vytváření dat v Dataverse, naleznete v tématu [Poradce při potížích s synchronizací v ostrém provozu](dual-write-troubleshooting-live-sync.md).

Informace o tom, jak zobrazit podrobnosti chyb při vytváření dat v Dataverse, naleznete v tématu [Povolení a zobrazení protokolu sledování modulu plug-in v aplikaci Dataverse, kde jsou zobrazeny podrobnosti o chybě](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
