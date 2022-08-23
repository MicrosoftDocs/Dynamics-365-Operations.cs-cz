---
title: Funkce registrační pokladny pro Norsko
description: Tento článek poskytuje přehled funkcí pokladny, které je dostupné pro Norsko v Microsoft Dynamics 365 Commerce a obsahuje pokyny pro nastavení funkcí.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-10-31
ms.openlocfilehash: 42eda805646dbb30b40528254a3137102e3075e4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292729"
---
# <a name="cash-register-functionality-for-norway"></a>Funkce registrační pokladny pro Norsko

[!include[banner](../includes/banner.md)]

Tento článek poskytuje přehled funkcí pokladny, které jsou dostupné pro Norsko v Dynamics 365 Commerce. Obsahuje také pokyny pro nastavení funkcí. Funkce jsou následující:

- Společné funkce pokladního místa (POS), které jsou dostupné zákazníkům ve všech zemích nebo oblastech. Jako příklad můžeme uvést možnost, která zabrání vytištění kopie příjemky více než jednou.
- Funkce specifické pro Norsko, jako jsou digitální podpisy pro prodejní transakce.

## <a name="overview-of-cash-register-functionality-for-norway"></a>Přehled funkce registrační pokladny pro Norsko

### <a name="common-pos-features"></a>Společné funkce POS

Chcete-li vědět o funkcích POS, které jsou dostupné zákazníkům ve všech zemích nebo oblastech, přejděte do tématu [Zdroje nápovědy pro Dynamics 365 Retail](../index.md).

Následující funkce lokalizace POS, které byly dříve implementovány a zpřístupněny zákazníkům ve všech zemích nebo oblastech, lze nyní používat speciálně pro Norsko:

- **Tisk textových polí na příjemku velkým písmem.** Můžete použít parametr **Velikost písma** v návrháři formátu příjemky, kterým určíte, že pro pole ve formátu příjemky má být použita velká velikost písma. (Velká velikost písma je přibližně dvojnásobná oproti obvyklé velikosti písma.) Tento parametr můžete například použít k vytištění indikátoru „Kopírovat“ na kopii příjemky velkými znaky.
- **Registrace tisku kopií příjemek v protokolu událostí auditu POS.** Můžete použít parametr **Audit** v profilu funkcí POS, čímž umožníte tisk kopií příjemek a registraci dalších událostí auditu POS. Události auditu jsou registrovány v databázi kanálů a v centrále. Události auditu můžete zobrazit na stránce **Události auditu**.
- **Zabranění opakovanému tisku kopie příjemky.** Když je parametr **Audit** povolen v profilu funkcí POS, oprávnění POS **Povolit tisk kopií příjemek** určuje, zda lze tisknout kopie příjemek. Je dostupná i možnost, která vám umožní zabránit vytištění kopie příjemky více než jednou.

Kromě toho byla pro Norsko implementována následující funkce POS, která je ale zpřístupněna zákazníkům ve všech zemích nebo oblastech:

- **Registrace dalších událostí v protokolu událostí auditu POS.** Pokud je v profilu funkce POS povolen parametr **Audit**, v protokolu událostí auditu POS jsou registrovány následující události:

    - Kontroly ceny
    - Přepsání daní
    - Opravy množství na řádcích
    - Vymazání transakcí z databáze kanálů

### <a name="norway-specific-pos-features"></a>Funkce POS specifické pro Norsko

Následující funkce POS specifické pro Norsko jsou povoleny, když je parametr **Kód ISO** v profilu funkcí POS nastaven na **Ne**.

#### <a name="digital-signing-of-sales-transactions"></a>Digitální podepisování prodejních transakcí

Každá prodejní transakce je digitálně podepsána. Podpis je vytvořen a zaznamenán do deníku transakcí POS ve stejnou dobu, kdy je transakce dokončena. Podpis je také dostupný v deníku, který je exportován pro účely auditu.

