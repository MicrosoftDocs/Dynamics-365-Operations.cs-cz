---
title: "Terminologie týkající se účtování nákladů"
description: "Toto téma definuje klíčové podmínky, které se používají v nákladovém účetnictví."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostControlWorkspace, CAMCostControlWorkspaceConfiguration
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 223114
ms.assetid: 1c798592-77d0-4a8f-beaa-9159c75957da
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 1f12e8e82430c79ee93f2284e5fdf47ac559525d
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---

# <a name="cost-accounting-terminology"></a>Terminologie týkající se účtování nákladů

[!include[banner](../includes/banner.md)]


Toto téma definuje klíčové podmínky, které se používají v nákladovém účetnictví.

**Nákladové účetnictví**

Nákladového účetnictví vám umožnuje shromažďovat data z různých zdrojů, jako jsou například hlavní knihy, dílčí knihy, rozpočty a statistické údaje. Pak můžete analyzovat, shrnout a vyhodnocení nákladová data, aby vedení mohlo přijmout nejlepší možná rozhodnutí v oblasti aktualizací cen, rozpočtů, řízení nákladů apod. Zdrojová data, která jsou použita k analýze nákladů, se zpracovávají nezávisle na nákladovém účetnictví. Aktualizace v nákladovém účetnictví tedy zdrojová data neovlivňují. Nicméně při shromažďování nákladových dat z různých zdrojů a zejména, pokud importujete hlavní účty z hlavní knihy v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise edition jako prvky nákladů, dochází k redundanci dat, protože stejná data existují v hlavní knize i v nákladovém účetnictví. Tato redundance je ale žádoucí, protože finanční správu využíváte k externímu vykazování a nákladového účetnictví pro interní vykazování.

**Hlavní kniha nákladového účetnictví**

Hlavní knihy nákladového účetnictví je specializovaná platforma, která určuje způsob, jakým se zadávají procesy, hodnoty a množství, a jak se zobrazují v konkrétní oblasti nákladového účetnictví. Hlavní knihy nákladového účetnictví definují procesy a pravidla pro měření nákladů na objekty nákladů. Zpracovávají transakce nákladů a spravují dokumenty, které zaznamenávají změny v hodnotách a množstvích, která transakce nákladů produkují.

**Záznam nákladů**

Položky nákladů jsou výsledkem převodu prostřednictvím datových konektorů z položek hlavní knihy, přidělení nákladů a zaúčtovaných položek nákladů v denících nákladů.

**Objekt nákladů**

Objekty nákladů jsou všechny objekty, k nimž jsou přiděleny náklady. Zde uvádíme některé typické objekty nákladů:

-   Produkty
-   Projekty
-   Zdroje
-   Oddělení
-   Nákladová střediska
-   Zeměpisné oblasti.

Vedení používá objekty nákladů, aby mohlo kvantifikovat náklady, ale také provést analýzu ziskovosti.

**Prvek nákladů**

Prvky nákladů se používají jako funkce ke sledování a kategorizaci toku nákladů. Existují dva typy prvků nákladů: primární a sekundární náklady. **Primární náklady** Prvky primárních nákladů představují tok nákladů z finančního účetnictví do nákladového účetnictví. Struktura prvku nákladů odpovídá ziskům a ztrátám účetní struktury v hlavní knize, kde prvek nákladů může odpovídat hlavnímu účtu. Ne všechny hlavní účty ale musejí být prezentovány jako prvky nákladů závisející na obchodních požadavcích. Zde je několik příkladů primárních prvků nákladů:

-   Náklady prodaného zboží
-   Nepřímé náklady na materiál
-   Osobní náklady
-   Náklady na energii

**Prvek druhotných nákladů** 

Sekundární prvky nákladů představují interní tok nákladů, protože tyto náklady vznikají a používají se pouze v nákladovém účetnictví. Sekundární prvky nákladů pomáhají zajistit, že lze sledovat zdroje nákladů. Tyto prvky nákladů se používají při přidělování nákladů a výpočtech režijních nákladů. Zde je několik příkladů sekundárních prvků nákladů:

-   Výrobní náklady
-   Výroba, materiál a režie marketingu

**Jednotka řízení nákladů**

Jednotka řízení nákladů představuje strukturu nákladů. Ta musí být přidružena k dimenzím nákladů objektu v nákladovém účetnictví hlavní knihy.

**Verze**

Verze se používají k simulaci, zobrazení a porovnání různých výsledků. Standardně jsou zobrazeny všechny skutečné náklady v jedné základní verzi, která se nazývá *Skutečné*. U rozpočtů a výpočtů můžete pracovat s libovolným počtem verzí. Můžete například importovat data rozpočtu do původní verze a poté revidovat rozpočet v revidované verzi. V případě výpočtů můžete vytvořit více verzí. V těchto různých verzích pak můžete vytvářet výpočty pomocí různých pravidel výpočtu, která se budou používat pro přidělení nákladů.

**Výkaz**

Výpisy jsou zobrazení pro vedoucí pracovníky, kteří odpovídají za řízení nákladů. Výkazy jsou definovány kontrolorem nákladů a poskytují rychlý přehled o skutečných a rozpočtovaných nákladech, včetně odchylek a verzí výpočtů. Ve snaze zajistit, aby vedoucí pracovníci viděli pouze data, za která jsou zodpovědní, podléhají data zobrazená ve výkazech přístupovým pravidlům.

