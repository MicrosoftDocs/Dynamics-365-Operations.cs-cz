---
title: Finanční analýza
description: Finanční analýza používá Microsoft Microsoft Power BI pro spojení finančních klíčových indikátorů výkonnosti, grafů a finančních výkazů.
author: kweekley
ms.date: 04/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 71fd1ad15320fda162a289e9c5741aec2ce76778
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894901"
---
# <a name="financial-analysis"></a>Finanční analýza

[!include [banner](../includes/banner.md)]

**Finanční analýza** používá Microsoft Power BI pro spojení finančních klíčových indikátorů výkonnosti, grafů a finančních výkazů. Power BI je vloženo do aplikace Záměrem **finanční analýzy** je sestava analýz. Osoby v rámci organizace mohou zobrazit, prohledávat, pochopit a jednat. 

**Finanční analýza** kombinuje data z hlavní knihy a dílčích hlavních knih, aby poskytla ucelenější obrázek o finančním stavu organizace.

> [!NOTE]
> Tento dokument používá následující terminologii Power BI:
> 
> - **Sestava** – Jeden soubor .pbix, do kterého jsou uloženy všechny vizuální prvky na všech kartách.
> - **Stránka** – Karta v jednom .pbix souboru. Každá stránka může obsahovat jeden nebo více vizuálních prvků.
> - **Vizuální prvek** – Jeden zdroj dat, například karta, indikátor KPI, diagram, graf, matice nebo finanční výkaz. Stránka s finančním výkazem jako vizuálním prvkem může neobsahovat jiné vizuální prvky z důvodu velikosti dat, která se vykazují.

V současné době se **Finanční analýza** používá k zobrazení dat pro aktivní právnickou osobu nebo všechny právnické osoby. V příštích verzích se pracovní prostor vyvine do místa, kde můžete používat Power BI k úpravám a vytváření vizuálních prvků.

Pracovní prostor **Přehled CFO** zobrazuje stejné vizuální prvky jako **Finanční analýza**, ale zaměřuje na se poskytnutí zobrazení a filtrování dat stávajících sestav. V dalších verzích bude moct přidávat nové vizuální prvky do pracovního prostoru **Finanční analýza**. Nové vizuální prvky mohou být také k dispozici v pracovních prostorech, které se zaměřují na jiné role, jako jsou projektoví manažeři nebo manažeři závazků. Pracovní prostor **Přehled CFO** nadále zobrazuje data pro všechny právnické osoby, bez ohledu na právnické osoby, ke kterým má role přístup.

## <a name="dynamics-365-finance-setup"></a>Nastavení Dynamics 365 Finance
**Hlavní kniha**

Typ hlavního účtu a kategorie hlavního účtu slouží k zadání do příslušných hlavních účtů na finančním výkazu **Rozvaha** a na různých finančních výkazech **Výsledovka** ve **finanční analýze**.

Na stránce **Hlavní účty** je nutné definovat váš hlavní účet, aby k němu byl přiřazen jeden z následujících typů:

- Výnosy
- Expense
- Majetek
- Závazky
- Jmění

Nepřiřazujte jiný typ hlavního účtu, jako je například **Rozvaha** nebo **Zisk a ztráta** ke svým hlavním účtům. Sestavy nemohou určit typ hlavního účtu, pokud byly přiřazeny jiné typy hlavního účtu, protože nejsou dostatečně podrobné. Typ hlavního účtu musí být určen k zobrazení závazků a výnosů jako kladných částek ve finančních sestavách.

Aby se zobrazil na finančních výkazech a byl zahrnut v různých dalších vizuálních prvcích, jako jsou například indikátory KPI, musí být ke každému hlavnímu účtu přiřazena kategorie hlavního účtu. Kategorie hlavního účtu byly rozšířeny, aby zahrnovaly pořadí zobrazení. Pořadí zobrazení se používá specificky na finančních výkazech ve **finanční analýze**. Po upravení nebo přidání nové kategorie hlavního účtu lze změnit hodnotu **Pořadí zobrazení** pro definování pořadí, ve kterém mají být zobrazeny kategorie hlavního účtu na finančním výkazu. Pokud musíte změnit pořadí zobrazení pro mnoho kategorií hlavního účtu, můžete použít funkci Otevřít v aplikaci Excel pro rychlou úpravu a publikování změn zpět do aplikace.

