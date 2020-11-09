---
title: Ověření, zda je v aplikacích Finance and Operations a Common Data Service nakonfigurován duální zápis
description: Toto téma vysvětluje, jak můžete určit, zda je dvojí zápis konfigurován v aplikacích Finance and Operations a Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2ddac76871a3ac574a1edcb5446be6c64e5e4682
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997223"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-common-data-service"></a>Ověření, zda je v aplikacích Finance and Operations a Common Data Service nakonfigurován duální zápis

[!include [banner](../../includes/banner.md)]



Toto téma obsahuje informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Common Data Service. Konkrétně vysvětluje, jak můžete určit, zda je dvojí zápis konfigurován v aplikacích Finance and Operations a Common Data Service.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Ověření, zda je v aplikaci Finance and Operations nakonfigurován duální zápis

Chcete-li zjistit, zda jsou chyby, které se zobrazí při pokusu o uložení záznamů pro aktualizaci, pocházet z duálního zápisů, ověřte nejprve, zda je konfigurován dvojí zápis.

+ Máte-li v aplikaci Finance and Operations oprávnění správce, přejděte na možnost **Pracovní prostory \> Správa dat** a vyberte dlaždici **Dvojí zápis**. Jsou-li zobrazeny podrobnosti o propojených prostředích a seznam spuštěných map entit, je nakonfigurován dvojí zápis.

    ![Ověřuje se připojení aplikace Finance and Operations, když máte oprávnění správce](media/verify_fin_ops_1.png)

+ Nemáte-li oprávnění správce, zobrazí se chybová zpráva *Nelze zapsat data do entity \<entity name\>*. V příkladu na následujícím obrázku nelze vytvořit záznam odběratele v aplikaci Finance and Operations, protože je nakonfigurován dvojí zápis, ale skupina odběratelů a referenční data platebních podmínek neexistují v Common Data Service.

    ![Ověřuje se připojení aplikace Finance and Operations, když nemáte oprávnění správce](media/verify_fin_ops_2.png)

Informace o tom, jak vyřešit problémy při vytváření dat v aplikacích Finance and Operations, naleznete v tématu [Poradce při potížích s synchronizací v ostrém provozu](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-common-data-service"></a>Ověření, zda je nakonfigurován duální zápis v Common Data Service

Pokud se při vytváření dat nachází pole **Společnost** na stránkách v aplikaci Common Data Service, je nakonfigurováno dvojí zapisování.

![Ověřování připojení Common Data Service](media/verify_cds.png)

Informace o tom, jak vyřešit problémy při vytváření dat v Common Data Service, naleznete v tématu [Poradce při potížích s synchronizací v ostrém provozu](dual-write-troubleshooting-live-sync.md).

Informace o tom, jak zobrazit podrobnosti chyb při vytváření dat v Common Data Service, naleznete v tématu [Povolení a zobrazení protokolu sledování modulu plug-in v aplikaci Common Data Service, kde jsou zobrazeny podrobnosti o chybě](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).
