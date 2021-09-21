---
title: Nejčastější dotazy k zásobování
description: Toto téma poskytuje odpovědi na často kladené otázky (FAQ) týkající se funkce zásobování v Supply Chain Management.
author: kamaybac
ms.date: 05/31/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 09c99b88bc47609158805cdba1291ae462cda178
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475745"
---
# <a name="procurement-faq"></a>Nejčastější dotazy k zásobování

[!include [banner](../includes/banner.md)]

Toto téma poskytuje odpovědi na často kladené otázky (FAQ) týkající se funkce zásobování v Supply Chain Management.

## <a name="can-i-show-only-purchase-orders-that-i-created"></a>Mohu zobrazit pouze nákupní objednávky, které jsem vytvořil/a?

Tato funkce není aktuálně k dispozici.

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a>Mohu rezervovat zásoby a vytvořit transakce proti registrovaným zásobám na nákupní objednávce?

### <a name="issue-description"></a>Popis problému

I když jsou položky ve stavu *Registrováno* na nákupní objednávce, zásoby si stále můžete rezervovat. Jinými slovy můžete vytvářet transakce proti registrovaným zásobám.

### <a name="reproduce-the-issue"></a>Reprodukování problému

Následující postup ukazuje jeden způsob, jak reprodukovat problém.

1. Vytvoření nákupní objednávky.
2. Zaregistrujte řádek nákupní objednávky.
3. Všimněte si, že můžete generovat rezervace nebo transakce proti registrovaným zásobám.

### <a name="issue-resolution"></a>Řešení problému

Toto chování je záměrné. Očekává se, že registrované položky fyzicky dorazily do skladu nebo zásob a že jsou proto k dispozici k rezervaci.

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a>Mohu najít uživatele, který zrušil nákupní objednávku?

Tyto informace jsou sledovány pouze v případě, že je u objednávky možné provádět změny. Pokud používáte správu změn, můžete vidět, kdo změnu (zrušení) odeslal a kdo ji schválil.

## <a name="why-cant-i-link-a-purchase-agreement-to-an-existing-purchase-order"></a>Proč nemohu propojit nákupní smlouvu s existující nákupní objednávkou?

Po vytvoření nákupní objednávky musí být k nákupní objednávce přiřazena nákupní smlouva. Jinak nelze řádky nákupní objednávky přidružit k řádkům kupní smlouvy.

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a>Jaká kontrola spustí zprávu „Aktualizovat ceny a slevy zadané ručně nebo externí dokument“?

Když změníte datum odeslání, může se zobrazit zpráva „Aktualizovat ceny a slevy zadané ručně nebo externí dokument.“ Tuto zprávu obdržíte proto, že když se změní datum odeslání, může být spuštěna jiná obchodní nebo prodejní smlouva a způsobit změnu ceny. Změna data odeslání může také ovlivnit plány skladu a další související informace.

Zpráva se spustí vždy, když dojde ke změně některého z dat nebo některých dalších parametrů. Účelem zprávy je ujistit se, že jste si vědomi cenových změn, které mohou na základě těchto změn nastat.

Zpráva je výzvou k vyhodnocení obchodní smlouvy. Celý popis najdete v tématu [Zásady hodnocení obchodní smlouvy](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).

## <a name="why-cant-i-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a>Proč nemohu zaúčtovat více než jednu fakturu za řádek nákupní objednávky, který obsahuje položky založené na kategoriích?

Množství je povinné, pokud chcete zaúčtovat faktury. Pokud tedy bylo celé množství řádku fakturováno pouze za částečnou částku, nebudete moci zbývající částku fakturovat na jiné faktuře.