Podepisují se pouze transakce pro hotovostní prodej. Zde je několik příkladů transakcí, které jsou vyloučeny z procesu podepisování:

- Zálohy (vklad na účet odběratele).
- Zálohy pro prodejní objednávky (vklad objednávky odběratele)
- Vydání dárkového poukazu
- Neprodejní transakce (plovoucí zůstatek, odstranění úhrad apod.)

Podepsaná data jsou textový řetězec, který se skládá z následujících datových polí. Datová pole jsou oddělena středníky.

1. Předchozí podpis pro stejné POS (A nula \[**0**\] se použije pro první transakci.)
2. Datum transakce
3. Čas transakce
4. Pořadové číslo podepsané transakce
5. Částka transakce včetně daně
6. Částka transakce bez daně

Proces digitálního podepisování používá 1024bitový klíč RSA, který má funkci hash SHA-1 (RSA-SHA1-1024). K podepisování se používá certifikát, který je nainstalován v Commerce Scale Unit. Jedinečný identifikátor certifikátu (stopa) je zaznamenán spolu s podpisem.

Podpis je uložen v databázi obchodu a v databázi centrály (HQ) spolu s transakčními daty. Na záložce s náhledem **Fiskální transakce** na stránce **Transakce obchodu** můžete vidět podpis transakce spolu s daty transakce použitými k jejímu vygenerování.

#### <a name="receipts"></a>Účtenky

Příjemky pro Norsko mohou obsahovat další informace, které byly implementovány pomocí vlastních polí:

- **Název příjemky** – Do rozložení formátu příjemky můžete přidat pole pro identifikaci typu příjemky. Například prodejní doklad bude obsahovat text „příjemka“.
- **Pořadové číslo podepsané transakce** – Na příjemce může být uvedeno pořadové číslo podepsané transakce, které přidruží tištěnou příjemku s digitálním podpisem v databázi.
- **Součty na příjemce** – Vlastní pole pro součty na příjmce nezahrnují neprodejní částky z celkových částek transakcí. Neprodejní částky zahrnují částky za následující operace:

    - Zálohy (vklad na účet odběratele).
    - Zálohy pro prodejní objednávky (vklad objednávky odběratele)
    - Vydání dárkového poukazu
    - Přidání finančních prostředků na dárkový poukazu

#### <a name="x-and-z-reports"></a>Sestavy X a Z

Informace na sestavách X a Z vycházejí z norských požadavků. Například částky **Celkový hotovostní prodej** zahrnují pouze částky za hotovostní prodejní transakce a nezahrnují operace vydávání dárkových poukazů a zálohy. Celkový hotovostní prodej je také uveden podle skupiny položek a způsobu platby. Navíc kumulativní částky **Celková hodnota prodeje** a **Celková hodnota vratek** jsou spravovány a tištěny.

#### <a name="saf-t-cash-register-audit-file"></a>Soubor auditu registrační pokladny SAF-T

Deník transakcí POS můžete exportovat v předdefinovaném formátu standardního souboru auditu – daňová (SAF-T) registrační pokladna. Soubor auditu obsahuje informace o organizaci, příslušná hlavní data (jako jsou skupiny položek, položky a daňové kódy), data transakcí hotovostních prodejů spolu s podpisy těchto transakcí, data neprodejních událostí a data sestavy ke konci data.

Soubor auditu lze exportovat pro následující scénáře:

- Podle obchodu
- Všechny obchody
- Podle terminálu
- Všechny terminály

Sestavu jedné právnické osoby můžete odeslat i jménem jiné právnické osoby. V tom případě musíte spustit export z operující právnické osoby a jako odesílatele sestavy uvést vykazující právnickou osobu.

Formát registrační pokladny SAF-T je implementován v centrále prostřednictvím [elektronického výkaznictví](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md). 

## <a name="setting-up-commerce-for-norway"></a>Nastavení Commerce pro Norsko