## <a name="entity-store"></a>Úložiště entit
Data pro **finanční analýzu** pocházejí z úložiště entit (**Správa systému** \> **Nastavení** \> **Úložiště entit**). Otevřete-li pracovní prostory **Přehled CFO** nebo **Finanční analýza** a zobrazí se následující upozornění ve vizuálních prvcích, je nutné aktualizovat entity.

![Upozornění](./media/Cantdisplay.png)

Je nutné aktualizovat následující entity pro zobrazení dat v pracovním prostoru **Finanční analýza**:

- Data transakce finančního výkaznictví -verze 3 
- Kredit a inkasa V2
- CustCollectionsBIMeasurements
- LedgerCovLiquidityMeasurement
- Krychle Nákup
- Krychle Prodej

Můžete definovat opakování dávek pro pravidelnou aktualizaci dat v entitách. Vzhledem k tomu, že každá entita je během aktualizace zcela přetvořena, vyberte čas a četnost aktualizace entity opatrně. FinancialReportingTransactionData je primární entita, používaná pro finanční výkazy. Proto se můžete rozhodnout pro aktualizaci této entity častěji.

## <a name="security"></a>Zabezpečení
V současné době data v integrovaných sestavách Power BI nelze omezit na právnické osoby, ke kterým má uživatel přístup. Proto jsou integrované sestavy Power BI řízeny prostřednictvím funkčních oprávnění v nastavení zabezpečení. Funkční oprávnění jsou definována pro povolení přístupu k datům všech právnických osob nebo pouze aktivní společnosti. Následující tabulka zobrazuje existující funkční oprávnění a role, ke kterým jsou přiřazena. Funkční oprávnění lze odebrat nebo přiřadit k různým rolím, na základě požadavků vaší společnosti.

| Funkční oprávnění                                    | Role | popis |
|-----------------------------------------|-------|------------|
| Zobrazit finanční analýzu aktuální společnosti | <ul><li>Účetní</li><li>Účetní manažer</li><li>Účetní supervizor</li><li>Auditor</li><li>Správce rozpočtu</li><li>Výkonný ředitel</li><li>Vedoucí finančního oddělení</li><li>Finanční kontrolor</li></ul> | Toto funkční oprávnění poskytuje přístup k finanční analýze. Standardně slouží aktivní společnost jako filtr. Nelze přidat další právnické osoby. |
| Zobrazit finanční analýzu celé společnosti   | In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3, toto funkční oprávnění není přiřazeno k roli. V další verzi bude toto funkční přiřazeno k roli vedoucího finančního oddělení. | Toto funkční oprávnění poskytuje přístup k položce nabídky pracovního prostoru Přehled CFO. Standardně slouží aktivní společnost jako filtr. Můžete však přidat všechny právnické osoby, bez ohledu na to, zda má uživatel přístup k jiným právnickým osobám. |


## <a name="financial-reporting-vs-financial-analysis"></a>Finanční výkaznictví versus Finanční analýza
Ačkoli **Finanční analýza** obsahuje finanční výkazy, není to náhrada za finanční výkaznictví v aplikaci. Výchozí finanční výkazy ve **finanční analýze** jsou omezeny rozsahem a nezahrnují všechny typy finančních výkazů. Finanční výkaznictví je stále primárním nástroj pro návrh, vytváření a generování zákonem požadovaných finančních výkazů.

Následující graf s porovnáním vám pomůže rozlišit tyto dvě možnosti:


|                                                          | Financial Reporting                                               | Finanční analýza |
|----------------------------------------------------------|-------------------------------------------------------------------|--------------------|
| **Upravit výchozí sestavy**                                 | Ano                                                               | Žádný |
| **Vytvořit nové sestavy**                                   | Ano                                                               | Žádný |
| **Tisk sestav**                                        | Ano                                                               | Žádný |
| **Export do aplikace Excel**                                      | Ano                                                               | Omezené exporty nezpracovaných dat do aplikace Excel, ne formátovaná sestava |
| **Podpora hierarchie vykazování/organizační hierarchie**   | Ano                                                               | Žádný |
| **Vykázat data dílčí knihy**                             | Ano omezeno pouze na dodavatele, zákazníka                              | Ano dodavatel, odběratel, skupiny odběratelů nebo dodavatelů, adresy odběratele nebo dodavatele, atd. |
| **Měna vykazování**                                   | Ano Zúčtovací měna a Převést na měnu vykazování       | Ne Pouze v zúčtovací měně |
| **Zabezpečení**                                             | Ano odpovídá Finance a vykazování stromového zabezpečení | Omezené zobrazení sestav pro všechny společnosti (bez ohledu na zabezpečení Finance and Operations) nebo jen aktivní společnost |
| **Podporuje různé účtové osnovy a fiskální roky** | Ano                                                               | Žádný |
| **vykázat externí data**                              | Žádný                                                                | Žádný |
| **Podpora konsolidací**                               | Ano                                                               | Omezené Lze vykázat více společností, ale používat pouze zúčtovací měnu |

K dispozici jsou následující finanční výkazy:

- Předvaha
- Rozvaha
- Výsledovka podle oblasti
- Výsledovka – skutečnost a rozpočet
- Výsledovka s odchylkami
- Výsledovka s 12měsíčním trendem
- Tříletý trend výdajů
- Výdaje podle dodavatele
- Prodej odběrateli

## <a name="edit-visuals"></a>Úprava vizuálních prvků
Předchozích vydáních **finanční analýzy** nešlo upravit žádný vizuální prvek. V dalších verzích uživatelé s příslušným zabezpečením budou moci vytvářet nové vizuální prvky, kopírovat stávající a upravovat je. Ačkoliv jsou soubory .pbix obsahující sestavy k dispozici jako zdroje, nedoporučujeme úpravu výchozích sestav. Další změny budou provedeny v datovém modelu, výchozích sestavách a vlastních vizuálních prvcích finančních výkazu, které se používají k tvorbě finančních výkazů. Proto abyste mohli využít nové funkce a změny datového modelu v další verzi, je třeba znovu provést změny provedené ve výchozích sestavách prostřednictvím Microsoft Power BI Desktop.

## <a name="filtering"></a>Filtrování
Uživatelé mohou filtrovat sestavu pomocí podokna **Filtr** na levé straně. Toto podokno je stejné, jako podokno dostupné prostřednictvím Power BI Desktop. Existují různé úrovně filtrování, z nichž některé nemusí být k dispozici v závislosti na výběru na stránce (kartě) nebo použíití podrobných možností:

- **Filtry na úrovni sestavy** – Tyto filtry se používají na všechny vizuální prvky na všech stránkách (kartách).
- **Filtry na úrovni stránek** – Tyto filtry se používají na všechny vizuální prvky na aktivní kartě. Tyto filtry se používají nad filtry na úrovni sestavy.
- **Filtry na úrovni vizuálních prvků** – Tyto filtry se používají pouze na vybrané vizuální prvky. Tyto filtry se používají nad filtry na úrovni stránek.
- **Podrobný filtr** – Tento filtr filtruje ze zdrojového vizuálního prvku, který je použit na aktuální vizuální prvek při procházení ze zdrojového na aktuální vizuální prvek.

![Možnosti filtrování](./media/filter.png)

Chcete-li odebrat konkrétní hodnotu filtru, vyberte symbol gumy vedle něj. Neodebírejte filtr pomocí výběru X. Když zvolíte X, je pole, které chcete filtrovat, odebráno jako možnost filtru. Pokud omylem odeberete pole z filtru, zavřete pracovní prostor a otevřete ho znovu. Výchozí nastavení filtru se znovu použije.

