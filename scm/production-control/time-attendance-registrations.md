---
title: "Registrace času a docházky"
description: "Pracovníci z oblasti registrace času mohou zadat různé typy registrace pracovní doby, například registraci příchodu, odchodu, registraci nepřímých aktivit a registraci absencí. Tento článek popisuje registrace, jejich výpočet, schválení a použití workflowu pro přidání struktury a automatického schválení pro proces schválení časových rozvrhů."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmWorker, JmgCalcApprovePickDialog, JmgGroupApprove, JmgGroupCalc, JmgGroupSigningTable, JmgRegistration, JmgTimeCalcParmeters, WorkflowTableListPageRnr
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53351
ms.assetid: 885b0cdf-53d7-4cb4-92fe-da1b9e32b39f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 12193e4c266abc7bf0349ba9a78dbbbd9d00938d
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="time-and-attendance-registration"></a>Registrace času a docházky

[!include[banner](../includes/banner.md)]


Pracovníci z oblasti registrace času mohou zadat různé typy registrace pracovní doby, například registraci příchodu, odchodu, registraci nepřímých aktivit a registraci absencí. Tento článek popisuje registrace, jejich výpočet, schválení a použití workflowu pro přidání struktury a automatického schválení pro proces schválení časových rozvrhů. 

<a name="registrations"></a>Registrace
-------------

Ve společnostech, které používají modul Čas a docházka, musí zaměstnanci zaregistrovat čas, který stráví v práci, a také jejich docházky. Některé společnosti mohou vyžadovat od zaměstnanců jen registraci časů příchodu a odchodu. V jiných společnostech může být také od zaměstnanců vyžadována registrace využití času na vlastních aktivitách, které vykonávají, a také registrace přestávek. Předpokládaní uživatelé modulu Čas a docházka:
-   Zaměstnanci, kteří musejí registrovat čas a docházku v pravidelných intervalech, například denně, týdně nebo čtrnáctidenně.
-   Nadřízení pracovníci, vedoucí a mzdoví účetní, kteří počítají, schvalují a převádějí registrace pracovníků k dalšímu zpracování.

| **Poznámka**                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pokud používáte modul Čas a docházka spolu s modulem Provádění výroby, všechny registrace pro uzly projektů, projektových aktivit, nepřímé činnosti, absence, přesčasu a pružného času budou zaznamenány a použity k výpočtu mzdy v obou modulech. |

## <a name="time-registrations-workers"></a> Pracovníci s registrací času
Aby bylo možné zaznamenávat čas a absenci, pracovníci musí být nastavení jako pracovníci s registrací pracovní doby ve společnosti, ve které pracují.

Po nastavení mohou pracovníci zadat různé typy registrací.

-   Příchod a odchod při příchodu nebo odchodu.
-   Čas a spotřeba položek ve výrobních úlohách.
-   Čas strávený u stroje na dílně, byl-li stroj definován jako prostředek.

| **Poznámka**                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Zaměstnanci mohou být automaticky přiřazeny časové registrace, které jsou provedené u určitého stroje na dílně, pokud se tento pracovník rozhodne pracovat jako asistent u stroje, když zahájí výrobní úlohu. |

-   Registrace času pro projekty a aktivity projektu.
-   Registrace poplatků projektu a spotřeby položky prostřednictvím příslušných deníků poplatků projektu a deníků položek projektu.
-   Plánovaná absence.
-   Absence při pozdním příchodu do práce nebo odchodu z práce dříve, než bylo v plánu.
-   Pracovní přestávky, registrovány ručně nebo automaticky vypočtené systémem.
-   Nepřímé činnosti, které jsou neproduktivními aktivitami, které může pracovník provádět během pracovního dne. Mezi tyto činnosti může patřit schůzka nebo čištění pracovního prostoru.
-   Přesčas, který lze registrovat jako hodiny navíc, pružnou pracovní dobou nebo přesčas.

## <a name="adding-clockout-registrations"></a>Přidání registrací odchodů
Pokud se pracovník zapomene odhlásit na konci pracovního dne, lze přidat chybějící registraci spuštěním dávkové úlohy. Systém porovná čas příchodu a odchodu čas podle přidruženého profilu pracovníka a automaticky vloží chybějící registraci odchodu v souladu s koncovým časem v profilu. Registrace příchodu a odchodu jsou důležité pro následující výpočet a schválení registrací času před jejich přenesením do mzdového systému.

## <a name="calculating-registrations"></a>Výpočet registrací
Je-li pracovníkovi s registrací přiřazena skupina výpočtu, které se obvykle týká určitého týmu, směny nebo pracovní skupiny. Vedoucí týmu nebo nadřízený obvykle ověří registrace provedené zaměstnanci a tím pádem odpovědnou osobou za spuštění každodenní kalkulace pro příslušné skupiny výpočtu. V rámci procesu výpočtu může vedoucí týmu nebo nadřízený provádět tyto činnosti:
-   Oprava chybných registrací Například může změnit přepínací kódy a upravit zpětné vazby u výrobních úloh.
-   Přidání chybějících registrací Například může vytvořit registrace odchodu a vytvořit transakce absencí.
-   Odstranění nesprávných registrací

