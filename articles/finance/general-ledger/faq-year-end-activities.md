---
title: Časté dotazy k aktivitám na konci roku
description: Toto téma popisuje aktivity související s roční uzávěrkou.
author: kweekley
ms.date: 01/25/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 379bb8a1f969a74618db0e57c84c2038db1b631c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822824"
---
# <a name="year-end-activities-faq"></a>Časté dotazy k aktivitám na konci roku 

[!include [banner](../includes/banner.md)]

Toto téma popisuje aktivity související s roční uzávěrkou. Primárně je zaměřeno na otázky ohledně roční uzávěrky hlavní knihy a závazků.

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
Šablona roční uzávěrky umožňuje organizacím zvolit úroveň finanční dimenze, která se má zachovat při převodu zůstatků zisků a ztrát do nerozděleného zisku. Nastavení umožňují organizaci uchovat podrobné finanční dimenze při přesunu zůstatků do nerozděleného zisku (**Zavřít vše**) nebo shrnout částky do jedné hodnoty dimenze (**Zavřít jednu**). Lze to definovat pro každou finanční dimenzi. Další informace o těchto nastaveních najdete v tématu [Roční uzávěrka](year-end-close.md).

Pro zlepšení výkonu doporučujeme vyhodnotit požadavky vaší organizace a pomocí možnosti roční uzávěrky **Zavřít jednu** zavřít co nejvíce dimenzí. Při zavření jedné hodnoty dimenze (což může být také prázdná hodnota) systém počítá méně podrobností při rozhodování o zůstatcích pro účetní položky nerozděleného zisku.

### <a name="10013-update-or-later"></a>Aktualizace 10.0.13 nebo novější
Pokud jste od posledního spuštění roční uzávěrky vaší organizace provedli aktualizaci na verzi 10.0.13, proces roční uzávěrky může trvat déle z důvodu [implementace funkce HashV2](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/verify-hash-function-changes-after-update-to-dynamics-365-finance-2020-release-wave-2). Termín *hash* odkazuje na pole, které se počítá z ostatních polí řetězce. Rozhraní API pro výpočet hodnoty hash GUID bylo aktualizováno kvůli lepšímu zabezpečení. Pro urychlení procesu roční uzávěrky doporučujeme před jeho spuštěním znovu vytvořit zůstatky sad dimenzí. Pokud už jste tak po aktualizaci učinili, můžete tento krok vynechat.
 
## <a name="general-ledger--what-does-the-period-close--year-end-close-do"></a>Hlavní kniha – Co nastane po provedení uzávěrky období / roční uzávěrky?
 
[![Uzávěrka období, roční uzávěrka](./media/faq-2020-yr-end-05.png)](./media/faq-2020-yr-end-05.png)

### <a name="performance-improvements-for-rebuilding-financial-dimension-sets-new-feature"></a>Vylepšení výkonu opětovného vytváření sad finančních dimenzí (nová funkce)
Nová funkce přidaná do verze 10.0.16 zlepšuje výkon roční uzávěrky a konsolidace. Funkce má název Vylepšení výkonu opětovného vytváření sad finančních dimenzí. Tato funkce opětovně vytvoří sady dimenzí jen pro příslušný časový rámec, zatímco v předchozích verzích to byla všechna kalendářní data. Pokud například uzavíráte rok 2020, systém opětovně vytvoří zůstatky pouze pro transakce, které spadají do fiskálního roku 2020. Pokud spustíte konsolidaci pro období od 1. listopadu 2020 do 30. listopadu 2020, systém opětovně vytvoří zůstatky pouze pro dané časové období.

Protože tato funkce přináší zásadní změnu, musíte ji povolit v pracovním prostoru **Správa funkcí**.
 
[![Roční uzávěrka](./media/faq-2020-yr-end-06.png)](./media/faq-2020-yr-end-06.png)

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2020"></a>Závazky: Jaké proběhly změny na podporu vykazování formulářem 1099 na konci roku 2020?

