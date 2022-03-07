---
title: Pracovní zátěže správy skladu pro cloudové a hraniční jednotky škálování
description: Toto téma poskytuje informace o funkci, která umožňuje jednotkám škálování spouštět vybrané procesy z vaší úlohy správy skladu.
author: perlynne
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, InventTransferOrders, SalesTable, SysSecRolesEditUsers, SysWorkloadDuplicateRecord
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 0d8b0f5a4878a924943f6f8876575d5247875811
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068102"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Pracovní zátěže správy skladu pro jednotky škálování cloudu a hraniční sítě

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Ne všechny obchodní funkce správy skladu jsou plně podporovány ve skladech, které provozují pracovní zátěž na škálovatelné jednotce. Používáte pouze takové procesy, které toto téma výslovně popisuje jako podporované.

## <a name="warehouse-execution-on-scale-units"></a>Spuštění skladu v jednotkách škálování

Úlohy řízení skladu umožňují cloudovým jednotkám a hraničním jednotkám škálování spouštět vybrané procesy z možností řízení skladu.

## <a name="prerequisites"></a>Předpoklady

Než začnete pracovat se úlohou warehouse management, musí být váš systém připraven tak, jak je popsáno v této části.

### <a name="deploy-a-scale-unit-with-the-warehouse-management-workload"></a>Nasazení jednotky škálování s úlohou warehouse management

Musíte mít centrum Dynamics 365 Supply Chain Management hub a jednotku škálování, která byla nasazena s úlohou správy skladu. Další informace o architektuře a procesu nasazení najdete v tématu [Jednotky škálování v distribuované hybridní topologii](cloud-edge-landing-page.md).

### <a name="turn-on-required-features-in-feature-management"></a>Zapnutí požadovaných funkcí ve správě funkcí

