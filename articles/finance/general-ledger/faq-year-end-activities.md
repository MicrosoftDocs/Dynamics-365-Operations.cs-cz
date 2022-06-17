---
title: Časté dotazy k aktivitám na konci roku
description: Tento článek uvádí otázky, které mohou vyvstat při uzavírání roku, a odpovědi, které mohou pomoci s činnostmi při roční uzávěrce.
author: moaamer
ms.date: 12/21/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1c5aca6180821dfc9fd1d475d4726c82acdf4d78
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865733"
---
# <a name="year-end-activities-faq"></a>Časté dotazy k aktivitám na konci roku 

[!include [banner](../includes/banner.md)]

Tento článek uvádí otázky, které mohou vyvstat při uzavírání roku, a odpovědi, které mohou pomoci s činnostmi při roční uzávěrce. Informace v tomto článku se primárně zaměřují na otázky ohledně aktivit roční uzávěrky pro hlavní knihu a závazky.

## <a name="general-ledger-year-end-enhancements"></a>Vylepšení roční uzávěrky v hlavní knize 
Verze 10.0.20 zavedla vylepšení roční uzávěrky, které je ve výchozím nastavení povoleno počínaje verzí 10.0.25. Pokud vaše organizace používá verzi starší než 10.0.25, doporučujeme tuto funkci povolit před zahájením procesu uzávěrky na konci roku. Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí pracovního prostoru Správa funkcí zkontrolovat stav funkce a zapnout ji v případě potřeby. Funkce je zde uvedena následujícím způsobem:

 - Modul: Hlavní kniha
 - Název funkce: Vylepšení roční uzávěrky v hlavní knize

Nastavení šablon uzávěrky na konci roku se přesunulo na novou stránku nastavení **Nastavení šablony uzávěrky na konci roku**. Stávající stránka uzávěrky roku se změní způsobem podobným přecenění cizí měny hlavní knihy, kde se při každém spuštění nebo stornování uzávěrky na konci roku zobrazí seznam. Vedoucí účetní může zahájit uzávěrku roku z nové stránky. 

Chcete-li stornovat uzávěrku na konci roku, vyberte poslední fiskální rok pro příslušnou právnickou osobu a vyberte tlačítko **Stornovat roční uzávěrku**. Stornováním se odstraní účetní záznamy za předchozí uzávěrku na konci roku a uzávěrka na konci roku se opětovně nespustí automaticky. 

Roční uzávěrku můžete znovu spustit restartováním procesu pro fiskální rok a právnickou osobu. Proces bude i nadále používat nastavení parametru hlavní knihy, aby určil, zda bude opakování uzávěrky na konci roku zohledňovat pouze nové nebo změněné transakce, nebo úplně stornuje předchozí uzávěrku, přičemž proces znovu spustí pro všechny transakce.  

## <a name="general-ledger-how-do-i-know-that-were-running-year-end-close-and-not-undoing-year-end-close"></a>Hlavní kniha: Jak poznám, kdy provádím roční uzávěrku a kdy ji stornuji?
Už se nám stalo, že některé organizace chtěly provést roční uzávěrku, ale místo toho ji stornovaly. Pokud roční uzávěrka proběhne nezvykle rychle nebo pokud nevytvoří počáteční zůstatky, ověřte nastavení **Vrátit zpět předchozí uzávěrku** v části **Roční uzávěrka** (**Hlavní kniha > Uzávěrka období > Roční uzávěrka > Spustit fiskální uzávěrku**). 

[![Provedení roční uzávěrky a stornování roční uzávěrky](./media/faq-2020-yr-end-01.png)](./media/faq-2020-yr-end-01.png)

Pokud je položka **Vrátit zpět předchozí uzávěrku** nastavena na **Ano**, dojde ke stornování předchozí roční uzávěrky. Při stornu roční uzávěrky jsou odstraněny konečné a počáteční zůstatky, jako kdyby roční uzávěrka nikdy neproběhla. Odstraněny jsou i doklady. Roční uzávěrka se znovu automaticky nespustí. Celý proces je třeba spustit znovu, ale tentokrát se změnou nastavení **Vrátit zpět předchozí uzávěrku** na **Ne**. 

