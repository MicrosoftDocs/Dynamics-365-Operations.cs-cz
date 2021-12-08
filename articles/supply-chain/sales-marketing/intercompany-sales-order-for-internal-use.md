---
title: Vytvoření mezipodnikové prodejní objednávky pro interní použití
description: Toto téma vysvětluje postup vytvoření mezipodnikové prodejní objednávky pro interní použití
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 0718a1560ec42df2a0a12e8b81484aa3be46d2d8
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548144"
---
# <a name="create-an-intercompany-sales-order-for-internal-use"></a>Vytvoření mezipodnikové prodejní objednávky pro interní použití

[!include [banner](../../includes/banner.md)]

Mezipodniková prodejní objednávka se obvykle vytvoří automaticky na základě mezipodnikové nákupní objednávky. Mezipodnikovou prodejní objednávku můžete také vytvořit ručně, a ta pak vygeneruje mezipodnikovou nákupní objednávku v právnické osobě mezipodnikového odběratele.

![Mezipodnikový interní prodejní proces](media/intercompanyinternalsalesprocess.png)

## <a name="create-an-intercompany-sales-order-manually"></a>Ruční vytvoření mezipodnikové prodejní objednávky

Tyto kroky proveďte v rámci právnické osoby B, jak je uvedeno na obrázku.

1. Přejděte na **Pohledávky \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. V podokně Akce vyberte možnost **Prodejní objednávka** a vytvořte prodejní objednávku.
1. Na stránce **Vytvořit prodejní objednávku** vyberte účet odběratele. Na záložce **Obecné** se ujistěte, že je zaškrtnuto políčko **Mezipodnikové**. To znamená, že vybraný odběratel je mezipodnikovým odběratelem.
1. Zadejte nebo změňte informace a pak vyberte **OK** a vyplňte řádky objednávky jako obvykle.

    Hodnota pole **Doručovací adresa** je zkopírována z hlavičky mezipodnikové prodejní objednávky do hlavičky mezipodnikové nákupní objednávky. Hodnota pole **Číslo položky**, včetně rozměrů produktu, a hodnoty polí **Datum doručení** a **Kód měny** se zkopírují z řádků mezipodnikové prodejní objednávky do řádků mezipodnikové nákupní objednávky.

1. V záhlaví objednávky vyberte **Mezipodnikové** a zobrazte tak související mezipodnikové nákupní objednávky.
1. Na řádcích objednávky vyberte pole **Mezipodnikové** a zobrazte tak informace o skladových zásobách pro mezipodnikový obchod.

> [!TIP]
> Mezipodnikové prodejní objednávky můžete zobrazit na stránce **Mezipodnikové objednávky**.

> [!NOTE]
> Při práci s mezipodnikovou položkou doporučujeme vypnout zaškrtávací políčko **Odstranit objednávku po fakturaci** na stránce **Parametry pohledávek**. V opačném případě bude příslušná nákupní objednávka odstraněna. Doporučujeme také vypnout zaškrtávací políčko **Odstranit nákupní objednávku po fakturaci** na stránce **Parametry závazků**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]