Pro vykazování formulářem 1099 na konci roku 2020 byly přidány dvě nové funkce týkající se předpisů. První funkce **Použít změny na formuláře 1099-NEC a 1099-MISC pro rok 2020** byla vydána v polovině roku jako povinná funkce, která má umožnit sledování transakčních dat formuláře 1099 za rok 2020 pro nový formulář 1099-NEC. Tato funkce přidala pole do formuláře 1099, která jsou potřebná pro podporu nového formuláře 1099-NEC, a aktualizovala pole formuláře 1099-MISC. Tato aktualizace také upgradovala data záznamu dodavatele propojená s údaji v poli formuláře 1099. 

Druhá funkce **Prohlášení na formuláři 1099 aktualizována pro daňový zákon 2020** obsahuje následující změny.

- 1099-OID – Finanční úřad tento formulář zmodernizoval, aby umožňoval nepřetržité používání.
   - Při tisku musí být vyplněna 3. a 4. číslice vykazovaného roku. Použijte 3. a 4. číslici z pole **Vykazovaný rok** v části **Možnosti tisku daně 1099**. 

- 1099-NEC – Nový formulář pro rok 2020. Tento formulář zaznamenává kompenzace nezaměstnaných. 

-   1099-MISC – Vzhledem k vytvoření formuláře 1099-NEC zrevidoval finanční úřad formulář 1099-MISC a upravil čísla polí pro vykazování určitých příjmů.
Níže jsou uvedeny změny ve vykazování příjmů a čísla polí formuláře.
   - Plátce uskutečnil přímý prodej za 5000 USD nebo více (zaškrtávací políčko) v poli 7.
   - Výnosy z pojištění úrody jsou uvedeny v poli 9.
   - Hrubý výnos advokátovi je uveden v poli 10.
   - Oddíl 409A s časově rozlišitelnými položkami je vykázán v poli 12.
   - Nekvalifikovaný výnos z odložené kompenzace je vykázán v poli 14.
   - Pole 15, 16 a 17 vykazují zadržené státní daně, identifikační číslo státu a výši příjmů dosažených v daném státě.

- Pro rok 2020 neproběhly žádné změny formulářů 1099-DIV a 1099-INT.

- Elektronické podání – Formát se změnil tak, aby vyhovoval novému formuláři NEC a výše popsaným změnám polí formuláře MISC. Konkrétní informace o požadavcích na elektronické podání viz [příručka 1220 finančního úřadu](https://www.irs.gov/pub/irs-pdf/p1220.pdf).

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Závazky: 1099 – Jak změním pole a hodnoty formuláře 1099 pro dodavatele, který během roku nesledoval informace potřebné pro formulář 1099?
Pomocí funkce Aktualizovat 1099 (**Závazky > Dodavatelé > Všichni dodavatelé > Vyberte dodavatele > Karta Dodavatel na pásu karet > Aktualizovat 1099**) projděte dříve zaplacené transakce na faktuře a znovu správně přiřaďte data formuláře 1099 podle nastavení na kartě **Daň 1099** na stránce **Dodavatel**.

## <a name="can-i-run-the-update-1099-for-all-my-vendors-at-once"></a>Mohu spustit funkci Aktualizovat 1099 pro všechny dodavatele najednou?
Ne. Rutinu Aktualizovat 1099 lze spustit vždy jen pro jednoho dodavatele. Pokud to vaše organizace vyžaduje, hlasujte pro nápad s názvem [Dávková aktualizace dat dodavatele na formuláři 1099](https://experience.dynamics.com/ideas/idea/?ideaid=5493d608-350e-eb11-b5d9-0003ff68ded8).

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-vs-update-all-in-the-update-1099-utility"></a>Závazky: 1099 – „Přepočítat stávající částky 1099“ vs. „Aktualizovat vše“ v nástroji Aktualizovat 1099.
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
