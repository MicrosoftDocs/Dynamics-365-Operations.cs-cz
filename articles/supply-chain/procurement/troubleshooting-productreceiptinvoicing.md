---
title: Řešení problémů s příjemkami a fakturací produktů
description: Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s příjemkami a fakturací produktů.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: d86fa3df1de13cc0e0fb94449207a326069da25b
ms.sourcegitcommit: 91e101d7a51a8b63bd196ec80e9224e5e6e6fc95
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/22/2020
ms.locfileid: "3834328"
---
# <a name="troubleshoot-product-receipts-and-invoicing"></a>Řešení problémů s příjemkami a fakturací produktů

Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s příjemkami a fakturací produktů.

## <a name="i-cant-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a>Nemohu zaúčtovat více než jednu fakturu za řádek nákupní objednávky, který obsahuje položky založené na kategoriích.

Množství je povinné, pokud chcete zaúčtovat faktury. Pokud tedy bylo celé množství řádku fakturováno pouze za částečnou částku, nebudete moci zbývající částku fakturovat na jiné faktuře.

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a>Během potvrzení nákupní objednávky se mi zobrazí chyba „Odkaz na objekt není nastaven“ nebo během zaúčtování faktury dodavatele dojde k výjimce „Byla vyvolána výjimka cílem vyvolání“.

K tomuto problému může dojít z důvodu nekonzistence v distribucích nákupních objednávek.

Chcete-li tento problém odblokovat a resetovat nákupní objednávku do stavu *Koncept*, přejděte na **Zásobování a zdroje \> Pravidelné úkoly \> Vyčistit \> Reset distribuce nákupní objednávky**. Další informace najdete v následujícím příspěvku na blogu: [Řešení chyb distribuce nákupní objednávky v Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="i-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a>Nemohu konsolidovat více příjemek produktu do jedné nákupní objednávky.

Nelze sloučit více příjemek produktu do jedné nákupní objednávky, pokud mají různé řádky příjemek produktu různá data zaúčtování.

V dřívějších verzích Microsoft Dynamics 365 Supply Chain Management byla konsolidace v této situaci povolena. Tento postup je však náchylný k chybám. Datum zaúčtování na řádcích nákupní objednávky, které jsou vytvořeny, by se nemělo lišit od účetního data na řádcích příjemky produktu, ze kterých byly tyto řádky nákupní objednávky vytvořeny. (Datum účtování na řádcích nákupní objednávky odpovídá datu účtování v záhlaví nákupní objednávky.) Konsolidace více příjemek produktu do jedné nákupní objednávky proto již není povolena.

Datum účtování se používá například pro rozpočtové rezervace a břemeno. Proto by mělo být uchováno během přechodu z příjemky produktu na nákupní objednávku.

## <a name="when-product-receipts-are-canceled-transactions-can-be-posted-to-a-suspended-ledger-account"></a>Když jsou zrušeny příjemky produktu, lze transakce zaúčtovat na pozastavený účet hlavní knihy.

### <a name="issue-description"></a>Popis problému

Pokud je příjemka produktu zrušena, systém umožňuje zaúčtování transakcí na pozastavené účty hlavní knihy, i když jsou pozastaveny hlavní účty.

### <a name="reproduce-the-issue"></a>Reprodukování problému

Následující postup ukazuje jeden způsob, jak reprodukovat problém.

1. Na stránce **Parametry závazků** na kartě **Obecné** se ujistěte, že možnost **Zaúčtovat příjemku produktu do hlavní knihy** je nastavena na *Ano*.
1. Vytvořte nákupní objednávku a přidejte řádek objednávky s množstvím *1 000* pro produkt.
1. Potvrďte nákupní objednávku.
1. Zaúčtujte příjemku produktu a zkontrolujte doklady.
1. Pozastavte příslušné hlavní účty, *200140* a *140200*.
1. Zrušte zaúčtovanou příjemku produktu.
1. Všimněte si, že transakce lze zaúčtovat na pozastavené účty hlavní knihy.

### <a name="issue-resolution"></a>Řešení problému

Transakce lze zaúčtovat na pozastavené účty hlavní knihy, když jsou zrušeny příjemky produktu, protože toto chování umožňuje správné zaúčtování.

## <a name="a-product-receipt-voucher-number-is-consumed-even-if-no-financial-voucher-is-generated-during-product-receipt"></a>Číslo dokladu příjemky produktu je spotřebováno, i když se během příjmu produktu nevygeneruje žádný finanční doklad.

Pokud je možnost **Časově rozlišit pasiva na příjemce produktu** nastavena na *Ne* pro skupinu modelů položek, nedojde k účtování do hlavní knihy. Fyzická událost však bude zaznamenána pro účely účtování v dílčí hlavní knize a tato událost vyžaduje číslo dokladu. Toto číslo dokladu je číslo dokladu, na které se odkazuje v transakcích zásob.

Doporučujeme nastavit možnost **Časově rozlišit pasiva na příjemce produktu** na *Ano*, jak je popsáno v následujícím příspěvku na blogu: [Zaúčtování vedlejších nákladů v době příjemky produktu](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).

## <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a>Nastavení možnosti Zaúčtovat na účet poplatků v hlavní knize není zapnuto.

### <a name="issue-description"></a>Popis problému

K tomuto problému dochází, když je nákupní objednávka fakturována, pokud je možnost **Zaúčtovat na účet poplatků v hlavní knize** nastavena na *Ano* na kartě **Faktura** stránky **Parametry závazků**.

### <a name="reproduce-the-issue"></a>Reprodukování problému

Následující postup ukazuje jeden způsob, jak reprodukovat problém.

1. Přejděte do nabídky **Závazky \> Nastavení \> Parametry závazků**.
1. Na kartě **Faktura** nastavte možnost **Zaúčtovat na účet poplatků v hlavní knize** na *Ano*.
1. Přejděte na **Řízení zásob \> Nastavit \> Zaúčtování \> Zaúčtování**.
1. Na kartě **Nákupní objednávka** se ujistěte, že jste odstranili všechny řádky v nákupních výdajích za produkt.
1. Přejděte na **Závazky \> Nákupní objednávky \> Všechny nákupní objednávky**.
1. Vytvoření nákupní objednávky. V poli **Účet dodavatele** vyberte *1001 kancelářské potřeby Acme*.
1. Přidejte řádek nákupní objednávky, který má následující nastavení:

    - **Číslo položky:** *Laserový projektor D0011*
    - **Lokalita:** *1*
    - **Sklad:** *11*
    - **Množství:** *4*

1. V podokně akcí na kartě **Nákup** ve skupině **Akce** zvolte **Potvrdit**.
1. V podokně Akce na kartě **Přijmout** ve skupině **Generovat** zvolte **Příjemka produktu**.
1. V dialogovém okně **Zaúčtování příjemky produktu** v poli **Příjemka produktu** zadejte libovolné číslo a poté vyberte **OK**.
1. V podokně akcí na kartě **Faktura** ve skupině **Generovat** zvolte **Faktura**.
1. V poli **Číslo** zadejte libovolné číslo jako číslo faktury.
1. Aktualizujte stav párování a zaúčtování.
1. Všimněte si, že nyní při generování faktury z nákupní objednávky se zobrazí následující chyba: „Číslo účtu pro typ transakce nákupního výdaje za produkt neexistuje.“

### <a name="issue-resolution"></a>Řešení problému

To závisí na nastavení parametrů pro faktury a skupiny faktur. Další informace najdete v následujícím příspěvku na blogu: [Účtování nákladů nákupu a odchylky zásob](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).
