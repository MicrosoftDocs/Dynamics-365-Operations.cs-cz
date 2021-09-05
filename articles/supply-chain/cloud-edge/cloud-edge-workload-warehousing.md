---
title: Pracovní zátěže správy skladu pro cloudové a hraniční jednotky škálování
description: Toto téma poskytuje informace o funkci, která umožňuje jednotkám škálování spouštět vybrané procesy z vaší úlohy správy skladu.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, SysSecRolesEditUsers, SysWorkloadDuplicateRecord
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 7541688e8428dbc17a3c53d696913365580c3db8
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343757"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Pracovní zátěže správy skladu pro jednotky škálování cloudu a hraniční sítě

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Ne všechny obchodní funkce správy skladu jsou plně podporovány ve skladech, které provozují pracovní zátěž na škálovatelné jednotce. Používáte pouze takové procesy, které toto téma výslovně popisuje jako podporované.

## <a name="warehouse-execution-on-scale-units"></a>Spuštění skladu v jednotkách škálování

Tato funkce umožňuje jednotkám škálování spouštět vybrané procesy z možností správy skladu.

V tomto tématu jsou spouštění správy skladu ve skladu, který je definován jako jednotka škálování, označovány jako *Systém spuštění skladu* (*WES*).

## <a name="prerequisites"></a>Předpoklady

Musíte mít centrum Dynamics 365 Supply Chain Management hub a jednotku škálování, která byla nasazena s úlohou správy skladu. Další informace o architektuře a procesu nasazení naleznete v části [Použití jednotek škálování ke zvýšení odolnosti pro úlohy Supply Chain Management](cloud-edge-landing-page.md).

## <a name="how-the-wes-workload-works-on-scale-units"></a>Jak funguje pracovní zátěž WES na jednotkách škálování

U procesů v úlohách správy skladu se data synchronizují mezi centrem a jednotkami škálování.

Jednotka škálování může udržovat pouze data, která vlastní. Koncept vlastnictví dat pro jednotky škálování pomáhá předcházet konfliktům multi-master. Proto je důležité, abyste pochopili, které procesy jsou vlastněny centrem a které jsou vlastněny jednotkami škálování.

Jednotky škálování vlastní následující data:

- **Vlnové zpracování dat dodávek** - Vybrané metody zpracování vln jsou zpracovávány v rámci vlnového zpracování jednotky škálování.
- **Zpracování údajů o práci** – Skladová práce vytvořená na jednotce škálování bude vlastněna touto konkrétní jednotkou škálování. Jsou podporovány následující typy zpracování pracovních příkazů:

  - **Pohyby zásob** (ruční pohyb a pohyb podle šablony práce)
  - **Počítání cyklů** a proces schválení/odmítnutí jako součást operací počítání
  - **Nákupní objednávky** (odložená práce prostřednictvím objednávky ve skladu, když nákupní objednávky nejsou spojeny s nákladem)
  - **Prodejní objednávky** (jednoduchá práce vyzvednutí a vložení)
  - **Objednávky převodu** (pouze odchozí s jednoduchým výběrem a nakládáním)

- **Údaje o přijetí skladové objednávky** - Tato data se používají pouze pro nákupní objednávky, které jsou uvolněny do skladu.
- **Údaje o registrační značce** - Registrační značky lze vytvářet v centru i na jednotce škálování. Bylo poskytnuto vyhrazené řešení konfliktů. 

    > [!IMPORTANT]
    > Data registrační značky nejsou specifická pro sklad. Pokud se během stejného synchronizačního cyklu vytvoří v centru a na jednotce měřítka stejné číslo registrační značky, dojde k další synchronizaci. Pokud k tomu dojde, přejděte na **Správa systému > Dotazy> Dotazy na pracovní zátěž > Duplicitní záznamy**, kde můžete zobrazit a sloučit data.

## <a name="outbound-process-flow"></a>Odchozí tok procesu

Centrum vlastní následující data:

- Všechny zdrojové dokumenty, například prodejní objednávky a objednávky přenosu
- Přidělení objednávky a zpracování odchozího zatížení
- Procesy uvolnění do skladu, vytvoření zásilky, vytvoření vlny a finalizace vlny

