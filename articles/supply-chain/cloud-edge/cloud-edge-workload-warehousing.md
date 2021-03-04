---
title: Pracovní zátěže správy skladu pro cloudové a hraniční jednotky škálování
description: Toto téma poskytuje informace o funkci, která umožňuje jednotkám škálování spouštět vybrané procesy z vaší úlohy správy skladu.
author: perlynne
manager: tfeyr
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, SysSecRolesEditUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4ac76ad5cd88c35ac312b8e73d942a692f35c8aa
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516742"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Pracovní zátěže správy skladu pro cloudové a hraniční jednotky škálování

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> Ne všechny obchodní funkce jsou ve veřejném náhledu plně podporovány, když se používají jednotky škálování pracovní zátěže. Používáte pouze takové procesy, které toto téma výslovně popisuje jako podporované.

## <a name="warehouse-execution-on-scale-units"></a>Spuštění skladu v jednotkách škálování

Tato funkce umožňuje jednotkám škálování spouštět vybrané procesy z možností správy skladu. Cloudové jednotky škálování spouští svá pracovní zatížení v cloudu pomocí vyhrazené kapacity zpracování ve vašem vybraném regionu Microsoft Azure. U hraničních jednotek škálování můžete spouštět některé úlohy nezávisle v prostorách, i když jsou jednotky škálování dočasně odpojené od cloudu.

V tomto tématu jsou spouštění správy skladu ve skladu, který je definován jako jednotka škálování, označovány jako *Systém spuštění skladu* (*WES*).

## <a name="prerequisites"></a>Předpoklady

Musíte mít centrum Dynamics 365 Supply Chain Management hub a jednotku škálování, která byla nasazena s úlohou správy skladu. Další informace o architektuře a procesu nasazení naleznete v části [Cloudové a hraniční jednotky škálování pro úlohy výroby a správy skladu](cloud-edge-landing-page.md).

## <a name="how-the-wes-workload-works-on-scale-units"></a>Jak funguje pracovní zátěž WES na jednotkách škálování

U procesů v úlohách správy skladu se data synchronizují mezi centrem a jednotkami škálování.

Jednotka škálování může udržovat pouze data, která vlastní. Koncept vlastnictví dat pro jednotky škálování pomáhá předcházet konfliktům multi-master. Proto je důležité, abyste pochopili, které procesy jsou vlastněny centrem a které jsou vlastněny jednotkami škálování.

Jednotky škálování vlastní následující data:

- **Vlnové zpracování dat** - Vybrané metody zpracování vln jsou zpracovávány v rámci vlnového zpracování jednotky škálování.
- **Údaje o zpracování práce** - Jsou podporovány následující typy zpracování pracovních příkazů:

    - Pohyby zásob (ruční pohyb a pohyb podle šablony práce)
    - Nákupní objednávky (odložená práce prostřednictvím skladové objednávky)
    - Prodejní objednávky (jednoduchá práce vyzvednutí a vložení)

- **Údaje o přijetí skladové objednávky** - Tato data se používají pouze pro nákupní objednávky, které jsou ručně uvolněny do skladu.
- **Údaje o registrační značce** - Registrační značky lze vytvářet v centru a jednotce škálování. Bylo poskytnuto vyhrazené řešení konfliktů. Tato data nejsou specifická pro sklad.

## <a name="outbound-process-flow"></a>Odchozí tok procesu

Centrum vlastní následující data:

- Všechny zdrojové dokumenty, například prodejní objednávky a objednávky přenosu
- Přidělení objednávky a zpracování odchozího zatížení
- Procesy uvolnění do skladu, vytvoření zásilky a vytvoření vlny

Jednotky stupnice vlastní skutečné vlnové zpracování (jako je přidělení práce, doplňovací práce a vytvoření poptávky práce) po vydání vlny. Pracovníci skladu proto mohou zpracovávat odchozí práci pomocí aplikace skladu, která je připojena k jednotce škálování.

![Tok zpracování vlny](./media/wes_wave_processing_flow.png "Tok zpracování vlny")

## <a name="inbound-process-flow"></a>Příchozí tok procesu

Centrum vlastní následující data:

- Všechny zdrojové dokumenty, například nákupní objednávky a objednávky vrácení prodeje
- Příchozího zpracování vytížení

> [!NOTE]
> Tok příchozích nákupních objednávek se koncepčně liší od odchozích toků, kde jednotka škálování, která provádí zpracování, závisí na tom, zda byla objednávka vydána do skladu.

