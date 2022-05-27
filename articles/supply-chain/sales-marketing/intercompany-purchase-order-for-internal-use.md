---
title: Vytvoření a fakturace mezipodnikové nákupní objednávky pro interní použití
description: Toto téma vysvětluje postup vytvoření a fakturace mezipodnikové nákupní objednávky pro interní použití
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 52b58b2dcecd5d9a83a47b425d6fb13b36c40b60
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675872"
---
# <a name="create-and-invoice-an-intercompany-purchase-order-for-internal-use"></a>Vytvoření a fakturace mezipodnikové nákupní objednávky pro interní použití

[!include [banner](../../includes/banner.md)]

Můžete vytvářet mezipodnikové nákupní objednávky pro mezipodnikového dodavatele. Tím se automaticky vytvoří mezipodniková prodejní objednávka u mezipodnikového dodavatele.

![Proces mezipodnikového interního nákupu](media/intercompanypurchaseprocess.png)

## <a name="create-an-intercompany-purchase-order-and-a-corresponding-intercompany-sales-order"></a>Vytvoření mezipodnikové nákupní objednávky a odpovídající mezipodnikové prodejní objednávky

Tyto kroky proveďte v rámci právnické osoby AAA, jak je uvedeno na obrázku.

1. Vyberte **Závazky** \> **Nákupní objednávky** \> **Všechny nákupní objednávky**.
1. Na stránce se seznamem **Všechny nákupní objednávky** vytvořte nákupní objednávku pro mezipodnikového dodavatele. Hodnoty pole se zkopírují z účtu dodavatele do nákupní objednávky.

    Vzhledem k tomu, že pracujete s mezipodnikovým dodavatelem, dojde v rámci právnické osoby, která odpovídá dodavateli, k vytvoření mezipodnikové prodejní objednávky. Číslo mezipodnikové prodejní objednávky může být stejné, jako číslo mezipodnikové nákupní objednávky, a může obsahovat ID právnické osoby. Použitá struktura čísla závisí na výběru v poli **Číslování prodejních objednávek** ve stránce **Mezipodnikové**. Například při vytvoření nákupní objednávky 00029\_064 v rámci právnické osoby AAA bude mít prodejní objednávka v rámci právnické osoby BBB číslo AAA00029\_64.

    Informační zpráva vám sdělí, že byla vytvořena mezipodniková nákupní objednávka a mezipodniková prodejní objednávka. Zpráva obsahuje jako referenci číslo mezipodnikové prodejní objednávky.

1. Přidejte řádkové položky do nákupní objednávky. Do mezipodnikové prodejní objednávky budou automaticky přidány odpovídající řádkové položky. Pokud položka neexistuje v rámci jiné právnické osoby, bude zobrazena zpráva a položky nebude možné přidat do nákupní objednávky. Chcete-li tento problém vyřešit, přejděte na jinou právnickou osobu a uvolněte produkt pro tuto právnickou osobu. Položky bude nyní možné přidat do prodejních objednávek u této právnické osoby. Potom se přepněte zpět na právnickou osobu z nákupní objednávky a pokračujte v přidávání řádkových položek.
1. Po dokončení zadávání informací pro nákupní objednávku akci vše potvrďte.

## <a name="process-the-intercompany-packing-slip-and-customer-invoice"></a>Zpracování mezipodnikového dodacího listu a faktury odběratele

Tyto kroky proveďte v rámci právnické osoby BBB, jak je uvedeno na obrázku.

1. Přejděte na **Pohledávky \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. Na stránce seznamu **Všechny prodejní objednávky** vyberte mezipodnikovou prodejní objednávku.
1. V podokně akcí vyberte kartu **Vyskladnit a zabalit** a poté vyberte **Dodací list**.
1. Zaškrtněte políčko **Zaúčtování**.
1. Vyberte **OK**. Dodací list je zaúčtován v rámci právnické osoby BBB.
1. Na stránce seznamu **Všechny prodejní objednávky** vyberte mezipodnikovou prodejní objednávku.
1. V části Podokno akcí vyberte kartu **Faktura** a potom vyberte možnost **Faktura**.
1. Zaškrtněte políčko **Zaúčtování**.
1. Vyberte **OK**.

    Dojde k zaúčtování faktury odběratele pro mezipodnikovou prodejní objednávku v rámci právnické osoby BBB.

## <a name="process-the-intercompany-product-receipt-and-vendor-invoice"></a>Zpracování mezipodnikové příjemky produktu a faktury dodavatele

Tyto kroky proveďte v rámci právnické osoby AAA, jak je uvedeno na obrázku.

1. Přejděte na **Závazky \> Nákupní objednávky \> Všechny nákupní objednávky**.
1. Na stránce seznamu **Všechny nákupní objednávky** vyberte mezipodnikovou nákupní objednávku.
1. V části Podokno akcí vyberte kartu **Příjemka** a potom vyberte možnost **Příjemka produktu**. Vytvoří se příjemka produktu. Číslo příjemky produktu je stejné jako číslo mezipodnikového dodacího listu.
1. Zaškrtněte políčko **Zaúčtování**.
1. Vyberte **OK**.
1. Na stránce seznamu **Všechny nákupní objednávky** vyberte mezipodnikovou nákupní objednávku.
1. V podokně akcí zvolte **Faktura** a poté vyberte **Faktura**. Bude vytvořena faktura dodavatele. Číslo faktury dodavatele je stejné jako číslo mezipodnikové faktury odběratele.
1. Dokončete zadávání faktury dodavatele a potom ji zaúčtujte.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
