---
title: Odstraněné nebo zastaralé funkce
description: Toto téma popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění.
author: sericks007
manager: AnnBe
ms.date: 04/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 21821
ms.assetid: 31019808-4cbf-47d7-b1ba-d791db4281ae
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7afe26b535ca2578d2db17f676c3cae4bafc355f
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1527664"
---
# <a name="removed-or-deprecated-features"></a>Odstraněné nebo zastaralé funkce

[!include [banner](../includes/banner.md)]

Toto téma popisuje funkce, které byly odebrány nebo jsou zastaralé pro aplikaci Dynamics 365 for Finance and Operations.

- *Odstraněná* funkce již není k dispozici v produktu.
- *Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.

Tento seznam je určen k tomu, aby vám pomohl zvážit tyto odstraněné a zastaralé funkce při svém plánování. 

> [!NOTE]
> Počínaje vydáním Dynamics 365 for Finance and Operations z července 2017 s aktualizací Platform Update 8 se uvádí typ nasazení pro každou odstraněnou nebo zastaralou funkci. Všechny předchozí verze uvedené v tomto tématu podporovaly cloudové nasazení.

> [!NOTE]
> Podrobné informace o objektech v aplikaci Finance and Operations lze nalézt v části [Sestavy technických informací](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Můžete srovnat různé verze těchto sestav a zjistíte, které objekty se změnily nebo byly odstraněny v každé z verzí aplikace Finance and Operations.


## <a name="dynamics-365-for-finance-and-operations-1002-with-platform-update-26"></a>Dynamics 365 for Finance and Operations 10.0.2 s aktualizací Platform Update 26

> [!IMPORTANT]
> Dynamics 365 for Finance and Operations 10.0.2 s aktualizací Platform Update 26 jsou k dispozici pro cílené uživatele jako součást verze Preview. Obsah a funkce se mohou změnit. Další informace o předchozích verzích naleznete v tématu [Dostupnost aktualizací služby](../../fin-and-ops/get-started/public-preview-releases.md).

### <a name="legacy-default-action-behavior"></a>Starší výchozí chování akce

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Starší chování výchozích akcí v mřížkách vede k nečekanému sloupci s výchozím odkazem na akci po změně pořadí sloupců mřížky přes přizpůsobení. Tuto akci napravuje nová výchozí akce jedním prstem. Další informace naleznete v tématu [Výchozí akce jedním prstem v mřížce](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/sticky-default-action). |
| **Nahrazeno jinou funkcí?**   | Od aktualizace Platformy 21 byla zavedena funkce výchozích akcí jedním prstem. Tuto funkci lze povolit na stránce **Možnosti výkonu klienta**. |
| **Ovlivněné oblasti produktu**         | Mřížky ve webovém klientovi |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: Od dubna 2020 budou výchozí akce jedním prstem výchozím chováním bez mechanismu výchozího chování. |

### <a name="legacy-is-one-of-filtering-experience"></a>Zastarání "je jedna z" možností filtrování

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Možnost "je jedna" filtrování prošla v aktualizaci Platform 22 změnou, přičemž plán je pravděpodobně možnost filtrování "je jedním z". |
| **Nahrazeno jinou funkcí?**   | Počínaje aktualizací Platform update 22 je vylepšená možnost filtrování "je jedním z" k dispozici na stránce **Možnosti výkonu klienta**. Více informací viz [Optimalizovaná možnost filtrování „je jeden z“](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/improved-isoneof-filtering). |
| **Ovlivněné oblasti produktu**         | Webový klient |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: Od dubna 2020 bude možnost "je jedním z" výchozím chováním bez mechanismu výchozího chování. |

### <a name="parameter-to-enable-sales-orders-with-multiple-project-contract-funding-sources"></a>Parametr umožňující prodejní objednávky s více zdroji financování projektové smlouvy
Podpora pro vytváření prodejních objednávek na základě projektů, kde měla projektová smlouva více zdrojů financování s nastavením **parametrů řízení projektů** **Povolit prodejní objednávky pro projekt v více zdroji financování**. Tento parametr není ve výchozím nastavení povolen. 

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Funkce bude vždy povolena po odebrání parametru. |
| **Nahrazeno jinou funkcí?**   | Č. Funkce pro podporu prodejních objednávek založených na projektu s více zdroji financování bude povolena vždy.   |
| **Ovlivněné oblasti produktu**         |Parametr **Povolit prodejní objednávky pro projekty s více zdroji financování** bude odebrán. Po odebrání parametru budou modifikovány následující metody: metoda **ctrlSalesOrderTable** ve třídě **ProjStatusType**, metoda **validate** pro pole **ProjId** a metoda **run** ve formuláři **SalescreateOrder**. Následující metody budou po odebrání parametru zastaralé: metoda **IsSalesOrderAllowedForMultipleFundingSources** v souboru tabulky **ProjTable**, metoda **IsAllowSalesOrdersForMultipleFundingSourcesParamEnabled** v souboru tabulky **ProjTable**, datové pole **AllowSalesOrdersForMultipleFundingSources** ve formuláři **ProjParameters** a v souborech **ProjParameterEntity**, soukromá metoda **IsAssociatedToMultipleFundingSourcesContract** v souboru tabulky **ProjTable**. |
| **Možnost nasazení**              | Vše  |
| **Stav**                         | Odpisování je plánováno pro vlnu vydání v dubnu 2020. |

### <a name="legacy-workflow-reports-for-tracking-and-instance-status"></a>Zastaralé sestavy workflowu pro sledování stavu instance

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Sestavy ze starší verze workflowu pro sledování a stav instance jsou odepsané, protože na ně již není odkazováno z navigace. Názvy sestavy jsou WorkflowWorkflowInstanceByStatusReport a WorkflowWorkflowTrackingReport. |
| **Nahrazeno jinou funkcí?**   | Místo toho lze použít formulář Historie workflowu. |
| **Ovlivněné oblasti produktu**         | Webový klient |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: Plánovaná doba pro odstranění funkcionality je duben 2020. |

## <a name="dynamics-365-for-finance-and-operations-1001-with-platform-update-25"></a>Dynamics 365 for Finance and Operations 10.0.1 s aktualizací Platform Update 25

> [!IMPORTANT]
> Dynamics 365 for Finance and Operations 10.0.1 s aktualizací Platform Update 25 jsou k dispozici pro cílené uživatele jako součást verze Preview. Obsah a funkce se mohou změnit. Další informace o předchozích verzích naleznete v tématu [Dostupnost aktualizací služby](../../fin-and-ops/get-started/public-preview-releases.md).

### <a name="deprecated-apis-and-potential-breaking-changes"></a>Zastaralá rozhraní API a možná přerušení změn


#### <a name="deriving-from-internal-classes-is-deprecated"></a>Odvození z interních tříd je zastaralé

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Před aktualizací Platform Update 25 bylo možné vytvořit třídu nebo tabulku odvozenou z interní třídy/tabulky, která je definována v jiném balíčku/modulu. Nejedná se o bezpečný postup kódování. Od aktualizace Platform update 25 bude kompilátor zobrazovat upozornění. |
| **Nahrazeno jinou funkcí?**   | Upozornění kompilátoru bude nahrazeno chybou v příští aktualizaci Platform update 26. Tato změna je zpětně kompatibilní za běhu, což znamená, že pokud používáte aktualizaci Platform Update 25 nebo novější, můžete ji nasadit do libovolného prostředí sandbox nebo do produkčního prostředí bez nutnosti upravovat vlastní kód. Tato změna ovlivní čas nasazení a kompilace.|
| **Ovlivněné oblasti produktu**         | Vývojové nástroje Visual Studio |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: Upozornění bude nahrazeno chybou kompilace v příští aktualizaci Platform Update 26. |

#### <a name="overriding-internal-methods-is-deprecated"></a>Přepsání interních metod je zastaralé

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Před aktualizací Platform Update 25 bylo možné přepsat interní metodu v odvozené třídě, která je definována v jiném balíčku/modulu. Nejedná se o bezpečný postup kódování. Od aktualizace Platform update 25 bude kompilátor zobrazovat upozornění. |
| **Nahrazeno jinou funkcí?**   | Toto upozornění kompilátoru bude nahrazeno chybou sestavení v příští aktualizaci Platform update 26. Tato změna je zpětně kompatibilní za běhu, což znamená, že pokud používáte aktualizaci Platform Update 25 nebo novější, můžete ji nasadit do libovolného prostředí sandbox nebo do produkčního prostředí bez nutnosti upravovat vlastní kód. Tato změna ovlivní čas nasazení a kompilace. |
| **Ovlivněné oblasti produktu**         | Vývojové nástroje Visual Studio |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: Upozornění bude nahrazeno chybou kompilace v příští aktualizaci Platform Update 26. |


## <a name="dynamics-365-for-finance-and-operations-813-with-platform-update-23"></a>Dynamics 365 for Finance and Operations 8.1.3 s aktualizací Platform Update 23

### <a name="sql-server-reporting-services-reportviewer-control"></a>Kontrola SQL Server Reporting Services ReportViewer
Zákazníci mohou použít akci **Exportovat** poskytovanou vestavěným ovládacím prvkem SQL Server Reporting Services (SSRS) ReportViewe ke stažení dokumentů vyprodukovaných aplikacemi Finance and Operations. Tato prezentace sestavy na bázi HTML nabízí uživatelům náhled dokumentu bez číslování stránek.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Povaha náhledu na bázi HTML bez čísel stránek **neposkytuje** věrnost s fyzickými dokumenty produkovanými aplikací Finance and Operations. Plným začleněním PDF jako standardního formátu pro obchodní dokumenty mohou uživatelé využívat moderní zobrazení prostředí se zvýšením výkonu při vytváření sestav aplikace. |
| **Nahrazeno jinou funkcí?**   | Do budoucna budou dokumenty PDF výchozím formátem pro sestavy vykreslované aplikací Finance and Operations.   |
| **Ovlivněné oblasti produktu**         | Tato změna **nemá** vliv na scénáře, kdy jsou sestavy rozesílány elektronicky nebo odesílány přímo na tiskárny.    |
| **Možnost nasazení**              | Vše  |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno. Funkce automatického náhledu sestav aplikací pomocí vestavěného prohlížeče ve formátu PDF je plánována na aktualizaci Platform Update v květnu 2019. |

### <a name="client-kpi-controls"></a>Ovládací prvky klíčových ukazatelů výkonu klienta
Vložené klíčové indikátory výkonnosti (KPI) mohou být vývojářem modelovány v aplikaci Visual Studio a dále upravovány koncovým uživatelem.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Nativní ovládací prvky klienta používané k definování KPI mají nízký vstup od zákazníka a spoléhají na vývojáře, který přidává sledovatelné metriky. |
| **Nahrazeno jinou funkcí?**   | Služba PowerBI.com poskytuje nástroje světové třídy pro definování a správu indikátorů KPI na základě dat z externích zdrojů.  V nadcházející verzi plánujeme umožnit vkládání řešení hostovaných na PowerBI.com v pracovních prostorech aplikací.   |
| **Ovlivněné oblasti produktu**         | Tato aktualizace zabrání vývojářům vkládání nových ovládacích prvků KPI v návrháři Visual Studio.    |
| **Možnost nasazení**              | Vše  |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno. |

### <a name="deprecated-apis-and-future-breaking-changes"></a>Zastaralá rozhraní API a budoucí přerušení změn

#### <a name="field-groups-containing-invalid-field-references"></a>Skupiny polí obsahující neplatné odkazy na pole

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Definice tabulkových metadat mohou mít skupiny polí obsahující neplatné odkazy na pole. Tento problém je v současné době kategorizován jako *varování kompilátoru*, nikoli jako *chyba*, což znamená, že vytvoření a nasazení zaváděcího balíčku může pokračovat bez opravení problému. Při nasazení to může způsobit chyby runtime ve finančním výkaznictví a službě SQL Server Reporting Services (SSRS). Chcete-li vyřešit tento problém:<br><br>1. Odeberte neplatný odkaz na pole z definice skupiny pole tabulky.<br><br>2. Proveďte kompilaci znovu.<br><br>3. Ujistěte se, že jsou adresovány veškeré chyby nebo upozornění. |
| **Nahrazeno jinou funkcí?**   | Upozornění bude nahrazeno kompilační chybou v budoucnosti.  |
| **Ovlivněné oblasti produktu**         | Vývojové nástroje Visual Studio. |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: Upozornění se v budoucnu stane chybou při kompilaci. Plánujeme to v aktualizaci Platform Update 30. |

#### <a name="complete-list"></a>Úplný seznam
Pro přístup k úplnému seznamu zastaralých rozhraní API nahlédněte do části [Zastarání metod a prvků metadat](deprecation-deletion-apis.md).

## <a name="dynamics-365-for-finance-and-operations-81-with-platform-update-20"></a>Dynamics 365 for Finance and Operations 8.1 s aktualizací Platform Update 20

### <a name="batch-transfer-rules-for-subledger-journal-account-entries"></a>Pravidla dávkových převodů pro položky účtu dílčí hlavní knihy
Režim synchronního převodu je zastaralý v parametrech hlavní knihy.  Tento režim je nahrazen pouze možnostmi Asynchronní a plánovaná dávka, které již existují jako možnosti pro převod. Další informace naleznete v blogu [Parametry hlavní knihy - pravidla dávkového přenosu ](https://community.dynamics.com/365/financeandoperations/b/financials/archive/2019/03/15/general-ledger-parameters-batch-transfer-rules).

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Odstraňujeme synchronní možnost kvůli dopadu na výkon systému. |
| **Nahrazeno jinou funkcí?**   | Asynchronní a plánovaná dávka jsou možnosti, které mají být použity místo synchronní možnosti.   |
| **Ovlivněné oblasti produktu**         | Hlavní kniha, Závazky, Pohledávky, Zásobování, Výdaje    |
| **Možnost nasazení**              | Vše  |
| **Stav**                         | Zastaralé: Plánovaná doba pro odstranění funkcionality je verze 10.0.|

### <a name="electronic-reporting-for-russia"></a>Elektronické výkaznictví pro Rusko
Funkce pro konfiguraci formátů souborů TXT a XML prohlášení. 

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Nahrazeno elektronickým výkaznictvím. |
| **Nahrazeno jinou funkcí?**   | Ano. |
| **Ovlivněné oblasti produktu**         | Hlavní kniha |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Odebráno od verze Dynamics 365 for Finance and Operations 8.1 s aktualizací Platform Update 20. |

### <a name="financial-reports-generator-for-russia"></a>Generátor finančních sestav pro Rusko
Nástroj pro nastavení shromažďování dat pro účetnictví a daňové sestavy a export dat do šablon sestavy XLS a DOC. Funkční části: jsou odstraněny export dat do šablon sestavy XLS , dotazy a pevné požadavky. 

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Odebrané části jsou nahrazeny elektronickým výkaznictvím. |
| **Nahrazeno jinou funkcí?**   | Ano. Uživatelské rozhraní nastavení finančních sestav by mělo být použito pro nastavení pravidel shromažďování dat účty hlavní knihy a daňovými registry. Export dat do různých typů souborů, pevné požadavky a pravidla shromažďování dat podobná dotazům musí být nakonfigurovány v elektronickém výkaznictví. |
| **Ovlivněné oblasti produktu**         | Hlavní kniha. |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Odebráno od verze Dynamics 365 for Finance and Operations 8.1 s aktualizací Platform Update 20. |

### <a name="integration-with-external-providers-for-sending-electronic-reporting-through-communication-channels-for-russia"></a>Integrování s externími poskytovateli pro odeslání elektronických sestav prostřednictvím komunikačních kanálů pro Rusko
Funkce exportující generované elektronické soubory deklarací do složky pro další zasílání oficiálním poskytovatelům elektronického výkaznictví, stejně jako import stavu zpět.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Nahrazeno konfigurovatelnou funkcí elektronických zpráv. |
| **Nahrazeno jinou funkcí?**   | Ano.  |
| **Ovlivněné oblasti produktu**         | Hlavní kniha, daň |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Odebráno od verze Dynamics 365 for Finance and Operations 8.1 s aktualizací Platform Update 20. |


### <a name="profit-tax-register-wizard"></a>Průvodce registrem daně ze zisku
Funkce pro vytvoření šablony pro nové registry daně ze zisku. Tato funkce vytváří objekty X ++ pro nové registry, které jsou pak vytvořeny jako šablony s přidanou odpovídající výpočetní logikou.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Funkce není kompatibilní s modelem rozšiřitelnosti Dynamics 365 for Finance and Operations. |
| **Nahrazeno jinou funkcí?**   | Žádný |
| **Ovlivněné oblasti produktu**         | Daň |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Odebráno od verze Dynamics 365 for Finance and Operations 8.1 s aktualizací Platform Update 20. |


## <a name="dynamics-365-for-finance-and-operations-80-with-platform-update-15"></a>Dynamics 365 for Finance and Operations 8.0 s aktualizací Platform Update 15
V této verzi nebyly odebrány ani odepsány žádné funkce. Aktualizace platformy 15 je kumulativní a obsahuje nové a změněné funkce aktualizace platformy 13, aktualizace platformy 14 a aktualizace platformy 15.

## <a name="dynamics-365-for-finance-and-operations-enterprise-edition-73-with-platform-update-12"></a>Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 s aktualizací Platform Update 12

### <a name="personalized-product-recommendations"></a>Doporučení přizpůsobeného produktu 
Od 15. února 2018 již nebudou maloobchodní prodejci schopní zobrazit doporučení přizpůsobeného produktu na zařízení POS. Další informace naleznete v tématu [Doporučení přizpůsobeného produktu](../../retail/personalized-product-recommendations.md).  

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Aktuální verzi služby doporučení produktu odstraňujeme, protože předěláváme tuto funkci s lepším algoritmem a novějšími funkčnostmi orientovanými na maloobchod.  |
| **Nahrazeno jinou funkcí?**   | Č. Nicméně po jaru 2018 plánujeme vrátit tuto funkci, abychom využili novou službu doporučení.   |
| **Ovlivněné oblasti produktu**         | Doporučení přizpůsobeného produktu v POS.                                                    |
| **Možnost nasazení**              | Všechna                                                                                      |
| **Stav**                         |Odstraněno od 15. února 2018. To má vliv na zákazníky s verzí Dynamics 365 for Operations 1611 a vyšší.  |

### <a name="extension-of-the-list-of-electronic-reporting-er-functions"></a>Rozšíření seznamu funkcí elektronického vykazování
Možnost zavést vlastní funkce pro použití v tvůrci výrazů ER (další informace naleznete v tématu [Rozšíření seznamu funkcí elektronického výkaznictví](../../dev-itpro/analytics/general-electronic-reporting-formulas-list-extension.md)) již není nadále podporována. Z důvodu změn rozhraní API pro elektronické výkaznictví se stalo API volající vestavěné funkce z tvůrce výkazů ER interním a již nelze rozšířit.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Iniciativa uzavření kódu  |
| **Nahrazeno jinou funkcí?**   | Žádný. Kdykoliv je potřeba nová vestavěná funkce, musí být adresován nová požadavek na rozšíření týmu architektury elektronického výkaznictví.<br><br>Jako dočasné řešení pro dobu, kdy je požadovaná funkce vyvíjena týmem elektronického výkaznictví, lze požadovanou logiku naprogramovat jako metodu vlastní třídy aplikace. K této metodě lze získat přístup ve výrazu elektronické výkaznictví jako vlastnost přidaného datového zdroje dat elektronické výkaznictví typu **Aplikace\Třída**, který se vztahuje k této vlastní třídě aplikace.  |
| **Ovlivněné oblasti produktu**         | Architektura elektronického výkaznictví                                                      |
| **Možnost nasazení**              | Vše                                                                                      |
| **Stav**                         | Odebráno od verze Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.    |

### <a name="inventory-by-item-group-and-inventory-by-inventory-dimension-aging-reports"></a>Zásoby podle prodlení skupiny zboží a Zásoby podle doby uskladnění za dimenzi zásob

Tyto dvě sestavy již nejsou podporovány v aplikaci Finance and Operations. Namísto toho lze použít sestavu **Prodlení zásob** k vylepšení uživatelské zkušenosti.

|   |  |
|--------------|-----------------------|
| **Důvod pro zrušení**       | Duplicitní funkce  |
| **Nahrazeno jinou funkcí?** | Ano. Tyto dvě sestavy byly nahrazeny sestavou **Prodlení zásob**.     |
| **Ovlivněné oblasti produktu**       | Řízení zásob, řízení nákladů        |
| **Možnost nasazení**        | Všechna|
| **Stav**                       | Zastaralé: Položky nabídky pro tyto dvě sestavy byly odstraněny ve verzi 7.3. Kód pro sestavy však zůstane v produktu. V plánu je kód odstranit v budoucích verzích. |

### <a name="power-bi-content-packs-available-on-appsource"></a>Balíčky obsahu Power BI dostupné v AppSource
Balíčky obsahu **Řízení nákladů**, **Finanční výkonnost** a **Výkonnost maloobchodního kanálu**, dostupné na webu [Microsoft AppSource](https://appsource.microsoft.com), jsou zastaralé v důsledku aktualizace produktů v Microsoft Power BI. Formuláře správy systému používané k nasazení těchto balíčků obsahu do PowerBI.com obsahu jsou také zastaralé v aplikaci Finance and Operations.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Aktualizace produktu v Microsoft Power BI. |
| **Nahrazeno jinou funkcí?**   | Balíčky obsahu **Řízení nákladů**, **Finanční výkonnost** a **Výkonnost maloobchodního kanálu**, které jsou k dispozici na webu [AppSource](https://appsource.microsoft.com), jsou nahrazeny analytickými aplikacemi umožňujícími integrace řešení na úrovni databáze. Další informace o analytických aplikacích naleznete v tématu [Power BI Embedded v pracovních prostorech](../../dev-itpro/analytics/embed-power-bi-workspaces.md).    |
| **Ovlivněné oblasti produktu**         | Řízení nákladů, Finance a Maloobchod                                                                                               |
| **Možnost nasazení**              | Pouze cloud (Inntegrace s PowerBI.com není podporována v místních nasazeních).                                                                                                            |
| **Stav**                         | Zastaralé: Plánovaná doba pro odstranění funkcionality je druhé čtvrtletí roku 2018.    |

### <a name="standard-ui-in-data-management-workspace"></a>Standardní uživatelské rozhraní v pracovním prostoru správy dat

Standardní uživatelské rozhraní ve správě dat je starší verze rozhraní, což je výchozí uživatelské rozhraní zobrazované uživatelům při návštěvě pracovního prostoru Správa dat.

|   |  |
|------------------|-------------------------|
| **Důvod pro zrušení/odstranění** | Investujeme do poskytnutí nových uživatelských možností v novém uživatelském rozhraní.             |
| **Nahrazeno jinou funkcí?**   | Nové uživatelské rozhraní s názvem *Rozšířené zobrazení* nahrazuje staré uživatelské rozhraní.            |
| **Ovlivněné oblasti produktu**         | Pracovní prostor správy dat                                                     |
| **Možnost nasazení**              | Všechna                                                                           |
| **Stav**                         | Zastaralé: Plánovaná doba pro odstranění funkcionality je první čtvrtletí roku 2018. |

### <a name="excise-sales-tax-service-tax-for-india"></a>Spotřební daň, DPH, daň ze služeb pro Indii

Tyto daně byly zahrnuty do indické GST.

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Důvod pro zrušení nebo odstranění**       | Tyto daně byly zahrnuty do indické GST.                          |
| **Nahrazeno jinou funkcí?**            | Indická GST                                                              |
| **Ovlivněné oblasti produktu**                  | Daň                                                                     |
| **Možnost nasazení**                       | Všechny moduly                                                   |
| **Stav**                                  | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno. |    

### <a name="file-validation-utility-fvu-for-india"></a>Nástroj ověření souboru (FVU) pro Indii

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Důvod pro zrušení nebo odstranění**       | Nepoužíváno odběrateli.                                                  |
| **Nahrazeno jinou funkcí?**            | Žádný                                                                      |
| **Ovlivněné oblasti produktu**                  | Srážková daň pro Indii                                                  |
| **Možnost nasazení**                       | Všechny moduly                                                                    |
| **Stav**                                  | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno.   |        

### <a name="tdstcs-certificate-for-india"></a>Certifikát TDS/STK pro Indii

Uživatelé si mohou stáhnout tento formulář ze státního portálu.

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Důvod pro zrušení nebo odstranění**       | Nepoužíváno odběrateli.                                                  |
| **Nahrazeno jinou funkcí?**            | Žádný                                                                      |
| **Ovlivněné oblasti produktu**                  | Srážková daň pro Indii                                                  |
| **Možnost nasazení**                       | Všechny moduly                                                                   |
| **Stav**                                  | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno.     |    

### <a name="exportimport-exim-incentive-scheme-for-india"></a>Export/import (EXIM) motivační schématu pro Indii


|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Důvod pro zrušení nebo odstranění**       | Nepoužíváno odběrateli.                                                  |
| **Nahrazeno jinou funkcí?**            | Žádný                                                                      |
| **Ovlivněné oblasti produktu**                  | Import a export                                                       |
| **Možnost nasazení**                       | Všechny moduly                                                                    |
| **Stav**                                  | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno.  |    


## <a name="dynamics-365-for-retail-72"></a>Dynamics 365 for Retail 7.2

### <a name="personalized-product-recommendations"></a>Doporučení přizpůsobeného produktu 
Od 15. února 2018 již nebudou maloobchodní prodejci schopní zobrazit doporučení přizpůsobeného produktu na zařízení POS. Další informace naleznete v tématu [Doporučení přizpůsobeného produktu](../../retail/personalized-product-recommendations.md).  

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Aktuální verzi služby doporučení produktu odstraňujeme, protože předěláváme tuto funkci s lepším algoritmem a novějšími funkčnostmi orientovanými na maloobchod.  |
| **Nahrazeno jinou funkcí?**   | Č. Nicméně po jaru 2018 plánujeme vrátit tuto funkci, abychom využili novou službu doporučení.   |
| **Ovlivněné oblasti produktu**         | Doporučení přizpůsobeného produktu v POS.                                                    |
| **Možnost nasazení**              | Všechna                                                                                      |
| **Stav**                         |Odstraněno od 15. února 2018. To má vliv na zákazníky s verzí Dynamics 365 for Retail 7.2 a vyšší. |


## <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-with-platform-update-8"></a>Dynamics 365 for Finance and Operations, Enterprise Edition červenec 2017 s aktualizací Platform Update 8

### <a name="currency-conversion-for-accounting-and-reporting-currencies"></a>Převod měny pro účetnictví a měny vykazování

Převod měny pro účetnictví a měny vykazování byl zaveden se zavedením eura.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Omezené použití a přidání funkce kopírování právnické osoby jako náhrady.      |
| **Nahrazeno jinou funkcí?**   | Ne, ale byly přidány funkce Kopírovat právnickou osobu a Konfigurace, aby se usnadnilo přesunutí společnosti, která má zásadní požadavky na změnu. |
| **Ovlivněné oblasti produktu**         | Správa financí     |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno.   |


### <a name="warehouse-mobile-devices-portal"></a>Portál skladu pro mobilní zařízení

Portál skladu pro mobilní zařízení (WMDP) byla samostatná komponenta, určená pro místní vlastní nasazení. Tato komponenta již není podporována v aplikaci Finance and Operations. Funkce portálu skladu pro mobilní zařízení byla nahrazena nativní aplikací, která vylepšuje uživatelské prostředí.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Duplicitní funkce.       |
| **Nahrazeno jinou funkcí?**   | Ano. Tato funkce byla nahrazena aplikací Finance and Operations - Warehousing. Další informace o nastavení a předpokladech naleznete v tématu [Instalace a konfigurace Microsoft Dynamics 365 for Finance and Operations – Sklady](../../supply-chain/warehousing/install-configure-warehousing-app.md). |
| **Ovlivněné oblasti produktu**         | Řízení skladu, Správa přepravy     |
| **Možnost nasazení**              | Portál skladu pro mobilní zařízení (WMDP) byla samostatná komponenta, určená pro místní vlastní nasazení.               |
| **Stav**                         | Zastaralé: Plánovaná doba pro odstranění funkcionality je čtvrté čtvrtletí roku 2019.   |

### <a name="advanced-bank-reconciliation-matching-rule-for-manual-matching"></a>Pravidlo párování rozšířeného odsouhlasení banky pro ruční párování

Bylo použito pravidlo párování k výběru a označení bankovního dokumentu při manuálním párování dokumentů v listu pro odsouhlasení.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Omezené použití.                                                                         |
| **Nahrazeno jinou funkcí?**   | Č. Pro nalezení dokumentů k odsouhlasení je třeba použít možnosti filtrování sloupce. |
| **Ovlivněné oblasti produktu**         | Pokladna a banka                                                               |
| **Možnost nasazení**              | Vše                                                                                    |
| **Stav**                         | Odstraněno od července 2017.                                                               |

## <a name="dynamics-365-for-operations-1611-with-platform-update-3"></a>Dynamics 365 for Operations 1611 s aktualizací Platform Update 3

### <a name="aeb-payment-formats-for-spain"></a>AEB formáty plateb pro Španělsko

Pro odesílání souborů úhrad s platbami odběratelů a dodavatelů do banky se používaly formáty CSB (Consejo Superior Bancario). Obsah těchto formátů byl stanoven asociací AEB (Asociación Española de Banca). Zahrnuty jsou také Cuaderno 19, 32, 58, 34.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Formáty plateb se již nepoužívají.                                  |
| **Nahrazeno jinou funkcí?**   | Ano, ISO20022 formáty bezhotovostních převodů a přímých debetních plateb pro Španělsko |
| **Ovlivněné oblasti produktu**         | Pohledávky, závazky                                    |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno.           |

### <a name="bank-payments-transfer-for-lithuania"></a>Bankovní převod plateb pro Litvu

Bankovní platební převody byly generované a tisknuté za použití formátu exportu platebního převodu pro Litvu (LT). Litevský trh začal v roce 2005 používat LITAS, sjednocený elektronický bankovní systém.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Formáty plateb se již nepoužívají.                        |
| **Nahrazeno jinou funkcí?**   | Ano, Litevský formát platby peněžního převodu ISO20022.     |
| **Ovlivněné oblasti produktu**         | Závazky                                               |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno. |

### <a name="bbs-direkte-remittering-payment-formats-for-norway"></a>Formáty plateb BBS Direkte Remittering pro Norsko

Formáty plateb BBS Direkte Remittering zahrnují export inkasní platby odběratele (inkaso) a import zprávy o vrácení.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Formáty plateb se již nepoužívají.  |
| **Nahrazeno jinou funkcí?**   | Formát platby odběratele AvtaleGiro pro Norsko lze využít ke generování zprávy o souhlasu s inkasem. Import zprávy o vrácení bude zahrnut do příštích verzí. |
| **Ovlivněné oblasti produktu**         | Pohledávky, závazky   |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno.                                                                                                 |

### <a name="chart-of-accounts-tool-for-spain"></a>Nástroj účtové osnovy pro Španělsko

Tento nástroj se používá, když účtová osnova ve Španělsku vyžaduje zásadní změny. Uživatelé mohou importovat nové účtové osnovy v aplikaci Microsoft Excel nebo v textovém formátu a mohou také importovat finanční výkazy.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Omezené použití                                                  |
| **Nahrazeno jinou funkcí?**   | Žádný                                                             |
| **Ovlivněné oblasti produktu**         | Hlavní kniha                                                 |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno. |

### <a name="dom80-payment-format-for-belgium"></a>Dom80 formát platby pro Belgii

Starý belgický formát platby pro inkaso platby (přímý debet).

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Formát plateb se již nepoužívá.                          |
| **Nahrazeno jinou funkcí?**   | Ano, specificky belgický formát inkasní platby ISO 20022.         |
| **Ovlivněné oblasti produktu**         | Pohledávky                                            |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno. |

### <a name="dtaezag-payment-formats-for-switzerland"></a>DTA/EZAG formáty plateb pro Švýcarsko

Formáty odložených daňových aktiv/EZAG jsou integrovány do systému ESR, jelikož mohou obsahovat referenční číslo. Jelikož referenční číslo není povinné, mohou být pomocí těchto formátů zpracovány všechny platby dodavatele. Tyto formáty využívají společnosti, které máte bankovní účet ve skladovém místě jiném než "Postfinance".

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Formáty plateb se již nepoužívají.                        |
| **Nahrazeno jinou funkcí?**   | Ano, švýcarský formát platby peněžního převodu ISO20022   |
| **Ovlivněné oblasti produktu**         | Závazky                                               |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno. |

### <a name="edifact-dirdeb-payment-format-for-austria"></a>Specificky rakouský formát inkasní platby EDIFACT-DIRDEB.

EDIFACT-DIRDEB formát platby pro inkaso platby (přímý debet).

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Formát plateb se již nepoužívá.                          |
| **Nahrazeno jinou funkcí?**   | Ano, specificky rakouský formát inkasní platby ISO 20022.         |
| **Ovlivněné oblasti produktu**         | Pohledávky                                            |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno. |

### <a name="edivat-for-belgium"></a>EDIVAT pro Belgii

EDIVAT je starý standard pro elektronické prohlášení prostřednictvím zabezpečení pošty v Belgii. Microsoft Dynamics AX 2012 zachovává řešení jen pro čtení pro umožnění přístupu k historickým datům.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Tato funkce se již nepoužívá.                           |
| **Nahrazeno jinou funkcí?**   | Žádný                                                             |
| **Ovlivněné oblasti produktu**         | Hlavní kniha                                                 |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno. |

### <a name="egiro-edifact-cremul-payment-import-format-for-norway"></a>Importní formát platby eGiro EDIFACT CREMUL pro Norsko

eGiro je založeno na mezinárodních standardech SN EDIFACT CREMUL (Multiple Credit Advice Message), které slouží pro automatické zaúčtování plateb odběratele. V aplikaci Microsoft Dynamics AX je implementováno eGiro jako formát importu platby odběratele.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Formát plateb se již nepoužívá.                                                     |
| **Nahrazeno jinou funkcí?**   | Č. Formát bude nahrazen formátem importu výpisu ISO 20022 v příštích verzích. |
| **Ovlivněné oblasti produktu**         | Pohledávky                                                                       |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno.                            |

### <a name="external-inventory-for-poland"></a>Externí zásoby v Polsku

Doklad o zboží, který je přijatý od dodavatele pro účely prodeje bez nákupu. Zboží, které je zpracováno v externím skladu, nemá vliv na standardní zásoby a lze ho prodat a pak zakoupit automaticky. Tento proces vytváří skutečné pohyby zásob.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Nahrazeno jinou funkcí                                    |
| **Nahrazeno jinou funkcí?**   | Ano, základní funkce příchozí zásilky                |
| **Ovlivněné oblasti produktu**         | Závazky, řízení zásob                         |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno. |

### <a name="financial-reports-generator-for-eastern-europe"></a>Generátor finančních sestav pro východní Evropu

Nástroj se používá pro nastavení shromažďování dat pro účetnictví a daňové sestavy a export dat do šablon sestavy XLS a DOC

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Omezené použití                                                                            |
| **Nahrazeno jinou funkcí?**   | Č. Tento nástroj bude nahrazen konfigurací elektronických sestav v budoucích verzích. |
| **Ovlivněné oblasti produktu**         | Hlavní kniha                                                                           |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno.                           |

### <a name="import-of-customer-payment-transactions-for-finland"></a>Import transakce plateb odběratelů pro Finsko

Můžete vybrat formát importu pro platby ve Finsku, ve kterém se importují platební transakce odběratelů z externího souboru, který zajišťuje banka.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Formát plateb se již nepoužívá.                                                     |
| **Nahrazeno jinou funkcí?**   | Č. Formát bude nahrazen formátem importu výpisu ISO 20022 v příštích verzích. |
| **Ovlivněné oblasti produktu**         | Pohledávky                                                                       |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno.                            |

### <a name="import-of-payment-transactions-into-a-general-ledger-journal-for-finland"></a>Import platebních transakcí do deníku hlavní knihy pro Finsko

Formát, který je specifický pro Finsko, se používá k importu transakcí účtování do hlavní knihy.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Formát plateb se již nepoužívá.                                                     |
| **Nahrazeno jinou funkcí?**   | Č. Formát bude nahrazen formátem importu výpisu ISO 20022 v příštích verzích. |
| **Ovlivněné oblasti produktu**         | Pohledávky                                                                       |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno.                            |

### <a name="integration-with-isabel-synchronized-cis-for-belgium"></a>Integrace s Isabel synchronizována (CIS) pro Belgii

Isabel je platforma pro elektronické bankovnictví v Evropě a je de facto standardní v Belgii.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Integrace s klientem Isabel již není nabízena.   |
| **Nahrazeno jinou funkcí?**   | Ne. Formáty plateb, které se již nepoužívají, jsou nahrazeny ISO20022 formátem platebního převod platby pro Belgii. |
| **Ovlivněné oblasti produktu**         | Závazky     |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno.    |

### <a name="modifications-in-the-chart-of-accounts-and-accounting-rules-for-spain"></a>Změny v účetní osnově a účetních pravidlech pro Španělsko

Tato funkce se používá pro změny v účtové osnově a účetních pravidlech ve Španělsku. Mapuje účty, aby pomohla transformovat původní účtovou osnovu do nové účtové osnovy a porovnává předchozí fiskální rok s novým fiskálním rokem i v případě, že byly zaúčtovány na různá čísla účtů.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Omezené použití                                                  |
| **Nahrazeno jinou funkcí?**   | Žádný                                                             |
| **Ovlivněné oblasti produktu**         | Hlavní kniha                                                 |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno. |

### <a name="pagamento-fornittori-vendor-payment-format"></a>Formát platby dodavatele Pagamento Fornittori

Starý italský formát platby peněžních převodů.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Formát plateb se již nepoužívá.                          |
| **Nahrazeno jinou funkcí?**   | Ano, italský formát platby peněžního převodu ISO20022.         |
| **Ovlivněné oblasti produktu**         | Závazky                                               |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno. |

### <a name="payment-export-formats-for-estonia"></a>Formáty pro export plateb v Estonsku

Formáty Telehansa a Teleservice se používají pro export bankovních plateb.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Formáty plateb se již nepoužívají.                        |
| **Nahrazeno jinou funkcí?**   | Ano, specificky estonský formát platby peněžního převodu ISO20022.       |
| **Ovlivněné oblasti produktu**         | Závazky                                               |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno. |

### <a name="payment-file-archive-for-norway"></a>Archiv souborů plateb pro Norsko

Když dojde ke generování souborů plateb, archiv souborů automaticky archivuje všechny soubory, které jsou vytvořeny, i soubory, které byly dříve zapsány nebo načteny.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Nahrazeno jinou funkcí                                        |
| **Nahrazeno jinou funkcí?**   | Ano, archivované úlohy elektronického výkaznictví                            |
| **Ovlivněné oblasti produktu**         | Závazky, pohledávky, správa organizace |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno.     |

### <a name="payment-import-formats-for-estonia"></a>Formáty pro import plateb v Estonsku

Formáty Telehansa a TeleTeenus se používají pro import bankovních plateb.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Formáty plateb se již nepoužívají.                                                    |
| **Nahrazeno jinou funkcí?**   | Č. Formáty budou nahrazeny formátem importu výpisu ISO 20022 v příštích verzích. |
| **Ovlivněné oblasti produktu**         | Pohledávky                                                                        |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno.                             |

### <a name="payroll-information-in-human-resources"></a>Mzdové informace v modulu Lidské zdroje

Mzdové informace lidských zdrojů

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Tato funkce byla nahrazena základními stránkami Mzdy a Lidské zdroje.  |
| **Nahrazeno jinou funkcí?**   | **Výhody**, **Příjmy** a další související stránky, které byly dříve v modulu Mzdy v USA, byly překonfigurovány a jsou nyní součásti základní konfigurace modulu Lidské zdroje pro podporu zpracování externích mezd. K této funkci se dostanete pomocí konfiguračního klíče **Lidské zdroje 1** \> **Mzdy**. |
| **Ovlivněné oblasti produktu**         | Lidské zdroje, Mzdy   |
| **Stav**                         | Odstraněno od verze Dynamics 365 for Operations 1611.    |

### <a name="performance-management-goal-workflow"></a>Pracovní postup cíle řízení výkonnosti

Řízení výkonnosti zahrnuje správu cílů a integraci s hodnocením výkonu.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Řízení výkonnosti bylo změněno a počet stránek cílů se snížil, aby došlo ke zjednodušení procesu.                 |
| **Nahrazeno jinou funkcí?**   | Ne. Cíle jsou viditelné pro vedoucí pracovníky pomocí portálu samoobslužných stránek správce a lze je změnit a zobrazit manažerem. |
| **Ovlivněné oblasti produktu**         | Správa lidského kapitálu       |
| **Stav**                         | Odstraněno od verze Dynamics 365 for Operations 1611.    |

### <a name="postgirot-and-postgirot-utland-payment-formats-for-sweden"></a>Formáty platby Postgirot a Postgirot Utland pro Švédsko

Formáty platby Postgirot a Postgirot Utland pro Švédsko.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Formáty plateb se již nepoužívají.                        |
| **Nahrazeno jinou funkcí?**   | Ano, specificky švédský formát platby peněžního převodu ISO20022.        |
| **Ovlivněné oblasti produktu**         | Závazky                                               |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno. |

### <a name="radio-frequency-identifier"></a>Radiofrekvenční identifikátor

Radiofrekvenční identifikace (RFID) představuje technologii shromažďování dat, která využívá elektronických značek k uložení identifikačních dat a nevyžaduje žádné zařízení ke čtení identifikačních dat, které by muselo být v přímé viditelnosti k označenému předmětu.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Málo používáno odběrateli a omezená sada funkcí.   |
| **Nahrazeno jinou funkcí?**   | Žádný                                              |
| **Ovlivněné oblasti produktu**         | Řízení zásob                            |
| **Stav**                         | Odstraněno od verze Dynamics 365 for Operations 1611. |

### <a name="report-about-state-invoices-numbering-for-latvia"></a>Zpráva o číslování státních faktur Lotyšska

Lotyšská legislativa poskytuje konkrétní pravidla týkající se číslování prodejních faktur. Funkce umožňuje přiřadit specifická čísla do prodejních faktur na základě uživatele nebo skupiny uživatelů. Pak lze vygenerovat sestavu nebo soubor XML. Lze také vytisknout sestavy s informacemi o použitých číslech faktur.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Není už nutné zachovávat číslování státních faktur. Hlášení o použitých číslech faktur již není požadováno. |
| **Nahrazeno jinou funkcí?**   | Žádný       |
| **Ovlivněné oblasti produktu**         | Pohledávky    |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno.  |

### <a name="set-up-the-names-of-the-manager-and-general-accountant-of-a-company-for-lithuania"></a>Nastavení jmen správce a hlavního účetního společnosti pro Litvu

Jména správce a hlavního účetního společnosti mohou být určena v informacích o společnosti a využita ve výtiscích různých místních sestav.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Nahrazeno jinou funkcí                                     |
| **Nahrazeno jinou funkcí?**   | Ano, nastavení úředních osob lze použít k tomuto účelu.   |
| **Ovlivněné oblasti produktu**         | Závazky, Pohledávky, Řízení zásob, Pokladna a banka |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno.  |

### <a name="shipping-carrier-interface"></a>Rozhraní dopravce

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Duplicitní funkce   |
| **Nahrazeno jinou funkcí?**   | Částečně nahrazeno správou přepravy |
| **Ovlivněné oblasti produktu**         | Prodeje a marketing, Řízení zásob  |
| **Stav**                         | Odstraněno od verze Dynamics 365 for Operations 1611.  |

### <a name="telepay-payment-formats-for-norway"></a>Telepay formáty plateb pro Norsko

Telepay formáty plateb zahrnují exporty plateb dodavatele (převod) a inkasa plateb odběratele (přímý debet).

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Formáty plateb se již nepoužívají.                                                        |
| **Nahrazeno jinou funkcí?**   | Ano, formátu platby platebního převodu ISO20022 a formát platby odběratele AvtaleGiro pro Norsko |
| **Ovlivněné oblasti produktu**         | Pohledávky, závazky                                                          |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno.                                 |

### <a name="vendor-payment-export-formats-for-finland"></a>Formáty exportu plateb dodavatele pro Finsko

Existují dva formáty pro export plateb pro Finsko. LM02 (FI) se používá pro domácí platby a LUM2 (FI) se používá pro zahraniční platby.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Formáty plateb se již nepoužívají.                        |
| **Nahrazeno jinou funkcí?**   | Ano, finský formát platby peněžního převodu ISO20022       |
| **Ovlivněné oblasti produktu**         | Závazky                                               |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno. |

### <a name="warehouse-management-ii"></a>Řízení skladu II

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Řešení Řízení skladu II (WMS II), které bylo k dispozici v modulu **Řízení zásob**, duplikuje funkce, které jsou v modulu **Řízení skladu** a byly vydány v aplikaci Microsoft Dynamics AX 2012 R3.                                                                         |
| **Nahrazeno jinou funkcí?**   | Modul **Řízení skladu**, který byl vydán v aplikaci AX 2012 R3, Microsoft Dynamics AX 2012 R3 CU8 a Dynamics AX 2012 R3 CU9, nahrazuje funkce modulu Řízení skladu II. V porovnání s funkcemi modulu Řízení skladu II má nový modul více rozšířené funkce a flexibilnější procesy řízení skladu. |
| **Ovlivněné oblasti produktu**         | Řízení zásob, prodeje a marketing, zásobování a zdroje   |
| **Stav**                         | Odstraněno od verze Dynamics 365 for Operations 1611.    |

### <a name="worker-reminders-in-human-resources"></a>Připomenutí pracovníka v modulu Lidské zdroje

Mzdové informace lidských zdrojů

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Malé využití                                                           |
| **Nahrazeno jinou funkcí?**   | Žádný                                                                  |
| **Ovlivněné oblasti produktu**         | Lidské zdroje                                                     |
| **Stav**                         | Odstraněno od verze Dynamics 365 for Operations 1611 |

### <a name="workflow-for-creating-goals"></a>Postup pro vytváření cíle

Workflow správy vytvoření cílů zaměstnanců je jednou z několika workflowů, které byly k dispozici pro pomoc koordinovat proces řízení výkonnosti.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Řízení výkonnosti bylo zcela přepracováno v aplikaci Microsoft Dynamics 365 for Finance and Operations.     |
| **Nahrazeno jinou funkcí?**   | Upravená funkce řízení výkonnosti poskytuje větší kontrolu nad obsahem cílů, měřeními, která se používají ke sledování vývoje, a připojováním podpůrné dokumentace. Cíle lze ukládat jako šablony a pak znovu použít. Tato funkce vám pomůže rychleji nastavit další cíle pro zaměstnance. |
| **Ovlivněné oblasti produktu**         | Správa lidského kapitálu                 |
| **Stav**                         | Odstraněno od verze Dynamics 365 for Operations 1611. |

## <a name="dynamics-ax-70"></a>Dynamics AX 7.0 


### <a name="ability-to-cancel-changes-to-a-vendor-invoice"></a>Možnost zrušení změn na faktuře dodavatele

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Zvýšení výkonnosti        |
| **Nahrazeno jinou funkcí?**   | Žádný                             |
| **Ovlivněné oblasti produktu**         | Závazky               |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0. |

### <a name="aif-axd-and-axbc-integrations"></a>Integrace rozhraní AIF, AxD a AxBC

V rozhraní AIF (Application Integration Framework) mohou být data vyměňována s externími systémy pomocí obchodní logiky, která je zveřejněna jako služba. Dynamics AX obsahuje služby, které jsou založeny na dokumentech a programu .NET Business Connector (AxBC). Dokument je vytvářen pomocí kódu XML. Soubor XML obsahuje informace v záhlaví, jež jsou přidány pro vytvoření *zprávy*, kterou lze přenést do a z aplikace Dynamics AX. Příkladem takovýchto dokumentů mohou být prodejní objednávky nebo nákupní objednávky. Dokumentem však může být reprezentována téměř jakákoliv entita, například odběratel. Služby, které jsou založeny na dokumentech, používají třídy **Axd \<Dokument\>**.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Architekturu rozhraní AIF a AxDs nelze škálovat do cloudové služby. Při hromadném importu docházelo k problémům s výkonem.                                        |
| **Nahrazeno jinou funkcí?**   | Tato funkce je nahrazena architekturou pro import a export dat, která podporuje opakovaný hromadný import/export. U rozhraní AxBC doporučujeme používat skutečné tabulky. |
| **Ovlivněné oblasti produktu**         | AxDs, AxBCs a AIF   |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0.   |

### <a name="billing-code-rate-scripts"></a>Skripty sazby účtovacího kódu

Účtovací skripty se používaly k výpočtu sazeb fakturace pro kódy fakturace. To skripty vyžadovaly vlastní vývoj v programovacím jazyce C Sharp nebo Visual Basic. V aktuální verzi aplikace Dynamics AX nejsou **kódy skriptu fakturační sazby** podporovány.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Podpora vlastních skriptů v jazyce C Sharp nebo Visual Basic snebyla v Dynamics AX 7.0 přidána. |
| **Nahrazeno jinou funkcí?**   | Ne                                                                                      |
| **Ovlivněné oblasti produktu**         | Veřejný sektor (pohledávky)                                    |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0.                                                          |

### <a name="boms-without-bom-versions"></a>Kusovníky bez verze kusovníku

Pokud byl konfigurační klíč **Verze kusovníku** zakázán, byly ve všech formulářích skryty verze kusovníku a systém vynutil vztahy 1:1 mezi uvolněnými produkty a kusovníky. V aktuální verzi aplikace Dynamics AX nelze konfigurační klíč **Verze kusovníku** zakázat.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Řízení verzí kusovníku pomocí konfiguračního klíče nelze škálovat v cloudovém prostředí. |
| **Nahrazeno jinou funkcí?**   | Žádný                                                                                      |
| **Ovlivněné oblasti produktu**         | Řízení informací o produktech, Řízení zásob                                    |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0.                                                          |

### <a name="brazilian-bordero"></a>Brazilský doklad Bordero

Specifická metoda platby pro brazilské společnosti

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Podpora pro brazilskou metodu platby Bordero již není k dispozici v brazilské lokalizaci |
| **Nahrazeno jinou funkcí?**   | Žádný   |
| **Ovlivněné oblasti produktu**         | Závazky   |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno. |

### <a name="brazilian-sintegra-statement"></a>Brazilský výpis Sintegra

Federální daňový výkaz ICMS

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Toto prohlášení se již v některých brazilských státech nepoužívá. |
| **Nahrazeno jinou funkcí?**   | Ne. Uživatelé mohou používat nástroj obecného elektronického vykazování pro konfiguraci výkazu, pokud je v určitých situacích požadován. |
| **Ovlivněné oblasti produktu**         | Fiskální knihy    |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno.   |

### <a name="brazilian-scan-contingency-mode-for-nf-e"></a>Brazilský pohotovostní režim SCAN pro NF e

Pohotovostní prostředí (SCAN) slouží k vygenerování, exportování a importování stavu Nota Fiscal eletrônica (NF-e), pokud není k dispozici prostředí Secretaría da Fazenda (SEFAZ).

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Tato záložní metoda už nebude k dispozici v žádném brazilském státě |
| **Nahrazeno jinou funkcí?**   | Žádný                                                                          |
| **Ovlivněné oblasti produktu**         | Pohledávky                                                         |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno.              |

### <a name="business-analyzer"></a>Obchodní analýza

S touto mobilní aplikací mohou uživatelé kontrolovat klíčoví obchodní metriky.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Tato funkce byla nahrazena jinou funkcí.   |
| **Nahrazeno jinou funkcí?**   | Balíček obsahu Sledování finanční výkonnosti pro Microsoft Power BI bude zahrnovat klíčové finanční metriky, které byly dříve dostupné v aplikaci Business Analyzer. |
| **Ovlivněné oblasti produktu**         | Hlavní kniha      |
| **Stav**                         | Zastaralé: Použití aplikace Business Analyzer je zastaralé.    |

### <a name="business-statistics"></a>Obchodní statistika

Nastavení dotazů na obchodní statistiky, která vám mohou pomoct s analýzou výkonnosti organizace

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Starší přístup k obchodnímu zpravodajství (BI), málo používáno odběrateli a omezená sada funkcí |
| **Nahrazeno jinou funkcí?**   | Nové řešení Power BI pro aktuální verzi aplikace Dynamics AX                                      |
| **Ovlivněné oblasti produktu**         | Zásobování a zdroje, Závazky, Prodej a marketing, Pohledávky         |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0.                                                               |

### <a name="change-document-date-function-in-invoice-approval-journal"></a>Funkce změny data dokumentu v modulu Deník schválených faktur

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Malé využití                                                               |
| **Nahrazeno jinou funkcí?**   | Ano. Datum dokumentu na zaúčtované transakci dodavatele lze změnit. |
| **Ovlivněné oblasti produktu**         | Závazky                                                        |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0.                                          |

### <a name="clieop03-payment-format-for-the-netherlands"></a>Formát platby ClieOp03 pro Nizozemsko

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Formát se již v Nizozemsku nepoužívá, protože byl nahrazen funkcí Jednotná oblast pro platby v eurech (SEPA). |
| **Nahrazeno jinou funkcí?**   | Export plateb SEPA  |
| **Ovlivněné oblasti produktu**         | Všechny moduly     |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno.   |

### <a name="compliance-center"></a>Centrum kompatibility

Centrum kompatibility byly stránky podnikového portálu pro správu požadavků na dokumentaci pro iniciativy kompatibility související se Sarbanes-Oxleyho zákonem.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Nepoužíváno odběrateli. Služba Microsoft SharePoint zahrnuje stejné možnosti, jaké byly k dispozici v centru kompatibility. |
| **Nahrazeno jinou funkcí?**   | Žádný   |
| **Ovlivněné oblasti produktu**         | Dodržování předpisů a vnitřní kontroly  |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0.    |

### <a name="connector-for-microsoft-dynamics"></a>Connector pro aplikaci Microsoft Dynamics

Tento nástroj byl použit k integraci klíčových dat z aplikace Microsoft Dynamics CRM do aplikace Microsoft Dynamics ERP.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Tato funkce byla nahrazena jinou funkcí. |
| **Nahrazeno jinou funkcí?**   | CDS (Common Data Service)                                      |
| **Ovlivněné oblasti produktu**         | Connector pro aplikaci Microsoft Dynamics                         |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0.                           |

### <a name="container-unit-and-multi-dimension-on-hand"></a>Jednotka kontejneru a více dimenzí zásob

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Duplicitní funkce |
| **Nahrazeno jinou funkcí?**   | Ano. Tuto funkce byla nahrazena od verze AX 2012 sadou funkcí konsolidované dávkové objednávky. Tato sada funkcí zahrnuje konsolidované zobrazení zásob na skladě. |
| **Ovlivněné oblasti produktu**         | Řízení informací o produktech, Řízení výroby, Řízení zásob, Prodej a marketing  |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0. |

### <a name="cue-group-metadata"></a>Metadata skupiny hromádek

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Skupiny hromádek byly použity k zobrazení jedné nebo více hromádek v oblasti okna s fakty. Byl omezený příjem a došlo k také k potížím s výkonem kvůli změně záznamu v nadřazeném formuláři, což způsobilo jeden dotaz na každou hromádku ve skupině hromádek. |
| **Nahrazeno jinou funkcí?**   | Žádný      |
| **Ovlivněné oblasti produktu**         | Všechny moduly    |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0.  |

### <a name="cue-metadata"></a>Metadata hromádky

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Metadata hromádky byla omezena na informace o počtu nebo součtu.    |
| **Nahrazeno jinou funkcí?**   | Kvůli flexibilnějším možnostem modelování byla zavedena metadata dlaždice. Modelova můžete například aktuální počty, navigaci a klíčové indikátory výkonnosti (KPI). Metadata dlaždice počtu jsou přímou náhradou za metadata hromádky. |
| **Ovlivněné oblasti produktu**         | Všechny moduly           |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0      |

### <a name="danish-check-format"></a>Formát šeku – Dánsko

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Byla zrušena podpora pro rozvržení dánského formátu šeku a sestava byla odebrána z dánské lokalizace. |
| **Nahrazeno jinou funkcí?**   | Žádný    |
| **Ovlivněné oblasti produktu**         | Všechny moduly    |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno.  |

### <a name="data-partitions"></a>Datové oddíly

Datové oddíly poskytují logické oddělení dat v databázi aplikace Microsoft Dynamics AX.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Datové oddíly byly zavedeny v aplikaci Microsoft Dynamics AX 2012 R2 a umožňují izolaci dat. V běžné situaci má společnost pobočky a data z jedné dceřiné společnosti by neměla být viditelná pro jiné dceřiné společnosti, přestože obě pobočky jsou spravovány ve stejném oddělení IT. Nicméně by byly vyžadovány dodatečné skripty a další správní režie v celém programu pro vytvoření nových oddílů, naplnění je daty a zálohování data oddílu. V cloudu, kde máte přístup k databázové službě Platforma jako služba (PaaS) (Microsoft Azure SQL Database), je mnohem efektivnější použít databázi pro izolační kontejner, než provádět izolaci v programu. Bez ohledu na to, zda je rozdělení dat požadované pro dceřiné společnosti, pro více klientů nebo pouze pro škálování, věříme, že situace je možné vyřešit efektivněji s využitím více instancí aplikace Finance and Operations. |
| **Nahrazeno jinou funkcí?**   | Odběratelé používající datové oddíly musí použít více instancí aplikace Finance and Operations, pokud je oddělení úrovně databáze kritickým problémem.    |
| **Ovlivněné oblasti produktu**         | Všechny moduly  |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0.  |


### <a name="database-and-file-share-storage-for-attachments"></a>Úložiště databáze a sdílené složky souborů pro přílohy

Povolené úložiště příloh v databázi a sdílených složkách souborů povolené v Microsoft Dynamics AX 2012. Ani jedna z těchto možností již není podporována.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Úložiště sdílených složek souborů již není podporováno, protože prostředí hostovaná v cloudu nemohou komunikovat s místními sdílenými souborovými složkami. Databáze úložiště je zastaralá a nahradilo ji úložiště Azure Blob. Úložiště Azure Blob odpovídá úložišti v databázi, protože dokumenty jsou přístupné pouze pro formuláře klientů Dynamics 365 for Finance and Operations. To zajišťuje další výhodu poskytování úložiště, které negativně neovlivňuje výkonnost databáze. Úložiště objektů blob je výchozí mechanismus úložiště pro správu dokumentů a funguje okamžitě. |
| **Nahrazeno jinou funkcí?**   | Databáze úložiště je zastaralá a nahradilo ji úložiště Azure Blob.   |
| **Ovlivněné oblasti produktu**         | Všechny moduly  |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0.   |

### <a name="delimitation"></a>Vymezení

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Funkce nebyla shledána potřebnou. |
| **Nahrazeno jinou funkcí?**   | Žádný                                     |
| **Ovlivněné oblasti produktu**         | Čas a docházka                    |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0.         |

### <a name="desktop-client"></a>Klient pro stolní počítače

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Prostředí klienta aplikace Dynamics AX bylo přepracováno, aby se lépe používalo na různých platformách a v různých zařízeních.                      |
| **Nahrazeno jinou funkcí?**   | Nový webový klient je založen na metadatech formuláře pracovní plochy a programovacím modelu, které byly změněny tak, aby poskytovaly bohatou webovou platformu. |
| **Ovlivněné oblasti produktu**         | Všechny moduly  |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0.   |

### <a name="direct-database-connection"></a>Přímé připojení k databázi

V aplikaci Dynamics AX 2012 R3 se Retail Modern POS připojoval přímo k databázi Channel DB podobným způsobem jako k Enterprise POS. Byla to nástavba ke standardní metodě komunikace Retail Modern POS prostřednictvím Retail Serveru.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Přímé připojení k databázi vyžadovalo nižší protokoly zabezpečení a primárně sloužilo k dosahování nejvyšších úrovní výkonnosti. Vzhledem k výkonu a vylepšení zabezpečení, ke kterým došlo v aplikaci Finance and Operations tato funkce nyní způsobuje mnohem více problémů, než řeší. |
| **Nahrazeno jinou funkcí?**   | Č. V současné době se podporuje pouze standardní komunikace Retail Server.  |
| **Ovlivněné oblasti produktu**         | Databáze kanálů/Retail Modern POS   |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0.  |

### <a name="dutch-swift-mt940"></a>Nizozemský SWIFT MT940

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Namísto lokalizované funkce se nyní používá obecná funkce.                    |
| **Nahrazeno jinou funkcí?**   | Ano, tato funkce byla nahrazena funkcí Rozšířené odsouhlasení banky. |
| **Ovlivněné oblasti produktu**         | Všechny moduly                                                                              |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno.                           |

### <a name="ebilanz-xbrl-for-germany"></a>eBilanz (XBRL pro Německo)

Tato funkce poskytuje výstup v jazyce eXtensible Business Reporting Language (XBRL), který je určený konkrétně pro německou taxonomii eBilanz.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Nepoužíváno odběrateli.  |
| **Nahrazeno jinou funkcí?**   | Tato funkce nebyla nahrazena jinou funkcí, avšak pro německý trh je k dispozici několik speciálních balíčků XBRL obsahujících mnoho funkcí XBRL. |
| **Ovlivněné oblasti produktu**         | Management Reporter      |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno.  |

### <a name="enterprise-portal-client"></a>Klient podnikového portálu

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Byla poskytnuta jediná platforma klienta.  |
| **Nahrazeno jinou funkcí?**   | Nový webový klient je založen na metadatech formuláře pracovní plochy a programovacím modelu, které byly změněny tak, aby poskytovaly bohatou webovou platformu. |
| **Ovlivněné oblasti produktu**         | Všechny moduly  |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0.   |

### <a name="environmental-sustainability"></a>Udržitelnost životního prostředí

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Málo používáno odběrateli a omezená sada funkcí.  |
| **Nahrazeno jinou funkcí?**   | Žádný              |
| **Ovlivněné oblasti produktu**         | Dodržování předpisů a vnitřní kontroly, Závazky  |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0. |

### <a name="form-activex-and-managed-host-controls"></a>Ovládací prvky formuláře ActiveX a spravovaného hostitele

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Ovládací prvky formuláře ActiveX a spravovaného hostitele jsou založeny na zastaralém klientovi pro stolní počítače. |
| **Nahrazeno jinou funkcí?**   | Rozšířitelná architektura ovládacích prvků podporuje vytváření nových ovládacích prvků založených na jazyku HTML, CSS a JavaScript a slouží k prvotřídnímu ovládání v prostředí nástroje Microsoft Visual Studio. |
| **Ovlivněné oblasti produktu**         | Všechny moduly     |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0.       |

### <a name="generate-prenotes-by-using-a-batch"></a>Generování verifikačních transakcí pomocí dávky

Verifikační transakce nelze generovat pomocí dávky, ale mohou být generovány uživatelem.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Neexistuje žádný formulář, který by po vygenerování pomocí dávky zachovával a zobrazoval výsledný soubor verifikačních transakcí. |
| **Nahrazeno jinou funkcí?**   | Verifikační transakce lze i nadále generovat a uživatel může nastavit umístění, kam má být soubor uložen.   |
| **Ovlivněné oblasti produktu**         | Závazky, Pohledávky, Řízení zásob, Pokladna a banka  |
| **Stav**                         | Odstraněno od verze AX 7.0.    |

### <a name="german-dtaus-payment-export-and-account-statement-import-totals-and-transactions"></a>Export německé platby DTAUS a import výpisu z účtu (souhrny a transakce)

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Formát se již v Německu nepoužívá, protože byl nahrazen funkcí Jednotná oblast pro platby v eurech (SEPA).                    |
| **Nahrazeno jinou funkcí?**   | Ano, tato funkce byla nahrazena exportem plateb SEPA a rozšířenou funkcí odsouhlasení banky pro import výpisů z účtu. |
| **Ovlivněné oblasti produktu**         | Všechny moduly  |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno. |

### <a name="german-dtazv-payment-format"></a>Německý formát platby DTAZV

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Formát se již v Německu nepoužívá, protože byl nahrazen funkcí Jednotná oblast pro platby v eurech (SEPA). |
| **Nahrazeno jinou funkcí?**   | Export plateb SEPA    |
| **Ovlivněné oblasti produktu**         | Všechny moduly   |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno.    |

### <a name="german-mt940-import"></a>Německý import MT940

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Namísto lokalizované funkce se nyní používá obecná funkce.                    |
| **Nahrazeno jinou funkcí?**   | Ano, tato funkce byla nahrazena funkcí Rozšířené odsouhlasení banky. |
| **Ovlivněné oblasti produktu**         | Všechny moduly                                                                              |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno.                           |

### <a name="german-xml-eu-sales-list"></a>Německé souhrnné hlášení (EU) ve formátu XML

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Formát XML pro německé souhrnné hlášení již není podporován. K odeslání německého souhrnného hlášení německému daňovému úřadu lze použít pouze formát textového souboru ELMA5. |
| **Nahrazeno jinou funkcí?**   | Žádný         |
| **Ovlivněné oblasti produktu**         | Daň        |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno.   |

### <a name="gl-ssrs-reports"></a>Sestavy GL SSRS

Byly odebrány sestavy, které zahrnují následující položky nabídky: **Souhrnná předvaha**, **Podrobná předvaha**, **Účtové osnovy**, **Záznam pro audit**, **Zůstatky** a **Výpis zůstatků**.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Finanční sestavy Microsoft SQL Server Reporting Services (SSRS) byly nahrazeny funkcemi nástroje Management Reporter a výchozími sestavami. |
| **Nahrazeno jinou funkcí?**   | Management Reporter (v aktuální verzi aplikace Dynamics AX označeno jako **Finanční výkaznictví**)    |
| **Ovlivněné oblasti produktu**         | Hlavní kniha   |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0.   |

### <a name="infopart-and-formpart-metadata"></a>Metadata InfoPart a FormPart

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Metadata InfoPart a FormPart povolovala vytváření okna s fakty pro dva různé klienty. |
| **Nahrazeno jinou funkcí?**   | Metadata InfoPart, která byla zjednodušenou definicí formuláře, je převedena do formuláře při upgradu nástrojů. Metadata FormPart, která odkazovala na formulář, jsou nahrazena přímějším odkazem, který je vytvářen při upgradu nástrojů. |
| **Ovlivněné oblasti produktu**         | Všechny moduly    |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0.        |

### <a name="main-account-list-page"></a>Stránka seznamu hlavních účtů

Seznam účtů pro právnickou osobu a související informace o zůstatku

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Informace o zůstatku jsou k dispozici na stránce seznamu **Předvaha** podle účtu a dimenze.  |
| **Nahrazeno jinou funkcí?**   | **Hlavní účty** obsahuje seznamu účtů, **hlavní účet** obsahuje stránku se seznamem. V zobrazení v podobě mřížky se na stránce **Hlavní účty** zobrazuje rovněž i menší pohled podobný mřížce. |
| **Ovlivněné oblasti produktu**         | Hlavní kniha      |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0.    |

### <a name="malaysia-and-singapore-bank-cash-flow-report"></a>Sestava bankovního cashflowu v Malajsii a Singapuru

S touto funkcí mohou uživatelé tisknout sestavu cashflowu, v níž jsou uvedeny transakce a podrobnosti o přírůstcích a úbytcích hotovosti pro určený časový interval pro vybraný bankovní účet.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Stejné informace lze získat z funkce Dotaz na bankovní transakce. |
| **Nahrazeno jinou funkcí?**   | Dotaz na bankovní transakce                                            |
| **Ovlivněné oblasti produktu**         | Pokladna a banka                                                |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno.          |

### <a name="mexican-cfd-electronic-invoice"></a>Mexická elektronická faktura CFD

Tato funkce povolovala generování mexické elektronické faktury pomocí metody CFD (Comprobante Fiscal Digital), u které společnost podepisuje faktury žádostí o příslušné schválení od vlády. Tato funkce rovněž poskytuje měsíční sestavu, která obsahuje všechny elektronické faktury, které byly v daném období vydány.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Metoda již není použitelná. Generování elektronických faktur metodou CFD bylo zrušeno ze strany finančního úřadu a nahrazeno metodou Comprobante Fiscal Digital a través de Internet (CFDI), u které je podepisování delegováno na poskytovatele třetí strany (PAC). Měsíční sestava byla odebrána, uživatelé mohou prostřednictvím dotazu získat informace o historických transakcích. |
| **Nahrazeno jinou funkcí?**   | Žádný    |
| **Ovlivněné oblasti produktu**         | Pohledávky, Projekt   |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno. |

### <a name="mexico-realized-and-unrealized-vat"></a>Uplatněná a neuplatněná DPH v Mexiku

Aplikace Microsoft Dynamics AX 2012 spravovala neuplatněnou daň z přidané hodnoty (DPH) pomocí funkce pro neuplatněnou daň specifické pro Mexiko.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Duplicitní funkce  |
| **Nahrazeno jinou funkcí?**   | Ano, tato funkce byla nahrazena standardní funkcí podmíněné DPH, která je k dispozici ve verzi Core. |
| **Ovlivněné oblasti produktu**         | Daň   |
| **Stav**                         | Zastaralé: Datum odebrání nebylo pro tuto funkci stanoveno. |

### <a name="microsoft-outlook-integration"></a>Integrace sady Microsoft Outlook


|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Tato funkce byla nahrazena integrací Microsoft Exchange Server. |
| **Nahrazeno jinou funkcí?**   | Ano                                                                            |
| **Ovlivněné oblasti produktu**         | Prodej a marketing                                                            |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0.                                                 |

### <a name="private-blocking-of-inventory-and-warehouse-management-journals"></a>Soukromé blokování deníků řízení zásob a skladu

Deníky skladů a zásob již nepodporují možnost označení deníku jako soukromého pro vybraného uživatele. Je podporován pouze proces blokování deníků jako soukromých pro skupiny uživatelů a blokování během úprav.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Funkce nebyla shledána potřebnou. |
| **Nahrazeno jinou funkcí?**   | Žádný                                     |
| **Ovlivněné oblasti produktu**         | Řízení zásob                   |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0.         |

### <a name="product-builder"></a>Konfigurátor výrobku

Konfigurátor výrobku byl používán k dynamické konfiguraci položek z prodejní objednávky, nákupní objednávky, výrobní zakázky, prodejní nabídky, nabídky projektu nebo požadavku na položku. Na základě modelu produktu s proměnnými modelování mohl uživatel volit hodnoty podle potřeb odběratele a získat jedinečnou variantu produktu s vlastním kusovníkem a postupem.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Konfigurátor výrobku zveřejňoval kód X ++ koncovým uživatelům a není v aktuální verzi aplikace Dynamics AX podporován. Byl odebrán kvůli zamezení duplicitní údržby na překrývajících se kódech.  |
| **Nahrazeno jinou funkcí?**   | Ano. Konfigurace založená na omezeních byla uvedena v aplikaci Dynamics AX 2012, kde již byl oznámen odpis konfigurátoru výrobku v budoucích verzích. Technologie konfigurace založené na omezeních je zvolena na základních produktech k umožnění konfigurace. Další informace naleznete v tématu [Vytvoření modelu konfigurace produktu](../../supply-chain/pim/build-product-configuration-model.md). |
| **Ovlivněné oblasti produktu**         | Řízení informací o produktech, Prodej a marketing  |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0.      |

### <a name="production-floor-app"></a>Aplikace Production Floor
Jedná se o aplikaci pro tablety se systémem Windows 8.1 RT a Windows 8.1 Pro.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Se změnou webového klienta je možné doručit podobnou funkci prostřednictvím nativního klienta Dynamics AX 7.0. Zařízení úkolového lístku poskytuje aplikaci Production Floor rozhraní, které je optimalizováno pro provedení dotykových zařízení a tabletů. |
| **Nahrazeno jinou funkcí?**   | Ano. Zařízení úkolového lístku, které je nativní součástí Dynamics AX 7.0.                                                                           |
| **Ovlivněné oblasti produktu**         | Řízení výroby                                                |
| **Stav**                         | Zastaralé: Datum odstranění z obchodu Microsoft nebylo dosud stanoveno pro tuto funkci.                                                |


### <a name="rename-product-dimension"></a>Změnit název dimenze produktu

Touto funkcí lze měnit název jedné ze tří standardních dimenzí produktu (velikosti, barva nebo styl) tak, aby lépe vyhovoval obchodním požadavkům. Přejmenování zahrnovalo všechny popisky, kde by použit název dimenze produktu.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Aktuální verze aplikace Dynamics AX nepodporuje změny popisků v době běhu. |
| **Nahrazeno jinou funkcí?**   | Žádný                                                                            |
| **Ovlivněné oblasti produktu**         | Řízení informací o produktech                                                |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0.                                                |

### <a name="retail-server-connectivity-using-http"></a>Konektivita Retail Server u využívající HTTP

V aplikaci Dynamics AX 2012 R3 může Retail Server fungovat pomocí komunikace HTTP (nezabezpečené). Byl to dodatek ke standardní komunikaci pomocí připojení HTTPS.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Z důvodu nových požadavků na zabezpečení je nyní podporována pouze zabezpečená komunikace pomocí TLS 1.2 (nebo vyšší podle dostupnosti). Samoobslužný instalační program bude automaticky konfigurovat počítač na tuto komunikaci. |
| **Nahrazeno jinou funkcí?**   | Č. V současné době se podporuje pouze standardní komunikace HTTPS. |
| **Ovlivněné oblasti produktu**         | Server maloobchodu  |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0. |

### <a name="role-center-pages"></a>Stránky pracovní plochy role

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Stránky pracovní plochy rolí byly vytvořeny na zastaralé platformě podnikového portálu, která byla v aktuální verzi aplikace Dynamics AX nahrazena novou platformu webového klienta. |
| **Nahrazeno jinou funkcí?**   | Nový vzor formulářů v pracovním prostoru nabízí uživatelům možnost návrhu zaměřeného na procesy, který zajišťuje snadný přístup k často používaným úkolům v rámci tohoto procesu.                       |
| **Ovlivněné oblasti produktu**         | Všechny moduly    |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0   |

### <a name="sales-tax-jurisdictions"></a>Příslušnosti k dani

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Málo používáno odběrateli a omezená sada funkcí. |
| **Nahrazeno jinou funkcí?**   | Žádný                                           |
| **Ovlivněné oblasti produktu**         | DPH v USA                                 |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0.               |

### <a name="sites-services"></a>Služba Sites Services

Služba Sites Services umožňuje vytvářet webové stránky, které rozšiřují obchodní procesy na Internet bez IT podpory.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Infrastruktura Microsoft Azure používaná aplikací Dynamics AX má nové funkce, které lze použít (například weby Azure). |
| **Nahrazeno jinou funkcí?**   | Žádný   |
| **Ovlivněné oblasti produktu**         | Nábor HR, správa případů, požadavek na cenovou nabídku, registrace dodavatele, pracovní prostory pro spolupráci pro příležitosti a kampaně  |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0.    |

### <a name="ssas-demand-forecasting-strategy"></a>Strategie prognózy poptávky SSAS

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Návrh funkce nemůže být podporován v nové cloudové architektuře. |
| **Nahrazeno jinou funkcí?**   | Strategie prognózy poptávky Azure Machine Learning                           |
| **Ovlivněné oblasti produktu**         | Hlavní plánování                                                              |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0.                                               |

### <a name="vendor-invoice-pool-excluding-posting-details"></a>Podrobnosti evidence faktur dodavatelů bez zaúčtování

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Malé využití. Tato funkce byla nahrazena deníkem faktur s funkcí workflowu. |
| **Nahrazeno jinou funkcí?**   | Možnosti workflowu v modulu Deník faktur.     |
| **Ovlivněné oblasti produktu**         | Závazky |
| **Stav**                         | Odstraněno od verze Dynamics AX 7.0.    |


### <a name="virtual-company-accounts"></a>Virtuální účty společnosti

Funkce virtuálních společností není aplikací Dynamics AX již podporována. Funkce virtuálních společností umožňovala uživatelům nastavit tabulky, které mohlo sdílet více společností. Popis funkce naleznete zde: [Účty společnosti a virtuální účty společnosti](https://msdn.microsoft.com/en-us/library/aa834382(v=ax.10).aspx). Funkce funguje tak, že seskupuje tabulky do kolekcí, které jsou přiřazeny k virtuálním společnostem, což jsou skupiny skutečně existujících společností. Dotazy jsou vytvářeny tak, aby všechny společnosti ve virtuální společnosti měli přístup k datům v tabulkách souvisejících kolekcí tabulek.

|   |  | 
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | - Virtuální společnosti je nutné nastavit před uložením dat do tabulek. Zpětné začlenění virtuálních společností do existující implementace je velmi obtížné.<br><br>- Vzhledem k tomu, že v aktuální verzi aplikace Microsoft Dynamics AX je spousta normalizací dat, je nyní těžké poznat, co přidat do kolekce tabulek. Například je obtížné poznat, které tabulky se mají sdílet. Také je nutné přidat všechny tabulky, na které je odkazováno z tabulek, které jsou ve virtuální společnosti. Kvůli normalizaci tabulky musí být i jednoduchá hlavní data, která jsou rozdělená do více tabulek, součástí virtuální společnosti. Jakákoli zde provedená chyba způsobí funkční problémy.<br><br>- Pokud je tabulka součástí virtuální společnosti, ztratí informace o původu dat a je zaznamenána pouze virtuální společnosti.   |
| **Nahrazeno jinou funkcí?** | Globální tabulky mohou být použity k zpřístupnění tabulek ze všech společností. V současné době neexistuje žádná náhrada. |   
| **Ovlivněné oblasti produktu**       | Všechny moduly |   
| **Stav**                       | Odstraněno od verze Dynamics AX 7.0.   |   

### <a name="windows-8-tablet-app"></a>Windows 8 - aplikace pro tablety

Aplikace pro tablety Windows 8 poskytovala funkci pro zadání a schválení výdajů.

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Finance and Operations je kompatibilní s tablety. Aplikace pro tablety již není požadována.    |
| **Nahrazeno jinou funkcí?**   | Č.          |
| **Ovlivněné oblasti produktu**         | Správa výdajů   |
| **Stav**                         | Odstraněno: Tato funkce je k dispozici pouze pro Dynamics AX 2012 R3. |

### <a name="workplanner"></a>Plánovač práce

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Malé využití |
| **Nahrazeno jinou funkcí?**   | Ne, ale stránka **Vztah profilu**, kterou lze otevřít ze stránky **Skupiny profilů**, podporuje stejný obchodní scénář jako zastaralá stránka **Plánovač práce**. |
| **Ovlivněné oblasti produktu**         | Čas a docházka     |
| **Stav**                         | Kód nebyl odstraněn. Formulář JmgWorkPlanner však nebyl migrován.    |

### <a name="x-financial-statements"></a>Finanční výkazy X++

|                                                 |                                                                                                          |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <strong>Důvod pro zrušení/odstranění</strong> |                         Tato funkce byla nahrazena jinou funkcí.                         |
|  <strong>Nahrazeno jinou funkcí?</strong>  | Management Reporter (v aktuální verzi aplikace Dynamics AX označeno jako <strong>Finanční výkaznictví</strong>) |
|     <strong>Ovlivněné oblasti produktu</strong>     |                                              Hlavní kniha                                              |
|             <strong>Stav</strong>             |                                      Odstraněno od verze Dynamics AX 2012                                      |