Pokud používáte proces *uvolnění do skladu*, vytvoří se objednávky skladu a vlastnictví příslušného toku příjmu se přiřadí jednotce škálování. Centrum nebude moci zaregistrovat příchozí příjem.

Pracovník může spustit proces příjmu pomocí aplikace skladu, která je připojena k jednotce škálování. Data se poté zaznamenají podle jednotky škálování a nahlásí se proti příchozí skladové objednávce. Vytvoření a zpracování následného odložení bude také zpracováno podle jednotky škálování.

Pokud nepoužíváte proces *vydání do skladu* a tím pádem ani *skladové objednávky*, centrum může zpracovávat příjem skladu a zpracování práce nezávisle na jednotkách škálování.

![Příchozí tok procesu](./media/wes_Inbound_flow.png "Příchozí tok procesu")

## <a name="supported-processes-and-roles"></a>Podporované procesy a role

Ne všechny procesy správy skladu jsou podporovány v pracovní zátěži WES na jednotce škálování. Proto doporučujeme přiřadit role, které odpovídají funkcím, které jsou k dispozici každému uživateli.

Pro usnadnění tohoto procesu je pojmenovaná ukázková role *Vedoucí skladu při úloze* je součástí ukázkových dat v okně **Správa systému \> Zabezpečení \> Konfigurace zabezpečení**. Účelem této role je umožnit správcům skladu přístup k WES na jednotce škálování. Role uděluje přístup ke stránkám, které jsou relevantní v kontextu úlohy, která je hostována na jednotce škálování.

Role uživatele na jednotce škálování jsou přiřazeny jako součást počáteční synchronizace dat z rozbočovače na jednotku škálování.

Chcete-li upravit role, které jsou přiřazeny uživateli, přejděte na **Správa systému \> Zabezpečení \> Přiřadit uživatele k rolím** v jednotce škálování. Uživatelům, kteří působí jako správci skladu pouze na jednotkách škálování, by měla být přiřazena pouze role *Vedoucí skladu na úloze*. Tento přístup zajistí, že tito uživatelé budou mít přístup pouze k podporovaným funkcím. Odeberte všechny další role, které jsou těmto uživatelům přiřazeny.

Uživatelům, kteří působí jako správci skladu v centru i na jednotkách škálování, by měla být přiřazena stávající role *pracovník skladu*. Uvědomte si, že tato role uděluje pracovníkům skladu přístup k funkcím (například zpracování objednávek přenosu), které se objevují v uživatelském rozhraní (UI), ale nejsou aktuálně podporovány na jednotkách škálování.

## <a name="supported-wes-processes"></a>Podporované procesy WES

Pro pracovní zátěž WES na jednotce škálování lze povolit následující procesy provádění skladu:

- Vybrané metody vln pro prodejní objednávky a doplnění poptávky
- Spouštění pracovních příkazů z prodejních objednávek a doplňování poptávky pomocí aplikace skladu
- Dotaz na zásoby po ruce pomocí aplikace skladu
- Vytváření a spouštění pohybů zásob pomocí aplikace skladu
- Registrace nákupních objednávek a odvedení práce pomocí aplikace skladu

Následující pracovní příkazy jsou aktuálně podporovány pro pracovní zátěže WES na nasazení jednotek škálování:

- Prodejní objednávky
- Doplnění
- Přesun zásob
- Nákupní objednávky, které jsou propojeny se skladovými objednávkami

V jednotkách škálování není aktuálně podporováno žádné jiné zpracování zdrojových dokumentů. Například pro pracovní zátěž WES na jednotce škálování nemůžete provádět následující akce:

- Vydejte příkaz k převodu.
- Zpracujte operace vychystávání a expedice odchozího skladu.

> [!IMPORTANT]
> Pokud používáte pracovní zátěž na jednotce škálování, nemůžete spustit nepodporované procesy pro konkrétní sklad v centru.

Následující funkce správy skladu nejsou aktuálně podporovány v jednotkách škálování:

- Příchozí a odchozí zpracování pro položky, které mají jakékoli aktivní sledovací dimenze (například dimenze dávky nebo sériového čísla)
- Zpracování změn stavu zásob
- Zpracování zásob, které mají hodnotu stavu blokování
- Integrace s řízením kvality
- Integrace s produkcí
- Zpracování položek se skutečnou hmotností
- Zpracování nadměrné a nedostatečné dodávky
- Zpracování negativních zásob na skladě

