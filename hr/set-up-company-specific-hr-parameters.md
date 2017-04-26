---
title: "Nastavení parametrů lidských zdrojů pro konkrétní společnost"
description: "Nastavení některých parametrů lidských zdrojů nesmí být sdílena napříč společnostmi, zatímco nastavení jiných parametrů jsou specifické pro společnost. Tento článek vysvětluje, jak nastavit parametry lidských zdrojů specifické pro společnost."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HRMParameters
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: aaf5c93a1ac71de27338c13218407616808ee001
ms.openlocfilehash: 39f2904a6b722ad0048ba1d94651098ee642079b
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-company-specific-hr-parameters"></a>Nastavení parametrů lidských zdrojů pro konkrétní společnost

[!include[banner](includes/banner.md)]


Nastavení některých parametrů lidských zdrojů nesmí být sdílena napříč společnostmi, zatímco nastavení jiných parametrů jsou specifické pro společnost. Tento článek vysvětluje, jak nastavit parametry lidských zdrojů specifické pro společnost.

Dvě stránky slouží k nastavení parametrů lidských zdrojů. Pro parametry, které jsou sdíleny napříč společnostmi, použijte stránku **Sdílené parametry lidských zdrojů**. Pro parametry, které jsou specifické pro společnost (jinými slovy nastavení se použije pro jednu společnost), můžete použít stránku **Parametry lidských zdrojů**. Na stránce **Parametry lidských zdrojů** jsou nastavení rozdělena mezi šest karet:

-   Obecné
-   Nábor
-   Kompenzace
-   Číselné řady
-   Opuštění z rodinných a lékařských důvodu (FMLA)
-   Samoobsluha pro zaměstnance

Každá karta obsahuje informace, které se vztahují na jednu společnost. Nastavení kartě **Obecné** určuje vzhled informací o absencích, zraněních a onemocněních a nově přijatých zaměstnancích. Nastavení na této kartě také definují některé výchozí položky, které se zobrazí při práci. Konkrétně tato karta vás nechá vybrat barvu, která má být použita při otevření transakcí absencí, určit šablonu stylů, která má být použita pro sestavy, dále určit, zda mají být aktivována integrace mezi vzdělávacími kurzy a registrací absence, a vyberte kód absence, který má být použit při řízení této integrace. Můžete také určit, jak dlouho mají být zachovány případy zranění a onemocnění, a určit výchozí číslo identifikace, které se zobrazí při přijetí nového pracovníka. 

Nastavení na kartě **Nábor** definuje typy dokumentů, které se používají pro korespondence, která bude automaticky zaslána uchazečům a náborovému projektu použitému pro nevyžádané přihlášky (přihlášky, které nejsou určeny pro daný náborový projekt). Období definované pro náborový projekt časově určuje náborové projekty, které jsou zahrnuty na dlaždici **Časové projekty** v pracovním prostoru **Řízení náboru**. Období, které je definováno pro upozornění na termín přihlášky slouží k zobrazení náborových projektů, kterým se blíží jejich konečný termín přihlášky na dlaždici **Blíží se termín přihlášky** v pracovním prostoru **Nábor**. 

Nastavení **kompenzace** karta, definovat, zda uživatelé musí potvrzovat, že chtějí uložit informace pro plán fixní nebo variabilní kompenzace. Vyberete-li **povolit uložit ověření** políčko, kdykoli uživatele, aby zavřeli kompenzace související stránky, obdrží zprávu s dotazem, zda chtějí uložit záznam. Některé stránky v řízení kompenzace Nenechte uživatelům odstranit informace. Vyzváním uživatelů k ověření, zda chtějí informace ukládat, budete schopni omezit informace, které jsou ukládány, a později nejdou odstranit. Pokud je zrušeno zaškrtnutí políčka **Povolit ověření ukládání**, záznamy budou vždy okamžitě uloženy případně již předtím, než je uživatel hotov. Pokud používáte funkci řízení výkonnosti, můžete na kartě **Kompenzace** vybrat model hodnocení, který má být použit namísto modelu přiřazeného k plánům kompenzace při hodnocení výkonnosti. 

Nastavení na kartě **Číselná řada** určují sekvence, které lze použít k automatickému přiřazení identifikátorů k položkám v modulu Lidské zdroje, například přihlášky, záznamy o absenci, výsledky procesu kompenzace, čísla případů, kurzy a agendy kurzů. Chcete-li zachovat číselné kódy a pořadí odkazů, použijte **číselné řady** stránku seznamu (klepněte na tlačítko **Správa organizace**&gt;**číselné řady**&gt;**číselné řady**). 

Nastavení na kartě **Pracovní volno** definují počet hodin, které musí zaměstnanec odpracovat má-li mít nárok na výhody pracovního volna. Délka zaměstnání, která je nutná pro vznik nároku a počáteční datum zaměstnání se používá k určení délky zaměstnání. Nastavení také definují počet hodin pracovního volna, na které mají zaměstnanci nárok a kalendář pracovního volna, který se používá k výpočtu počtu hodin využitého pracovního volna zaměstnancem. Karta **Pracovní volno** je k dispozici pouze pro společnosti v USA. 

**Poznámka:** Počet hodin, které jsou odpracovány nesmí překročit 1 250 a délka zaměstnání nesmí přesáhnout 12 měsíců. Tyto maximální hodnoty jsou v souladu s federálním právem ve Spojených státech amerických. Nakonec nastavení na kartě **Samoobslužné stránky zaměstnanců** určují informace, které manažer zadává jménem svých zaměstnanců.

<a name="see-also"></a>Viz také
--------

[Nastavení parametrů lidských zdrojů mezi právnickými osobami](set-up-hr-parameters-across-legal-entities.md)