Tato část popisuje nastavení, která jsou specifická a doporučená pro Norsko. Další informace naleznete v tématu [Zdroje nápovědy pro Dynamics 365 Retail](../index.md).

Chcete-li používat funkce specifické pro Norsko, musíte provést tyto úkoly:

- V primární adrese právnické osoby nastavte pole **Země/oblast** na **NOR** (Norsko).
- V profilu funkce POS každého obchodu, který se nachází v Norsku, nastavte pole **Kód POS** na **NO** (Norsko).

Zadejte také následující nastavení pro Norsko.

### <a name="set-up-the-legal-entity"></a>Nastavení právnické osoby

Ujistěte se, že je zadán název právnické osoby. Tento název bude vytištěn na sestavách X a Z.

Kromě toho na záložce s náhledem **Informace o bankovním účtu** v poli **Směrový kód banky** zadejte číslo organizace.

### <a name="set-up-value-added-tax-vat-per-norwegian-requirements"></a>Nastavení daně z přidané hodnoty (DPH) podle norských požadavků


Musíte vytvořit kódy DPH, skupiny daní DPH a skupiny DPH za zboží. Musíte také nastavit informace o DPH pro produkty a služby. Další informace o způsobu nastavení a použití DPH získáte v části [Přehled DPH](../../finance/general-ledger/indirect-taxes-overview.md).

Musíte také zadat skupiny DPH a povolit možnost **Ceny zahrnují DPH** pro obchody, které se nacházejí v Norsku.

### <a name="set-up-functionality-profiles"></a>Nastavení funkčních profilů

Musíte povolit auditování a nastavit číslování příjemek.

### <a name="update-pos-permissions-groups-and-individual-permission-settings-for-store-workers"></a>Aktualizace skupin oprávnění POS a individuálních nastavení oprávnění pro pracovníky v obchodu

Nastavte oprávnění **Povolit tisk kopie příjemky** na příslušnou hodnotu:

- **Vždy povolit** – Obsluha může vícekrát vytisknout kopii příjemky.
- **Povolit pouze jednou** – Obsluha může vytisknout kopii příjemky pouze jednou.
- **Povolit pouze jednou a pouze v případě, že je k dispozici databáze centrály** – Obsluha může vytisknout kopii příjemky pouze jednou a pouze v případě, že je dostupná databáze centrály prostřednictvím Commerce Data Exchange: služby v reálném čase, aby systém mohl ověřit, že v žádném obchodě nebyly dříve vytištěny žádné kopie příjemky.
- **Nikdy** – Obsluha nesmí vytisknout kopii příjemky.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Nakonfigurujte vlastní pole tak, aby bylo možné použít je ve formátech příjemky pro prodejní příjemky

Na stránce **jazykový text** přidejte následující záznamy popisků vlastního pole rozvržení účtenky. Upozorňujeme, že hodnoty **ID jazyka**, **ID textu** a **Text**, které jsou zobrazeny v tabulce, jsou jenom příklady. Lze je změnit tak, aby splňovaly vaše požadavky.

| ID jazyka | Text                   | ID textu |
|-------------|------------------------|---------|
| cs       | Název příjemky          | 900011  |
| cs       | Je dárkový poukaz           | 900012  |
| cs       | Celkem (prodej)          | 900013  |
| cs       | Celková daně (prodej)      | 900014  |
| cs       | Celkem s daní (prodej) | 900015  |
| cs       | Částka daně (prodej)     | 900016  |
| cs       | ID hotovostní transakce    | 900017  |

Na stránce **Vlastní pole** přidejte následující záznamy popisků vlastního pole rozvržení účtenky. Upozorňujeme, že hodnoty **ID textu titulku** musí odpovídat hodnotám **ID textu**, které jste zadali na stránce **Text jazyka**.