### <a name="outbound-supported-only-for-sales-orders-and-demand-replenishment"></a>Odchozí (podporováno pouze pro prodejní objednávky a doplnění poptávky)

Následující tabulka ukazuje, které odchozí funkce jsou podporovány a kde jsou podporovány, když se úlohy správy skladu používají v cloudových a hraničních jednotkách.

> [!WARNING]
> Protože je podporováno pouze zpracování prodejní objednávky, nelze zpracování odchozích skladů použít pro objednávky přenosu.
>
> Některé funkce skladu nebudou k dispozici ve skladech, kde jsou spuštěny úlohy správy skladu v jednotce škálování.

| Zpracovat                                                      | Centrum | Pracovní zátěž WES na jednotce škálování |
|--------------------------------------------------------------|-----|------------------------------|
| Zpracování zdrojového dokumentu                                   | Ano | Žádný |
| Zpracování správy nakládky a přepravy                | Ano | Žádný |
| Uvolnit do skladu                                         | Ano | Žádný |
| Konsolidace dodávky                                       | Žádný  | Žádný |
| Práce cross docking (práce vyskladnění)                                 | Žádný  | Žádný |
| Zpracování vlny dodávky                                     | Ne, ale finalizace stavu vlny je řešena v centru |<p>Ale, nejsou podporovány následující schopnosti:</p><ul><li>Paralelní tvorba práce</li><li>Sestavení a třídění nakládky</li><li>Vytváření kontejnerů</li><li>Tisk štítků vlny</li></li></ul><p><b>Poznámka:</b> Přístup k centru je nutný pro finalizaci stavu vln jako součást zpracování vln.</p> |
| Zpracování skladových prací (vč. tisku registrační značky)     | Žádný  | <p>Ano, ale pouze pro následující schopnosti:</p><ul><li>Výběr prodeje (bez použití aktivních dimenzí sledování)</li><li>Nakládání prodeje (bez použití aktivních dimenzí sledování)</li></ul> |
| Výdej seskupení                                              | Žádný  | Žádný |
| Zpracování balení                                           | Žádný  | Žádný |
| Zpracování odchozího třídění                                  | Žádný  | Žádný |
| Tisk dokumentů souvisejících se zátěží                           | Ano | Žádný |
| Přepravní doklad a generování ASN                            | Ano | Žádný |
| Potvrzení o odeslání a zpracování dodacího listu                | Ano | Žádný |
| Krátký výběr (prodejní objednávky)                                 | Žádný  | Žádný |
| Zrušení práce                                            | Žádný  | Žádný |
| Změna pracovních míst (prodejní objednávky)                      | Žádný  | Žádný |
| Kompletní práce (prodejní objednávky)                                 | Žádný  | Žádný |
| Práce blokování a odblokování                                       | Žádný  | Žádný |
| Změnit uživatele                                                  | Žádný  | Žádný |
| Vytisknout sestavu práce                                            | Žádný  | Žádný |
| Štítek vlny                                                   | Žádný  | Žádný |
| Stornovat práci                                                 | Žádný  | Žádný |

### <a name="inbound"></a>Příchozí

Následující tabulka ukazuje, které příchozí funkce jsou podporovány a kde jsou podporovány, když se úlohy správy skladu používají v cloudových a hraničních jednotkách.

| Zpracovat                                                          | Centrum | Pracovní zátěž WES na jednotce škálování |
|------------------------------------------------------------------|-----|------------------------------|
| Zpracování&nbsp;zdrojového&nbsp;dokumentu                                       | Ano | Žádný |
| Zpracování správy nakládky a přepravy                    | Ano | Žádný |
| Potvrzení zásilky                                            | Ano | Žádný |
| Uvolnění nákupní objednávky do skladu (zpracování objednávky skladu) | Ano | Žádný |
| Přijetí zboží nákupní objednávky a odložení                        | <p>Ano,&nbsp;když&nbsp;tam&nbsp;není skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | <p>Ano, když existuje skladová objednávka a když nákupní objednávka není součástí <i>zatížení</i>. Musí však být použity dvě položky nabídky mobilního zařízení, jedna pro příjem (<i>Příjem položky nákupní objednávky</i>) a další s povolenou možností <b>Použít existující práci</b> ke zpracování výdeje.</p><p>Ne, pokud neexistuje skladová objednávka.</p> |
| Přijetí řádku nákupní objednávky a odložení                        | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | Žádný |
| Přijatá a odložená vratka                               | Ano | Žádný |
| Přijetí a odložení smíšené registrační značky                        | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | Žádný |
| Přijetí položky nákladu                                              | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | Žádný |
| Přijetí a odložení registrační značky                              | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | Žádný |
| Přijetí a odložení zboží převodního příkazu                        | Ano | Žádný |
| Převést řádek nákupní objednávky a odložení                        | Ano | Žádný |
| Zrušení práce                                                | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | <p>Ano, ale možnost <b>Zrušit registraci potvrzení při rušení práce</b> (na stránce <b>Parametry správy skladu</b>) není podporována.</p> |
| Zpracování příjmu produktu z nákupní objednávky                        | Ano | Žádný |
| Vytvoření práce v rámci dokování jako součást příjmu                 | <p>Ano, pokud neexistuje skladová objednávka</p><p>Ne, pokud existuje skladová objednávka</p> | Žádný |

