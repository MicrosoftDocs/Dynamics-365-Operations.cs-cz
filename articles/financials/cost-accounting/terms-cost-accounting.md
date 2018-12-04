---
title: "Terminologie týkající se účtování nákladů"
description: "Toto téma definuje klíčové podmínky, které se používají v nákladovém účetnictví."
author: ShylaThompson
manager: AnnBe
ms.date: 08/31/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostAccountingLedger
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 223114
ms.assetid: 1c798592-77d0-4a8f-beaa-9159c75957da
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 1ec2f4a407c705fb37681f5593d0f7ea31f4cf0f
ms.contentlocale: cs-cz
ms.lasthandoff: 03/26/2018

---

# <a name="cost-accounting-terminology"></a>Terminologie týkající se účtování nákladů

[!include [banner](../includes/banner.md)]

Toto téma definuje klíčové podmínky, které se používají v nákladovém účetnictví.

**Základ přidělení**

Základ přidělení se používá k měření a stanovení množství aktivit, jako například použité strojohodiny, spotřebované kilowatthodiny nebo obsazená plocha. Používá se jako základ pro přidělení nákladů k jednomu nebo několika objektům nákladů.

**Nákladové účetnictví**

Nákladového účetnictví vám umožnuje shromažďovat data z různých zdrojů, jako jsou například hlavní knihy, dílčí knihy, rozpočty a statistické údaje. Pak můžete analyzovat, shrnout a vyhodnocení nákladová data, aby vedení mohlo přijmout nejlepší možná rozhodnutí v oblasti aktualizací cen, rozpočtů, řízení nákladů apod. Zdrojová data, která jsou použita k analýze nákladů, se zpracovávají nezávisle na nákladovém účetnictví. Aktualizace v nákladovém účetnictví tedy zdrojová data neovlivňují. Nicméně při shromažďování nákladových dat z různých zdrojů a zejména, pokud importujete hlavní účty z hlavní knihy v aplikaci Microsoft Dynamics 365 for Finance and Operations jako prvky nákladů, dochází k redundanci dat, protože stejná data existují v hlavní knize i v nákladovém účetnictví. Tato redundance je ale žádoucí, protože finanční správu využíváte k externímu vykazování a nákladového účetnictví pro interní vykazování.

**Hlavní kniha nákladového účetnictví**

Definovaná podle kalendáře, měny a dimenze nákladového prvku řídí procesy a zásady měření nákladů. 

**Záznam nákladů**

Položky nákladů jsou výsledkem převodu prostřednictvím datových konektorů z položek hlavní knihy, přidělení nákladů a zaúčtovaných položek nákladů v denících nákladů.

**Objekt nákladů**

Jakýkoli typ objektu, který je vybrán pro řízení nákladů. Náklady nebo výnosy jsou buď přímo zaúčtované nebo přidělené k objektům nákladů. Některé typické objekty nákladů jsou:

-  Produkty
-  Projekty
-  Oddělení
-  Nákladová střediska

Vedení používá objekty nákladů, aby mohlo kvantifikovat náklady, ale také provést analýzu ziskovosti.

**Prvek nákladů**

Používá se jako funkce ke sledování a klasifikaci nákladů. Existují dva typy prvků nákladů: primární a sekundární.

Primární prvky nákladů představují tok nákladů z finančního účetnictví do nákladového účetnictví. Struktura typicky odpovídá ziskům a ztrátám účetní struktury v hlavní knize, kde prvek nákladů může odpovídat hlavnímu účtu. Ne všechny hlavní účty ale musejí být prezentovány jako prvky nákladů závisející na obchodních požadavcích. 

Sekundární prvky nákladů představují interní tok nákladů, protože tyto náklady se používají pouze v nákladovém účetnictví. Jsou použity v pravidlech shrnutí nákladů, aby agregovaly náklady do smysluplných sad používaných výpočtem režijních nákladů. 

**Klasifikace nákladů**

Klasifikace nákladů třídí náklady podle jejich sdílených vlastností. Náklady lze seskupit například seskupit podle prvků, vysledovatelnosti a chování.

-   **Podle prvků** – materiál, práce a výdaje.
-   **Podle vysledovatelnosti** – přímé a nepřímé náklady. Přímé náklady jsou přiřazeny přímo k objektům nákladů. Nepřímé náklady nejsou přímo vysledovatelné k objektům nákladů. Nepřímé náklady jsou přiděleny k objektům nákladů.
-   **Podle chování** – pevné, proměnné a poloproměnné.

**Chování nákladů**

Chování nákladů klasifikuje náklady na základě jejich chování ve vztahu ke změnám klíčových obchodních činností. Pro efektivní řízení nákladů musí vedení rozumět chování nákladů. Existují tři typy vzorců chování nákladů: pevné, proměnné a poloproměnné.