Ve výchozím nastavení se při prvním otevření pracovních prostorů použije aktivní právnická osoba jako filtr na úrovni sestavy. V závislosti na svých zabezpečeních mohou uživatelé přidávat další právnické osoby nebo měnit výchozí právnickou osobu, která je vybrána ve filtru.

Filtr **Fiskální kalendář** je povinný, aby se použil pro vizuální prvek správný kalendář. Filtr na úrovni sestavy je nastaven ve výchozím nastavení na fiskální kalendář aktivní právnické osoby. Pokud změníte filtr na fiskální kalendář, který má jiné počáteční nebo koncové datum, nebudou zahrnuty počáteční zůstatky. Z toho vyplývá, že vaše finanční výkazy **Rozvaha** nezobrazí správné zůstatky. Pokud vyberete další fiskální kalendář ve filtru, budete mít další sadu sloupců. Každá dodatečná sada sloupců zobrazuje částky pro odlišný fiskální kalendář.

Filtr **Účtovací vrstva** je rovněž povinný. Standardně je tento filtr nastaven na Aktuální. Můžete vybrat další účtovací vrstvy ve filtru pro zobrazení souhrnných částek.

Filtry jsou také dostupné pro pole **Datum** a **Fiskální rok**. Tyto filtry se obvykle vztahují na úroveň stránky. Standardně používá filtr **Datum** relační datum, které lze změnit. Lze také odstranit filtr relačního data a použít namísto něj filtr **Fiskální rok**.

## <a name="currency"></a>Měna

Všechny vizuální prvky, které vykazují data hlavní knihy, zobrazují částky v zúčtovací měně. Proto při filtrování právnické osoby musíte důkladně zahrnout pouze právnické osoby, které mají stejnou zúčtovací měnu. V opačném případě budete agregovat data v různých měnách.

Všechny vizuální prvky, které vykazují data dílčí knihy, jako jsou například vizuální prvky **Prognóza cashflow** a **Prvních 10**, zobrazují částky v měně systému. Systémová měna a typ směnného kurzu systému jsou definovány na stránce **Systémové parametry**.

Vizuální prvek **Zůstatek podle bankovních účtů** používá částky v měně bankovních účtů.

## <a name="dimensions"></a>Dimenze

Výchozí finanční výkazy nezahrnují finanční dimenze, ale jsou zaměřeny pouze na hlavní účet. Podpora pro finanční dimenze bude dostupná v příštích verzích, až bude možné sestavy upravit. Organizace pak budou moci filtrovat podle hodnot finančních dimenzí.

Některé finanční výkazy obsahují dimenze, které jsou založeny na transakcích dílčí knihy. Cílem nových finančních výkazů je povolit filtrování dimenzí, které ještě nejsou nastaveny jako finanční dimenze. Například výchozí sestava Výdaje podle dodavatele vám umožní podrobnější zobrazení za hlavním účtem, abyste mohli vidět zůstatky podle jednotlivých dodavatelů. Dodavatel není nastaven jako finanční dimenze. Místo se toho systém vrátí na původní transakci dílčí hlavní knihy pro vyhledání dodavatele.

Následující dimenze se používají ve výchozích sestavách. Žádná z těchto dimenzí není finanční dimenzí.

- Dodavatel
- Skupina dodavatelů
- Zákazník
- Skupina odběratelů
- Země/oblast
- Kraj
- Město

> [!IMPORTANT] 
> Pokud shrnete transakce pro více dodavatelů nebo odběratelů do jednoho dokladu pomocí finančních deníků, data budou nesprávná. Proces výkaznictví nemůže určit, který odběratel nebo dodavatel se vztahuje ke konkrétnímu účtu hlavní knihy v položce deníku, protože informace nejsou uchovávány všude. Z tohoto důvodu nedoporučujeme zadávat více dodavatelů, odběratelů, dlouhodobého majetku nebo projektů do jediného dokladu.

## <a name="drill-on-data"></a>Procházení k podrobnostem dat

