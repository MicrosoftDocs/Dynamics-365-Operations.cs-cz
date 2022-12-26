---
title: Časté dotazy k aktivitám na konci roku
description: Tento článek uvádí otázky, které mohou vyvstat při uzavírání roku, a odpovědi, které mohou pomoci s činnostmi při roční uzávěrce.
author: moaamer
ms.date: 12/01/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2e33c1dcbfa4da74f2e8acc6e29f04fda3abd185
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853033"
---
# <a name="year-end-activities-faq"></a>Časté dotazy k aktivitám na konci roku 

[!include [banner](../includes/banner.md)]

Tento článek uvádí otázky, které mohou vyvstat při uzavírání roku, a odpovědi, které mohou pomoci s činnostmi při roční uzávěrce. Informace v tomto článku se primárně zaměřují na otázky ohledně aktivit roční uzávěrky pro hlavní knihu a závazky.

## <a name="general-ledger-year-end-enhancements"></a>Rozšíření roční uzávěrky v hlavní knize

Microsoft Dynamics 365 Finance verze 10.0.20 přinesla rozšíření roční uzávěrky. Toto rozšíření je ve výchozím nastavení povoleno od verze 10.0.25 a povinné od verze 10.0.29. Pokud vaše organizace používá verzi starší než 10.0.25, doporučujeme tuto funkci povolit před tím, než zahájíte proces roční uzávěrky. Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí pracovního prostoru **Správa funkcí** zkontrolovat stav funkce a zapnout ji v případě potřeby. Funkce je zde uvedena následujícím způsobem:

- **Modul**: Hlavní kniha
- **Název funkce**: Rozšíření roční uzávěrky v hlavní knize

Nastavení šablon roční uzávěrky se přesunulo na novou stránku nastavení **Nastavení šablony roční uzávěrky**. Stávající stránka roční uzávěrky bude podobná jako stránka **Přecenění cizí měny v hlavní knize**, kde se při každém spuštění nebo zrušení roční uzávěrky zobrazí seznam. Na stránce se nebudou zobrazovat historické informace o ročních uzávěrkách, které byly provedeny před povolením této funkce. Vedoucí účetní může zahájit roční uzávěrku z nové stránky.

Pokud chcete stornovat roční uzávěrku, vyberte poslední fiskální rok pro příslušnou právnickou osobu a potom vyberte možnost **Stornovat roční uzávěrku**. Stornováním se odstraní účetní záznamy za předchozí roční uzávěrku a roční uzávěrka se opětovně nespustí automaticky. Pokud povolíte funkci **Rozšíření hlavní knihy na konci roku** poté, co jste dokončili roční uzávěrku, a chcete stornovat historické výsledky na konci roku, spusťte historickou roční uzávěrku znovu poté, co povolíte parametr hlavní knihy **Odstranit existující záznamy roční uzávěrky při opětovné uzávěrce**.

Roční uzávěrku můžete znovu spustit restartováním procesu pro fiskální rok a právnickou osobu. Proces bude i nadále používat nastavení parametru hlavní knihy, aby určil, zda bude opakování roční uzávěrky zohledňovat pouze nové nebo změněné transakce, nebo zda se proces opakovaně provede pro všechny transakce a zcela zruší předchozí uzávěrku.

## <a name="general-ledger-the-general-ledger-year-end-enhancements-feature-is-enabled-why-cant-i-view-my-previous-year-closings-in-the-history-section-of-the-year-end-close-page"></a>Hlavní kniha: Funkce rozšíření hlavní knihy na konci roku je povolena. Proč nemohu zobrazit své uzávěrky za předchozí rok v části Historie na stránce Roční uzávěrka?

Před zapnutím funkce **Rozšíření hlavní knihy na konci roku** je sledován datum a čas, kdy byl spuštěn poslední proces roční uzávěrky. Historie nebyla sledována při každé roční uzávěrce. Z tohoto důvodu není možné zobrazit podrobnosti o každém spuštění roční uzávěrky. Po povolení této funkce jsou následné informace o procesu roční uzávěrky zachovány. Doklady ze všech procesů roční uzávěrky, dokonce i z těch, které byly spuštěny před povolením funkce, lze zobrazit na stránce **Transakce dokladů**. 