- **Pevné náklady** - Pevné náklady jsou náklady, které se v krátkém časovém horizontu nemění, bez ohledu na změny na úrovni aktivity. Pevné náklady mohou být například základní provozní výdaje podniku, jako je například nájem. Na tyto náklady nemá žádný vliv zvýšení ani snížení úrovně aktivity.

- **Variabilní náklady** - Variabilní náklady se mění podle změn na úrovni aktivity. Například: Ke každému prodanému výrobku se přidružují přímé specifické náklady na materiál. Čím více produktů se prodá, tím více přímých nákladů na materiál se musí zaplatit.

- **Poloproměnné náklady** - tyto náklady jsou částečně pevné a částečně proměnné náklady. Například poplatek za přístup k internetu zahrnuje standardní měsíční poplatek za přístup a poplatek za širokopásmové použití. Standardní měsíční poplatek za přístup jsou pevné náklady, zatímco širokopásmové použití jsou náklady proměnné.

**Jednotka řízení nákladů**

Jednotka řízení nákladů představuje strukturu nákladů. Struktura určuje tok nákladů v hierarchickém uspořádání mezi dimenzemi objektů nákladů a jejich odpovídajícími objekty nákladů. 

**Distribuce nákladů**

Používá se k distribuci nákladů z jednoho objektu nákladů na jeden nebo více dalších objektů nákladů použitím příslušného základu přidělení. Distribuce nákladů a přidělení nákladů se liší v tom, že k distribuci nákladů dochází vždy na úrovni primárního prvku nákladů původních nákladů, nikoliv na úrovni vzájemného zpracování.

**Přidělení nákladů**

Používá se k přidělení zůstatku objektu nákladů do jiných objektů nákladů použitím základu přidělení. Aplikace Finance and Operations podporuje reciproční metodu přidělování. V metodě vzájemného přidělení jsou plně rozpoznány vzájemné služby, které si vyměňují pomocné objekty nákladů. Systém automaticky určí pořadí, ve kterém se bude provádět přidělení, a bude přes něj iterovat. Zůstatek objektu nákladů je přidělen jedním základem přidělení. Je podporováno přidělování napříč dimenzemi objektů nákladů a jejich příslušných členů. Pořadí přidělení je řízeno jednotkou řízení nákladů.

**Politika přidělování nákladů**

Zásady přidělování nákladů definují částky a množství, která musí být přiřazena. Pravidla přiřazování zahrnují pravidla přidělování zdrojů, které určují náklady, které jsou přiděleny, a pravidla cíle přidělení, které určují, které náklady jsou přidělovány. Například: Všechny náklady na služby v zařízení jsou zdrojem přidělení, který lze přidělit k různým oddělením v rámci společnosti (to znamená k cílům přidělení).

**Shrnutí nákladů**

Účelem pravidel shrnutí nákladů je agregování nákladů do smysluplných sad. Úroveň seskupení je definovaná uživatelem a zahrnuje přiřazení sekundární prvku nákladů. Pokud shrnutí nákladů nepoužíváte, každý prvek nákladů se přiděluje z jednoho objektu nákladů na jiný.

**Zásady nákladové sazby**

Nákladová sazba se používá k výpočtu ceny za objekt nákladů. Pro pochopení prvků ceny musíte definovat zásady nákladové sazby. Existují dva typy nákladové sazby: historická nákladová sazba a plánovaná nákladová sazba. Historické nákladová sazba je vypočítaná sazba, která se používá jako koeficient pro základ přidělení objektu nákladů. Sazba se počítá na základě přidělení nákladů v předchozím období. Plánovaná sazba je sazba definovaná uživatelem.

**Hierarchie dimenzí**

Existují dvě hierarchie dimenzí: kategorizační hierarchie a klasifikační hierarchie. Typ hierarchie kategorizace dimenze se používá pro účely vykazování. Podporuje pouze dimenze prvku nákladů. Typ hierarchie klasifikace dimenze se používá k definování zásad pro účely vykazování. Podporuje všechny dimenze, například objekty nákladů, prvky nákladů a statistické dimenze. 

**Datový konektor**

Nákladové účetnictví podporuje integraci dat ze zdrojových systémů prostřednictvím sady datových konektorů. K dispozici jsou následující datové konektory:

-  Importované transakce (předem nakonfigurované)
-  Dynamics 365 for Finance and Operations (předem nakonfigurované)
-  Dynamics AX (vyžaduje se konfigurace)

**Poznámka:** Datový konektor Importované transakce vychází z datových entit.

**Poskytovatel dat**

Většina zdrojových systémů může poskytovat data, která odpovídají jednomu nebo více datovým zdrojům v nákladovém účetnictví. Chcete-li sladit data ze zdrojových systémů s datovým zdrojem v nákladovém účetnictví, je třeba nakonfigurovat poskytovatele dat. V následující tabulce je uvedena dostupnost poskytovatelů dat podle datového konektoru a datového zdroje.

