---
title: Ověření, zda je v aplikacích Finance and Operations a Dataverse nakonfigurován duální zápis
description: Toto téma vysvětluje, jak můžete určit, zda je dvojí zápis konfigurován v aplikacích Finance and Operations a Dataverse.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 0a1da32713f3d4d19b4d343c5b67b416a6c4ffbb
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566758"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Ověření, zda je v aplikacích Finance and Operations a Dataverse nakonfigurován duální zápis

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Toto téma obsahuje informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Dataverse. Konkrétně vysvětluje, jak můžete určit, zda je dvojí zápis konfigurován v aplikacích Finance and Operations a Dataverse.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Ověření, zda je v aplikaci Finance and Operations nakonfigurován duální zápis

Chcete-li zjistit, zda jsou chyby, které se zobrazí při pokusu o uložení řádků pro aktualizaci, pocházet z duálního zápisů, ověřte nejprve, zda je konfigurován dvojí zápis.

+ Máte-li v aplikaci Finance and Operations oprávnění správce, přejděte na možnost **Pracovní prostory \> Správa dat** a vyberte dlaždici **Dvojí zápis**. Jsou-li zobrazeny podrobnosti o propojených prostředích a seznam spuštěných map tabulek, je nakonfigurován dvojí zápis.

    ![Ověřuje se připojení aplikace Finance and Operations, když máte oprávnění správce](media/verify_fin_ops_1.png)

+ Nemáte-li oprávnění správce, zobrazí se chybová zpráva *Nelze zapsat data do entity \<entity name\>*. V příkladu na následujícím obrázku nelze vytvořit řádek odběratele v aplikaci Finance and Operations, protože je nakonfigurován dvojí zápis, ale skupina odběratelů a referenční data platebních podmínek neexistují v Dataverse.

    ![Ověřuje se připojení aplikace Finance and Operations, když nemáte oprávnění správce](media/verify_fin_ops_2.png)

Informace o tom, jak vyřešit problémy při vytváření dat v aplikacích Finance and Operations, naleznete v tématu [Poradce při potížích s synchronizací v ostrém provozu](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Ověření, zda je nakonfigurován duální zápis v Dataverse

Pokud se při vytváření dat nachází sloupec **Společnost** na stránkách v aplikaci Dataverse, je nakonfigurováno dvojí zapisování.

![Ověřování připojení Dataverse](media/verify_cds.png)

Informace o tom, jak vyřešit problémy při vytváření dat v Dataverse, naleznete v tématu [Poradce při potížích s synchronizací v ostrém provozu](dual-write-troubleshooting-live-sync.md).

Informace o tom, jak zobrazit podrobnosti chyb při vytváření dat v Dataverse, naleznete v tématu [Povolení a zobrazení protokolu sledování modulu plug-in v aplikaci Dataverse, kde jsou zobrazeny podrobnosti o chybě](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]