| Název                            | Typ    | ID textu titulku |
|---------------------------------|---------|-----------------|
| ReceiptTitle                    | Příjemka | 900011          |
| IsGiftCard                      | Příjemka | 900012          |
| SalesTotalExt                   | Příjemka | 900013          |
| TaxTotalExt                     | Příjemka | 900014          |
| TotalWithTaxExt                 | Příjemka | 900015          |
| AmountPerTaxExt                 | Příjemka | 900016          |
| CashTransactionSequentialNumber | Příjemka | 900017          |

> [!NOTE]
> Je důležité, abyste zadali správné názvy vlastních polí, jak jsou uvedeny v tabulce výše. Nesprávný název vlastního pole způsobí chybějící data v příjemkách.

### <a name="configure-receipt-formats"></a>Konfigurace formátů příjemky

Pro všechny požadované formáty příjemky změňte hodnotu pole **Chování tisku** na **Vždy tisknout**.

V Návrháři formátu příjemky přidejte následující vlastní pole do příslušných oddílů příjemky. Všimněte si, že názvy polí odpovídají jazykovým textům, které jste definovali v předchozím oddílu.

1. Záhlaví:

    - **Název příjemky** – Toto pole udává typ příjemky.
    - **ID hotovostní transakce** – Toto pole vytiskne pořadové číslo podepsané hotovostní transakce.

2. Řádky:

    - **Je dárkový poukaz** – Toto pole označuje řádek příjemky jako související s operací Vydání dárkového pouzkazu nebo Přidat na dárkový poukaz.

3. Zápatí:

    - **Celkem (prodej)** – Toto pole vytiskne celkovou částku hotovostního prodeje příjemky. Částka neobsahuje daň. Operace záloh a dárkových poukazů jsou vyloučeny.
    - **Daň celkem (prodej)** – Toto pole vytiskne celkovou částku daně hotovostního prodeje. Operace záloh a dárkových poukazů jsou vyloučeny.
    - **Celkem s daní (prodej)** – Toto pole vytiskne celkovou částku hotovostního prodeje příjemky. Částka zahrnuje daň. Operace záloh a dárkových poukazů jsou vyloučeny.
    - **Částka daně (prodej)** – Toto pole vytiskne částku daně hotovostního prodeje podle daňového kódu. Operace záloh a dárkových poukazů jsou vyloučeny.

Další informace o tom, jak pracovat s formáty příjemek, naleznete v tématu [Nastavení a návrh formátů příjmu](../receipt-templates-printing.md).

### <a name="configure-the-saf-t-cash-register-export-format"></a>Konfigurace formátu exportu registrační pokladny SAF-T

Konfigurace registrační pokladny SAF-T je k dispozici ke stažení z Microsoft Dynamics Lifecycle Services (LCS). Další informace získáte v tématu [Import konfigurací elektronického výkaznictví](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-import-ger-configurations.md). Musíte si stáhnout následující konfigurace:

- **Data maloobchodní sítě.verze.1** – Konfigurace datového modelu.
- **Data maloobchodní sítě DMM.verze.1.14** – Konfigurace mapování datového modelu.
- **Registrační pokladna NO SAF T.verze.1.20** – Konfigurace formátu.

Když konfigurace importujete, na stránce **Parametry Commerce** na kartě **Elektronické dokumenty** v poli **Formát exportu registrační pokladny SAF-T** vyberte název konfigurace formátu, která byla importována.

Musíte také namapovat potřebná hlavní data na předdefinované standardní kódy SAF-T. Další informace naleznete v dokumentaci k registrační pokladně SAF-T od norské daňové správy. Chcete-li vytvořit mapování, musíte nastavit nové pole **Kód registrační pokladny SAF-T** na následujících stránkách:

- Sk. položek
- Způsoby platby
- Kódy DPH

### <a name="configure-channel-components"></a>Konfigurace komponent kanálu

Chcete-li povolit funkce specifické pro Norsko, musíte nakonfigurovat komponenty kanálu. Další informace získáte v [pokynech k nasazení](emea-nor-fi-deployment.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
