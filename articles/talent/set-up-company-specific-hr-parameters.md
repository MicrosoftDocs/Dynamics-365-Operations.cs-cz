---
title: "Nastavení parametrů lidských zdrojů pro konkrétní společnost"
description: "Nastavení některých parametrů lidských zdrojů nesmí být sdílena napříč společnostmi, zatímco nastavení jiných parametrů jsou specifické pro společnost. Tento článek vysvětluje, jak nastavit parametry lidských zdrojů specifické pro společnost."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HRMParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e195f9976465a933ceaaeb0bd2cbec4f814bc5f8
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="set-up-company-specific-hr-parameters"></a>Nastavení parametrů lidských zdrojů pro konkrétní společnost

[!include [banner](includes/banner.md)]

Nastavení některých parametrů lidských zdrojů nesmí být sdílena napříč společnostmi, zatímco nastavení jiných parametrů jsou specifické pro společnost. Tento článek vysvětluje, jak nastavit parametry lidských zdrojů specifické pro společnost.

Dvě stránky slouží k nastavení parametrů lidských zdrojů. Pro parametry, které jsou sdíleny napříč společnostmi, použijte stránku **Sdílené parametry lidských zdrojů**. Pro parametry, které jsou specifické pro společnost (jinými slovy nastavení se použije pro jednu společnost), můžete použít stránku **Parametry lidských zdrojů**. Na stránce **Parametry lidských zdrojů** jsou nastavení rozdělena mezi šest karet:

-   Obecné
-   Nábor - není součástí aplikace Dynamics 365 for Talent
-   Kompenzace
-   Číselné řady
-   Opuštění z rodinných a lékařských důvodu (FMLA)
-   Samoobsluha pro zaměstnance

Každá karta obsahuje informace, které se vztahují na jednu společnost. Nastavení kartě **Obecné** určuje vzhled informací o absencích, zraněních a onemocněních a nově přijatých zaměstnancích. Nastavení na této kartě také definují některé výchozí položky, které se zobrazí při práci. Konkrétně tato karta vás nechá vybrat barvu, která má být použita při otevření transakcí absencí, určit šablonu stylů, která má být použita pro sestavy, dále určit, zda mají být aktivována integrace mezi vzdělávacími kurzy a registrací absence, a vyberte kód absence, který má být použit při řízení této integrace. Můžete také určit, jak dlouho mají být zachovány případy zranění a onemocnění, a určit výchozí číslo identifikace, které se zobrazí při přijetí nového pracovníka. 

Nastavení na kartě **Nábor** definuje typy dokumentů, které se používají pro korespondence, která bude automaticky zaslána uchazečům a náborovému projektu použitému pro nevyžádané přihlášky (přihlášky, které nejsou určeny pro daný náborový projekt). Období definované pro náborový projekt časově určuje náborové projekty, které jsou zahrnuty na dlaždici **Časové projekty** v pracovním prostoru **Řízení náboru**. Období, které je definováno pro upozornění na termín přihlášky slouží k zobrazení náborových projektů, kterým se blíží jejich konečný termín přihlášky na dlaždici **Blíží se termín přihlášky** v pracovním prostoru **Nábor**. 

Nastavení na kartě **Kompenzace** definuje, zda uživatelé musí potvrzovat, že chtějí uložit informace pro plán fixní nebo variabilní kompenzace. Vyberete-li políčko **Povolit ověření ukládání**, kdykoli uživatelé zavřou stránku související s kompenzacemi, obdrží zprávu s dotazem, zda chtějí uložit záznam. Některé stránky v řízení kompenzace neumožní uživatelům odstranit informace. Vyzváním uživatelů k ověření, zda chtějí informace ukládat, budete schopni omezit informace, které jsou ukládány, a později nejdou odstranit. Pokud je zrušeno zaškrtnutí políčka **Povolit ověření ukládání**, záznamy budou vždy okamžitě uloženy případně již předtím, než je uživatel hotov. Pokud používáte funkci řízení výkonnosti, můžete na kartě **Kompenzace** vybrat model hodnocení, který má být použit namísto modelu přiřazeného k plánům kompenzace při hodnocení výkonnosti. 

### <a name="previously-released-functionality"></a>Dříve vydané funkce
Nastavení na kartě **Číselná řada** určují sekvence, které lze použít k automatickému přiřazení identifikátorů k položkám v modulu Lidské zdroje, například přihlášky, záznamy o absenci, výsledky procesu kompenzace, čísla případů, kurzy a agendy kurzů. Spravovat odkazy číselných řad a kódy můžete na stránce se seznamem **Číselné řady** (klikněte na **Správa organizace** &gt; **Číselné řady** &gt; **Číselné řady**).

### <a name="if-youre-using-dynamics-365-for-talent"></a>Pokud používáte Dynamics 365 for Talent
Nastavení na kartě **Číselná řada** určují sekvence, které lze použít k automatickému přiřazení identifikátorů k položkám v modulu Lidské zdroje, například přihlášky, záznamy o absenci, výsledky procesu kompenzace, čísla případů, kurzy a agendy kurzů. Spravovat odkazy číselných řad a kódy můžete na stránce se seznamem **Číselné řady** (klikněte na **Správa systému** &gt; **karta Odkazy** &gt; **Číselné řady** &gt; **Číselné řady**). 

Nastavení na kartě **Pracovní volno** definují počet hodin, které musí zaměstnanec odpracovat má-li mít nárok na výhody pracovního volna. Délka zaměstnání, která je nutná pro vznik nároku a počáteční datum zaměstnání se používá k určení délky zaměstnání. Nastavení také definují počet hodin pracovního volna, na které mají zaměstnanci nárok a kalendář pracovního volna, který se používá k výpočtu počtu hodin využitého pracovního volna zaměstnancem. Karta **Pracovní volno** je k dispozici pouze pro společnosti v USA. 

**Poznámka:** Počet hodin, které jsou odpracovány nesmí překročit 1 250 a délka zaměstnání nesmí přesáhnout 12 měsíců. Tyto maximální hodnoty jsou v souladu s federálním právem ve Spojených státech amerických. Nakonec nastavení na kartě **Samoobslužné stránky zaměstnanců** určují informace, které manažer zadává jménem svých zaměstnanců.

<a name="additional-resources"></a>Další zdroje
--------

[Nastavení parametrů lidských zdrojů mezi právnickými osobami](set-up-hr-parameters-across-legal-entities.md)




