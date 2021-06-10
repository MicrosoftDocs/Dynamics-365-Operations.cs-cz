---
title: Vysvětlení polí data a času
description: Zjistěte, co je třeba očekávat při používání polí data a času v aplikaci Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/03/2020
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
ms.openlocfilehash: b7e5726f7e4beea1584b9a8e142212531ba1db56
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051730"
---
# <a name="understand-date-and-time-fields"></a><span data-ttu-id="41120-103">Pochopení polí data a času</span><span class="sxs-lookup"><span data-stu-id="41120-103">Understand Date and Time fields</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="41120-104">Pole **Datum a čas** jsou základním konceptem v aplikaci Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="41120-104">**Date and Time** fields are a fundamental concept in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="41120-105">Je důležité pochopit, jak pracovat s údaji **Datum a čas** ve formulářích, Dataverse a externích zdrojích.</span><span class="sxs-lookup"><span data-stu-id="41120-105">It's important to understand how to work with **Date and Time** data in forms, Dataverse, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="41120-106">Vysvětlení rozdílu mezi datovými typy v polích Datum a Čas</span><span class="sxs-lookup"><span data-stu-id="41120-106">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="41120-107">Pole **Datum a čas** obsahují informace o časovém pásmu, zatímco pole **Datum** ne.</span><span class="sxs-lookup"><span data-stu-id="41120-107">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="41120-108">Pole **Datum** zobrazují stejné informace v libovolném umístění.</span><span class="sxs-lookup"><span data-stu-id="41120-108">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="41120-109">Když zadáte datum do pole **Datum**, Human Resources zapíše stejné datum do databáze.</span><span class="sxs-lookup"><span data-stu-id="41120-109">When you enter a date into a **Date** field, Human Resources writes that same date to the database.</span></span>