Použijte pracovní prostor [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zapněte obě následující funkce: (Obě funkce jsou uvedeny pod modulem *Warehouse management*.)

- Odpojit odloženou práci od ASN
- (Náhled) Podpora jednotky škálování pro příchozí a odchozí objednávky skladu

## <a name="how-the-warehouse-execution-workload-works-on-scale-units"></a>Jak funguje pracovní zátěž spuštění skladu na jednotkách škálování

U procesů v úlohách správy skladu se data synchronizují mezi centrem a jednotkami škálování.

Jednotka škálování může udržovat pouze data, která vlastní. Koncept vlastnictví dat pro jednotky škálování pomáhá předcházet konfliktům multi-master. Proto je důležité, abyste pochopili, která data procesů jsou vlastněna centrem a které jsou vlastněny jednotkami škálování.

V závislosti na obchodních procesech může stejný datový záznam změnit vlastnictví mezi centrem a jednotkami škálování. Příklad tohoto scénáře je uveden v následující části.

> [!IMPORTANT]
> Některá data lze vytvořit v centru i na jednotce měřítka. Příklady zahrnují **Registrační značky** a **Čísla šarží**. Vyhrazené zvládání konfliktů je k dispozici v případě scénáře, kdy se ve stejném cyklu synchronizace vytvoří stejný jedinečný záznam v centru i na jednotce měřítka. Když k tomu dojde, další synchronizace se nezdaří a budete muset přejít na **Správa systému > Dotazy > Dotazy na zátěž > Duplicitní záznamy**, kde můžete data zobrazit a sloučit.

## <a name="outbound-process-flow"></a>Odchozí tok procesu

Před nasazením úlohy správy skladu do cloudové nebo hranové jednotky se ujistěte, že máte funkci *Podpora jednotek škálování pro uvolnění odchozích objednávek do skladu* aktivní ve vašem centru Enterprise. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, je-li to potřeba. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Řízení skladu*
- **Název funkce** *Podpora jednoty škálování pro uvolnění odchozích objednávek do skladu*

Proces vlastnictví odchozích dat závisí na tom, zda používáte proces plánování zatížení. Ve všech případech centrum vlastní *zdrojové dokumenty*, jako jsou prodejní objednávky a převodní objednávky, jakož i proces přidělování objednávek a související údaje o transakcích objednávky. Když ale použijete proces plánování vytížení, vytížení budou vytvořena v centru, a proto budou původně ve vlastnictví centra. V rámci procesu *Uvolnit do skladu* se vlastnictví dat o zatížení přenese na vyhrazené nasazení jednotky měřítka, které se stane vlastníkem následného *zpracování vlny dodávky* (jako je přidělení práce, doplňovací práce a tvorba práce na vyžádání). Pracovníci skladu proto mohou zpracovávat odchozí prodeje a práci s objednávkami pouze pomocí mobilní aplikace Warehouse Management, která je připojena k nasazení, na němž běží konkrétní pracovní zátěž jednotky škálování.

Jakmile konečný pracovní proces umístí zásoby na konečné místo odeslání (dveře doku), jednotka škálování signalizuje centru, aby aktualizovalo transakce zdrojového dokumentu na *Vybráno*. Dokud se tento proces nespustí a nebude synchronizován zpět, zásoby na pracovním vytížení jednotky škálování bude fyzicky rezervován na úrovni skladu a vy můžete okamžitě zpracovat potvrzení odchozí zásilky bez čekání na dokončení této synchronizace. Následný prodejní dodací list a zásilka fakturace nebo převodní objednávky za náklad budou zpracovány v centru.

Tento následující diagram ukazuje odchozí tok a ukazuje, kde probíhají jednotlivé obchodní procesy. (Kliknutím na diagram jej zvětšíte.)

[![Odchozí tok procesu.](media/wes_outbound_warehouse_processes-small.png "Odchozí tok procesu")](media/wes_outbound_warehouse_processes.png)

### <a name="outbound-processing-with-load-planning"></a>Odchozí zpracování s plánováním vytížení

Když používáte proces plánování vytížení, vytížení a zásilky se vytvářejí v rozbočovači a vlastnictví dat se přenáší do jednotek škálování jako součást procesu *Uvolnit do skladu*, jak je znázorněno na následujícím obrázku.

![Odchozí zpracování s plánováním vytížení.](./media/wes_outbound_processing_with_load_planning.png "Odchozí zpracování s plánováním vytížení")

### <a name="outbound-processing-without-load-planning"></a>Odchozí zpracování bez plánování vytížení

Když nepoužíváte proces plánování vytížení, zásilky se vytvářejí na jednotkách škálování. V rámci procesu zahrnutí do vln se na jednotkách škálování také vytváří vytížení.

![Odchozí zpracování bez plánování vytížení.](./media/wes_outbound_processing_without_load_planning.png "Odchozí zpracování bez plánování vytížení")

## <a name="inbound-process-flow"></a>Příchozí tok procesu

Centrum vlastní následující data:

- Všechny zdrojové dokumenty, například nákupní objednávky a výrobní zakázky
- Příchozího zpracování vytížení
- Všechny nákladové a finanční aktualizace

> [!NOTE]
> Tok příchozích objednávek se koncepčně liší od odchozích toků. Stejný sklad můžete provozovat na jednotce škálování nebo v centru v závislosti na tom, zda byla nákupní objednávka uvolněna do skladu. Jakmile uvolníte objednávku do skladu, můžete s touto objednávkou pracovat pouze po přihlášení na jednotce škálování.
>
> Pokud používáte proces *Uvolnit do skladu*, vytvoří se [*skladové objednávky*](cloud-edge-warehouse-order.md) a vlastnictví souvisejícího toku přijímání se přiřadí jednotce škálování. Centrum nebude moci zaregistrovat příchozí příjem.

Abyste mohli použít proces *Uvolnit do skladu*, musíte být přihlášeni v centru. Pro zpracování nákupní objednávky přejděte na jednu z následujících stránek:

- **Zásobování a zdroje > Nákupní objednávky > Všechny nákupní objednávky > Sklad > Akce > Uvolnit do skladu**
- **Řízení skladu > Uvolnění do skladu > Automatické uvolnění nákupních objednávek**

Při použití možnosti **Automatické uvolnění nákupních objednávek** můžete vybrat konkrétní řádky nákupní objednávky na základě dotazu. Typickým scénářem by bylo nastavení opakované dávkové úlohy, která uvolní všechny potvrzené řádky nákupní objednávky, které se očekávají příští den.

Pracovník může spustit proces příjmu pomocí mobilní aplikace Řízení skladu, která je připojena k jednotce škálování. Data se poté zaznamenají podle jednotky škálování a nahlásí se proti příchozí skladové objednávce. Vytvoření a zpracování následného odložení bude také zpracováno podle jednotky škálování.

Pokud nepoužíváte proces *vydání do skladu* a tím pádem ani *skladové objednávky*, centrum může zpracovávat příjem skladu a zpracování práce nezávisle na jednotkách škálování.

![Příchozí tok procesu.](./media/wes-inbound-ga.png "Příchozí tok procesu")

Když pracovník provede příchozí registraci pomocí procesu příjmu mobilní aplikace Warehouse Management proti jednotce škálování, zaznamená se příjem proti související skladové objednávce, která je uložena na jednotce škálování. Pracovní vytížení jednotky škálování poté signalizuje rozbočovači, aby aktualizoval související transakce řádku nákupní objednávky na *Registrovaná*. Jakmile to bude hotové, budete moci spustit příjem produktu z nákupní objednávky na centru.

Tento následující diagram ukazuje příchozí tok a ukazuje, kde probíhají jednotlivé obchodní procesy. (Kliknutím na diagram jej zvětšíte.)

[![Příchozí tok procesu](media/wes_inbound_warehouse_processes-small.png "Příchozí tok procesu")](media/wes_inbound_warehouse_processes.png)

## <a name="production-control"></a>Řízení výroby

Úloha warehouse management podporuje následující tři toky výroby v aplikaci Warehouse management:

- Ohlásit jako dokončené a odložit
- Spustit výrobní zakázku
- Zaregistrovat spotřebu materiálu

### <a name="report-as-finished-and-put-away"></a>Ohlásit jako dokončené a odložit

Pracovníci mohou používat tok **Nahlásit jako hotové a odložit** v aplikaci Warehouse management k ohlašování výrobní nebo dávkové objednávky jako dokončené. Mohou také hlásit koprodukty a vedlejší produkty v dávkové objednávce jako hotové. Když je úloha nahlášena jako dokončená, systém obvykle vygeneruje skladovou práci na jednotce škálování. Pokud nepotřebujete práci s odkladem, můžete nastavit zásady práce tak, aby byla vynechána.

### <a name="start-production-order"></a>Spustit výrobní zakázku

Pracovníci mohou používat tok **Spustit výrobní zakázku** v aplikaci Warehouse Management k registraci zahájení výroby nebo dávkové objednávky.

### <a name="register-material-consumption"></a>Zaregistrovat spotřebu materiálu

Pracovníci mohou používat tok **Registrovat spotřebu materiálu** v aplikaci Warehouse Management k hlášení spotřeby materiálu pro objednávku výroby nebo dávkovou objednávku. Poté se vytvoří deník výdejky pro vykázaný materiál na výrobní nebo dávkové zakázce na jednotce škálování. Řádky deníku provádějí fyzickou rezervaci spotřebovaných zásob. Když jsou data synchronizována mezi jednotkou škálování a centrem, vygeneruje se deník výdejky a odešle se na instanci centra.

## <a name="supported-processes-and-roles"></a>Podporované procesy a role

Ne všechny procesy správy skladu jsou podporovány v pracovní zátěži provedení ve skladu na jednotce škálování. Proto doporučujeme přiřadit role, které odpovídají funkcím, které jsou k dispozici každému uživateli.

Pro usnadnění tohoto procesu je pojmenovaná ukázková role *Vedoucí skladu při úloze* je součástí ukázkových dat v okně **Správa systému \> Zabezpečení \> Konfigurace zabezpečení**. Účelem této role je umožnit správcům skladu přístup k úloze provádění skladu na jednotce škálování. Role uděluje přístup ke stránkám, které jsou relevantní v kontextu úlohy, která je hostována na jednotce škálování.

Role uživatele na jednotce škálování jsou přiřazeny jako součást počáteční synchronizace dat z rozbočovače na jednotku škálování.

Chcete-li upravit role, které jsou přiřazeny uživateli, přejděte na **Správa systému \> Zabezpečení \> Přiřadit uživatele k rolím**. Uživatelům, kteří působí jako správci skladu pouze na jednotkách škálování, by měla být přiřazena pouze role *Vedoucí skladu na úloze*. Tento přístup zajistí, že tito uživatelé budou mít přístup pouze k podporovaným funkcím. Odeberte všechny další role, které jsou těmto uživatelům přiřazeny.

Uživatelům, kteří působí jako správci skladu v centru i na jednotkách škálování, by měla být přiřazena stávající role *pracovník skladu*. Uvědomte si, že tato role uděluje pracovníkům skladu přístup k funkcím (například zpracování příjmu objednávek přenosu), které se objevují v uživatelském rozhraní (UI), ale nejsou aktuálně podporovány na jednotkách škálování.

### <a name="supported-warehouse-execution-processes"></a>Podporované procesy provádění skladu

Pro pracovní zátěž WES na jednotce škálování lze povolit následující procesy provádění skladu:

- Vybrané metody vln pro prodejní a převodové objednávky (ověření, vytvoření vytížení, přidělení doplnění poptávky, kontejnerizace, tvorba díla a tisk štítků vln)

- Zpracování skladových a prodejních zakázek pomocí aplikace skladu (včetně doplňovacích prací)
- Dotaz na zásoby po ruce pomocí aplikace skladu
- Vytváření a spouštění pohybů zásob pomocí aplikace skladu
- Vytváření a zpracování cyklu počítání prací pomocí aplikace skladu
- Provádění úprav zásob na skladě pomocí aplikace skladu
- Registrace nákupních objednávek a odvedení práce pomocí aplikace skladu

Následující typy prací lze vytvořit na jednotce škálování, a proto je lze zpracovat jako součást úlohy správy skladu:

- **Pohyby zásob** – ruční pohyb a pohyb podle šablony práce.
- **Počítání cyklů** – včetně schválení/odmítnutí nesrovnalosti jako součást operací počítání.
- **Nákupní objednávky** – odložená práce prostřednictvím objednávky ve skladu, když nákupní objednávky nejsou spojeny s nákladem.
- **Prodejní objednávky** – jednoduchá práce vyzvednutí a vložení.
- **Potvrzení o převodu** – Prostřednictvím zpracování příjmu registrační značky.
- **Problém s převodem** - Jednoduché vychystávání a nakládání.
- **Doplnění** – nezahrnuje suroviny pro výrobu.
- **Odložení hotového zboží** - Po procesu nahlášení výroby jako dokončené.
- **Vedlejší produkt a odložení vedlejšího produktu** - Po ukončení výroby jako sestavy.
<!-- - **Packed container picking** - After manual packing station processing. -->

V jednotkách škálování nejsou v současné době podporovány žádné jiné typy zdrojových dokumentů ani skladových prací. Když například spouštíte proti úloze provádění skladu na jednotce škálování, nemůžete ke zpracování objednávek vrácení použít proces příjmu prodejní objednávky. Místo toho musí toto zpracování provádět instance centra.

> [!NOTE]
> Položky nabídky mobilních zařízení a tlačítka pro nepodporované funkce se v _mobilní aplikaci Řízení skladu_ nezobrazí, když je připojena k nasazení jednotky škálování.
>
> K nastavení mobilní aplikace Warehouse Management, aby fungovala proti jednotce škálování cloudu a hrany, je potřeba provést několik dalších kroků. Další informace naleznete v části [Konfigurace mobilní aplikace Warehouse Management pro jednotky škálování cloudu a hrany](cloud-edge-workload-setup-warehouse-app.md).
>
> Když spustíte úlohu na jednotce škálování, nemůžete spustit nepodporované procesy pro konkrétní sklad v centru. Tabulky uvedené dále v tomto tématu dokumentují podporované funkce.
>
> Vybrané typy skladové práce lze vytvořit jak v centru, tak na jednotkách škálování, ale lze je udržovat pouze prostřednictvím vlastnícího centra nebo jednotky škálování (nasazení, které data vytvořilo).
>
> I když je určitý proces podporován na jednotce škálování, mějte na paměti, že se nemusí synchronizovat všechna potřebná data z centra na jednotku škálování nebo z jednotky škálování v centru, což může mít za následek neočekávané zpracování systému. Mezi příklady tohoto scénáře patří:
>
> - Pokud používáte dotaz na direktivu umístění, která se připojí k záznamu datové tabulky, který existuje pouze při nasazení centra.
> - Pokud používáte stav umístění a / nebo funkci volumetrického zatížení místa. Tato data nebudou synchronizována mezi nasazeními a budou proto fungovat pouze při aktualizaci umístění majetku na skladě na jednom z nasazení.

Následující funkce správy skladu nejsou aktuálně podporovány v úlohách jednotky škálování:

- Příchozí zpracování řádků nákupní objednávky přiřazených k vytížení.
- Příchozí zpracování nákupních objednávek projektu.
- Správa nákladů na doručení, používání cest a sledování zboží při přepravě.
- Příchozí a odchozí zpracování pro položky, které mají jakékoli aktivní sledovacích dimenzí **Vlastník** a/nebo **Sériové číslo**.
- Zpracování zásob, které mají hodnotu stavu blokování.
- Změna stavu zásob během jakéhokoli procesu pracovního pohybu.
- Flexibilní rezervace dimenze na úrovni skladu potvrzené podle objednávky.
- Použití funkce *Stav umístění skladu* (data se mezi nasazeními nesynchronizují).
- Použití funkce *Umístění registrační značky*.
- Použití nastavení *Filtry produktu* a *Skupiny filtrů produktů*, včetně nastavení **Počet dní ke kombinování šarží**.
- Integrace s řízením kvality.
- Zpracování s položkami se skutečnou hmotností.
- Zpracování s položkami povolenými pouze pro správu dopravy (TMS).
- Zpracování s negativními zásobami na skladě.
- Sdílení dat mezi společnostmi pro produkty. <!-- Planned -->
- Zpracování skladové práce s dodacími listy.
- Zpracování skladové práce s manipulací s materiálem / automatizací skladu.
- Obrázky hlavních dat produktu (například v mobilní aplikaci Warehouse Management).

> [!WARNING]
> Některé funkce skladu nebudou k dispozici pro sklady se spuštěnými úlohami správy skladu na jednotce škálování a také nejsou podporovány na rozbočovači nebo na úlohách jednotky škálování.
>
> Jiné funkce mohou být zpracovány na obou, ale budou vyžadovat pečlivé použití v některých scénářích, například když se zásoby na skladě aktualizují ro stejný čas v centru i jednotce škálování kvůli procesu aktualizace asynchronních dat.
>
> Specifické funkce (např. *blokovat práci*), které jsou podporovány jak v centru, tak v jednotkách škálování, budou podporovány pouze pro vlastníka dat.

### <a name="outbound-supported-only-for-sales-and-transfer-orders"></a>Odchozí (podporováno pouze pro prodejní a objednávky a převodní příkazy)

Následující tabulka ukazuje, které odchozí funkce jsou podporovány a kde jsou podporovány, když se úlohy správy skladu používají v cloudových a hraničních jednotkách.

| Zpracovat                                                      | Centrum | Pracovní zatížení provedení skladu na jednotce škálování |
|--------------------------------------------------------------|-----|------------------------------|
| Zpracování zdrojového dokumentu                                   | Ano | Ne |
| Zpracování správy nakládky a přepravy                | Ano, ale pouze procesy plánování vytížení. Zpracování správy dopravy není podporováno  | Ne |
| Uvolnit do skladu                                         | Ano | Ne |
| Plánovaný cross docking                                        | Ne  | Ne |
| Konsolidace dodávky                                       | Ano, při použití plánování vytížení | Ano |
| Zpracování vlny dodávky                                     | Ne  |Ano, kromě **Stavba a třídění nákladu** |
| Udržování zásilek pro vlnu                                  | Ne  | Ano|
| Zpracování skladových prací (vč. tisku registrační značky)        | Ne  | Ano, ale pouze pro dříve uvedené podporované funkce |
| Výdej seskupení                                              | Ne  | Ano|
| Ruční zpracování balení, vč. „Zpracování vychystávání zabaleného kontejneru“ | Číslo <P>Některé zpracování lze provést po počátečním procesu vychystávání zpracovaném jednotkou škálování, ale nedoporučuje se to kvůli následujícím blokovaným operacím.</p>  | Ne |
| Odebrat kontejner ze skupiny                                  | Ne  | Ne |
| Zpracování odchozího třídění                                  | Ne  | Ne |
| Tisk dokumentů souvisejících se zátěží                           | Ano | Ano|
| Přepravní doklad a generování ASN                            | Ne  | Ano|
| Potvrzení zásilky                                             | Ne  | Ano|
| Potvrzení zásilky s příkazem „Potvrdit a převést“            | Ne  | Ano|
| Zpracování dodacího listu a fakturace                        | Ano | Ne |
| Krátký výběr (prodejní a převodové objednávky)                    | Ne  | Ano, bez odstranění rezervací zdrojových dokumentů|
| Výběr nadměrného množství (prodejní a převodové objednávky)                     | Číslo  | Ano|
| Konsolidovat registrační značky                                   | Číslo  | Ano|
| Změna pracovních míst (prodejní a převodní objednávky)         | Ne  | Ano|
| Kompletní práce (prodejní a převodní objednávky)                    | Ne  | Ano|
| Vytisknout sestavu práce                                            | Ano | Ano|
| Štítek vlny                                                   | Ne  | Ano|
| Rozdělení práce                                                   | Ne  | Ano|
| Zpracování práce - režie 'Naložení přenosu'            | Ne  | Ne |
| Snížit vyskladněné množství                                       | Ne  | Ano|
| Stornovat práci                                                 | Číslo  | Ano|
| Zrušit potvrzení expedice                                | Číslo  | Ano|
| Žádost o zrušení řádků skladových objednávek                      | Ano | Ne, ale žádost bude schválena nebo zamítnuta |
| <p>Uvolnit převodní příkazy pro příjem</p><p>Tento proces proběhne automaticky jako součást procesu odeslání převodního příkazu. Lze jej však ručně použít k povolení příjmu registrační značky na jednotce škálování, pokud byly zrušeny řádky příchozích skladových objednávek nebo jako součást procesu nasazení nové úlohy.</p> | Ano | Číslo|

### <a name="inbound"></a>Příchozí

Následující tabulka ukazuje, které příchozí funkce jsou podporovány a kde jsou podporovány, když se úlohy správy skladu používají v cloudových a hraničních jednotkách.

| Zpracovat                                                          | Centrum | Pracovní zatížení provedení skladu na jednotce škálování<BR>*(Položky označené „Ano“ platí pouze pro skladové objednávky)* |
|------------------------------------------------------------------|-----|----------------------------------------------------------------------------------|
| Zpracování&nbsp;zdrojového&nbsp;dokumentu                             | Ano | Ne |
| Zpracování správy nakládky a přepravy                    | Ano | Ne |
| Náklady na doručení a příjem přepravovaného zboží                       | Ano | Ne |
| Potvrzení příchozí dodávky                                    | Ano | Ne |
| Uvolnění nákupní objednávky do skladu (zpracování objednávky skladu) | Ano | Číslo |
| Žádost o zrušení řádků skladových objednávek                            | Ano | Ne, ale žádost bude schválena nebo zamítnuta |
| Zpracování příjmu produktu zdrojového dokumentu z nákupní objednávky                        | Ano | Číslo |
| Přijetí zboží nákupní objednávky a odložení                       | <p>Ano,&nbsp;když&nbsp;tam&nbsp;není skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | <p>Ano, když nákupní objednávka není součástí <i>vytížení</i></p> |
| Přijetí řádku nákupní objednávky a odložení                       | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | <p>Ano, když nákupní objednávka není součástí <i>vytížení</i></p></p> |
| Přijatá a odložená vratka                              | Ano | Ne |
| Přijetí a odložení smíšené registrační značky                       | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | Ano |
| Přijetí položky nákladu                                              | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | Číslo |
| Přijetí registrační značky nákupní objednávky a odložení              | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | Číslo |
| Přenos registrační značky nákupní objednávky a odložení             | Číslo | Ano |
| Přijetí a odložení zboží převodního příkazu                       | Ano | Číslo |
| Převést řádek nákupní objednávky a odložení                       | Ano | Číslo |
| Příjem nákupní objednávky s nedostatečným doručením                      | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | Ano, ale pouze podáním žádosti o zrušení z centra |
| Příjem nákupní objednávky s nadměrným doručením                       | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | Ano  |
| Příjem s vytvořením práce *Cross docking*                 | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | Ne |
| Příjem s vytvořením práce *Objednávka kvality*                  | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | Ne |
| Příjem s vytvořením práce *Vzorek položky kvality*          | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | Ne |
| Příjem s vytvořením práce *Kvalita v kontrole kvality*       | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | Ne |
| Příjem s vytvořením objednávky kvality                            | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | Ne |
| Zpracování práce - Režie *Cluster putaway*                 | Ano | Číslo |
| Zpracování práce s *Krátký výběr*                               | Ano | Číslo |
| Zrušení práce (příchozí)                                            | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | <p>Ano, ale pouze, když možnost <b>Zrušit registraci potvrzení při rušení práce</b> (na stránce <b>Parametry Warehouse management</b>) není podporována</p> |
| Načtení registrační značky                                           | Ano | Ano |

### <a name="warehouse-operations-and-exception-handing"></a>Skladové operace a zpracování výjimek

Následující tabulka ukazuje, které funkce skladových operací a zpracování výjimek jsou podporovány a kde jsou podporovány, když se úlohy správy skladu používají v cloudových a hraničních jednotkách.

| Zpracovat                                            | Centrum | Pracovní zatížení provedení skladu na jednotce škálování |
|----------------------------------------------------|-----|------------------------------|
| Dotaz na registrační značku                              | Ano | Ano                          |
| Dotaz na zboží                                       | Ano | Ano                          |
| Dotaz na umístění                                   | Ano | Ano                          |
| Změnit sklad                                   | Ano | Ano                          |
| Přesun                                           | Ano | Ano                          |
| Pohyb podle šablony                               | Ano | Ano                          |
| Převod skladu                                 | Ano | Ne                           |
| Vytvoření převodního příkazu z aplikace skladu           | Ano | Ne                           |
| Úprava (příchozí/odchozí)                                | Ano | Ano, ale ne pro scénář úpravy, kdy je třeba rezervaci inventáře odstranit pomocí nastavení **Odebrat rezervace** na typech úprav zásob</p>                           |
| Změna stavu zásob                            | Ano | Ne                           |
| Zpracování nesrovnalostí cyklické inventury a počítání | Ano | Ano                           |
| Opakovaný tisk štítku (tisk registrační značky)             | Ano | Ano                          |
| Sestavení registrační značky vozidla                                | Ano | Ne                           |
| Seskupení registračních značek                                | Ano | Ne                           |
| Zabalit do vnořených registračních značek                      | Ano | Ne                           |
| Přihlášení řidiče                                    | Ano | Ne                           |
| Odhlášení řidiče                                   | Ano | Ne                           |
| Změnit kód dispozice dávky                      | Ano | Ano                          |
| Zobrazit otevřený seznam úkolů                             | Ano | Ano                          |
| Zpracování doplnění min./max. a prahové hodnoty zóny| Ano <p>Nedoporučuje se zahrnout stejná umístění jako součást dotazů</p>| Ano                          |
| Slotting procesu doplnění                  | Ano  | Ano<p>Pamatujte, že nastavení musí být provedeno na jednotce škálování</p>                           |
| Práce blokování a odblokování                             | Ano | Ano                          |
| Změnit uživatele                                        | Ano | Ano                          |
| Změnit fond práce u práce                           | Ano | Ano                          |
| Zrušit práci                                        | Ano | Ano                          |

### <a name="production"></a>Výrobní

Následující tabulka shrnuje, které provozní scénáře správy skladu jsou v současné době v pracovních zatíženích jednotky škálování podporovány.

| Zpracovat | Centrum | Pracovní zatížení provedení skladu na jednotce škálování |
|---------|-----|----------------------------------------------|
| Zpracování zdrojového dokumentu výrobní zakázky    | Ano | Číslo |
| Uvolnění do skladu                           | Ano | Číslo |
| Spustit výrobní zakázku                         | Ano | Ano|
| Vytvoření skladových objednávek                        | Ano | Číslo |
| Žádost o zrušení řádků skladových objednávek        | Ano | Ne, ale žádost bude schválena nebo zamítnuta |
| Ohlásit jako dokončené a vyskladnit dokončené zboží | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | Ano|
| Vyskladnění vedlejšího produktu             | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | Ano|
| Zaregistrovat spotřebu materiálu                  | Ano | Ano|
| Vlnové zpracování výroby                     | Ano | Číslo |
| Výdej suroviny                           | Ano | Číslo |
| Kanban – odložení                                | Ano | Číslo |
| Kanban – výdej                                 | Ano | Číslo |
| Prázdný kanban                                   | Ano | Číslo |
| Výrobní odpad                               | Ano | Číslo |
| Poslední paleta výroby                         | Ano | Číslo |
| Doplnění surovin                     | Číslo  | Číslo |

## <a name="maintaining-scale-units-for-warehouse-execution"></a>Udržování jednotek škálování pro provedení skladu

Několik dávkových úloh spuštěných v jednotce centra i škály.

V nasazení centra můžete následující dávkové úlohy spravovat ručně:

- Následující dávkové úlohy můžete spravovat v okně **Warehouse management \> Pravidelné úkoly \> Správa úlohy v kanceláři**:

    - Zpracovatel zprávy jednotky škálování do centra
    - Registrovat příjmy zdrojové objednávky
    - Dokončit skladové objednávky

- Následující dávkové úlohy můžete spravovat v okně **Warehouse management \> Pravidelné úkoly \> Správa úlohy**:

    - Zpracovatel zprávy z centra skladu do jednotky škálování
    - Zpracovat příjmy řádku skladové objednávky pro zaúčtování příjmu skladu

V nasazeních jednotek škálování můžete spravovat následující dávkové úlohy v okně **Warehouse management \> Pravidelné úkoly \> Správa úlohy**:

- Zpracovat záznamy tabulky vln
- Zpracovatel zprávy z centra skladu do jednotky škálování
- Zpracovat příjmy řádku skladové objednávky pro zaúčtování příjmu skladu

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