V Power BI jsou k dispozici různé úrovně přechodu na podrobnosti. Každá úroveň má jiný název a jiné funkce. Rovněž můžete přejít na podrobnosti řádků a sloupců. Tato část se zabývá různými možnostmi použitím finančního výkazu **Předvaha** jako příkladu a zobrazuje, jakým způsobem je možné přejít na řádky. Stejná funkce existuje pro sloupce. Musíte pouze změnit nastavení **Procházení na podrobnosti**.

Na následujícím obrázku je výkaz **Předvaha** sbalen na nejvyšší úroveň hierarchie řádku, hlavní typ účtu.

![Výkaz předvahy](./media/trial-balance.png)

Chcete-li zobrazit další úroveň hierarchie, kategorie hlavního účtu, lze nastavit pole **Přejít na podrobnosti** na **Řádky** a poté vybrat tlačítko **Rozbalit** (třetí tlačítko po poli přechodu na podrobnosti). Nyní se rozbalí všechny kategorie hlavního účtu. V současné Power BI neumožňuje rozbalit pouze jeden řádek nebo sloupec, ale stále se zobrazují všechny ostatní řádky nebo sloupce.

![Rozpis předvahy v řádcích](./media/trial-balance2.png)

Chcete-li rozbalit na úrověň hlavních účtů pro všechny řádky, můžete znovu použíttlačítko **Rozbalit**. Chcete-li však přejít dolů na podrobnosti hlavních účtů pro jeden řádek, nejprve zvolte tlačítko **Přejít dolů k podrobnostem** (jednoduchá šipka směrem dolů na pravé straně okna) a pak vyberte řádek, na který chcete přejít. Následující obrázek znázorňuje výsledek při volbě řádku **Prodej** po zvolení tlačítka **Přejít dolů k podrobnostem**.

![Tlačítko rozbalení předvahy](./media/trial-balance3.png)

Po přechodu dolů k podrobnostem na jeden řádek je třeba několik kliknutí, abyste se vrátili k plné předvaze. Tlačítko **Přejít nahoru k podrobnostem** (první tlačítko po poli **Přejít k podrobnostem**) přejde nahoru pouze v kontextu kategori **Prodej**, jak je uvedeno na následujícím obrázku.

![Tlačítko přechodu nahoru k podrobnostem předvahy](./media/trial-balance4.png)

Můžete nadále používat tlačítko **Přejít nahoru k podrobnostem** pro návrat na nejvyšší úrověň souhrnu řádků.

Power BI má také tlačítko, které vám umožní přejít na další úroveň v hierarchii (druhé tlačítko po poli **Přejít na podrobnosti**). Účinek tohoto tlačítka se liší od účinku tlačítka **Rozbalit** (třetí tlačítko po poli **Přejít na podrobnosti**), které se používá k rozbalení hierarchie. Po rozbalení hierarchie se hierarchie uchová v sestavě. Jak bylo zobrazeno dříve, pokud například rozbalíte na úrověň typu hlavního účtu, stále uvidíte v sestavě typ hlavního účtu. Pokud všask přejdete na další úroveň v hierarchii, tato sestava již nezobrazuje nadřazenou položku v hierarchii, jak je zobrazeno na následujícím obrázku.

![Tlačítko přechodu zpět předvahy](./media/trial-balance5.png)

Chcete-li zobrazit podrobnosti o transakcích za souhrnnými zůstatky, můžete vybrat některé částky pro přechod zpět do aplikace Finance and Operations.

Přechod zpět z finančních výkazů vás zavede na průzkumníka zdroje účetnictví, nikoli na transakce dokladu. Průzkumník zdroje účetnictví nezobrazuje pouze účetní položky v hlavní knize. Místo toho zobrazuje podrobnosti transakce dílčí knihy. Proto získáte velmi podrobné informace o původní transakci a můžete je použít k analýze. Například uvidíte, kdo byl dodavatelem nebo odběratelem, co odběratel koupil nebo dodavatel prodal, a dokonce i to, jaký projekt byl na transakci.

