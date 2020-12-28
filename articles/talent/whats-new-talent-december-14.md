---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Talent - Core HR (14. prosince 2018)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 12/14/2018
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
ms.search.validFrom: 2018-12-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 9887d22a513e820c35c51b6c702e2d9d34ab1214
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529749"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-december-14-2018"></a>Co je nového nebo upraveného v aplikaci Dynamics 365 Talent - Core HR (14. prosince 2018)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**Sestavení 8.1.2085**

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Core HR.

## <a name="changes"></a>Změny

### <a name="us---aca-affordable-care-act-support-for-tax-year-2018-1095-b-and-1095-c-forms"></a>US - ACA (Provedení dostupné péče) podpora daňového roku 2018 1095-B a formulářů 1095-C

Každý rok musí příslušní velcí zaměstnavatelů poskytovat každému zaměstnanci na plný úvazek formulář 1095-C. Dále, pokud zaměstnavatel poskytuje vlastní pojistné krytí, musí zaměstnanci (na plný či částečný úvazek), který je krytý jedním ze zdravotních plánů zaměstnance, poskytnout formulář 1095-C (pokud se jedná o příslušného velkého zaměstnavatele) a formulář 1095-B (pokud se jedná o malé zaměstnavatele). Tato funkce poskytuje vytisknutelné formuláře 1095-C i 1095-B.

### <a name="during-import-submittedbypersonid-field-on-hcmperfjournalentity-is-ignored"></a>Při importu pole SubmittedByPersonId na HcmPerfJournalEntity je ignorováno

Při importu/exportu výkonu záznamů v deníku je pole **odeslal** ignorováno. Touto změnou hodnota **import a export** představuje hodnotu, která v tabulce během exportu při importu systému bude aktualizována o hodnotu zadanou v importovaném souboru.

### <a name="analytics-tab-on-leave-and-absence-workspace-displays-openconnectionerror-error-for-non-system-admin-roles"></a>Analytika v pracovním prostoru 'Volna a absence' zobrazuje chybu "OpenConnectionError" pro role správce, které nejsou systémové

S touto aktualizací nebudou při otevírání záložky **Analýza** v pracovním prostoru **Dovolená a absence** zobrazeny žádné chyby.

### <a name="employee-self-service-position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a>Samoobsluha pro zaměstnance, rozbalení hierarchie pozic ze selhání dlaždic za účelem získání nadřazeného uzlu

Byla provedena změna opravy chyby "Získání nadřazeného uzlu se nezdařilo", když došlo k úpravě hierarchie pozice, aby s zobrazila ve stávajícím praocvním prostoru a pozice je vybrána v hierarchii.  

### <a name="must-be-system-admin-to-see-the-payroll-tab-in-the-position-page"></a>Musí být správce systému,a by na stránce Pozice bylo možné zobrazit záložku Mzda

Byla provedena změna, která má zahrnout správné bezpečnostní prvky do stávajícího právnění: "Udržovat podrobnosti mezd a pozice pracovníka". Touto změnou standardně Správce mezd bude mít přístup k polím mezd na stránce pozice.

### <a name="error-when-submitting-performance-review-to-manager-and-the-reviewsperfperiod-placeholder-is-used-in-the-submission-instructions"></a>Došlo k chybě při odeslání kontroly výkonu vedoucímu pracovníkovi a v pokynech odeslání je použit zástupný znak %Reviews.PerfPeriod%

Byla provedena změny, která opravuje chybu "Odkaz s hodnotou null" při použití zástupného textu %Reviews.PerfPeriod% v pokynech odeslání.

### <a name="workforce-power-bi-report-shows-error-when-worker-seniority-date-is-a-leap-day"></a>Výkaz pracovní síly Power BI zobrazuje chybu, když je datum mzdového služebního věku v přestupný den

Touto změnou jsou nyní v Power BI podporovány přestupné dny.

### <a name="integration-between-core-hr-and-attract"></a>Integrace mezi aplikacemi Core HR a Attract

