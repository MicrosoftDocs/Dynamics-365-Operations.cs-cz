---
title: Služba výpočtu daně (Preview)
description: Toto téma vysvětluje celkový rozsah a funkce služby výpočtu daní.
author: wangchen
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 518d3fda7b97e55d23beea6a1ba0e50b44a7aa0e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818217"
---
# <a name="tax-calculation-service-preview"></a>Služba výpočtu daně (Preview)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Služba výpočtu daně je hyperškálovatelná multiklientová služba, která umožňuje globálnímu daňovému modulu automatizovat a zjednodušit proces stanovení a výpočtu daně. Daňový modul je plně konfigurovatelný. Mezi prvky, které lze konfigurovat, patří mimo jiné model zdanitelných dat, daňový kód, matice použitelnosti daně a vzorec výpočtu daně. Daňový modul běží na platformě základních služeb Microsoft Azure a nabízí moderní technologie a exponenciální škálovatelnost.

Služba výpočtu daní je integrována s Dynamics 365 Finance a Dynamics 365 Supply Chain Management. Kromě toho se také integruje s Dynamics 365 Project Operations, Dynamics 365 Commerce a dalšími aplikacemi prvních stran a jiných výrobců.

Služba výpočtu daně je daňový modul založený na technologiích Microsoftu, který nabízí exponenciální škálovatelnost. Pomůže vám provést následující úlohy:

- Konfigurujte službu výpočtu daně prostřednictvím služby Regulatory Configuration Service (RCS). RCS je vylepšená verze návrháře elektronických zpráv (ER) a je k dispozici jako samostatná služba.
- Nakonfigurujte daňovou matici tak, aby automaticky určovala daňové kódy a sazby.
- Nakonfigurujte daňovou matici tak, aby automaticky určovala daňové identifikační číslo (DIČ).
- Nakonfigurujte návrháře výpočtu daně tak, aby definoval vzorce a podmínky.
- Sdílejte řešení stanovení a výpočtu daně mezi právnickými osobami.

Chcete-li použít službu výpočtu daně, nainstalujte doplněk služby výpočtu daně ze svého projektu ve službách Microsoft Dynamics Lifecycle Services (LCS). Poté dokončete nastavení v RCS a povolte službu výpočtu daně v aplikacích Finance a Supply Chain Management. Více informací najdete v tématu [Začínáme s daňovou službou](https://go.microsoft.com/fwlink/?linkid=2138482).

## <a name="availability"></a>Dostupnost

Služba výpočtu daně je k dispozici pouze v prostředích sandbox a pro vybrané zákazníky, a to prostřednictvím programu Public Preview. Nakonec bude obecně k dispozici všem zákazníkům a v produkčních prostředích.

Nové funkce budou i nadále dodávány ve službě výpočtu daně. Nezapomeňte proto často zkontrolovat nejaktuálnější dokumentaci, abyste se dozvěděli o pokrytí a rozsahu podporovaných funkcí.

Služba výpočtu daně je nasazena v následujících geografických oblastech Azure. Bude také nasazena do dalších geografických oblastí Azure, a to na základě potřeb zákazníků:

- Spojené státy americké
- Evropa
- Francie
- Spojené království

> [!NOTE]
> Služba výpočtu daně nepodporuje místní nasazení Dynamics 365. Nepodporuje také dřívější verze, například Dynamics AX 2012.

## <a name="feature-highlights"></a>Zvýrazněné funkce

- Konfigurovatelná matice daní, která automaticky určuje a vypočítá daň
- Podpora více DIČ pro daň z přidané hodnoty (DPH)
- Podpora převodních příkazů pro stanovení a výpočet daně
- Podpora převodních příkazů pro určení více DIČ pro DPH

## <a name="supported-transactions"></a>Podporované transakce

Služba výpočtu daně může být povolena podle právnické osoby a transakce. Podporovány jsou následující transakce:

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

[Začínáme s daňovou službou](https://go.microsoft.com/fwlink/?linkid=2138482)

[Vícenásobné daňové identifikační číslo](https://go.microsoft.com/fwlink/?linkid=2153387)

[Podpora daňové funkce u převodního příkazu](https://go.microsoft.com/fwlink/?linkid=2153388)

[Jak vytvořit rozšíření v daňové službě](https://go.microsoft.com/fwlink/?linkid=2138483)