|  **Datové zdroje** |  **datový konektor Importované transakce** | **Datový konektor Dynamics 365 for Finance and Operations**  | **Datový konektor Dynamics AX**  |
|---|---|---|---|
| Členy dimenze prvku nákladů  |  Ano | Ano  | Ano  |
|  Členy dimenze objektu nákladů |  Ano | Ano  | Ano  |
|  Členy statistické dimenze | Ano  | Žádný  | Žádný  |
|  Hlavní kniha | Ano  | Ano  | Ano  |
|  Položky rozpočtu  | Ano  | Ano  | Ano  |
|  Statistická měření | Ano  | Ano  | Ano  |

**Vzorec**

Základy přidělení vzorce umožňují definovat rozšířené vzorce k dosažení správného základu přidělení. Základy přidělení vzorce lze vytvořit ručně. Chcete-li definovat svůj vzorec, můžete použít následující operátory.

|  **Symboly** | **Text**  |
|---|---|
|  ( ) | Závorky  |
|  < |  Menší než |
|  > |  Větší než |
|  + |  Dodatek |
|  – |  Odčítání |
| *  | Násobení  |

Tradiční výkazy IF nejsou podporovány. Můžete však vytvořit výkazy a ověřit, zda jsou pravdivé.

|  **Ověření výkazu** | **Výsledek**  |
|---|---|
|  a > b| True  |
|  a > b |  False |

**Režijní náklady**

Režijní náklady odkazují k probíhajícím výdajům na provozní náklady. Jde o náklady, které nelze přímo spojit s konkrétními obchodními aktivitami. Následuje několik příkladů režijních nákladů:

-   Účetní poplatky
-   Odpisy
-   Pojištění
-   Zájmy
-   Právní poplatky
-   Daně
-   Provozní náklady

**Výše režijních nákladů**

Výše jsou definovány podle objektu nákladů a prvku nákladů. Existují dva typy částky: fiskální období a specifikované uživatelem. Částky fiskálního období sazby se počítají podle výpočtu režijních nákladů. Částka specifikovaná uživatelem je definovaná uživatelem a lze ji použít pro přidělení nákladů mezi objekty nákladů s použitím předem určené sazby pro výpočet režijních nákladů

**Publikováno**

Pokud nastavíte toto pole na Ano, uživatel, kterému je přiřazena jedna z následujících rolí, může zobrazit sestavu v pracovním prostoru Řízení nákladů:

-  Správce nákladového účetnictví
-  Nákladový účetní
-  Úředník na pozici nákladového účetního
-  Kontrolor objektu nákladů

Pokud nastavíte toto pole na Ne, pouze uživatelé, kterým je přiřazena jedna z následujících rolí, může zobrazit sestavu v pracovním prostoru Řízení nákladů:

-  Správce nákladového účetnictví
-  Nákladový účetní
-  Úředník na pozici nákladového účetního

**Statistická dimenze**

Statistické dimenzí a jejich členy se používají pro registraci a kontrole nefinančních položek v nákladovém účetnictví. Členy statistické dimenze lze použít pro dva účely:

-  Jako základ pro přidělení v zásadách, jako je distribuce nebo přidělení nákladů.
-  Pro vykazování nefinanční spotřeby.

Statistická dimenze je výraz výpočtu nebo součtu aktivity a slouží jako základ pro přidělení nebo výpočty sazeb. Tvoří se buď ručně nebo se importuje ze zdrojového systému. Příklady statistických dimenzí zahrnují počet zaměstnanců, počet licencí softwaru na jednotlivých zařízení, spotřebu energie každého stroje nebo čtvereční metry nákladového střediska.

**Výkaz**

Výpisy jsou zobrazení pro vedoucí pracovníky, kteří odpovídají za řízení nákladů. Výkazy jsou definovány kontrolorem nákladů a poskytují rychlý přehled o skutečných nákladech, rozpočtovaných nákladech a odchylkách. Manažer může přejít na podrobnosti v případě potřeby. Ve snaze zajistit, aby vedoucí pracovníci viděli pouze data, za která jsou zodpovědní, podléhají data zobrazená ve výkazech přístupovým pravidlům.

**Verze**

Verze se používají k simulaci, zobrazení a porovnání různých výsledků. Standardně jsou zobrazeny všechny skutečné náklady v jedné základní verzi, která se nazývá *Skutečné*. U rozpočtů a výpočtů můžete pracovat s libovolným počtem verzí. Můžete například importovat data rozpočtu do původní verze a poté revidovat rozpočet v revidované verzi. V případě výpočtů můžete vytvořit více verzí. V těchto různých verzích pak můžete vytvářet výpočty pomocí různých pravidel výpočtu, která se budou používat pro přidělení nákladů.



