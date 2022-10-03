---
title: Aktualizujte přenesený rozpočet po snížení nákupních objednávek a faktur
description: Tento článek popisuje, jak řídit, co se stane s přeneseným rozpočtem při zrušení nebo snížení nákupních objednávek a při snížení faktur.
author: TaylorVH
ms.date: ''
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: TaylorVH
ms.search.validFrom: 2022-02-01
ms.dyn365.ops.version: Version 1611
ms.search.form: LedgerFund
ms.openlocfilehash: 790f1e770fd77d5209436c1c89e0f6125aac150f
ms.sourcegitcommit: 1a7729a6ce4f3fcf68bdc4cfdad746a5553da3c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573039"
---
# <a name="update-the-carry-forward-budget-after-reductions-in-purchase-orders-and-invoices"></a>Aktualizujte přenesený rozpočet po snížení nákupních objednávek a faktur

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tento článek popisuje, jak řídit, co se stane s přeneseným rozpočtem při zrušení nebo snížení nákupních objednávek a při snížení faktur.

Informace o tom, jak jsou nákupní objednávky zpracovávány na konci roku, viz [Zpracovávejte nákupní objednávky na konci roku](/dynamicsax-2012/appuser-itpro/process-purchase-orders-at-year-end).

## <a name="turn-carry-forward-budget-reductions-for-invoice-variances-on-or-off"></a>Zapněte nebo vypněte snížení přeneseného rozpočtu pro odchylky faktur

Systém vždy může aktualizovast přenesený rozpočet, když je nákupní objednávka zrušena nebo snížena. Pokud však chcete aktualizovat přenesený rozpočet při snížení faktury, musíte zapnout funkci *Snížit přenesený rozpočet, když je faktura oproti nákupní objednávce snížena s odchylkou*. Správci mohou tuto funkci zapnout nebo vypnout jejím vyhledáním v pracovním prostoru **[Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)**.

## <a name="purchase-order-reductions-and-cancellations"></a>Snížení a zrušení objednávky

Bez ohledu na to, zda je zapnutá funkce *Snížit přenesený rozpočet, když je faktura oproti nákupní objednávce snížena s odchylkou*, bude přenesený rozpočet aktualizován, když je oprávněná nákupní objednávka zrušena nebo snížena. Každý fond hlavní knihy můžete nastavit tak, aby reagoval jedním z následujících způsobů:

- Zachovat přenesený rozpočet tak, jak byl vytvořen.
- Automaticky upravit přenesený rozpočet, abyste odstranili zrušenou nebo sníženou částku.

Pro automatickou úpravu rozpočtu jsou k dispozici pouze řádky nákupní objednávky, které mají distribuce obsahující fond. K automatické úpravě rozpočtu dochází, když je objednávka dokončena nebo je potvrzeno snížení objednávky.

## <a name="invoice-reductions"></a>Snížení faktury

Když je funkce *Snížit přenesený rozpočet, když je faktura oproti nákupní objednávce snížena s odchylkou* zapnutá, můžete zadat, jednotlivé fondy mají snížit přenesený rozpočet aktualizován, když dojde ke snížení faktury, vedle snížení nebo zrušení nákupní objednávky. Faktura musí být za nákupní objednávku, která má přenesený rozpočet. Snížení zahrnuje cenové rozdíly, rozdíly poplatků a daňové rozdíly. Když se během fakturace sníží přenesená nákupní objednávka, vytvoří se odchylka. Při zaúčtování faktury bude zatížení objednávky sníženo o částku odchylky. Funkce také vytvoří automatickou úpravu rozpočtu pro výši odchylky.

Pokud je vypnutá funkce *Snížit přenesený rozpočet, když je faktura oproti nákupní objednávce snížena s odchylkou*, přenesený rozpočet se v tomto scénáři nesníží. Zbývající přenesený rozpočet pro výši odchylky proto zůstává pozadu.

## <a name="configure-the-carry-forward-budget-options-for-each-fund"></a>Nakonfigurujte možnosti převodu rozpočtu pro každý fond

Postupujte podle těchto kroků pro každý fond hlavní knihy, který by měl být schopen snížit přenesený rozpočet při snížení nákupní objednávky nebo faktury.

1. Přejděte do části **Hlavní kniha \> Účtová osnova \> Fondy \> Fondy**.
1. Vyberte fond, který chcete nastavit.
1. V **Procesu nákupní objednávky na konci roku** se ujistěte, že je možnost **Přepsat vybranou možnost na konci roku** nastavena na *Ano*.
1. Ve **Stavu přeneseného rozpočtu** nastavte pole **Obnovte rozpočet při zrušení nebo snížení objednávky převodu** tak, jak požadujete. Nastavení má mírně odlišné účinky v závislosti na tom, zda je funkce *Snižte přenesený rozpočet, když je faktura oproti nákupní objednávce snížena s odchylkou* ve vašem systému zapnutá.

    - Když je funkce vypnutá, systém reaguje pouze na zrušené nebo snížené objednávky. Nastavení možností funguje následujícím způsobem:

        - *Ne* – Systém vytvoří záznam rozpočtové evidence pro zbývající zůstatek nákupních objednávek, které byly zrušeny nebo sníženy.
        - *Ano* – Systém umožňuje zrušit nebo snížit nákupní objednávky, ale nevytváří položku rozpočtového registru. Přenesený rozpočet zůstává k dispozici pro použití jinými dokumenty.

    - Když je funkce zapnutá, systém reaguje na odchylky faktur i na zrušené nebo snížené objednávky. Nastavení možností funguje následujícím způsobem:

        - *Ne* – Pro odchylky faktur systém vytvoří záznam rozpočtové evidence proti nákupní objednávce pro částku snížení odchylky. U zrušených nebo snížených objednávek má toto nastavení stejný účinek, jako když je funkce vypnuta.
        - *Ano* – U odchylek faktur systém umožňuje snížení faktury, ale nevytváří položku rozpočtové evidence. Přenesený rozpočet zůstává k dispozici pro použití jinými dokumenty. U zrušených nebo snížených objednávek má toto nastavení stejný účinek, jako když je funkce vypnuta.

## <a name="additional-resources"></a>Další prostředky

- [Zpracování nákupních objednávek na konci roku](/dynamicsax-2012/appuser-itpro/process-purchase-orders-at-year-end)
- [Udržovat rezervace účelových položek rozpočtu](general-budget-reservation-tasks.md)
- [Fondy ve veřejném sektoru](funds-public-sector.md)
- [Nastavení fondu ve veřejném sektoru](tasks/set-up-fund-public-sector.md)