Jednotky stupnice vlastní skutečné vlnové zpracování (jako je přidělení práce, doplňovací práce a vytvoření poptávky práce) po vydání vlny. Pracovníci skladu proto mohou zpracovávat odchozí práci pomocí mobilní aplikace Řízení skladu, která je připojena k jednotce škálování.

![Tok zpracování vlny.](./media/wes-wave-processing-ga.png "Tok zpracování vlny")

### <a name="process-work-and-ship"></a>Zpracování práce a odeslání

Jakmile konečný pracovní proces umístí zásoby na konečné místo odeslání (dveře doku), jednotka škálování signalizuje centru, aby aktualizovalo transakce zdrojového dokumentu na *Vybráno*. Dokud tento proces nebude spuštěn a nebude synchronizován zpět, zásoby na skladě na úloze jednotky škálování budou fyzicky vyhrazeny na úrovni skladu.

Jakmile centrum aktualizuje transakce na *Vybráno*, může zpracovat potvrzení odchozí zásilky a související dodací list nebo zásilku s převodem objednávky pro náklad.

![Odchozí tok procesu.](./media/WES-outbound-processing-19.png "Odchozí tok procesu")

## <a name="inbound-process-flow"></a>Příchozí tok procesu

Centrum vlastní následující data:

- Všechny zdrojové dokumenty, například nákupní objednávky a objednávky vrácení prodeje
- Příchozího zpracování vytížení
- Všechny nákladové a finanční aktualizace

> [!NOTE]
> Tok příchozích objednávek se koncepčně liší od odchozích toků. Stejný sklad můžete provozovat na jednotce škálování nebo v centru v závislosti na tom, zda byla nákupní objednávka uvolněna do skladu nebo ne. Jakmile uvolníte objednávku do skladu, můžete s touto objednávkou pracovat pouze po přihlášení na jednotce škálování.
>
> Pokud používáte proces *Uvolnit do skladu*, vytvoří se [*skladové objednávky*](cloud-edge-warehouse-order.md) a vlastnictví souvisejícího toku přijímání se přiřadí jednotce škálování. Centrum nebude moci zaregistrovat příchozí příjem.

Abyste mohli použít proces *Uvolnit do skladu*, musíte být přihlášeni v centru. Chcete-li jej spustit nebo naplánovat, přejděte na jednu z následujících stránek:

- **Zásobování a zdroje > Nákupní objednávky > Všechny nákupní objednávky > Sklad > Akce > Uvolnit do skladu**
- **Řízení skladu > Uvolnění do skladu > Automatické uvolnění nákupních objednávek**

Při použití možnosti **Automatické uvolnění nákupních objednávek** můžete vybrat konkrétní řádky nákupní objednávky na základě dotazu. Typickým scénářem by bylo nastavení opakované dávkové úlohy, která uvolní všechny potvrzené řádky nákupní objednávky, které se očekávají příští den.

Pracovník může spustit proces příjmu pomocí mobilní aplikace Řízení skladu, která je připojena k jednotce škálování. Data se poté zaznamenají podle jednotky škálování a nahlásí se proti příchozí skladové objednávce. Vytvoření a zpracování následného odložení bude také zpracováno podle jednotky škálování.

Pokud nepoužíváte proces *vydání do skladu* a tím pádem ani *skladové objednávky*, centrum může zpracovávat příjem skladu a zpracování práce nezávisle na jednotkách škálování.

![Příchozí tok procesu.](./media/wes-inbound-ga.png "Příchozí tok procesu")

Když provádíte příchozí registraci prostřednictvím procesu přijímání aplikace skladu proti objednávce skladové jednotky škálování, úloha jednotky škálování bude signalizovat centru, aby aktualizovalo související transakce řádku nákupní objednávky na *Registrováno*. Jakmile to bude hotové, budete moci spustit příjem produktu z nákupní objednávky na centru.

![Příchozí tok procesu.](./media/WES-inbound-processing-19.png "Příchozí tok procesu")

## <a name="supported-processes-and-roles"></a>Podporované procesy a role

Ne všechny procesy správy skladu jsou podporovány v pracovní zátěži WES na jednotce škálování. Proto doporučujeme přiřadit role, které odpovídají funkcím, které jsou k dispozici každému uživateli.

