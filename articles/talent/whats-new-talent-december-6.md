---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Talent - Core HR (6. prosince 2018)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-12-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 462b87a655e3e4017cffd2ba41cb6d1f18de3e50
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529155"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-december-6-2018"></a>Co je nového nebo upraveného v aplikaci Dynamics 365 Talent - Core HR (6. prosince 2018)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**Sestavení 8.1.2071**

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Core HR.


## <a name="platform-update-22-for-finance-and-operations"></a>Aktualizace Platform 22 pro Finance and Operations

### <a name="export-up-to-1-million-rows-to-excel"></a>Export až 1 milionu řádků do aplikace Excel

Funkci Export do aplikace Excel lze nyní konfigurovat, aby uživatelům umožnila exportovat až 1 milion řádků z mřížky aplikace Talent. Jedná se o značný nárůst z předchozího limitu 10 000 řádku. 

### <a name="restyled-personalization-toolbar"></a>Upravený Panel nástrojů

Panel nástrojů byl upraven v rámci aktualizace Platform update 22 pro aplikaci Finance and Operations, aby uživatelům pomohl snadněji si přizpůsobit prostředí aplikace Talent. Byly provedeny tyto změny: 

-  Název každého nástroje přizpůsobení je nyní zobrazen s ikonou, která uživatelům pomáhá rychle rozpoznat nástroj, o který mají zájem.
-  Popis způsobu použití nástroje je odteď také zobrazen a pomáhá uživatelům pochopit, jak potřebné změny provést.  
-  Celý panel nástrojů přizpůsobení lze přesunout na obrazovce přetažením do konkrétní oblasti na levém panelu nástrojů. To umožňuje uživatelům přizpůsobit prvky, které byly dříve skryty panelem nástrojů.   

### <a name="optimized-is-one-of-filtering-experience"></a>Optimalizované filtrování "je jeden z“

Filtr "je jeden z“ lze použít pro většinu polí, když používáte podokno filtru a rozevírací seznamy záhlaví mřížky. Tento operátor umožňuje filtrovat pole podle vícera hodnot. Novinka operátoru "je jeden z" je k dispozici s aktualizací Platform update 22 pro aplikaci Finance and Operations. Pro více informací viz [Optimalizovaná možnost filtrování „je jeden z“](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/improved-isoneof-filtering).

### <a name="paste-lists-from-excel-into-filter-fields-with-the-is-one-of-operator"></a>Vkládání seznamů z Excelu do polí filtru s operátorem "je jeden z"

U některých úkolů mohou uživatelé pracovat se seznamem hodnot v Excelu, který si přejít použít k filtrování dat v aplikaci Talent. Například může uživatel lidských zdrojů identifikovat sadu zaměstnanců ze sestavy, kteří vyžadují další průzkum v systému a bylo by vhodné pro tohoto uživatele, aby bylo možné zkopírovat seznam přímo z Excelu do pole filtru v aplikaci Talent.

S aktualizací Platform update 22 pro aplikaci Finance and Operations nyní operátor „je jeden z“ v podokně filtru a sloupci mřížky filtrování nyní rozpozná seznamy zkopírované z aplikace Excel, aby je bylo možné přímo vložit do pole filtr. To zahrnuje řadu hodnot zkopírovaných z různých řádků a sloupců v Excelu. Další informace o této funkci naleznete v tématu [Vkládání seznamů z Excelu do polí filtru s operátorem "je jeden z"](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/paste-filter-lists-from-excel).

## <a name="in-preview"></a>Náhled

### <a name="configure-uk-payroll-integration-between-talent-and-dayforce"></a>Konfigurace integrace mezd UK mezi aplikacemi Talent a Dayforce