Byla provedena změna, která má aktualizovat integraci mezi aplikacemi Core HR a Attract související s nabíranými uchazeči. Aby nabíraní kandidáti byli vidět v pracovním prostoru **Správa zaměstnanců**, jsou použity následující entity Common Data Service:

Žádost o práci
- Stav důvodů je třeba nastavit na přijetí nabídky
-   Poskytuje kandidát a pracovní místo

Kandidát
-   Poskytuje informace o kandidátovi

Volné pracovní místo
-   Poskytuje ID volné pozice a účastníky volné pracovní pozice

Účastníci volné pracovní pozice
-   Uvádí náborového manažera

Když je kandidát přidán do Správy zaměstnanců, může být zamítnut pomocí nové možnosti dostupné na kartě kandidáta.

## <a name="coming-soon"></a>Již brzy

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a>Dovolená a absence: budoucí volno a prognózy volna

Se změnami, které zaměstnancům umožňují předpovídat dobu volna a požaddat žádosti u boudcí volno, aniž by došlo k ovlivnění stávajících rozložení volna, se mění také způsob zobrazení rozložení volna. 

Dostupný zůstatek, který je aktuálně zobrazen, je množství volna dostupného pro žádosti, včetně nárůstů během dne a všech schválených žádostí o volno do konce období. 

Jakmile bude možné předpovídat, zobrazený zůstatek se změní na aktuální zůstatek volna, včetně nárůstu během dne a žádostí během dne. Zaměstnanci a řídící pracovníci uvidí tyto aktualizované rozložení volna na kartě **Pracovní volno** karty a v okně **Rozložení volna**. Manažeři HR uvidí tyto aktualizované zůstatky v pracovní prostoru **Lidé** a v okně **Přiřazené plány volna** zaměstance.

## <a name="known-issue"></a>Známý problém

### <a name="mapping-errors-in-the-integration-with-finance"></a>Chyby mapování integrace s aplikací Finance

Byly zjištěny následující chyby v aktuální šabloně pro integraci aplikace Talent s aplikací Dynamics 365 Finance. Nová šablona bude publikována brzy a bude použita pro všechny nové integrace projektů, které jsou vytvořeny. Pro existující integrace projektů lze mapování úkolu aktualizovat. Aktualizované mapování naleznete v následující tabulce. 

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

Aktualizované mapování by mělo vypadat jako následující obrázek.

![Úkol oddělení do operačních jednotek](./media/DepartmentMapping.png)


Úkol úloh do podrobnosti úlohy vyžaduje aktualizaci následujících mapování.

| Stávající pole zdroje          | Pole nového zdroje                   |
| -------------------------------|------------------------------------|
| cdm_name (název)                | cdm_description (popis)      |
| cdm_name (popis)         | cdm_description (popis práce)|


Aktualizované mapování by mělo vypadat jako obrázek níže.

![Úkol úloh do podrobnosti úlohy](./media/JobMapping.png)

Úkol pracovníci do práce vyžaduje aktualizaci následujících mapování.

| Stávající pole zdroje                 | Pole nového zdroje                               |
| --------------------------------------|------------------------------------------------|
| cdm_emailaddress1 (e-mailová adresa 1)   | cdm_primaryemailaddress (primární e-mailová adresa |
| cdm_telephone1 (telefon 1)          | cdm_primarytelephone (primární telefon)       |

Transformace pole pohlaví je rovněž třeba aktualizovat. Vyberte typ mapy **fn** (funkce) pro pohlaví a aktualizujte následující mapování hodnot.

| Hodnota Common Data Service                   | Hodnota Finance and Operations                     |
| ----------------------------|--------------------------------------------------|
| 75440000                    | Muž                                             |
| 75440001                    | Žena                                           |
| 75440002                    | Není                                             | 
| 75440003                    | Nespecifické                                      |

Aktualizované mapování by mělo vypadat jako následující obrázky.

![Úkol pracovníci pracovníkovi](./media/WorkerMapping.png)

![Transformace pole pohlaví](./media/WorkerTransform.png)
