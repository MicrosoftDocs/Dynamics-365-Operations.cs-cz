---
title: Srážková daň v prodejních transakcích
description: Tento článek uvádí kroky, jak se vyhnout výpočtu srážkové daně u vybraných zákazníků. Zákazníkům, kteří ve svých platbách ve váš prospěch určují srážkovou daň, můžete přiřadit výchozí skupinu srážkové daně.
author: kailiang
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 75a7fc62c1d493007f3aa88a723465828c557df7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910077"
---
# <a name="withholding-tax-in-sales-transactions"></a>Srážková daň v prodejních transakcích

Tento článek uvádí kroky, jak se vyhnout výpočtu srážkové daně u vybraných zákazníků. Zákazníkům, kteří ve svých platbách ve váš prospěch určují srážkovou daň, můžete přiřadit výchozí **Skupinu srážkové daně** na stránce **Odběratelé**. 

1. Přejděte na **Navigační podokno > Moduly > Pohledávky > Odběratelé > Všichni odběratelé**.

2. Klikněte na příslušný účet odběratele, klikněte na **Upravit**.

3. Na kartě **Faktura a doručení** nastavte pole **Vypočítat srážkovou daň** na **Ano**.

   > [!NOTE] 
   > Srážková daň se nebude počítat, pokud není možnost **Vypočítat srážkovou daň** pro tohoto odběratele v zapnutá v hlavních datech.

4. Vyberte skupinu srážkové daně ve **Skupině srážkové daně**.

5. Klikněte na možnost **Uložit**.

U položek / služeb, které podléhají srážkové dani, můžete přiřadit výchozí **Skupinu srážkové daně položky** ve volbě **Uvolněné produkty**.

1. Klikněte na **Navigační podokno > Moduly > Řízení informací o produktech > Produkty > Vydané produkty**.

2. Klikněte na příslušné číslo položky, klikněte na **Upravit**.

3. Na kartě **Prodej** klikněte na **Vypočítat srážkovou daň**.

   > [!NOTE] 
   > Srážková daň se nebude počítat, pokud není volba **Vypočítat srážkovou daň** nastavena na **Ano** pro tuto položku na kartě **Prodej** na stránce **Uvolněný produkt**.

4. Vyberte položku skupiny srážkové daně v seznamu **Skupina srážkové daně položky**.

5. Klikněte na možnost **Uložit**.

Skupiny srážkové daně a Skupiny srážkové daně položky lze přiřadit pomocí stránky **Prodejní objednávka**. 

Výchozí skupina srážkové daně a skupina srážkové daně položky se použijí jako výchozí záznamy na řádcích prodejní objednávky při vytváření nové prodejní objednávky.

Srážková daň se vypočítá a zaúčtuje s **Deníkem plateb odběratele**. Můžete ručně upravit příslušný kód srážkové daně i skutečnou částku srážkové daně na kartě **Srážková daň** na stránce **Vypořádat transakce**.

Vypočtená částka srážkové daně bude odečtena z platby odběratele a zaúčtována na **Protiúčet srážkové daně** v souvisejícím dokladu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
