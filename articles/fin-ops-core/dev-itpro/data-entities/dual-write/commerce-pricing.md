---
title: Používání cenového modulu Dynamics 365 Commerce s Dynamics 365 Sales
description: V tomto článku je popsán způsob použití cenového modulu v aplikaci Microsoft Dynamics 365 Commerce k vytvoření prodejních nabídek v Dynamics 365 Sales.
author: ShalabhjainMSFT
ms.date: 11/19/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: global
ms.author: shajain
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 11a164ec15c8b7a69172a153b961011a8b324712
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881387"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a>Používání cenového modulu Dynamics 365 Commerce s Dynamics 365 Sales

[!include [banner](../../includes/banner.md)]

V tomto článku je popsán způsob použití cenového modulu v aplikaci Microsoft Dynamics 365 Commerce k vytvoření prodejních nabídek v Dynamics 365 Sales.

Cenový modul Dynamics 365 Commerce podporuje většinu scénářů cen mezi podniky a spotřebiteli (B2C), jako jsou ceny na úrovni obchodů, ceny založené na přidělení a věrnosti, kombinační slevy, množstevní slevy a mezní slevy. Cenový modul používá složitá pravidla k určení nejvhodnější ceny pro danou nabídku nebo objednávku.

Když používáte [duální zápis](./dual-write-overview.md), máte tři možnosti pro vaše potřeby něco ocenit. Můžete použít statické ceny, které vycházejí z ceníku v Dynamics 365 Sales, cenový modul Dynamics 365 Supply Chain Management nebo cenový modul v Dynamics 365 Commerce. Z těchto možností je pro scénáře B2C nejvhodnější cenový modul Commerce.

## <a name="use-the-commerce-pricing-engine-in-sales"></a>Používání cenového modulu Commerce v Sales

> [!NOTE]
> V současné době lze cenový modul Commerce použít pouze pro vytvoření nabídky v Sales. Integrace prodejní objednávky s cenovým modulem Commerce ještě není k dispozici.

Když uživatelé iniciují nabídku v Sales, zkopíruje architektura duálního zápisu podrobnosti nabídky do Commerce. Veškeré změny stávajících řádků nabídek nebo nově přidaných řádků nabídek v Sales jsou zkopírovány do Commerce. Pokud uživatelé chtějí k ocenění nabídky použít cenový modul Commerce, mohou si vybrat možnost **Cenová nabídka** a aktualizovat ceny nabídky na základě cenového modulu Commerce. Ceny se poté automaticky aktualizují v aplikacích Sales i Commerce.

## <a name="prerequisites"></a>Předpoklady

- Než budete moci použít cenový modul Commerce v Sales, musíte postupovat podle pokynů v části [Zpeněžení potenciálního zákazníka ve dvojím připisování](./dual-write-prospect-to-cash.md).
- Vyhodnocení obchodní dohody pro ruční zadávání musíte vypnout pomocí následujících kroků:

    1. V prostředí Commerce přejděte do nabídky **Pohledávky \> Nastavení \> Parametry pohledávek**.
    1. Na kartě **Ceny** na pevné záložce **Hodnocení obchodní smlouvy** vypněte zaškrtávací políčko **Ruční zadání**.

## <a name="additional-resources"></a>Další prostředky

[Zpeněžení potenciálního zákazníka ve dvojím připisování](./dual-write-prospect-to-cash.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]