## <a name="general-ledger-the-year-end-close-process-is-failing-because-of-the-following-error-the-year-end-close-cant-be-run-because-one-or-more-ledger-transactions-posted-into-the-fiscal-year-that-you-are-closing-were-settled-to-a-ledger-transaction-in-a-different-fiscal-year-what-does-this-error-mean"></a>Hlavní kniha: Proces roční uzávěrky selhává kvůli následující chybě: „Roční uzávěrku nelze provést, protože jedna nebo více transakcí hlavní knihy zaúčtovaných do fiskálního roku, který uzavíráte, byly vyrovnány s transakcí hlavní knihy v jiném fiskálním roce.” Co tato chyba znamená?

Protože je povolena funkce **Sledování mezi vyrovnáním hlavní knihy a roční uzávěrkou**, jsou z počátečního zůstatku vyloučeny pouze vyrovnané transakce hlavní knihy z fiskálního roku, který se uzavírá. Toto chování způsobuje, že debety a kredit nejsou vyrovnané. Další informace naleznete v tématu [Sledování mezi vypořádáním hlavní knihy a roční uzávěrkou](awareness-between-ledger-settlement-year-end-close.md).

## <a name="general-ledger-reversal-of-the-year-end-close-process-is-failing-because-of-the-following-error-the-year-end-close-for-112022-cant-be-reversed-because-beginning-balance-transaction-have-been-ledger-settled-in-fiscal-year-112023-what-does-this-error-mean"></a>Hlavní kniha: Storno procesu roční roční uzávěrky selhává kvůli následující chybě: „Roční uzávěrku z 1. 1. 2022 nelze stornovat, protože transakce počátečního zůstatku byly vyrovnány v účetní knize ve fiskálním roce 1. 1. 2023.” Co tato chyba znamená?

Protože je povolena funkce **Sledování mezi vyrovnáním hlavní knihy a roční uzávěrkou**, není povoleno storno zpracování na konci roku, pokud byly počáteční transakce vyrovnány v novém fiskálním roce. Před stornováním účetní roční uzávěrky k 1. lednu 2022 proveďte storno vyrovnání hlavní knihy v novém fiskálním roce 2023. Případně znovu uzavřete rok k 1. lednu 2022, ale pouze pro nové opravné položky. Pokud chcete znovu uzavřít rok pouze kvůli úpravám, zakažte parametr hlavní knihy **Odstranit existující záznamy na konci roku při opětovném uzavření roku**.

## <a name="general-ledger-why-isnt-the-ledger-settlement-automation-processing-decembers-ledger-settlement-transactions"></a>Hlavní kniha: Proč automatizace vyrovnání hlavní knihy nezpracovává prosincové transakce vyrovnání hlavní knihy?

Funkce **Automatizace vyrovnání hlavních knih** spustí automatizaci pro transakce, které jsou datovány od prvního dne fiskálního roku do aktuálního data, kdy je výskyt spuštěn. U fiskálních roků, které končí 31. prosince, budete možná muset upravit datum spuštění události tak, aby byla spuštěna v prosinci. Například automatizace je nastavena tak, aby se spouštěla každý první den v měsíci. Tato automatizace bude spuštěna 1. prosince 2022 a její spuštění je naplánováno na 1. ledna 2023. Doporučujeme, abyste změnili událost z 1. lednu 2023 tak, aby byla spuštěna 31. prosinci 2022. Tato změna zajistí, že pro automatické vyrovnání budou brány v úvahu transakce s datem 2. až 31. prosince.

## <a name="general-ledger-whats-the-difference-between-the-reverse-year-end-close-action-and-the-delete-existing-year-end-entries-when-reclosing-parameter-for-year-end-close"></a>Hlavní kniha: Jaký je rozdíl mezi akcí Storno roční uzávěrky a parametrem Odstranit existující záznamy na konci roku při opětovném uzavření roku?

