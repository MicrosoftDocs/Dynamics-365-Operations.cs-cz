---
title: Sledování zásob dodávky s použitím dodavatelské spolupráce
description: Tato procedura ukazuje, jak použít spolupráci dodavatele k zobrazení informací o úrovni zásob produktu, který jste umístili v zásilce pro zákazníka.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, PurchVendorPortalConfirmedOrders, DefaultDashboard, ConsignmentVendorPortalOnhand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1c75db4ef5d07e4ae396401a851389b7ecb9242
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244368"
---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a>Sledování zásob dodávky s použitím dodavatelské spolupráce

[!include [banner](../../includes/banner.md)]

Tato procedura ukazuje, jak použít spolupráci dodavatele k zobrazení informací o úrovni zásob produktu, který jste umístili v zásilce pro zákazníka. Můžete také sledovat spotřebu zásob, když zákazník převezme vlastnictví zásob. Tento postup můžete projít v ukázkových datech společnosti USMF. Tento postup je určen pro funkci, která byla přidána do Dynamics 365 for Operations, verze 1611.


## <a name="view-consumed-inventory"></a>Zobrazení spotřebovaných zásob
1. Přejděte do nabídky Spolupráce dodavatele > Zásoby dodávky > Produkty přijaté ze zásob dodávky.
    * V seznamu jsou uvedeny řádky příjemky, které byly vytvořeny při změně vlastnictví šarže zásob dodávky z dodavatele na odběratele. Bude pravděpodobně nutné přejít doprava, chcete-li zobrazit množství a další informace. Informace v tomto seznamu slouží ke generování faktur pro odběratele. Můžete také exportovat data do aplikace Microsoft Excel.   
2. Klikněte na možnost Zobrazit nákupní objednávku.
3. Rozbalte sekci Podrobnosti řádku.
    * Řádek je označen jako Zásilka a oddílu v záhlaví ukazuje, že má nákupní objednávka stav Přijato.  
4. Zavřete stránku.

## <a name="view-on-hand-inventory"></a>Zobrazení zásob na skladě
1. Přejděte do nabídky Spolupráce dodavatele > Zásoby dodávky > Zásoby dodávky na skladě.
    * Stránka Zásoby dodávky na skladě ukazuje zásobu, kterou vlastníte ve skladu zákazníka. Další dimenze, například pracoviště a sklad, můžete zobrazit klepnutím na kartu Zobrazit dimenze.   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]