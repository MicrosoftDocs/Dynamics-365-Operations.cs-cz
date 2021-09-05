---
title: Přehled výpočtu daně
description: Toto téma vysvětluje celkový rozsah a funkce výpočtu daně.
author: wangchen
ms.date: 08/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 72895cc18368ebf38818f30510cec999391c7910
ms.sourcegitcommit: 03f53980a4bc67b73ac2be76a3b3e7331d0db705
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/18/2021
ms.locfileid: "7394579"
---
# <a name="tax-calculation-overview"></a>Přehled výpočtu daně

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Výpočet daně je hyperškálovatelná multiklientová služba, která umožňuje globálnímu daňovému modulu automatizovat a zjednodušit proces stanovení a výpočtu daně. Daňový modul je plně konfigurovatelný. Mezi prvky, které lze konfigurovat, patří mimo jiné model zdanitelných dat, daňový kód, matice použitelnosti daně a vzorec výpočtu daně. Daňový modul běží na platformě základních služeb Microsoft Azure a nabízí moderní technologie a exponenciální škálovatelnost.

Výpočet daně je integrován s Dynamics 365 Finance a Dynamics 365 Supply Chain Management. Kromě toho se také integruje s Dynamics 365 Project Operations, Dynamics 365 Commerce a dalšími aplikacemi prvních stran a jiných výrobců.

> [!IMPORTANT]
> Když povolíte Výpočet daně, některé operace se souvisejícími daty mohou být prováděny v jiném datovém centru než v datovém centru, které udržuje vaše data služby. Zkontrolujte [Smluvní podmínky](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) před povolením Výpočtu daně. Ochrana vašich osobních údajů je pro nás důležitá. Chcete-li se dozvědět více, přečtěte si naše [Prohlášení o ochraně osobních údajů](https://go.microsoft.com/fwlink/?LinkId=521839).

Výpočet daně je daňový modul založený na mikroslužbách, který nabízí exponenciální škálovatelnost a může vám pomoci provést následující úkoly:

- Automaticky určit správnou skupinu DPH, skupinu DPH zboží a daňové kódy pomocí vylepšeného mechanismu určování.
- Podpora více daňových registračních čísel v jedné právnické osobě a automatické určení správného daňového registračního čísla u zdanitelných transakcí.
- Podpora stanovení, výpočtu, zaúčtování a vypořádání daně u převodních příkazů.
- Definovat konfigurovatelné vzorce a podmínky výpočtu daně pro vaše konkrétní obchodní požadavky.
- Sdílet řešení pro stanovení a výpočet daně mezi právnickými osobami, abyste ušetřili náklady na údržbu a předešli chybám.
- Podpora určení daňového registračního čísla zákazníka a dodavatele.
- Určení kódu seznamu podpory.
- Podpora parametrů výpočtu daně na úrovni daňové jurisdikce.

Chcete-li použít Výpočet daně, nainstalujte doplněk Výpočet daně ze svého projektu ve Microsoft Dynamics Lifecycle Services (LCS). Poté dokončete nastavení v [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/) a povolte Výpočet daně v aplikacích Finance a Supply Chain Management. Více informací najdete v tématu [Začínáme s daňovou službou](global-get-started-with-tax-calculation-service.md).

## <a name="availability"></a>Dostupnost

Od verze 10.0.21 je Výpočet daně obecně dostupný v produkčním prostředí všem zákazníkům.

Nové funkce budou i nadále dodávány. Kontrola nejaktuálnější plán vydání, abyste se dozvěděli o pokrytí a rozsahu podporovaných funkcí.

Výpočet daně je nasazen v následujících geografických oblastech Azure. Budou také přidány další geografické oblasti Azure na základě potřeb zákazníků.

- Asie a Tichomoří
- Austrálie
- Kanada
- Evropa
- Japonsko
- Spojené království
- Spojené státy americké

> [!NOTE]
> Výpočet daně nepodporuje dřívější verzi Dynamics 365, například Dynamics AX 2012 nebo místní nasazení Dynamics 365.

## <a name="data-flow"></a>Tok dat

Zde je přehled procesu toku dat pro výpočet tTax. 

1. V RCS zobrazujte a importujte konfigurace modelu zdanitelných dokumentů a konfigurace mapování modelu. Pokud musíte rozšířit konfigurace pro pokročilý scénář, viz [Přidejte datová pole do daňových konfigurací](tax-service-add-data-fields-tax-configurations.md).
2. V RCS můžete vytvářet nebo udržovat daňové funkce. Pomocí daňových funkcí můžete zachovat daňové sazby a pravidla daňové použitelnosti.
3. Po dokončení nastavení daňové funkce zveřejněte daňové konfigurace a daňové funkce z RCS do globálního úložiště.
4. Ve Finance vyberte, kterou verzi nastavení daňových funkcí použijete pro konkrétní právnickou osobu.
5. Ve Finance a Supply Chain Management provozujte transakce jako obvykle. Když je potřeba Výpočet daně, klient shromáždí informace z transakce, jako je prodejní objednávka nebo nákupní objednávka, a zabalí informace jako datovou část. Poté bude odeslán požadavek na výpočet daně.
6. Od klienta je přijata žádost o výpočet daně a výpočet je dokončen. Výsledek daně je poté vrácen klientovi.
7. Klient Dynamics 365 obdrží výsledek daně a výsledek výpočtu daně zobrazí na stránce DPH.

## <a name="supported-transactions"></a>Podporované transakce

Výpočet daně lze povolit transakcemi. 

Ve verzi 10.0.21 jsou podporovány následující transakce: 

- Prodej.

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

- Nákup

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

- Zásoby

    - Převodní příkaz – expedice
    - Převodní příkaz – příjem

## <a name="supported-countriesregions"></a>Podporované země/oblasti

Výpočet daně lze povolit dle právnické osoby. 

Ve verzi 10.0.21 jsou podporovány následující země/oblasti pro primární adresu právnické osoby:

- Rakousko
- Belgie
- Dánsko
- Estonsko
- Finsko
- Francie
- Německo
- Maďarsko
- Island
- Itálie
- Lotyšsko
- Litva
- Nizozemsko
- Norsko
- Polsko
- Švédsko
- Švýcarsko
- Spojené království
- Spojené státy americké

## <a name="related-resources"></a>Související prostředky

[Začínáme s daňovou službou](./global-get-started-with-tax-calculation-service.md)

[Vícenásobné daňové identifikační číslo](./emea-multiple-vat-registration-numbers.md)

[Podpora daňové funkce u převodního příkazu](./tasks/tax-feature-support-for-transfer-order.md)

[Jak vytvořit rozšíření v daňové službě](./tax-service-add-data-fields-tax-integration-by-extension.md)
