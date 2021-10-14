---
title: Časté dotazy týkající se prodejních objednávek
description: Tato stránka řeší často kladené otázky, které se objevují při práci s prodejními objednávkami v Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 3cee75b1d740e7cb414c674157dde0146e8faa50
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571610"
---
# <a name="sales-order-faqs"></a>Nejčastější dotazy k prodejní objednávce

Tato stránka řeší často kladené otázky, které se objevují při práci s prodejními objednávkami v Dynamics 365 Supply Chain Management.

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a>Mohu propojit nákupní objednávku s prodejní objednávkou, abych splnil/a poptávku?

Můžete vytvořit nákupní objednávku z prodejní objednávky. Další informace najdete ve [Vytvoření nákupní objednávky z prodejní objednávky](/dynamics365/supply-chain/sales-marketing/tasks/create-purchase-order-sales-order).

## <a name="can-i-cancel-or-delete-a-sales-order-or-return-order"></a>Můžu zrušit nebo odstranit prodejní objednávku nebo vrácenou objednávku?

Můžete zrušit pouze prodejní objednávky a vratky, které jsou ve stavu *Vytvořeno*. Další informace naleznete v tématu [Zrušení vratky](/dynamics365/supply-chain/service-management/cancel-return-order).

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a>Mohu obnovit fakturovanou prodejní objednávku, která byla odstraněna?

Pokud byla fakturovaná prodejní objednávka omylem odstraněna, můžete ji obnovit nebo zobrazit její podrobnosti.

Jděte na **Zákaznický účet \> Transakce \> Původní dokument \> Zobrazit podrobnosti**. Najděte fakturu, kterou hledáte, a jejím výběrem zobrazíte její podrobnosti. Mezi tyto podrobnosti patří odkaz na prodejní objednávku. Na této stránce byste také měli mít přístup k podrobnostem prodejní objednávky.

## <a name="how-do-i-delete-orphaned-sales-order-records"></a>Jak mám odstranit osamocené záznamy prodejní objednávky?

Chcete-li vyčistit osamocené záznamy prodejní objednávky, spusťte periodickou úlohu *Odstranění prodejní objednávky* přechodem na jedno z následujících míst:

- Prodej a marketing \> Periodické úkoly \> Vyčistit \> Odstranit prodejní objednávky
- Retail a Commerce \> Retail a Commerce IT \> Vyčistit \> Odstranit prodejní objednávky

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a>Existuje způsob, jak vypočítat provize z faktur, které již byly zaúčtovány?

Supply Chain Management aktuálně nepodporuje výpočet provizí za zaúčtované faktury.