**Datový konektor**

Data lze importovat do nákladového účetnictví z externích systémů prostřednictvím datových konektorů. Můžete například importovat účetní struktury, dimenze a položky hlavní knihy nebo položky rozpočtu. Pro import dat a vytváření datových připojení můžete použít konektory přednastavených dat nebo vlastní konektory.

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

**Režijní náklady**

Režijní náklady odkazují k probíhajícím výdajům na provozní náklady. Jde o náklady, které nelze přímo spojit s konkrétními obchodními aktivitami. Následuje několik příkladů režijních nákladů:

-   Účetní poplatky
-   Odpisy
-   Pojištění
-   Zájmy
-   Právní poplatky
-   Daně
-   Provozní náklady

**Distribuce nákladů**

Distribuce nákladů se používá k rozdělení nákladů z jednoho objektu nákladů na jeden nebo více dalších objektů nákladů použitím příslušného základu přidělení. Distribuce nákladů a přidělení nákladů se liší v tom, že k distribuci nákladů dochází vždy na úrovni primárního prvku nákladů původních nákladů.

**Přidělování nákladů**

Přidělení se používá k přidělení zůstatku objektu nákladů do jiných objektů nákladů použitím základu přidělení. Aplikace Finance and Operations podporuje reciproční metodu přidělování. V metodě vzájemného přidělení jsou plně rozpoznány vzájemné služby, které si vyměňují pomocné objekty nákladů. Systém automaticky určí provádění přidělení ve správném pořadí. Zůstatek objektu nákladů je přidělen jedním základem přidělení. Je podporováno přidělování napříč dimenzemi objektů nákladů a jejich příslušných členů. Pořadí přidělení je řízeno jednotkou řízení nákladů.

**Politika přidělování nákladů**

Zásady přidělování nákladů definují částky a množství, která musí být přiřazena. Pravidla přiřazování zahrnují pravidla přidělování zdrojů, které určují náklady, které jsou přiděleny, a pravidla cíle přidělení, které určují, které náklady jsou přidělovány. Například: Všechny náklady na služby v zařízení jsou zdrojem přidělení, který lze přidělit k různým oddělením v rámci společnosti (to znamená k cílům přidělení).

**Základ přidělení**

Základ přidělení je báze, kterou lze použít na měření a kvantifikování činností. Jde například o použité strojohodiny, spotřebované kilowatthodiny, přímé odpracované hodiny nebo obsazenou plochu. Používá se pro přidělení nákladů k jednomu nebo několika objektům nákladů.

**Zásady přidělení**

Jedním z principů přidělování je přidělování nákladů podle nákladové sazby. Můžete přidělit náklady pomocí stávající nebo historické sazby. Přidělení, které využívá reciproční metodu pomáhá zajistit, že základ přidělení je určován řadou simultánních rovnic před samotným přidělením za využití aktuální sazby.

**Shrnutí nákladů**

Cílem shrnutí nákladů je zahrnout všechny náklady pro daný objekt nákladů. Úroveň seskupení je definována uživatelem. Pomocí shrnutí nákladů můžete seskupit prvky nákladů, které musí být přiděleny od jednoho objektu nákladů k jinému. Pokud shrnutí nákladů nepoužíváte, každý jednotlivý prvek nákladů se přiděluje z jednoho objektu nákladů na jiný.

**Zásady nákladové sazby**

Nákladová sazba se používá k výpočtu ceny za objekt nákladů. Pro pochopení prvků ceny musíte definovat zásady nákladové sazby. Existují dva typy nákladové sazby: historická nákladová sazba a plánovaná nákladová sazba. Historické nákladová sazba je vypočítaná sazba, která se používá jako koeficient pro základ přidělení objektu nákladů. Sazba se počítá na základě přidělení nákladů v předchozím období. Plánovaná sazba je sazba definovaná uživatelem.

**Hierarchie dimenzí**

Hierarchie dimenzí se používají jako výkazové struktury, kde můžete definovat pravidla pro přidělení, nákladové sazby a shrnutí nákladů, zobrazení výkazů nebo dat v aplikaci Microsoft Excel a definovat přístup k souhrnným údajům. Existují dvě hierarchie dimenzí: kategorizační hierarchie a klasifikační hierarchie. Kategorizační hierarchie je definována na základě prvků nákladů, klasifikační hierarchie je zase definována na základě objektů nákladů.

**Statistická dimenze**

Statistická dimenze je výraz výpočtu nebo součtu objektu a slouží jako základ pro přidělení nebo výpočty nákladových sazeb. Tvoří se buď ručně nebo se importuje ze zdrojového systému. Příklady statistických dimenzí zahrnují počet zaměstnanců, počet licencí softwaru na jednotlivých zařízení, spotřebu energie každého stroje nebo čtvereční metry nákladového střediska.

**Statistická položka**

Statistické položky nesou zaznamenaný součet nebo účetní hodnotu dané statistické dimenze. Zaznamenaný součet nebo účetní hodnota se také označuje jako hodnota.




