---
title: Mezisoučet souhrnu objednávek nezahrnuje daně z poplatků při použití přizpůsobených modulů souhrnu objednávek
description: Toto téma obsahuje pokyny k odstraňování problémů, které vám mohou pomoci, když používáte přizpůsobené moduly souhrnu objednávek a mezisoučet souhrnu objednávek nezahrnuje daně z poplatků ve scénáři „cena zahrnuje DPH“.
author: gvrmohanreddy
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-04-22
ms.openlocfilehash: 1a47561a3ac984bc554b5b93546592237c16cf18
ms.sourcegitcommit: 48d094d083c1bd45c3d72f8b666926b48ec7ae35
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2022
ms.locfileid: "8767950"
---
# <a name="order-summary-subtotal-doesnt-include-taxes-on-charges-when-using-customized-order-summary-modules"></a>Mezisoučet souhrnu objednávek nezahrnuje daně z poplatků při použití přizpůsobených modulů souhrnu objednávek

Toto téma obsahuje pokyny k odstraňování problémů, které vám mohou pomoci, když používáte přizpůsobené moduly souhrnu objednávek a mezisoučet souhrnu objednávek nezahrnuje daně z poplatků ve scénáři „cena zahrnuje DPH“.

## <a name="description"></a>Popis

V aplikaci Microsoft Dynamics 365 Commerce verze 10.0.27 byly provedeny následující změny ve scénáři „cena zahrnuje DPH“, aby bylo zajištěno konzistentní používání modulů souhrnu objednávek na stránkách webu elektronického obchodu.

- Byla přidána dvě nová pole: **TaxOnShippingCharge** a **TaxOnNonShippingCharges**.
- Rozhraní API **GetSalesOrderBySalesId** a **GetSalesOrderByTransactionId** mají přesné hodnoty pro následující pole ve scénáři „cena zahrnuje DPH“:

    - SubtotalSalesAmount
    - SubtotalAmountWithoutTax
    - SubtotalAmount
    - ShippingChargeAmount
    - OtherChargeAmount

Pokud však používáte přizpůsobené moduly souhrnu objednávek, mohou tyto změny ovlivnit hodnoty mezisoučtu souhrnu objednávek tím, že nezahrnou daně z poplatků.

## <a name="resolution"></a>Řešení

Pokud používáte přizpůsobené moduly souhrnu objednávek a nechcete zdědit změny v Commerce verze 10.0.27 a novější provedené ve scénáři „cena zahrnuje DPH“, postupujte podle pokynů v této části.

Návratem k předchozímu (před verzí 10.0.27) chování polí **salesTransaction.SubtotalAmount** a **salesTransaction.SubtotalAmountWithoutTax** souhrnu objednávky obnovíte zahrnutí celkové částky účtované daně (**TaxOnShippingCharge** a **TaxOnNonShippingCharges**) v částkách mezisoučtu (**SubtotalAmount** a **SubtotalAmountWithoutTax**).

Chcete-li se vrátit k předchozímu chování souhrnu objednávky, postupujte takto.

1. V Commerce headquarters otevřete stránku parametrů Commerce (**Maloobchod a obchod \> Nastavení centrály \> Parametry \> Parametry Commerce**).
1. V levém navigačním podokně vyberte **Parametry konfigurace**.
1. Přidejte následující konfigurační parametry a nastavte hodnotu každého z nich na **true**:

    - IsLegacyTaxOnChargeInSubtotalAmountIncludedInTaxIncusiveEnabled
    - IsLegacyOrderSummaryHydrationEnabled

> [!NOTE]
> Pokud jste dříve používali konfigurační parametr **IsUpdatedPriceIncludesTaxSubtotalCalculationEnabled** a chcete zachovat stejné chování také pro vlastnost **order.NetAmountWithoutTax**, přidejte konfigurační parametr **IsLegacyPriceIncludesTaxNetAmountWithoutTaxCalculationEnabled** a nastavte jeho hodnotu na **true**.

## <a name="additional-resources"></a>Další prostředky

[Skrytí informací o daňovém rozdělení v souhrnech objednávek](../hide-taxes-breakup.md)