Pro usnadnění tohoto procesu je pojmenovaná ukázková role *Vedoucí skladu při úloze* je součástí ukázkových dat v okně **Správa systému \> Zabezpečení \> Konfigurace zabezpečení**. Účelem této role je umožnit správcům skladu přístup k WES na jednotce škálování. Role uděluje přístup ke stránkám, které jsou relevantní v kontextu úlohy, která je hostována na jednotce škálování.

Role uživatele na jednotce škálování jsou přiřazeny jako součást počáteční synchronizace dat z rozbočovače na jednotku škálování.

Chcete-li upravit role, které jsou přiřazeny uživateli, přejděte na **Správa systému \> Zabezpečení \> Přiřadit uživatele k rolím**. Uživatelům, kteří působí jako správci skladu pouze na jednotkách škálování, by měla být přiřazena pouze role *Vedoucí skladu na úloze*. Tento přístup zajistí, že tito uživatelé budou mít přístup pouze k podporovaným funkcím. Odeberte všechny další role, které jsou těmto uživatelům přiřazeny.

Uživatelům, kteří působí jako správci skladu v centru i na jednotkách škálování, by měla být přiřazena stávající role *pracovník skladu*. Uvědomte si, že tato role uděluje pracovníkům skladu přístup k funkcím (například zpracování příjmu objednávek přenosu), které se objevují v uživatelském rozhraní (UI), ale nejsou aktuálně podporovány na jednotkách škálování.

## <a name="supported-wes-processes"></a>Podporované procesy WES

Pro pracovní zátěž WES na jednotce škálování lze povolit následující procesy provádění skladu:

- Vybrané metody vln pro prodejní a převodové objednávky (alokace, doplnění poptávky, kontejnerizace, tvorba díla a tisk štítků vln)

- Zpracování skladových a prodejních zakázek pomocí aplikace skladu (včetně doplňovacích prací)
- Dotaz na zásoby po ruce pomocí aplikace skladu
- Vytváření a spouštění pohybů zásob pomocí aplikace skladu
- Vytváření a zpracování cyklu počítání prací pomocí aplikace skladu
- Provádění úprav zásob na skladě pomocí aplikace skladu
- Registrace nákupních objednávek a odvedení práce pomocí aplikace skladu

Následující pracovní příkazy jsou aktuálně podporovány pro pracovní zátěže WES na nasazení jednotek škálování:

- Prodejní objednávky
- Vydání převodního příkazu
- Doplnění (nezahrnuje suroviny pro výrobu)
- Přesun zásob
- Cyklická inventura
- Nákupní objednávky (které jsou propojeny se skladovými objednávkami)

V jednotkách škálování nejsou v současné době podporovány žádné jiné typy zdrojových dokumentů ani skladových prací. Například pro pracovní zátěž WES na jednotce měřítka nemůžete provést proces přijetí objednávky přenosu (potvrzení o převodu). Musí to být zpracováno instancí centra.

> [!NOTE]
> Položky nabídky mobilních zařízení a tlačítka pro nepodporované funkce se v _mobilní aplikaci Řízení skladu_ nezobrazí, když je připojena k nasazení jednotky škálování.

> [!WARNING]
> Když spustíte úlohu na jednotce škálování, nemůžete spustit nepodporované procesy pro konkrétní sklad v centru. Tabulky uvedené dále v tomto tématu dokumentují podporované funkce.
>
> Vybrané typy skladové práce lze vytvořit jak v centru, tak na jednotkách škálování, ale lze je udržovat pouze prostřednictvím vlastnícího centra nebo jednotky škálování (nasazení, které data vytvořilo).
>
> I když je určitý proces podporován na jednotce škálování, mějte na paměti, že se nemusí synchronizovat všechna potřebná data z centra na jednotku škálování nebo z jednotky škálování v centru, což může mít za následek neočekávané zpracování systému. Příklady:
> 
> - Pokud používáte dotaz na direktivu umístění, která se připojí k záznamu datové tabulky, který existuje pouze při nasazení centra.
> - Pokud používáte stav umístění a / nebo funkci volumetrického zatížení místa. Tato data nebudou synchronizována mezi nasazeními a budou proto fungovat pouze při aktualizaci umístění majetku na skladě na jednom z nasazení.

Následující funkce správy skladu nejsou aktuálně podporovány v úlohách jednotky škálování:

- Příchozí zpracování řádků nákupní objednávky přiřazených k vytížení
- Příchozí zpracování nákupních objednávek projektu
- Příchozí a odchozí zpracování pro položky, které mají jakékoli aktivní sledovacích dimenzí **Vlastník** a/nebo **Sériové číslo**
- Zpracování zásob, které mají hodnotu stavu blokování
- Změna stavu zásob během jakéhokoli procesu pracovního pohybu
- Flexibilní rezervace dimenze na úrovni skladu potvrzené podle objednávky
- Použití funkce *Stav umístění skladu* (data se mezi nasazeními nesynchronizují)
- Použití funkce *Umístění registrační značky*
- Použití nastavení *Filtry produktu* a *Skupiny filtrů produktů*, včetně nastavení **Počet dní ke kombinování šarží**
- Integrace s řízením kvality
- Zpracování s položkami se skutečnou hmotností
- Zpracování s položkami povolenými pouze pro správu dopravy (TMS)
- Zpracování s negativními zásobami na skladě
- Zpracování skladové práce s vlastními typy prací
- Zpracování skladové práce s dodacími listy
- Zpracování skladové práce s manipulací s materiálem / automatizací skladu
- Použití obrazu hlavních dat produktu (například v mobilní aplikaci Řízení skladu)

> [!WARNING]
> Některé funkce skladu nebudou k dispozici pro sklady se spuštěnými úlohami správy skladu na jednotce škálování a také nejsou podporovány na rozbočovači nebo na úlohách jednotky škálování.
> 
> Jiné funkce mohou být zpracovány na obou, ale budou vyžadovat pečlivé použití v některých scénářích, například když se zásoby na skladě aktualizují ro stejný čas v centru i jednotce škálování kvůli procesu aktualizace asynchronních dat.
> 
> Specifické funkce (např. *blokovat práci*), které jsou podporovány jak v centru, tak v jednotkách škálování, budou podporovány pouze pro vlastníka dat.

### <a name="outbound-supported-only-for-sales-and-transfer-orders"></a>Odchozí (podporováno pouze pro prodejní a objednávky a převodní příkazy)

Následující tabulka ukazuje, které odchozí funkce jsou podporovány a kde jsou podporovány, když se úlohy správy skladu používají v cloudových a hraničních jednotkách.

| Zpracovat                                                      | Centrum | Pracovní zátěž WES na jednotce škálování |
|--------------------------------------------------------------|-----|------------------------------|
| Zpracování zdrojového dokumentu                                   | Ano | Žádný |
| Zpracování správy nakládky a přepravy                | Ano | Žádný |
| Uvolnit do skladu                                         | Ano | Žádný |
| Plánovaný cross docking                                        | Žádný  | Žádný |
| Konsolidace dodávky                                       | Ano | Žádný |
| Zpracování vlny dodávky                                     | Ano, ale v centru je zpracována pouze inicializace a finalizace vlny. To znamená, že odchozí přenos a zpracování prodejní objednávky lze zpracovat pouze pomocí jednotky škálování.|<p>Ne, inicializaci a finalizaci zvládne centrum a **Vytváření a třídění nákladu** nejsou podporovány<p><b>Poznámka:</b> Přístup k centru je nutný pro finalizaci stavu vln jako součást zpracování vln.</p> |
| Udržování zásilek pro vlnu                                  | Ano | Žádný |
| Zpracování skladových prací (vč. tisku registrační značky)        | Žádný  | <p>Ano, ale pouze pro výše uvedené podporované funkce. |
| Výdej seskupení                                              | Žádný  | Ano|
| Ruční zpracování balení, vč. „Zpracování vychystávání zabaleného kontejneru“ | Žádný <P>Některé zpracování lze provést po počátečním procesu vychystávání zpracovaném jednotkou škálování, ale nedoporučuje se to kvůli následujícím blokovaným operacím.</p>  | Žádný |
| Odebrat kontejner ze skupiny                                  | Žádný  | Žádný |
| Zpracování odchozího třídění                                  | Žádný  | Žádný |
| Tisk dokumentů souvisejících se zátěží                           | Ano | Žádný |
| Přepravní doklad a generování ASN                            | Ano | Žádný |
| Potvrzení zásilky                                             | Ano | Žádný |
| Potvrzení zásilky s příkazem „Potvrdit a převést“            | Žádný  | Žádný |
| Zpracování dodacího listu a fakturace                        | Ano | Žádný |
| Krátký výběr (prodejní a převodové objednávky)                    | Žádný  | Žádný |
| Výběr nadměrného množství (prodejní a převodové objednávky)                     | Žádný  | Žádný |
| Změna pracovních míst (prodejní a převodní objednávky)         | Žádný  | Ano|
| Kompletní práce (prodejní a převodní objednávky)                    | Žádný  | Ano|
| Vytisknout sestavu práce                                            | Ano | Žádný |
| Štítek vlny                                                   | Žádný  | Ano|
| Rozdělení práce                                                   | Žádný  | Ano|
| Zpracování práce - režie 'Naložení přenosu'            | Žádný  | Žádný |
| Snížit vyskladněné množství                                       | Žádný  | Žádný |
| Stornovat práci                                                 | Žádný  | Žádný |
| Zrušit potvrzení expedice                                | Ano | Žádný |