Integrace aplikace Talent a Ceridian Dayforce je k dispozici v náhledu pro Velkou Británii. Další informace naleznete v tématu [konfigurovat integraci mezd mezi aplikacemi Talent a Dayforce](https://docs.microsoft.com/dynamics365/unified-operations/talent/configure-payroll-integration).

## <a name="coming-soon"></a>Již brzy

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a>Dovolená a absence: budoucí volno a prognózy volna

Se změnami, kteeré zaměstnancům umožňují předpovídat dobu volna a požaddat žádosti u boudcí volno, aniž by došlo k ovlivnění stávajících rozložení volna, se mění také způsob zobrazení rozložení volna. 

Dostupný zůstatek, který je aktuálně zobrazen, je množství volna dostupného pro žádosti, včetně nárůstů během dne a všech schválených žádostí o volno do konce období. 

Jakmile bude možné předpovídat, zobrazený zůstatek se změní na aktuální zůstatek volna, včetně nárůstu během dne a žádostí během dne. Zaměstnanci a řídící pracovníci uvidí tyto aktualizované rozložení volna na kartě **Pracovní volno** karty a v okně **Rozložení volna**. Manažeři HR uvidí tyto aktualizované zůstatky v pracovní prostoru **Lidé** a v okně **Přiřazené plány volna** zaměstance.

## <a name="other-changes"></a>Další změny 

### <a name="termination-code-is-not-populated-to-the-worker-position-assignment-record"></a>Kód ukončení není vyplněn do záznamu přiřazení pozice pracovníka

Byla provedena změna, která vyplní kód důvodu v záznamu přiřazení pozice během procesu ukončení pracovního poměru.

### <a name="validation-for-personnel-number-being-in-use-needs-additional-details"></a>Ověření používaného osobního čísla potřebuje dodatečné informace

Další informace se zobrazí , když se používají číselné řady, abyste lépe pochopili problémy, když není možné vygenerovat nové číslo.
 
### <a name="attachments-buttons-not-available-for-workers"></a>Tlačítka příloh nejsou pro pracovníky k dispozici

Za účelem nápravy příloh byly provedeny změny. Při přidávání nové přílohy k pracovníkovi jsou nyní k dispozici tlačítka **Nová** a **Upravit**, když jsou v okně pracovníka otevřena okna s fakty. 

## <a name="known-issues"></a>Známé problémy

### <a name="mapping-errors-in-the-integration-with-finance"></a>Chyby mapování integrace s aplikací Finance

Byly zjištěny následující chyby v aktuální šabloně pro integraci aplikace Talent s aplikací Finance. Nová šablona bude publikována brzy a bude použita pro všechny nové integrace projektů, které jsou vytvořeny. Pro existující integrace projektů lze mapování úkolu aktualizovat. Aktualizované mapování naleznete v následující tabulce. 

>[!NOTE]
> Úkol Pracovní pozice do  přiřazení práce nadřazené pozice neintegruje data. Toto je problém, který je právě zkoumán. Aktuální mapování nelze nijak obejít. 

Úkol oddělení do provozní jednotky vyžaduje aktualizaci následujících mapování.

| Stávající pole zdroje          | Pole nového zdroje |
| -------------------------------|------------------|
| cdm_description (popis)  | cdm_name (název)  |

Také je třeba přidat další mapování. Vyberte poslední pole **Žádná** pro přidání následujícího mapování.

| Zdrojové pole                   | Cílové pole    |
| -------------------------------|----------------------|
| cdm_description (popis)  | NAMEALIAS (NAMEALIAS)|

Aktualizované mapování by mělo vypadat takto.

![Úkol oddělení do operačních jednotek](./media/DepartmentMapping.png)


Úkol úloh do podrobnosti úlohy vyžaduje aktualizaci následujících mapování.

| Stávající pole zdroje          | Pole nového zdroje                   |
| -------------------------------|------------------------------------|
| cdm_name (název)                | cdm_description (popis)      |
| cdm_name (popis)         | cdm_description (popis práce)|


Aktualizované mapování by mělo vypadat takto.

![Úkol úloh do podrobnosti úlohy](./media/JobMapping.png)

Úkol pracovníci do práce vyžaduje aktualizaci následujících mapování.

| Stávající pole zdroje                 | Pole nového zdroje                               |
| --------------------------------------|------------------------------------------------|
| cdm_emailaddress1 (e-mailová adresa 1)   | cdm_primaryemailaddress (primární e-mailová adresa |
| cdm_telephone1 (telefon 1)          | cdm_primarytelephone (primární telefon)       |

Transformace pole pohlaví je rovněž třeba aktualizovat. Vyberte typ mapy **fn** (funkce) pro pohlaví a aktualizujte následující mapování hodnot.

| Hodnota Common Data Service   | Hodnota Finance and Operations | | ------------|------------------ -----------| | 75440000    | Muž                         | | 75440001    | Žena                       | | 75440002    | Není                         | | 75440003    | Nezadáno                  |

Aktualizované mapování by mělo vypadat takto.

![Úkol pracovníci pracovníkovi](./media/WorkerMapping.png)

![Transformace pole pohlaví](./media/WorkerTransform.png)

