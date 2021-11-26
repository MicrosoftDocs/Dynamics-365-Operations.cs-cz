---
title: Ověření, zda je v aplikacích Finance and Operations a Dataverse nakonfigurován duální zápis
description: Toto téma vysvětluje, jak můžete určit, zda je dvojí zápis konfigurován v aplikacích Finance and Operations a Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 1f82705f3d8bc11eacbc13d32c14ad1765dcc559
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782620"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Ověření, zda je v aplikacích Finance and Operations a Dataverse nakonfigurován duální zápis

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Toto téma obsahuje informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Dataverse. Konkrétně vysvětluje, jak můžete určit, zda je dvojí zápis konfigurován v aplikacích Finance and Operations a Dataverse.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Ověření, zda je v aplikaci Finance and Operations nakonfigurován duální zápis

Chcete-li zjistit, zda jsou chyby, které se zobrazí při pokusu o uložení řádků pro aktualizaci, pocházet z duálního zápisů, ověřte nejprve, zda je konfigurován dvojí zápis.

+ Máte-li v aplikaci Finance and Operations oprávnění správce, přejděte na možnost **Pracovní prostory \> Správa dat** a vyberte dlaždici **Dvojí zápis**. Jsou-li zobrazeny podrobnosti o propojených prostředích a seznam spuštěných map tabulek, je nakonfigurován dvojí zápis.

    ![Ověřuje se připojení aplikace Finance and Operations, když máte oprávnění správce.](media/verify_fin_ops_1.png)

+ Nemáte-li oprávnění správce, zobrazí se chybová zpráva *Nelze zapsat data do entity \<entity name\>*. V příkladu na následujícím obrázku nelze vytvořit řádek odběratele v aplikaci Finance and Operations, protože je nakonfigurován dvojí zápis, ale skupina odběratelů a referenční data platebních podmínek neexistují v Dataverse.

    ![Ověřuje se připojení aplikace Finance and Operations, když nemáte oprávnění správce.](media/verify_fin_ops_2.png)

Informace o tom, jak vyřešit problémy při vytváření dat v aplikacích Finance and Operations, naleznete v tématu [Poradce při potížích s synchronizací v ostrém provozu](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Ověření, zda je nakonfigurován duální zápis v Dataverse

Pokud se při vytváření dat nachází sloupec **Společnost** na stránkách v aplikaci Dataverse, je nakonfigurováno dvojí zapisování.

![Ověřování připojení Dataverse.](media/verify_cds.png)

Informace o tom, jak vyřešit problémy při vytváření dat v Dataverse, naleznete v tématu [Poradce při potížích s synchronizací v ostrém provozu](dual-write-troubleshooting-live-sync.md).

Informace o tom, jak zobrazit podrobnosti chyb při vytváření dat v Dataverse, naleznete v tématu [Povolení a zobrazení protokolu sledování modulu plug-in v aplikaci Dataverse, kde jsou zobrazeny podrobnosti o chybě](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]