### <a name="inbound"></a>Příchozí

Následující tabulka ukazuje, které příchozí funkce jsou podporovány a kde jsou podporovány, když se úlohy správy skladu používají v cloudových a hraničních jednotkách.

| Zpracovat                                                          | Centrum | Pracovní zátěž WES na jednotce škálování<BR>*(Položky označené „Ano“ platí pouze pro skladové objednávky)*</p> |
|------------------------------------------------------------------|-----|----------------------------------------------------------------------------------|
| Zpracování&nbsp;zdrojového&nbsp;dokumentu                             | Ano | Žádný |
| Zpracování správy nakládky a přepravy                    | Ano | Žádný |
| Potvrzení příchozí dodávky                                    | Ano | Žádný |
| Uvolnění nákupní objednávky do skladu (zpracování objednávky skladu) | Ano | Žádný |
| Zrušení řádků skladových objednávek<p>Upozorňujeme, že toto je podporováno pouze v případě, že nedošlo k žádné registraci proti řádku</p> | Ano | Žádný |
| Přijetí zboží nákupní objednávky a odložení                       | <p>Ano,&nbsp;když&nbsp;tam&nbsp;není skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | <p>Ano, když nákupní objednávka není součástí <i>vytížení</i></p> |
| Přijetí řádku nákupní objednávky a odložení                       | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | <p>Ano, když nákupní objednávka není součástí <i>vytížení</i></p></p> |
| Přijatá a odložená vratka                              | Ano | Žádný |
| Přijetí a odložení smíšené registrační značky                       | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | Žádný |
| Přijetí položky nákladu                                              | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | Žádný |
| Přijetí a odložení registrační značky                             | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | Žádný |
| Přijetí a odložení zboží převodního příkazu                       | Ano | Žádný |
| Převést řádek nákupní objednávky a odložení                       | Ano | Žádný |
| Zrušení práce (příchozí)                                            | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | <p>Ano, ale pouze, když možnost <b>Zrušit registraci potvrzení při rušení práce</b> (na stránce <b>Parametry správy skladu</b>) není podporována.</p> |
| Zpracování příjmu produktu z nákupní objednávky                        | Ano | Žádný |
| Příjem nákupní objednávky s nedostatečným doručením                      | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | Ano, ale pouze podáním žádosti o zrušení z centra |
| Příjem nákupní objednávky s nadměrným doručením                       | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | Ano  |
| Příjem s vytvořením práce *Cross docking*                 | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | Žádný |
| Příjem s vytvořením práce *Objednávka kvality*                  | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | Žádný |
| Příjem s vytvořením práce *Vzorek položky kvality*          | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | Žádný |
| Příjem s vytvořením práce *Kvalita v kontrole kvality*       | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | Žádný |
| Příjem s vytvořením objednávky kvality                            | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | Žádný |
| Zpracování práce - Režie *Cluster putaway*                 | Ano | Žádný |
| Zpracování práce s *Krátký výběr*                               | Ano | Žádný |
| Načtení registrační značky                                           | Ano | Ano |

### <a name="warehouse-operations-and-exception-handing"></a>Skladové operace a zpracování výjimek

Následující tabulka ukazuje, které funkce skladových operací a zpracování výjimek jsou podporovány a kde jsou podporovány, když se úlohy správy skladu používají v cloudových a hraničních jednotkách.