<span data-ttu-id="41120-110">Při zobrazení dat v poli **Datum a čas** Human Resources upraví datum a čas na základě časového pásma uživatele nastaveného ve formuláři **Možnosti uživatele** (**Společné > Nastavení > Možnosti uživatele**).</span><span class="sxs-lookup"><span data-stu-id="41120-110">When displaying data in a **Date and Time** field, Human Resources adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="41120-111">Informace o datu a čase, které zadáte do pole, nemusí být stejné jako informace zapsané do databáze.</span><span class="sxs-lookup"><span data-stu-id="41120-111">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="41120-112">[![Formulář Možnosti uživatele](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="41120-112">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="41120-113">Informace o polích Datum a čas ve formulářích</span><span class="sxs-lookup"><span data-stu-id="41120-113">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="41120-114">Data **Datum a čas** zobrazená na obrazovce se neshodují s daty uloženými v databázi, pokud časové pásmo uživatele není nastaveno na Koordinovaný světový čas (UTC).</span><span class="sxs-lookup"><span data-stu-id="41120-114">**Date and Time** data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="41120-115">Data v polích **Datum a čas** jsou vždy uložena ve formátu UTC.</span><span class="sxs-lookup"><span data-stu-id="41120-115">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="41120-116">[![Formulář pracovníka UTC](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="41120-116">[![Worker form UTC](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="41120-117">Informace o polích Datum a čas v databázi</span><span class="sxs-lookup"><span data-stu-id="41120-117">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="41120-118">Když Human Resources zapíše hodnotu **Datum a čas** do databáze, uloží data v UTC.</span><span class="sxs-lookup"><span data-stu-id="41120-118">When Human Resources writes a **Date and Time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="41120-119">To uživatelům umožňuje zobrazit **Datum a čas** ve vztahu k časovému pásmu definovanému ve svých uživatelských možnostech.</span><span class="sxs-lookup"><span data-stu-id="41120-119">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="41120-120">Ve výše uvedeném příkladu je počátečním časem okamžik, ne konkrétní datum.</span><span class="sxs-lookup"><span data-stu-id="41120-120">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="41120-121">Změnou časového pásma přihlášeného uživatele z GMT + 12:00 na čas GMT UTC se v tomtéž záznamu zobrazí 04/30/2019 12:00:00 místo 05/01/2019 12:00:00.</span><span class="sxs-lookup"><span data-stu-id="41120-121">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="41120-122">V níže uvedeném příkladu bude zaměstnání zaměstnance 000724 aktivní ve stejnou dobu bez ohledu na časové pásmo.</span><span class="sxs-lookup"><span data-stu-id="41120-122">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="41120-123">Zaměstnanec bude aktivní dne 04/30/2019 v časovém pásmu GMT, který je stejný jako 05/01/2019 v časovém pásmu GMT + 12:00.</span><span class="sxs-lookup"><span data-stu-id="41120-123">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="41120-124">Oba odkazují na stejný bod v čase a ne na konkrétní datum.</span><span class="sxs-lookup"><span data-stu-id="41120-124">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="41120-125">[![Formulář pracovníka GMT](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="41120-125">[![Worker form GMT](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a><span data-ttu-id="41120-126">Datum a čas v Data Management Framework, Excel, Dataverse a Power BI</span><span class="sxs-lookup"><span data-stu-id="41120-126">Date and Time data in Data Management Framework, Excel, Dataverse, and Power BI</span></span> 

<span data-ttu-id="41120-127">Data Management Framework, doplněk aplikace Excel, Dataverse a sestavy Power BI jsou navrženy tak, aby spolupracovaly s daty přímo na úrovni databáze.</span><span class="sxs-lookup"><span data-stu-id="41120-127">The Data Management Framework, Excel Add-In, Dataverse, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="41120-128">Vzhledem k tomu, že neexistuje žádný klient pro úpravu údajů **Datum a čas** na časové pásmo uživatele, všechny hodnoty **Datum a čas** jsou v UTC, což může při zadávání a zobrazování dat vést k nesprávným předpokladům.</span><span class="sxs-lookup"><span data-stu-id="41120-128">Since there's no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="41120-129">Údaje **Datum a čas** odeslané prostřednictvím DMF, Excel nebo Dataverse jsou považována databází za standard UTC.</span><span class="sxs-lookup"><span data-stu-id="41120-129">**Date and Time** data submitted via DMF, Excel, or Dataverse is assumed to be in UTC by the database.</span></span> <span data-ttu-id="41120-130">To může způsobit nějakou záměnu, pokud se odeslaná hodnota **Datum a čas** nezobrazuje očekávaným způsobem, protože uživatel, který zobrazuje data, nemá uživatelské časové pásmo nastavené na čas UTC.</span><span class="sxs-lookup"><span data-stu-id="41120-130">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="41120-131">Při exportu dat může dojít k obrácení stejné věci.</span><span class="sxs-lookup"><span data-stu-id="41120-131">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="41120-132">Údaje **Datum a čas** v exportované entitě DMF se mohou lišit podle toho, co se zobrazí v klientu Dynamics.</span><span class="sxs-lookup"><span data-stu-id="41120-132">The **Date and Time** data in the exported DMF entity can be different than what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="41120-133">Při použití externích zdrojů, například DMF pro zobrazení nebo data o autorovi, je mějte na paměti, že hodnoty **Datum a čas** jsou ve výchozím nastavení považovány za čas UTC, bez ohledu na časové pásmo počítače uživatele nebo na jeho aktuální uživatelské časové pásmo.</span><span class="sxs-lookup"><span data-stu-id="41120-133">When using external sources like DMF to view or author data, keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="41120-134">Příklady stejného záznamu, který je zobrazen v různých oblastech produktu</span><span class="sxs-lookup"><span data-stu-id="41120-134">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="41120-135">**Human Resources s uživatelským časovým pásmem nastaveným na UTC**</span><span class="sxs-lookup"><span data-stu-id="41120-135">**Human Resources with user time zone set to UTC**</span></span>

<span data-ttu-id="41120-136">[![Pracovní formulář nastaven na UTC](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="41120-136">[![Worker form set to UTC](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="41120-137">**Human Resources s uživatelským časovým pásmem nastaveným na GMT +12:00**</span><span class="sxs-lookup"><span data-stu-id="41120-137">**Human Resources with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="41120-138">[![Pracovní formulář nastaven na GMT](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="41120-138">[![Worker form set to GMT](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="41120-139">**Excel přes OData**</span><span class="sxs-lookup"><span data-stu-id="41120-139">**Excel Via OData**</span></span>

<span data-ttu-id="41120-140">[![Excel přes OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="41120-140">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="41120-141">**Fázování DMF**</span><span class="sxs-lookup"><span data-stu-id="41120-141">**DMF Staging**</span></span>

<span data-ttu-id="41120-142">[![Fázování DMF](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="41120-142">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="41120-143">**Export DMF**</span><span class="sxs-lookup"><span data-stu-id="41120-143">**DMF Export**</span></span>

<span data-ttu-id="41120-144">[![Export DMF](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="41120-144">[![DMF Export](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="41120-145">**Excel přes Dataverse**</span><span class="sxs-lookup"><span data-stu-id="41120-145">**Excel via Dataverse**</span></span>

<span data-ttu-id="41120-146">[![Excel přes Dataverse](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="41120-146">[![Excel via Dataverse](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="41120-147">Viz také</span><span class="sxs-lookup"><span data-stu-id="41120-147">See also</span></span>

[<span data-ttu-id="41120-148">Údaje Datum a čas</span><span class="sxs-lookup"><span data-stu-id="41120-148">Date and time data</span></span>](/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="41120-149">Upřednostňované časové pásmo uživatele</span><span class="sxs-lookup"><span data-stu-id="41120-149">User preferred time zones</span></span>](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]