Kvůli rozdílu mezi akcí **Storno roční uzávěrky** a parametrem **Odstranit existující záznamy na konci roku při opětovném uzavření roku** v hlavní knize může docházet k nejasnostem (**Hlavní kniha \> Nastavení hlavní knihy \> Parametry hlavní knihy**).

Pokud při spuštění procesu roční uzávěrky vyberete akci **Storno roční uzávěrky**, dojde k odstranění všech konečných i počátečních zůstatků, jako by roční uzávěrka nikdy nebyla spuštěna. V takovém případě budou vymazány doklady. Roční uzávěrka se znovu automaticky nespustí. Pokud chcete spustit roční uzávěrku, vyberte akci **Spustit roční uzávěrku**.

Parametr v hlavní knize **Odstranit existující záznamy na konci roku při opětovném uzavření roku** se používá pouze tehdy, když spouštíte (nikoliv stornujete) roční uzávěrku. Pokud je parametr nastaven na **Ano**, veškeré konečné i počáteční zůstatky budou odstraněny a roční uzávěrka bude opět spuštěna. Tato možnost je určena pro organizace, které chtějí všechny transakce, včetně vyrovnání od poslední roční uzávěrky, zaúčtovat jako jednu účetní položku pro konečné a počáteční zůstatky. Pokud je tento parametr nastaven na **Ne**, všechny konečné a počáteční zůstatky zůstanou. Nejsou vymazány. Místo toho bude nový konečný a počáteční zůstatek vytvořen pouze pro deltu nebo nové transakce, které byly zaúčtovány od poslední roční uzávěrky pro daný fiskální rok.

> [!NOTE]
> Konečný zůstatek je vytvořen v uzavíraném roce. Platí to pouze v případě, že parametr hlavní knihy **Vytvořit uzávěrkové transakce při převodu** je nastaven na **Ano**. Počáteční zůstatek je vytvořen vždy, protože se jedná o zahajovací zůstatek pro následující rok.

## <a name="general-ledger-what-is-the-difference-between-close-all-and-close-single-options-on-the-transfer-profit-and-loss-dimension-section-of-the-year-end-close-process"></a>Hlavní kniha: Jaký je rozdíl mezi možnostmi „Uzavřít vše” a „Uzavřít jednotlivé” v části Převod dimenze zisku a ztráty v procesu roční uzávěrky?

Možnost **Uzavřít vše** udržuje původní hodnoty finanční dimenze ze zaúčtovaných transakcí a používá je pro vytvoření počátečních zůstatků pro účet nerozdělených zisků. Vytvoří se samostatné počáteční zůstatky nerozdělených zisků pro každou jedinečnou kombinaci hodnot finančních dimenzí. Pokud je zvolena možnost **Uzavřít jednotlivě**, všechny transakce zaúčtované s touto finanční dimenzí budou shrnuty do počátečního zůstatku nerozdělených zisků pro hodnotu dimenze zadanou v poli po **Uzavřít jednotlivé**. 

Například s účetní strukturou Hlavní účet – oddělení byly zaúčtovány všechny transakce pro daný fiskální rok. Ve finanční dimenzi oddělení v šabloně je vybrána možnost **Uzavřít jednotlivé** a je zadána hodnota 100 jako hodnota dimenze. Pokud celkový příjem u všech transakcí zaúčtovaných do oddělení 200, 300 a 400 činí 100 000 USD, bude vytvořen jeden počáteční zůstatek pro Nerozdělené zisky – 100. Pokud vyberete možnost **Uzavřít jednotlivě**, avšak ponecháte pole pro hodnotu finanční dimenze prázdné, všechny transakce se zaúčtují do nerozdělených zisků, přičemž tato hodnota dimenze nebude zadána.

## <a name="general-ledger-when-i-select-close-single-option-on-the-transfer-profit-and-loss-dimension-section-of-the-year-end-close-process-will-my-detailed-transactional-information-be-lost"></a>Hlavní kniha: Když v části Přenos dimenze zisku a ztráty v procesu roční roční uzávěrky zvolím možnost „Uzavřít jednotlivě”, ztratí se podrobné informace o transakcích?