Následující filtry z finančních výkazů jsou odeslány do průzkumníka zdroje účetnictví, aby zobrazil agregované transakce:

Povinná pole pro filtrování:

- Právnická osoba
- Fiskální kalendář
- Rok
- ID hlavního účtu

Volitelná pole pro filtrování:

- Čtvrtletí
- Měsíc
- Období

Pokud nerozbalíte dolů dostatečně daleko na řádek, přechod dolů na podrobnosti nefunguje. Například pokud rozbalíte dolů pouze na kategorii hlavního účtu, nelze přejít dolů do průzkumníka zdroje účetnictví na zůstatek, protože pro filtrování v průzkumníkovi zdroje účetnictví je vyžadováno pole hlavního účtu.

Pokud rozbalíte příliš dolů na řádek, další filtry ve finančních výkazech nejsou odeslány do průzkumníka zdroje účetnictví. Z toho vyplývá, že můžete mít rozdíl ve vašich číslech. Například pokud rozbalíte dolů na zemi nebo oblast na řádky výsledovky podle oblasti, finančí výkaz, země nebo oblast nebudou zahrnuty do průzkumníka zdroje účetnictví jako filtr.

> [!NOTE]
> Je možné přejít na řádky finančního výkazu nebo sloupce níže, než průzkumník zdroje účetnictví pro filtrování aktuálně podporuje. V některých situacích tedy součet podrobných transakcí v průzkumníkovi zdroje účetnictví nebude odpovídat zůstatku, na jehož podrobnosti se vracíte. Tato funkce bude v budoucnosti vylepšena.

## <a name="hierarchies"></a>Hierarchie

Výchozí finanční výkazy používají dvě hierarchie pro procházení a rozbalení dat. Jedna hierarchie je pro řádky a druhá hierarchie je pro sloupce. Obě hierarchie jsou předdefinovány v návrhu finančního výkazu. U většiny finančních výkazů je hierarchií řádku **Typ hlavního účtu** \> **Kategorie hlavního účtu** \> **Hlavní účet**. Některé sestavy mají však další pole, jako například Země a Oblast. Další uzly hierarchie jsou založeny na údajích dílčí hlavní knihy pro každou transakci.

Pro sloupce je hierarchie zaměřena na právnické osoby a fiskální období. U většiny finančních výkazů je hierarchií sloupce **Právnická osoba** \> **Fiskální kalendář** \> **Fiskální rok** \> **Čtvrtletí** \> **Období**.

V současné době finanční výkazy nepodporují organizační hierarchie, které umožňují agregovat data.

## <a name="data-limitations"></a>Limitace dat
Vizuální prvky finančního výkazu mají limit na počet řádků, které mohou být zobrazeny. V současné době je limit nastaven na 30 000. Pokud překročíte tento limit, bude mít vizuální prvek varovný symbol upozorňující na tuto situaci.

![Limitace dat](./media/data-limit.png)

Při překročení maxima budou součty, které se objevují ve finančním výkazu, nesprávné, protože nebyly načteny všechny řádky do vizuálního prvku.

### <a name="empty-rows"></a>Prázdné řádky
Power BI nenabízí možnost skrytí a zobrazení prázdných řádků. Pokud řádek neobsahuje žádná data, řádek se ve vizuálním prvku nezobrazí.


## <a name="additional-resources-for-power-bi"></a>Další zdroje pro Power BI

Informace v následujících zdrojích není vyžadována, aby bylo možné povolit integrované sestavy pro pracovní prostor **Finanční analýza** v produkčním prostředí. Namísto toho jsou užitečné pro vývojářská pole a pokud chcete integrovat sestavy Power BI.

- [Přístup k analytickým pracovním prostorům a sestavám v prostředí s topologií 1-box](/archive/blogs/dynamicsaxbi/accessing-analytical-workspaces-on-1box-environment)

- [Přidání analýz do pracovního prostoru pomocí Power BI Embedded](/dynamics365/unified-operations/dev-itpro/analytics/add-analytics-tab-workspaces)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]