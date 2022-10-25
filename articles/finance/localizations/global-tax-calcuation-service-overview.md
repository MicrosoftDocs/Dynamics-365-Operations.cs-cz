---
title: Přehled výpočtu daně
description: Tento článek vysvětluje celkový rozsah a funkce výpočtu daně.
author: EricWangChen
ms.date: 09/08/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.search.form: TaxIntegrationTaxServiceParameters
ms.openlocfilehash: cafc4c7089e0c042fc65c1e3fd21f8f1e930b785
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689877"
---
# <a name="tax-calculation-overview"></a>Přehled výpočtu daně

[!include [banner](../includes/banner.md)]

Výpočet daně je hyperškálovatelná multiklientová služba, která umožňuje globálnímu daňovému modulu automatizovat a zjednodušit proces stanovení a výpočtu daně. Daňový modul je plně konfigurovatelný. Mezi prvky, které lze konfigurovat, patří mimo jiné model zdanitelných dat, daňový kód, matice použitelnosti daně a vzorec výpočtu daně. Daňový modul běží na platformě základních služeb Microsoft Azure a nabízí moderní technologie a exponenciální škálovatelnost.

Služba výpočtu daní je integrována s Dynamics 365 Finance a Dynamics 365 Supply Chain Management. Kromě toho se také integruje s Dynamics 365 Project Operations, Dynamics 365 Commerce a dalšími aplikacemi prvních stran a jiných výrobců.