Volby **Uzavřít vše** a **Uzavřít jednotlivě** slouží k určení, které finanční dimenze transakcí zaúčtovaných na účty zisků a ztrát budou převedeny na hlavní účet nerozděleného zisku. Historické, podrobné zaúčtování do účtů zisku a ztráty není ovlivněno a zůstane podrobné. Tato možnost ovlivňuje úroveň podrobnosti, která se v novém roce přenáší na účty nerozděleného zisku jako počáteční zůstatek. 

## <a name="general-ledger-the-year-end-close-process-is-failing-because-the-reporting-currency-for-the-year-does-not-balance-what-does-this-mean"></a>Hlavní kniha: Proces roční uzávěrky selhává, protože měna vykazování za rok není vyrovnaná. Co to znamená?

Tato chyba se může vyskytnout po povolení funkce **Sledování mezi vyrovnáním hlavní knihy a roční uzávěrkou** (funkce Sledování). Pokud je tato funkce povolena, transakce hlavní knihy, které byly vyrovnány, již nebudou zahrnuty do počátečního zůstatku příštího fiskálního roku při spuštění uzávěrky hlavní knihy na konci roku. Vyloučení transakcí z hlavní knihy, které jsou vyrovnány, může pro zákazníky představovat problém při roční uzávěrce, pokud je hlavní kniha definována s měnou vykazování.   
Vyrovnání hlavní knihy se provádí pouze pro zúčtovací měnu.  Při vyrovnání transakcí v hlavní knize se ověření pouze ujistí, že se debety v zúčtovací měně rovnají kreditům v měně účetnictví. Částky v měně vykazování pro tyto transakce v hlavní knize nejsou ověřeny a debety se nemusí rovnat kreditům.  Kromě toho se při vyrovnání v hlavní knize automaticky nevypočítá a nezaúčtuje zisk/ztráta v měně vykazování.  Vzhledem k těmto omezením musí transakce zisku/ztráty při vyrovnávání hlavní knihy existovat v měně vykazování.  Pokud není zisk/ztráta zahrnuta do vyrovnání hlavní knihy, bude výsledkem roční uzávěrky zpráva o nevyrovnanosti.  Další informace naleznete v tématu [Sledování mezi funkcí vyrovnání hlavní knihy a měnou vykazování je nevyrovnané](reporting-currency-yec.md).

## <a name="general-ledger-what-can-be-changed-to-help-enhance-the-performance-of-year-end-processing"></a>Hlavní kniha: Co lze změnit, aby se zvýšila výkonnost zpracování na konci roku?

Můžete provést několik změn, které pomohou zlepšit výkonnost roční uzávěrky. Doporučujeme, abyste tyto navrhované změny posoudili a zjistili, zda jsou pro vaši organizaci vhodné.

### <a name="optimize-year-end-close-service"></a>Služba optimalizace roční uzávěrky

Služba **Optimalizace roční uzávěrky** umožňuje zákazníkům Microsoft Dynamics 365 Finance urychlit roční uzávěrku přesunutím náročného zpracování na konci roku do mikroslužby. Čas, který se ušetří díky efektivní roční uzávěrce, umožňuje každému finančnímu týmu včas reagovat na požadované úpravy, které končí generováním finančních sestav. Zpracováním roční uzávěrky v mikroslužbě se uvolní cenné prostředky. Zvýšení zpracování minimalizuje vytížení SQL Serveru a dává zákazníkům možnost urychlit zpracování roční uzávěrky.

Služba **Optimalizace roční uzávěrky** je dostupná ve verzi 10.0.31, takže novou službu může pro období roční uzávěrky 2022 využívat více zákazníků. Kromě toho byla služba zpětně vložena do verzí 10.0.30 a 10.0.29. Další informace najdete v tématu [Optimalizace roční uzávěrky](optimize-year-end-close.md).

### <a name="dimension-sets"></a>Sady dimenzí

