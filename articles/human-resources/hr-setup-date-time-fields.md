---
title: Pochopení polí data a času
description: Toto téma vysvětluje, co je třeba očekávat při používání polí data a času v aplikaci Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 06c783c1e4a2961f1445909ea03d557c0985064e
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/01/2021
ms.locfileid: "7728582"
---
# <a name="understand-date-and-time-fields"></a>Pochopení polí data a času

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Pole **Datum a čas** jsou základním konceptem v aplikaci Microsoft Dynamics 365 Human Resources. Je důležité pochopit, jak pracovat s údaji **Datum a čas** na stránkách, v Dataverse a v externích zdrojích.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>Vysvětlení rozdílu mezi datovými typy v polích Datum a Čas

Pole **Datum a čas** obsahují informace o časovém pásmu, zatímco pole **Datum** ne. Pole **Datum** zobrazují stejné informace v libovolném umístění. Když zadáte datum do pole **Datum**, zapíše se stejné datum do databáze.

Při zobrazení dat v poli **Datum a čas** upraví se datum a čas na základě časového pásma uživatele vybraného na stránce **Možnosti uživatele** (**Společné \> Nastavení \> Možnosti uživatele**). Informace o datu a čase, které zadáte do pole, nemusí být stejné jako informace zapsané do databáze.

[![Stránka Možnosti uživatele.](./media/Useroptionsform.png)](./media/Useroptionsform.png)

## <a name="understanding-date-and-time-fields-on-pages"></a>Informace o polích Datum a čas na stránkách 

Data **Datum a čas** zobrazená na obrazovce se neshodují s daty uloženými v databázi, pokud časové pásmo uživatele není nastaveno na Koordinovaný světový čas (UTC). Data v polích **Datum a čas** jsou vždy uložena ve formátu UTC.

[![Stránka pracovníka UTC.](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>Informace o polích Datum a čas v databázi 

Když se zapíše hodnota **Datum a čas** do databáze, uloží data jako formát UTC. Proto mohou uživatelé zobrazit **Datum a čas** ve vztahu k časovému pásmu definovanému ve svých uživatelských možnostech.
 
Ve výše uvedeném příkladu je počátečním časem okamžik, ne konkrétní datum. Změnou časového pásma přihlášeného uživatele z GMT + 12:00 na čas GMT UTC se v tomtéž záznamu zobrazí 04/30/2019 12:00:00 místo 05/01/2019 12:00:00.

V níže uvedeném příkladu bude zaměstnání zaměstnance 000724 aktivní ve stejnou dobu bez ohledu na časové pásmo. Zaměstnanec bude aktivní dne 04/30/2019 v časovém pásmu GMT, který je stejný jako 05/01/2019 v časovém pásmu GMT + 12:00. Oba odkazují na stejný bod v čase a ne na konkrétní datum. 

[![Stránka pracovníka GMT.](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a>Datum a čas v Data Management Framework, Excel, Dataverse a Power BI 

Data Management Framework (DMF), doplněk aplikace Excel, Dataverse a sestavy Power BI jsou navrženy tak, aby spolupracovaly s daty přímo na úrovni databáze. Vzhledem k tomu, že neexistuje žádný klient pro úpravu údajů **Datum a čas** na časové pásmo uživatele, všechny hodnoty **Datum a čas** jsou v UTC, což může při zadávání a zobrazování dat vést k nesprávným předpokladům.
 
Když jsou údaje **Datum a čas** odeslané prostřednictvím DMF, Excel nebo Dataverse, jsou považována databází za standard UTC. Pokud však uživatelé, kteří si data prohlížejí, nemají časové pásmo uživatele nastavené na UTC, hodnota **Datum a čas** se nezobrazí podle očekávání a uživatelé mohou být zmateni. 
 
Při exportu dat může dojít k obrácení stejné věci. Údaje **Datum a čas** v exportované entitě DMF se mohou lišit podle toho, co se zobrazí v klientu Dynamics. 
 
Při použití externích zdrojů, například DMF pro zobrazení nebo data o autorovi, je mějte na paměti, že hodnoty **Datum a čas** jsou ve výchozím nastavení považovány za čas UTC, bez ohledu na časové pásmo počítače uživatele nebo na jeho aktuální uživatelské časové pásmo. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>Příklady stejného záznamu, který je zobrazen v různých oblastech produktu 

**Human Resources s uživatelským časovým pásmem nastaveným na UTC**

[![Pracovní stránka nastavena na UTC.](./media/worker-form3.png)](./media/worker-form3.png)

**Human Resources s uživatelským časovým pásmem nastaveným na GMT +12:00** 

[![Pracovní stránka nastavena na GMT.](./media/worker-form4.png)](./media/worker-form4.png)

**Excel přes OData**

[![Excel přes OData.](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**Fázování DMF**

[![Fázování DMF.](./media/DMFStaging.png)](./media/DMFStaging.png)

**Export DMF**

[![Export DMF.](./media/DMFExport.png)](./media/DMFExport.png)

**Excel přes Dataverse**

[![Excel přes Dataverse.](./media/ExcelCDS.png)](./media/ExcelCDS.png)

## <a name="see-also"></a>Viz také

[Údaje Datum a čas](/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[Upřednostňované časové pásmo uživatele](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
