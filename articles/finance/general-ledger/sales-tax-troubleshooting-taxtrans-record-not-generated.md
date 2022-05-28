---
title: Záznam TaxTrans se negeneruje
description: Toto téma poskytuje informace o řešení potíží, které mohou pomoci, když se záznam TaxTrans negeneruje.
author: qire
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 969d086c77b40b59495ae0d9e631579abf5e0ec6
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686400"
---
# <a name="taxtrans-record-isnt-generated"></a>Záznam TaxTrans se negeneruje

[!include [banner](../includes/banner.md)]

Pokud vyberete pro transakci možnost **Zaúčtování DPH**, ale stránka **Zaúčtování DPH** buď nezobrazuje žádné daňové řádky, nebo chybí daňový řádek, záznam **TaxTrans** se možná nevygeneroval.

[![Stránka Zaúčtování DPH neobsahuje žádné řádkové položky.](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)

Chcete-li tento problém vyřešit, postupujte podle pokynů v následujících částech.

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a>Kontrola DPH před zaúčtováním

1. Před zaúčtováním transakce na stránce **Zaúčtování faktury** vyberte ke kontrole výpočtu možnost **DPH**.

    [![Tlačítko DPH na stránce Zaúčtování faktury.](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)

2. Na stránce **Dočasné transakce DPH** zkontrolujte výsledek výpočtu. Pokud není vypočítána žádná daň, viz [Daň se nevypočítá nebo je částka daně nulová](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a>Nalezení záznamu TaxTrans ve všech zaúčtovaných DPH

1. Přejděte na k nabídce **Daň** \> **Dotazy a sestavy** \> **Dotazy na DPH** > **Zaúčtování DPH**.
2. V záhlaví sloupce **Doklad** vyberte symbol filtru a najděte záznam **TaxTrans**.
3. Pokud najdete záznamy o DPH, které hledáte, zkontrolujte datum. Pokud se datum liší od data záhlaví deníku, vytvořte požadavek na službu Microsoft pro další podporu.

    [![Zaúčtovaná stránka DPH.](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)

## <a name="debug-to-check-details"></a>Ladění ke kontrole podrobností

1. Informace o tom, jak ladit a zjistit, zda se správně vygenerovaly záznamy **TmpTaxWorkTrans** a **TaxUncommitted**, viz [Nesprávná hodnota pole v záznamu TaxTrans](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).
2. Je-li záznam **TaxTmpWorkTrans** nebo **TaxUncommitted** správně vygenerován, přidejte zarážku na **TaxPost::SaveAndPost()** a **Tax::SaveAndPost** k ladění důvodu, proč se nevložil záznam **TaxTrans**.

    [![Zarážky přidané v kódu.](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)

    [![Výsledky přidaných zarážek.](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)

## <a name="determine-whether-customization-exists"></a>Zjištění, zda existuje přizpůsobení

Pokud jste dokončili kroky v předchozích částech, ale problém se vám nepodařilo vyřešit, zjistěte, zda existuje přizpůsobení. Pokud neexistuje žádné přizpůsobení, vytvořte požadavek na službu Microsoft pro další podporu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