> [!NOTE]
> Konečný zůstatek je volitelně vytvořen v uzavíraném roce. Platí to pouze v případě, že parametr hlavní knihy **Vytvořit uzávěrkové transakce při převodu** je nastaven na **Ano**. Počáteční zůstatek je vytvořen vždy, protože se jedná o zahajovací zůstatek pro následující rok.  
 
## <a name="general-ledger-what-is-the-difference-between-undo-and-delete-gl-parameter-for-year-end-close"></a>Hlavní kniha: Jaký je rozdíl mezi parametry hlavní knihy Zpět a Odstranit pro roční uzávěrku?
Rozdíl mezi parametrem **Vrátit zpět předchozí uzávěrku** v dialogovém okně **Roční uzávěrka** a parametrem **Odstranit transakce roční uzávěrky během převodu** v hlavní knize (**Hlavní kniha> Uzávěrka období > Roční uzávěrka > Spustit fiskální uzávěrku**) nemusí být úplně jasný.  

[![Rozdíl mezi parametrem hlavní knihy Zpět a Odstranit pro roční uzávěrku](./media/faq-2020-yr-end-02.png)](./media/faq-2020-yr-end-02.png)

Pokud při spuštění roční uzávěrky vyberete v rozevíracím seznamu **Vrátit zpět předchozí uzávěrku**, dojde k odstranění všech konečných i počátečních zůstatků, jako by roční uzávěrka nikdy neproběhla. Odstraní se i doklady. Roční uzávěrka se znovu automaticky nespustí. Chcete-li provést roční uzávěrku, musíte tento proces znovu spustit, ale tentokrát změňte hodnotu parametru **Vrátit zpět předchozí uzávěrku** na **Ne** (**Hlavní kniha > Nastavení hlavní knihy > Parametry hlavní knihy**). 

[![Nastavení parametru hlavní knihy](./media/faq-2020-yr-end-03.png)](./media/faq-2020-yr-end-03.png)

Parametr **Odstranit transakce roční uzávěrky během převodu** v hlavní knize se používá pouze při spuštění (nikoli stornování) roční uzávěrky (parametr **Vrátit zpět předchozí uzávěrku** je nastaven na **Ne**). Pokud je tento parametr nastaven na **Ano**, veškeré konečné i počáteční zůstatky budou odstraněny a roční uzávěrka bude opět spuštěna. Tento proces je určen pro organizace, které chtějí všechny transakce, včetně vyrovnání od poslední roční uzávěrky, zaúčtovat jako jednu účetní položku pro konečné a počáteční zůstatky. 

Pokud je tato možnost nastavena na **Ne**, všechny konečné a počáteční zůstatky zůstanou zachovány. Místo toho bude nový konečný a počáteční zůstatek vytvořen pouze pro deltu nebo nové transakce zaúčtované od poslední roční uzávěrky pro daný fiskální rok.  

> [!NOTE]
> Konečný zůstatek je vytvořen v uzavíraném roce. Platí to pouze v případě, že parametr hlavní knihy **Vytvořit uzávěrkové transakce při převodu** je nastaven na **Ano**. Počáteční zůstatek je vytvořen vždy, protože se jedná o zahajovací zůstatek pro následující rok. 

## <a name="general-ledger-what-can-be-changed-to-enhance-performance-of-year-end-processing"></a>Hlavní kniha: Jak lze zlepšit výkon zpracování roční uzávěrky? 
Výkon roční uzávěrky lze zlepšit řadou změn. Doporučujeme je nejprve vyhodnotit a zvážit, zda jsou vhodné pro vaši organizaci.  

### <a name="dimension-sets"></a>Sady dimenzí
Při spuštění roční uzávěrky je znovu vytvořen zůstatek sady dimenzí, což má přímý dopad na výkon. Některé organizace vytvářejí sady dimenzí zbytečně, protože byly nebo mohou být v jednu chvíli použity.  Tyto nepotřebné sady dimenzí jsou během roční uzávěrky vytvářeny stále znovu a prodlužují čas pracování. Věnujte čas vyhodnocení sad dimenzí a odstraňte všechny, které nepotřebujete.