### <a name="warehouse-operations-and-exception-handing"></a>Skladové operace a zpracování výjimek

Následující tabulka ukazuje, které funkce skladových operací a zpracování výjimek jsou podporovány a kde jsou podporovány, když se úlohy správy skladu používají v cloudových a hraničních jednotkách.

| Zpracovat                                            | Centrum | Pracovní zátěž WES na jednotce škálování |
|----------------------------------------------------|-----|------------------------------|
| Dotaz na registrační značku                              | Ano | Ano                          |
| Dotaz na zboží                                       | Ano | Ano                          |
| Dotaz na umístění                                   | Ano | Ano                          |
| Změnit sklad                                   | Ano | Ano                          |
| Přesun                                           | Žádný  | Ano                          |
| Pohyb podle šablony                               | Žádný  | Ano                          |
| Úprava (příchozí/odchozí)                                | Ano | Žádný                           |
| Zpracování nesrovnalostí cyklické inventury a počítání | Ano | Žádný                           |
| Opakovaný tisk štítku (tisk registrační značky)             | Ano | Žádný                           |
| Sestavení registrační značky vozidla                                | Ano | Žádný                           |
| Seskupení registračních značek                                | Ano | Žádný                           |
| Přihlášení řidiče                                    | Ano | Žádný                           |
| Odhlášení řidiče                                   | Ano | Žádný                           |
| Změnit kód dispozice dávky                      | Ano | Žádný                           |
| Zobrazit otevřený seznam úkolů                             | Ano | Žádný                           |
| Konsolidovat registrační značky                         | Žádný  | Žádný                           |
| Odebrat kontejner ze skupiny                        | Žádný  | Žádný                           |
| Zrušit práci                                        | Žádný  | Žádný                           |
| Vytvoření procesu minimálního/maximálního doplňování                   | Žádný  | Žádný                           |
| Slotting procesu doplnění                  | Žádný  | Žádný                           |

### <a name="production"></a>Výrobní

Integrace správy skladu pro produkční scénáře není aktuálně podporována, jak je uvedeno v následující tabulce.

| Zpracovat | Centrum | Pracovní zátěž WES na jednotce škálování |
|---------|-----|------------------------------|
| <p>Všechny procesy správy skladu, které souvisí s výrobou. Několik příkladů:</p><li>Uvolnit do skladu</li><li>Vlnové zpracování výroby</li><li>Výdej suroviny</li><li>Výdej dokončeného zboží</li><li>Vyskladnění vedlejšího produktu</li><li>Kanban – odložení</li><li>Kanban – výdej</li><li>Spustit výrobní zakázku</li><li>Výrobní odpad</li><li>Poslední paleta výroby</li><li>Zaregistrovat spotřebu materiálu</li><li>Prázdný kanban</li></ul> | Žádný | Žádný |

## <a name="maintaining-scale-units-for-wes"></a>Údržba jednotek škálování pro WES

Několik dávkových úloh spuštěných v jednotce centra i škály.

V nasazení centra můžete dávkové úlohy spravovat ručně. Následující tři úlohy můžete spravovat v okně **Vedení skladu \> Pravidelné úkoly \> Správa pracovní zátěže v kanceláři**:

- Zpracovat události aktualizace stavu práce
- Zpracovat události přenosu kontroly provedení vlny
- Registrovat příjmy zdrojové objednávky

V úloze v jednotkách škálování můžete spravovat následující dvě dávkové úlohy v okně **Správa skladu \> Pravidelné úkoly \> Správa úlohy**:

- Zpracování záznamů tabulky vln
- Zpracovat události přenosu kontroly provedení vlny


[!INCLUDE[footer-include](../../includes/footer-banner.md)]