| Zpracovat                                            | Centrum | Pracovní zátěž WES na jednotce škálování |
|----------------------------------------------------|-----|------------------------------|
| Dotaz na registrační značku                              | Ano | Ano                          |
| Dotaz na zboží                                       | Ano | Ano                          |
| Dotaz na umístění                                   | Ano | Ano                          |
| Změnit sklad                                   | Ano | Ano                          |
| Přesun                                           | Ano | Ano                          |
| Pohyb podle šablony                               | Ano | Ano                          |
| Převod skladu                                 | Ano | Žádný                           |
| Vytvoření převodního příkazu z aplikace skladu           | Ano | Žádný                           |
| Úprava (příchozí/odchozí)                                | Ano | Ano, ale ne pro scénář úpravy, kdy je třeba rezervaci inventáře odstranit pomocí nastavení **Odebrat rezervace** na typech úprav zásob.</p>                           |
| Změna stavu zásob                            | Ano | Žádný                           |
| Zpracování nesrovnalostí cyklické inventury a počítání | Ano | Ano                           |
| Opakovaný tisk štítku (tisk registrační značky)             | Ano | Ano                          |
| Sestavení registrační značky vozidla                                | Ano | Žádný                           |
| Seskupení registračních značek                                | Ano | Žádný                           |
| Zabalit do vnořených registračních značek                                | Ano | Žádný                           |
| Přihlášení řidiče                                    | Ano | Žádný                           |
| Odhlášení řidiče                                   | Ano | Žádný                           |
| Změnit kód dispozice dávky                      | Ano | Ano                          |
| Zobrazit otevřený seznam úkolů                             | Ano | Ano                          |
| Konsolidovat registrační značky                         | Ano | Žádný                           |
| Zpracování doplnění min./max. a prahové hodnoty zóny| Ano <p>Nedoporučuje se zahrnout stejná umístění jako součást dotazů</p>| Ano                          |
| Slotting procesu doplnění                  | Ano  | Ano<p>Pamatujte, že nastavení musí být provedeno na jednotce škálování</p>                           |
| Práce blokování a odblokování                             | Ano | Ano                          |
| Změnit uživatele                                        | Ano | Ano                          |
| Změnit fond práce u práce                           | Ano | Ano                          |
| Zrušit práci                                        | Ano | Ano                          |

### <a name="production"></a>Výrobní

Následující tabulka shrnuje, které provozní scénáře správy skladu jsou (či nejsou) v současné době v pracovních zatíženích jednotky škálování podporovány.

| Zpracovat | Centrum | Pracovní zátěž WES na jednotce škálování |
|---------|-----|------------------------------|
| Ohlásit jako dokončené a vyskladnit dokončené zboží | Ano | Ano |
| Vyskladnění vedlejšího produktu | Ano | Ano |
| <p>Všechny ostatní procesy správy skladu, které souvisí s výrobou, včetně:</p><li>Uvolnit do skladu</li><li>Vlnové zpracování výroby</li><li>Výdej suroviny</li><li>Kanban – odložení</li><li>Kanban – výdej</li><li>Spustit výrobní zakázku</li><li>Výrobní odpad</li><li>Poslední paleta výroby</li><li>Zaregistrovat spotřebu materiálu</li><li>Prázdný kanban</li></ul> | Ano | Žádný |
| Doplnění surovin | Žádný | Žádný |

## <a name="maintaining-scale-units-for-wes"></a>Údržba jednotek škálování pro WES

Několik dávkových úloh spuštěných v jednotce centra i škály.

V nasazení centra můžete dávkové úlohy spravovat ručně. Následující dávkové úlohy můžete spravovat v okně **Vedení skladu \> Pravidelné úkoly \> Správa pracovní zátěže v kanceláři**:

- Zpracovatel zprávy jednotky škálování do centra
- Registrovat příjmy zdrojové objednávky
- Dokončit skladové objednávky

V úloze v jednotkách škálování můžete spravovat následující dávkové úlohy v okně **Správa skladu \> Pravidelné úkoly \> Správa úlohy**:

- Zpracování záznamů tabulky vln
- Zpracovatel zprávy z centra skladu do jednotky škálování
- Zpracovat požadavky na aktualizaci množství pro řádky objednávky skladu

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