Při provedení roční uzávěrky se znovu vytvoří zůstatek každé sady dimenzí. Toto chování má přímý dopad na výkon. Některé organizace vytvářejí sady dimenzí zbytečně, protože byly kdysi použity nebo by mohly být někdy použity. Vzhledem k tomu, že tyto nepotřebné sady dimenzí jsou během roční uzávěrky obnovovány, dochází k prodloužení procesu. Věnujte čas vyhodnocení svých sad dimenzí a odstraňte všechny nepotřebné sady.

Nepotřebné sady dimenzí také ovlivní dávkovou úlohu **BudgetDimensionFocusInitializeBalance** (**Hlavní kniha \> Účtová osnova \> Dimenze \> Sady finančních dimenzí**).

[![Sady finančních dimenzí](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>Konfigurace šablon roční uzávěrky

Šablona roční uzávěrky umožňuje organizacím zvolit úroveň finanční dimenze, která se má zachovat při převodu zůstatků zisků a ztrát do nerozděleného zisku. Nastavení umožňují organizaci uchovat podrobné finanční dimenze při přesunu zůstatků do nerozděleného zisku (**Zavřít vše**) nebo shrnout částky do jedné hodnoty dimenze (**Zavřít jednu**). Lze to definovat pro každou finanční dimenzi. Další informace o těchto nastaveních naleznete v tématu [Roční uzávěrka](year-end-close.md).

Pro zlepšení výkonu doporučujeme vyhodnotit požadavky vaší organizace a zavřít co největší počet dimenzí pomocí možnosti roční uzávěrky **Zavřít jednu**. Při zavření jedné hodnoty dimenze (což může být také prázdná hodnota) systém počítá méně podrobností při rozhodování o zůstatcích pro účetní položky nerozděleného zisku.

### <a name="degenerate-dimensions"></a>Degenerované dimenze

Degenerovaná dimenze sama o sobě a v kombinaci s jinými rozměry poskytuje jen malé nebo žádné opětovné využití. Existují dva různé typy degenerovaných dimenzí. První typ je dimenze, která je individuálně degenerovaná. Obvykle se tento typ degenerované dimenze objeví pouze u jedné transakce nebo u malých sad transakcí. Druhým typem je dimenze, která se stává degenerovanou v kombinaci s jednou nebo více dalšími dimenzemi, které vykazují stejný potenciál na základě možných permutací, které lze generovat. Degenerovaná dimenze může mít významný dopad na výkonnost procesu roční uzávěrky. Pokud chcete minimalizovat problémy s výkonem, definujte všechny degenerované dimenze jako **Uzavřít jednotlivě** v nastavení roční uzávěrky, jak je popsáno v předchozí části.

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2022"></a>Závazky: Jaké proběhly změny na podporu vykazování formulářem 1099 na konci roku 2022?

#### <a name="update-to-all-1099-forms"></a>Aktualizace všech formulářů 1099

Ve všech formulářích 1099 byly pro zdaňovací období 2022 provedeny následující změny:

- V roce 2021 byl na formulářích 1099 stanoven rok. Od roku 2022 se rok vyplňuje podle sestavy.

#### <a name="1099-misc"></a>1099-MISC

Ve formuláři 1099-MISC byly pro zdaňovací období 2022 provedeny následující úpravy:

- Pole 13: Nyní označuje požadavek na vyplnění zákona o dodržování daňových předpisů u zahraničních účtů (FATCA).
- Pole 14: Nyní se používá pro vykazování nadměrných plateb tzv. zlatého padáku.
- Pole 15: Nyní se používá pro vykazování plateb v rámci nekvalifikovaných plánů odloženého odměňování (NQDC).
- Pole 16: Nyní se používá pro hlášení státem sražených daní.
- Pole 17: Nyní se používá k uvedení čísla státu plátce.
- Pole 18: Nyní se používá pro vykazování státních příjmů.

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Závazky: 1099 – Jak změním pole a hodnoty formuláře 1099 pro dodavatele, který během roku nesledoval informace potřebné pro formulář 1099?

Pomocí funkce **Aktualizovat 1099** projděte dříve zaplacené transakce faktur a znovu přiřaďte data formuláře 1099 vhodným způsobem podle nastavení na kartě **Daň 1099** na stránce **Dodavatel**. Pokud chcete použít funkci **Aktualizovat 1099**, přejděte do části **Závazky \> Dodavatelé \> Všichni dodavatelé**, vyberte dodavatele a poté na panelu akcí na kartě **Dodavatel** vyberte možnost **Aktualizovat 1099**.

## <a name="can-i-run-the-update-1099-functionality-for-all-my-vendors-at-once"></a>Mohu spustit funkci Aktualizovat 1099 pro všechny dodavatele najednou?

Na stránce **Aktualizace informací formuláře 1099 pro více dodavatelů** můžete aktualizovat pole 1099 na záznamu dodavatele a aktualizovat transakce pomocí informací z pole 1099. Pokud chcete otevřít tuto stránku, přejděte na **Závazky \> Periodický úkol \> Daň 1099**. Pokud chcete mít přístup k této stránce, musíte mít přiděleno oprávnění zabezpečení **Aktualizace pole 1099 a transakcí pro více dodavatelů**.

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-versus-update-all-in-the-update-1099-utility"></a>Závazky: 1099 – „Přepočítat stávající částky 1099“ vs. „Aktualizovat vše“ v nástroji Aktualizovat 1099

Zaškrtávací políčko **Přepočítat stávající částky 1099** obnoví částku formuláře 1099 na celkové zaplacené hodnoty, pokud se použije spolu se zaškrtávacím políčkem **Aktualizovat vše**.

[![Transakce daně 1099: Před spuštěním rutiny aktualizace](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

Zaškrtávací políčko **Přepočítat stávající částky 1099** se bere v potaz pouze v případě, že na faktuře jsou částečné hodnoty formuláře 1099 nebo pokud byla faktura změněna na daňovém formuláři 1099. Například máte fakturu v hodnotě 1 000,00 USD, ale uživatel na ni ručně zadá částku formuláře 1099 ve výši 500,00 USD.

[![Transakce daně 1099: zaškrtnutí obou políček Aktualizovat vše a Přepočítat stávající částky 1099](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

Po zaplacení faktury bude na formuláři 1099 zaplacená částka ve výši 500 USD. Pokud spustíte rutinu přepočtu, změní se částka formuláře 1099 na 1 000,00 USD, což je celková částka, která byla zaplacena.

[![Transakce daně 1099: Po spuštění rutiny 1099](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>Závazky: 1099 – Ruční vytvoření transakcí formuláře 1099

Některá organizace může chtít ručně vytvořit transakce formuláře 1099, které nejsou přidruženy k faktuře. Ruční transakce formuláře 1099 můžete přidat v části **Závazky \> Pravidelné úkoly \> Daň 1099 \> Vyrovnání dodavatele pro formuláře 1099**. Vyberte tlačítko **Ruční transakce 1099**.

Ručně vytvořené transakce formuláře 1099 nejsou aktualizovány procesy **Aktualizovat vše** nebo **Přepočítat stávající částky 1099** v nástroji **Aktualizovat 1099**.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>Závazky: 1099 – Podporuje aplikace Dynamics 365 Finance formulář 1096?

Aplikace Dynamics 365 Finance netiskne formulář 1096 Annual Summary and Transmittal of US Information Returns.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>Závazky: 1099 – Existují nějaké nové funkce, které podporují vykazování formulářem 1099 pro veřejný sektor?

Byla přidána nová funkce veřejného sektoru **Aktualizovat údaje formuláře 1099 podle hlavního účtu**, kterou můžete povolit v pracovním prostoru **Správa funkcí**. Tato funkce umožňuje přidružit hodnoty dodavatele na formuláři 1099 podle hlavního účtu v rozúčtování namísto výchozího účtu v záznamu dodavatele.

Další informace naleznete v tématu [Nastavení dodavatelů pro vykazování 1099](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