Nepotřebné sady dimenzí také ovlivní dávkovou úlohu **BudgetDimensionFocusInitializeBalance** (**Hlavní kniha > Účtová osnova > Dimenze > Sady finančních dimenzí**).

[![Sady finančních dimenzí](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>Konfigurace šablon roční uzávěrky
Šablona roční uzávěrky umožňuje organizacím zvolit úroveň finanční dimenze, která se má zachovat při převodu zůstatků zisků a ztrát do nerozděleného zisku. Nastavení umožňují organizaci uchovat podrobné finanční dimenze při přesunu zůstatků do nerozděleného zisku (**Zavřít vše**) nebo shrnout částky do jedné hodnoty dimenze (**Zavřít jednu**). Lze to definovat pro každou finanční dimenzi. Další informace o těchto nastaveních najdete v článku [Roční uzávěrka](year-end-close.md).

Pro zlepšení výkonu doporučujeme vyhodnotit požadavky vaší organizace a pomocí možnosti roční uzávěrky **Zavřít jednu** zavřít co nejvíce dimenzí. Při zavření jedné hodnoty dimenze (což může být také prázdná hodnota) systém počítá méně podrobností při rozhodování o zůstatcích pro účetní položky nerozděleného zisku.

## <a name="degenerate-dimensions"></a>Degenerované dimenze

Degenerovaná dimenze sama o sobě a v kombinaci s jinými rozměry poskytuje jen malé nebo žádné opětovné využití. Existují dva různé typy degenerovaných dimenzí. První typ je dimenze, která je individuálně degenerovaná. Obvykle se tento typ degenerované dimenze objeví pouze u jedné transakce nebo u malých sad transakcí. Druhým typem je dimenze, která se stává degenerovanou v kombinaci s jednou nebo více dalšími dimenzemi, které vykazují stejný potenciál na základě možných permutací, které lze generovat. Degenerovaná dimenze může mít významný dopad na výkonnost procesu uzávěrky na konci roku. Chcete-li minimalizovat problémy s výkonem, definujte všechny degenerované dimenze jako **Zavřít jednu** v nastavení uzávěrky na konci roku, jak je popsáno v předchozí části.

## <a name="general-ledger-what-does-the-period-close-year-end-close-do"></a>Hlavní kniha: Co uzávěrka období, roční uzávěrka dělá?
 
[![Uzávěrka období, roční uzávěrka](./media/faq-2020-yr-end-05.png)](./media/faq-2020-yr-end-05.png)

### <a name="performance-improvements-for-rebuilding-financial-dimension-sets"></a>Vylepšení výkonu pro opětovné sestavení sad finančních dimenzí
Nová funkce, která byla přidaná do verze 10.0.16, zlepšuje výkon roční uzávěrky a proces konsolidace. Funkce má název Vylepšení výkonu opětovného vytváření sad finančních dimenzí. Tato funkce opětovně vytvoří sady dimenzí jen pro příslušný časový rámec, zatímco v předchozích verzích to byla všechna kalendářní data. Pokud například uzavíráte rok 2020, systém opětovně vytvoří zůstatky pouze pro transakce, které spadají do fiskálního roku 2020. Pokud spustíte konsolidaci pro období od 1. listopadu 2020 do 30. listopadu 2020, systém opětovně vytvoří zůstatky pouze pro dané časové období.

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí pracovního prostoru Správa funkcí zkontrolovat stav funkce a zapnout ji v případě potřeby. Funkce je zde uvedena následujícím způsobem:
 
- Modul: Hlavní kniha
- Název funkce: Vylepšení výkonu opětovného vytváření sad finančních dimenzí

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2021"></a>Závazky: Jaké proběhly změny na podporu vykazování formulářem 1099 na konci roku 2021?

V roce 2021 byly formuláře DIV, NEC a MISC mírně změněny a byla přidána některá další pole.

#### <a name="div-new-box2e-2f"></a>DIV: nové pole 2e, 2f
 
- Pole 2e. Ukazuje část částky v poli 1a, která představuje zisk podle oddílu 897 připadající na nakládání USRPI.  
- Pole 2f. Ukazuje část částky v poli 2a, která představuje zisk podle oddílu 897 připadající na nakládání USRPI. Všimněte si, že pole 2e a 2f se vztahují pouze na zahraniční osoby a subjekty, jejichž příjmy si zachovávají svůj charakter, pokud jsou převedeny nebo rozděleny jejich přímým nebo nepřímým zahraničním vlastníkům nebo příjemcům. Obecně se považují za skutečně spojené s obchodem nebo podnikáním na území Spojených států. Podívejte se na pokyny k daňovému přiznání. 
 
#### <a name="nec-new-box-2"></a>NEC: nové pole 2 
 
Pokud je zaškrtnuto pole 2, nahlaste spotřebitelské produkty v celkové hodnotě 5 000 USD nebo více, které vám byly prodány za účelem dalšího prodeje, na základě nákupu-prodeje, provize za vklad nebo na jiném základě. Obecně platí, že veškeré příjmy z prodeje těchto produktů nahlaste v seznamu C (formulář 1040). 
 
Mezitím se změní velikost formuláře NEC. Během tisku jsou na jedné stránce tři formuláře. 
 
#### <a name="misc-new-box-11"></a>MISC: nové pole 11 
 
V poli 11 je uvedena částka zaplacená za nákup ryb za účelem dalšího prodeje od jakékoli osoby zapojené do obchodování v oblasti rybolovu. Pro vykázání tohoto příjmu si přečtěte pokyny k daňovému přiznání. 
 
#### <a name="electronic-filing"></a>Elektronické podání 
Informace o elektronickém podání viz [Publikace pro požadavky na elektronické podání](https://www.irs.gov/pub/irs-pdf/p1220.pdf).

Aktualizujte specifikace formátu a rozvržení záznamů pro e-report za rok 2021 
- Sek. 2 Záznam A vydavatele. 
- Kódy částky – zvýšená pozice pole 28-45, délka 18. 
 
#### <a name="sec-2-issuer-a-record-for-reporting-payments-on-form-1099-div"></a>Sek. 2 Záznam A vydavatele, pro hlášení plateb ve formuláři 1099-DIV: 
- Typ částky – přidán oddíl 897 Běžné dividendy a přidán kód částky H. 
- Typ částky – přidán oddíl 897 Kapitálové zisky a přidán kód částky J. 
 
#### <a name="sec-3-payee-b-record"></a>Sek. 3 Záznam B příjemce platby 
- Záznamy obecných informací – Aktualizována třetí odrážka z 16 na 18 polí s částkou platby. 
- Pole názvu platby H – Aktualizovaná pozice pole 247-258, název pole, délka a obecný popis pole. 
- Pole názvu platby J – Aktualizovaná pozice pole 259-270, název pole, délka a obecný popis pole. 
- Aktualizováno prázdné pole na pozici pole 271-286. 
- Aktualizován ukazatel cizí země na pozici pole 287. 
- Aktualizováno pole prvního řádku se jménem příjemce platby na pozici pole 288-327. 
- Aktualizováno pole druhého řádku se jménem příjemce platby na pozici pole 328-367. 
- Pozice rozvržení záznamů, formulář 1099-MISC – Odstraněná pozice pole 548 a název pole Indikátor požadavku na podání FATCA. 
- Pozice rozvržení záznamů, formulář 1099-NEC – aktualizována pole 545-546 na prázdná, pole 547 aktualizováno na indikátor přímého prodeje, délka a popis a poznámky aktualizovány 548-722 na prázdné. 
 
#### <a name="sec-4-end-of-issuer-c-record"></a>Sek. 4 Záznam C Konec emitenta 
- Pole názvu platby H – Aktualizovaná pozice pole 304-321, název pole, délka a obecný popis pole. 
- Pole názvu platby J – Aktualizovaná pozice pole 322-339, název pole, délka a obecný popis pole. 
- Název pole 340-499 – Aktualizována délka na 160. 
 
#### <a name="sec-5-state-totals-k-record"></a>Sek. 5 Záznam K Stav součtů 
- Pole názvu platby H – Aktualizovaná pozice pole 304-321, název pole, délka a obecný popis pole. 
- Pole názvu platby J – Aktualizovaná pozice pole 322-339, název pole, délka a obecný popis pole. 
- Název pole 340-499 – Aktualizována délka na 160.  

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Závazky: 1099 – Jak změním pole a hodnoty formuláře 1099 pro dodavatele, který během roku nesledoval informace potřebné pro formulář 1099?
Pomocí funkce Aktualizovat 1099 (**Závazky > Dodavatelé > Všichni dodavatelé > Vyberte dodavatele > Karta Dodavatel na pásu karet > Aktualizovat 1099**) projděte dříve zaplacené transakce na faktuře a znovu správně přiřaďte data formuláře 1099 podle nastavení na kartě **Daň 1099** na stránce **Dodavatel**.

## <a name="can-i-run-the-update-1099-for-all-my-vendors-at-once"></a>Mohu spustit funkci Aktualizovat 1099 pro všechny dodavatele najednou?
Ne. Rutinu Aktualizovat 1099 lze spustit vždy jen pro jednoho dodavatele. Pokud to vaše organizace vyžaduje, hlasujte pro nápad s názvem [Dávková aktualizace dat dodavatele na formuláři 1099](https://experience.dynamics.com/ideas/idea/?ideaid=5493d608-350e-eb11-b5d9-0003ff68ded8).

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-versus-update-all-in-the-update-1099-utility"></a>Závazky: 1099 – „Přepočítat stávající částky 1099“ vs. „Aktualizovat vše“ v nástroji Aktualizovat 1099.
Zaškrtávací políčko **Přepočítat stávající částky 1099** obnoví částku formuláře 1099 na celkové zaplacené hodnoty, pokud se použije ve spojení se zaškrtávacím políčkem **Aktualizovat vše**. 

[![Transakce daně 1099: Před spuštěním rutiny aktualizace](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

Zaškrtávací políčko **Přepočítat stávající částky 1099** se bere v potaz v případě, že na faktuře jsou částečné hodnoty formuláře 1099 nebo pokud byla faktura změněna na daňovém formuláři 1099. Dejme tomu, že máte fakturu v hodnotě 1000 USD, ale uživatel ručně zadá do formuláře 1099 částku faktury ve výši 500 USD.

[![Transakce daně 1099: zaškrtnutí obou políček Aktualizovat vše a Přepočítat stávající částky 1099](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

Po zaplacení bude na formuláři 1099 zaplacená částka ve výši 500 USD. Pokud spustíte rutinu přepočtu, systém změní částku formuláře 1099 na 1000 USD, což je celková částka, která byla zaplacena.

[![Transakce daně 1099: Po spuštění rutiny 1099](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>Závazky: 1099 – Ruční vytvoření transakcí formuláře 1099
Některá organizace může chtít ručně vytvořit transakce formuláře 1099, které nejsou přidruženy k faktuře. Ruční transakce formuláře 1099 můžete přidat v části **Závazky > Pravidelné úkoly > Daň 1099 > Vyrovnání dodavatele pro formuláře 1099**. Vyberte tlačítko **Ruční transakce 1099**. 

Ručně vytvořené transakce formuláře 1099 nejsou aktualizovány procesy **Aktualizovat vše** nebo **Přepočítat stávající částky 1099** v obslužném programu **Aktualizovat 1099**.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>Závazky: 1099 – Podporuje aplikace Dynamics 365 Finance formulář 1096? 

Aplikace Dynamics 365 Finance neumí vytisknout formulář 1096 Roční shrnutí a přenos informačních výkazů z USA.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>Závazky: 1099 – Existují nějaké nové funkce, které podporují vykazování formulářem 1099 pro veřejný sektor? 
Byla přidána nová funkce veřejného sektoru **Aktualizovat údaje formuláře 1099 podle hlavního účtu**, kterou můžete povolit v pracovním prostoru **Správa funkcí**. Tato funkce umožňuje přidružit hodnoty dodavatele na formuláři 1099 podle hlavního účtu v rozúčtování namísto výchozího účtu v záznamu dodavatele.

Další informace naleznete v tématu [Nastavení dodavatelů pro vykazování 1099](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