> [!IMPORTANT]
> Když povolíte Výpočet daně, některé operace se souvisejícími daty mohou být prováděny v jiném datovém centru než v datovém centru, které udržuje vaše data služby. Zkontrolujte [Smluvní podmínky](https://go.microsoft.com/fwlink/?linkid=2156043) před povolením Výpočtu daně. Ochrana vašich osobních údajů je pro nás důležitá. Chcete-li se dozvědět více, přečtěte si naše [Prohlášení o ochraně osobních údajů](https://go.microsoft.com/fwlink/?LinkId=521839).

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
- Brazílie
- Kanada
- Evropa
- Francie
- Indie
- Japonsko
- Jižní Afrika
- Švýcarsko
- Spojené arabské emiráty
- Spojené království
- Spojené státy

> [!NOTE]
> Výpočet daně nepodporuje dřívější verzi Dynamics 365, například Dynamics AX 2012 nebo místní nasazení Dynamics 365.

## <a name="versions"></a>Verze
Doporučujeme importovat a nastavit konfiguraci výpočtu daně s verzí, která odpovídá vaší verzi Finance nebo Supply Chain Management.

| Verze Finance nebo Supply Chain Management | Verze konfigurace daně               |
| --------------- | --------------------------------------- |
| 10.0.31         | Konfigurace výpočtu daně 40.56.240 |
| 10.0.30         | Konfigurace výpočtu daně 40.55.239 |
| 10.0.29         | Konfigurace výpočtu daně 40.55.236 |
| 10.0.28         | Konfigurace výpočtu daně 40.54.234 |
| 10.0.27         | Konfigurace výpočtu daně 40.54.234 |


## <a name="data-flow"></a>Tok dat

Zde je přehled procesu toku dat pro výpočet daně. 

1. V RCS zobrazujte a importujte konfigurace modelu zdanitelných dokumentů a konfigurace mapování modelu. Pokud musíte rozšířit konfigurace pro pokročilý scénář, viz [Přidejte datová pole do daňových konfigurací](tax-service-add-data-fields-tax-configurations.md).
2. V RCS můžete vytvářet nebo udržovat daňové funkce. Pomocí daňových funkcí můžete zachovat daňové sazby a pravidla daňové použitelnosti.
3. Po dokončení nastavení daňové funkce zveřejněte daňové konfigurace a daňové funkce z RCS do globálního úložiště.
4. Ve Finance vyberte, kterou verzi nastavení daňových funkcí použijete pro konkrétní právnickou osobu.
5. Ve Finance a Supply Chain Management provozujte transakce jako obvykle. Když je potřeba Výpočet daně, klient shromáždí informace z transakce, jako je prodejní objednávka nebo nákupní objednávka, a zabalí informace jako datovou část. Poté bude odeslán požadavek na výpočet daně.
6. Od klienta je přijata žádost o výpočet daně a výpočet je dokončen. Výsledek daně je poté vrácen klientovi.
7. Klient Dynamics 365 obdrží výsledek daně a výsledek výpočtu daně zobrazí na stránce DPH.

## <a name="supported-transactions"></a>Podporované transakce

Výpočet daně lze povolit transakcemi. 

V následující tabulce jsou uvedeny transakce podporované v odpovídající verzi.

| Verze | Transakce |
|---------|--------------|
| 10.0.29 | Periodické deníky |
| 10.0.28 | Platební deník dodavatele<br> Deník plateb odběratele | 
| 10.0.26 | Hlavní deníky<br> Deník faktur dodavatele |
| 10.0.23 | Volná faktura |
| 10.0.21| Prodej<br><ul><li>Prodejní nabídka</li><li>Prodejní objednávka</li><li>Potvrzení</li><li>Výdejka</li><li>Dodací list</li><li>Prodejní faktura</li><li>Dobropis</li><li>Vratka</li><li>Záhlaví – vedlejší náklady</li><li>Řádek - vedlejší náklady</li></ul>Nákup<br><ul><li>Nákupní objednávka</li><li>Potvrzení</li><li>Příjemka</li><li>Příjemka produktu</li><li>Nákupní faktura</li><li>Záhlaví – vedlejší náklady</li><li>Řádek - vedlejší náklady</li><li>Dobropis</li><li>Vratka</li><li>Nákupní žádanka</li><li>Řádek nákupní žádanky – vedlejší náklady</li><li>Požadavek na nabídku</li><li>Záhlaví požadavku na nabídku – vedlejší náklady</li><li>Řádek požadavku na nabídku – vedlejší náklady</li></ul>Zásoby<ul><li>Převodní příkaz – expedice</li><li>Převodní příkaz – příjem</li></ul>|

## <a name="supported-countriesregions"></a>Podporované země/oblasti

Výpočet daně lze spustit s podporovanými funkcemi lokalizace. V následující tabulce jsou uvedeny země/oblasti pro primární adresu právnické osoby.

| Verze | Země / oblast |
|---------|----------------|
| 10.0.26 | - Čína <br>- Česko<br>- Španělsko |
| 10.0.24 | Mexiko |
| 10.0.23 | - Thajsko <br>- Japonsko <br>- Malajsie <br>- Singapur |
| 10.0.22 | - Austrálie<br>- Bahrajn <br>- Kanada<br>- Egypt <br>- Hongkong – zvláštní administrativní oblast <br>- Kuvajt <br>- Nový Zéland <br>- Omán <br>- Katar <br>- Saúdská Arábie <br>- Jihoafrická republika <br>- Spojené arabské emiráty |
| 10.0.21 | - Rakousko <br>- Belgie <br>- Dánsko <br>- Estonsko <br>- Finsko <br>- Francie <br>- Německo <br>- Maďarsko <br>- Island <br>- Irsko <br>- Itálie <br>- Lotyšsko <br>- Litva <br>- Nizozemsko <br>- Norsko <br>- Polsko <br>- Švédsko <br>- Švýcarsko <br>- Spojené království <br>- Spojené státy |

Pro libovolnou zemi/oblast, která není lokalizována společností Microsoft, lze také povolit a spustit výpočet daně s dalšími globálními funkcemi.

## <a name="related-resources"></a>Související prostředky

[Začínáme s daňovou službou](./global-get-started-with-tax-calculation-service.md)

[Vícenásobné daňové identifikační číslo](./emea-multiple-vat-registration-numbers.md)

[Podpora daňové funkce u převodního příkazu](./tasks/tax-feature-support-for-transfer-order.md)

[Jak vytvořit rozšíření v daňové službě](./tax-service-add-data-fields-tax-integration-by-extension.md)
