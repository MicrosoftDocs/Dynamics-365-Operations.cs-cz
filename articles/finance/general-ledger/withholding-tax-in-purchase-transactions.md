---
title: Srážková daň v nákupních transakcích
description: U prodejců, kteří podléhají srážkové dani, můžete přiřadit výchozí **Skupinu srážkové daně** na stránce **Všichni dodavatelé**.
author: roschlom
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: a1d1ddf108e5e79ca7684ecc26df1c016a0362bbec43868c7dfed6970a097a76
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731421"
---
# <a name="withholding-tax-in-purchase-transactions"></a>Srážková daň v nákupních transakcích

U prodejců, kteří podléhají srážkové dani, můžete přiřadit výchozí **Skupinu srážkové daně** na stránce **Všichni dodavatelé**.

1. Přejděte na **Navigační podokno > Moduly > Závazky > Dodavatelé > Všichni dodavatelé**.

2. Klikněte na příslušný účet dodavatele, klikněte na **Upravit**.

3. Na kartě **Faktura a doručení** nastavte pole **Vypočítat srážkovou daň** na **Ano**.

   > [!NOTE] 
   > Srážková daň se nebude počítat, pokud není možnost **Vypočítat srážkovou daň** pro tohoto dodavatele v datech zapnutá.

4. Vyberte skupinu srážkové daně ve **Skupině srážkové daně**.

5. Klikněte na možnost **Uložit**.

U položek / služeb, které podléhají srážkové dani, můžete přiřadit výchozí **Skupinu srážkové daně položky** ve volbě **Uvolněné produkty**.

1. Klikněte na **Navigační podokno > Moduly > Řízení informací o produktech > Produkty > Vydané produkty**.

2. Klikněte na příslušné číslo položky, klikněte na **Upravit**.

3. Na kartě **Nákup** klikněte na **Vypočítat srážkovou daň**.

   > [!NOTE] 
   > Srážková daň se nebude počítat, pokud není volba **Vypočítat srážkovou daň** nastavena na **Ano** pro tuto položku na kartě **Nákup** na stránce **Uvolněný produkt**.

4. Vyberte položku skupiny srážkové daně v seznamu **Skupina srážkové daně položky**.

5. Klikněte na možnost **Uložit**.

Skupiny srážkové daně a Skupiny srážkové daně položky lze přiřadit na stránkách: 

- **Nákupní objednávka**
- **Faktury dodavatele**
- **Deník faktur**

Výchozí skupina srážkové daně a skupina srážkové daně položky budou při vytváření **Nákupních objednávek** a/nebo **Nevyřízených faktur dodavatele** přeneseny do řádků. Pro **Deník faktur dodavatele** můžete zapnout možnost **Vypočítat srážkovou daň** a vybrat **Skupinu srážkové daně položky** na kartě **Obecné** v deníku.

Dočasná částka srážkové daně je k dispozici v poli **Upravená srážková daň** na kartě **Součty** na stránce **Nákupní objednávka**.

![V nákupní objednávce je zahrnuta srážková daň.](media/withholding-tax-adjusted.png)

Srážková daň se počítá v **Deníku plateb dodavatele**. Můžete ručně upravit příslušné kódy srážkové daně i skutečné částky srážkové daně na kartě **Srážková daň** na stránce **Vypořádat transakce**.

![Srážky lze ručně upravit na stránce Vyrovnat transakce.](media/withholding-tax-vendor-payment-tab.png)

Odvozená částka srážkové daně bude odečtena z platby dodavatele a zaúčtována na **Účet srážkové daně** v souvisejícím dokladu.

![Účet srážkové daně zobrazující související dokument.](media/withholding-tax-adjusted.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]