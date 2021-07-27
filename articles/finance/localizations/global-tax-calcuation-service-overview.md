---
title: Výpočet daně (Preview)
description: Toto téma vysvětluje celkový rozsah a funkce výpočtu daně.
author: wangchen
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bab6e0e0ea1b9fb7f598e37843b52e3ba9c7f94e
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/03/2021
ms.locfileid: "6336625"
---
# <a name="tax-calculation-preview"></a>Výpočet daně (Preview)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Výpočet daně je hyperškálovatelná multiklientová služba, která umožňuje globálnímu daňovému modulu automatizovat a zjednodušit proces stanovení a výpočtu daně. Daňový modul je plně konfigurovatelný. Mezi prvky, které lze konfigurovat, patří mimo jiné model zdanitelných dat, daňový kód, matice použitelnosti daně a vzorec výpočtu daně. Daňový modul běží na platformě základních služeb Microsoft Azure a nabízí moderní technologie a exponenciální škálovatelnost.

Výpočet daně je integrován s Dynamics 365 Finance a Dynamics 365 Supply Chain Management. Kromě toho se také integruje s Dynamics 365 Project Operations, Dynamics 365 Commerce a dalšími aplikacemi prvních stran a jiných výrobců.

> [!IMPORTANT]
> Když povolíte službu Výpočet daně, některé operace se souvisejícími daty mohou být prováděny v jiném datovém centru než v datovém centru, které udržuje vaše data služby. Zkontrolujte [Smluvní podmínky](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) před povolením služby Výpočet daně. Ochrana vašich osobních údajů je pro nás důležitá. Chcete-li se dozvědět více, přečtěte si naše [Prohlášení o ochraně osobních údajů](https://go.microsoft.com/fwlink/?LinkId=521839).

Výpočet daně je daňový modul založený na mikroslužbách, který nabízí exponenciální škálovatelnost. Pomůže vám provést následující úlohy:

- Konfigurujte výpočet daně prostřednictvím služby Regulatory Configuration Service (RCS). RCS je vylepšená verze návrháře elektronických zpráv (ER) a je k dispozici jako samostatná služba.
- Nakonfigurujte daňovou matici tak, aby automaticky určovala daňové kódy a sazby.
- Nakonfigurujte daňovou matici tak, aby automaticky určovala daňové identifikační číslo (DIČ).
- Nakonfigurujte návrháře výpočtu daně tak, aby definoval vzorce a podmínky.
- Sdílejte řešení stanovení a výpočtu daně mezi právnickými osobami.

Chcete-li použít službu výpočtu daně, nainstalujte doplněk služby výpočtu daně ze svého projektu ve službách Microsoft Dynamics Lifecycle Services (LCS). Poté dokončete nastavení v RCS a povolte službu výpočtu daně v aplikacích Finance a Supply Chain Management. Více informací najdete v tématu [Začínáme s daňovou službou](./global-get-started-with-tax-calculation-service.md).

## <a name="availability"></a>Dostupnost

Výpočet daně je k dispozici pouze v prostředích sandbox a pro vybrané zákazníky, a to prostřednictvím programu Public Preview. Nakonec bude obecně k dispozici všem zákazníkům a v produkčních prostředích.

Budou dodávány nové funkce, proto nezapomeňte často zkontrolovat nejaktuálnější dokumentaci, abyste se dozvěděli o pokrytí a rozsahu podporovaných funkcí.

Výpočet daně je nasazen v následujících geografických oblastech Azure. Bude také nasazena do dalších geografických oblastí Azure, a to na základě potřeb zákazníků:

- Spojené státy americké
- Evropa

> [!NOTE]
> Výpočet daně nepodporuje místní nasazení Dynamics 365. Nepodporuje také dřívější verze, například Dynamics AX 2012.

## <a name="feature-highlights"></a>Zvýrazněné funkce

- Konfigurovatelná matice daní, která automaticky určuje a vypočítá daň
- Podpora více DIČ
- Podpora převodních příkazů pro stanovení a výpočet daně
- Podpora převodních příkazů pro určení více DIČ

## <a name="supported-transactions"></a>Podporované transakce

Výpočet daně může být povolen podle právnické osoby a transakce. Podporovány jsou následující transakce:

- Proces prodeje

    - Prodejní nabídka
    - Prodejní objednávka
    - Potvrzení
    - Výdejka
    - Dodací list
    - Prodejní faktura
    - Dobropis
    - Vratka
    - Záhlaví – vedlejší náklady
    - Řádek - vedlejší náklady

- Proces nákupu

    - Nákupní objednávka
    - Potvrzení
    - Příjemka
    - Příjemka produktu
    - Nákupní faktura
    - Záhlaví – vedlejší náklady
    - Řádek - vedlejší náklady
    - Dobropis
    - Vratka
    - Nákupní žádanka
    - Řádek nákupní žádanky – vedlejší náklady
    - Požadavek na nabídku
    - Záhlaví požadavku na nabídku – vedlejší náklady
    - Řádek požadavku na nabídku – vedlejší náklady

- Proces zásob

    - Převodní příkaz – expedice
    - Převodní příkaz – příjem

## <a name="related-resources"></a>Související prostředky

[Začínáme s daňovou službou](./global-get-started-with-tax-calculation-service.md)

[Vícenásobné daňové identifikační číslo](./emea-multiple-vat-registration-numbers.md)

[Podpora daňové funkce u převodního příkazu](./tasks/tax-feature-support-for-transfer-order.md)

[Jak vytvořit rozšíření v daňové službě](./tax-service-add-data-fields-tax-integration-by-extension.md)