Vzhledem k tomu, že registrovaný čas musí odpovídat profilu doby pracovníka před výpočtem registrací, je nutné přepsat profil pracovní doby pro každého pracovníka, který má výjimku z profilu standardní pracovní doby. V případě, kdy je profil pracovníka denní směna a pracovník souhlasil s prací v noční směnu bez zaplacení přesčasu, musí vedoucí týmu nebo nadřízený přepsat výchozí profil pracovníka, aby bylo možné provést výpočet pracovní doby se standardní noční sazbou a nikoli jako přesčas. Ve výpočtu se zobrazí chyba při chybějící registraci absence. Před dokončením výpočtu je třeba ji přidat.

## <a name="approving-registrations"></a>Schvalování registrací
Stejným způsobem, jakým přiřadíte skupinu výpočtu k pracovníkovi s registrací času, musíte přiřadit také skupinu schválení. Skupina je obvykle specifická pro tým, směnu nebo pracovní skupinu. Musíte schválit registrace času, které byly vypočteny správně (to znamená provádění výpočtů bez chyb), před generováním mzdových položek, které lze poté převést do mzdového systému. Správce mezd bude obvykle schvalovat registrace a před schválením může provést tyto činnosti:
-   Přepsání platební dohody pro jednotlivé pracovníky
-   Přidání ručních prémií
-   Zadání dalších informací o registracích absence

| **Poznámka**                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Jestliže byl pro určité zaměstnance vypočítán přesčas, lze jej přidělit ke specifickým úkolům během dne. Toto je relevantní, pokud se náklady pozice počítají na základě mzdy pracovníka. |

## <a name="approving-registrations-using-workflow"></a> Schvalování registrací pomocí workflowu
Můžete nastavit proces schválení workflowu, který automaticky schvaluje registrace vyhovující pravidlům workflowu s tím, že pouze odchylky budou zpracovány ručně. Pokud je aktivováno schválení workflowu, odešle vedoucí týmu nebo nadřízený vypočítané registrace ke schválení. Proces workflowu vygeneruje odpovídající schválení a úlohy a potom je přiřadí správným uživatelům a rolím, jak je uvedeno v rámci workflowu. Pro modul Čas a docházka jsou k dispozici dvě schválení workflowu.

| Workflow                                  | Účel                                                                                                   | Typ registrace                                                                                                                                                                                                                                     |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Celkový čas a dny docházky            | Workflow ověří registrace například oproti očekávanému počtu pracovních hodin za den. |                                                                                                                                                                                                                                                       |
| Registrace deníku času a docházky | Workflow ověří každý typ registrace pro datum registrace.                           | Čas a docházka • Odchod • Příchodu • Absence • Přestávka • Přepínací kód • Projekt • Aktivita projektu • Výrobní úlohy (nepřímá aktivita) • Čekání před operací • Nastavení • Proces • Překrytí • Přeprava • Čekání po operaci • Zahájit asistenci • Ukončit asistenci |

 

## <a name="transferring-approved-registrations"></a>Převedení schválených registrací
Po schválení registrací je lze převést do pravidelné mzdové úlohy. Převedená registrace je zaúčtována v aktivitě nebo úloze, která se týká například výrobní zakázky nebo projektu. Mzdové transakce jsou generovány pro každého podle registrací.  

## <a name="reversing-transferred-registrations"></a>Stornování převedených registrací
Úkol stornování transakcí (jejich vrácení) lze provést až do okamžiku, kdy bude spuštěn platební převod mzdového období. To znamená, že mzdová data byla převedena do externího souboru. Při stornování jsou všechny registrace staženy a veškeré transakce, které jsou zaúčtovány u výrobních zakázek nebo projektů, jsou vyrovnány a vynulovány.

| **Poznámka**                                                 |
|----------------------------------------------------------|
| Externí soubor lze importovat do mzdového systému. |

## <a name="registrations-in-electronic-timecards"></a>Registrace na elektronických kartách docházky
Zaměstnanci s pracovními úkoly, které nevyžadují okamžitou zpětnou vazbu, jak je tomu u výrobních úloh, kteří ale pracují na aktivitách projektu, mohou využívat elektronické karty docházky. S elektronickými kartami docházky získáte flexibilitu zadávání registrací kdykoliv a nejvhodněji podle obchodního plánu – denně, týdně nebo při návratu pracovníka do kanceláře poté, co byl pryč. Chcete-li využívat elektronické karty docházky nebo tyto pracovníky, ve formuláři podrobností pracovníka je nutné nastavit možnost Použít kartu docházky. Elektronické karty docházky umožňují pracovníkovi registraci těchto dat:

-   Datum
-   Typ registrace
-   Odkaz úlohy, například projekt, nepřímá aktivita nebo výrobní zakázka
-   Identifikace úlohy
-   Spotřeba času
-   Poplatky projektu
-   Položky projektu





