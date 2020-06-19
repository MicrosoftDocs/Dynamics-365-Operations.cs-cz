---
title: Vysvětlení polí data a času
description: Zjistěte, co je třeba očekávat při používání polí data a času v aplikaci Microsoft Dynamics 365 Human Resources. Získejte srozumitelnost, co by bylo možné očekávat při interakci s daty data a času ve formuláři v aplikaci Human Resources, v externím zdroji nebo v Common Data Service.
author: Darinkramer
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: be1e28d0b842184ce3c4f7bd9748f5e76ac67489
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430088"
---
# <a name="understand-date-and-time-fields"></a><span data-ttu-id="0f4da-104">Vysvětlení polí data a času</span><span class="sxs-lookup"><span data-stu-id="0f4da-104">Understand Date and Time fields</span></span>

<span data-ttu-id="0f4da-105">Pole **Datum a čas** jsou základním konceptem v aplikaci Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0f4da-105">**Date and Time** fields are a fundamental concept in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="0f4da-106">Je důležité pochopit, jak pracovat s údaji **Datum a čas** ve formulářích Dynamics 365 Human Resources, Common Data Service a externích zdrojích.</span><span class="sxs-lookup"><span data-stu-id="0f4da-106">It's important to understand how to work with **Date and Time** data in Dynamics 365 Human Resources forms, Common Data Service, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="0f4da-107">Vysvětlení rozdílu mezi datovými typy v polích Datum a Čas</span><span class="sxs-lookup"><span data-stu-id="0f4da-107">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="0f4da-108">Pole **Datum a čas** obsahují informace o časovém pásmu, zatímco pole **Datum** ne.</span><span class="sxs-lookup"><span data-stu-id="0f4da-108">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="0f4da-109">Pole **Datum** zobrazují stejné informace v libovolném umístění.</span><span class="sxs-lookup"><span data-stu-id="0f4da-109">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="0f4da-110">Když zadáte datum do pole **Datum**, Human Resources zapíše stejné datum do databáze.</span><span class="sxs-lookup"><span data-stu-id="0f4da-110">When you enter a date into a **Date** field, Human Resources writes that same date to the database.</span></span>

<span data-ttu-id="0f4da-111">Při zobrazení dat v poli **Datum a čas** Human Resources upraví datum a čas na základě časového pásma uživatele nastaveného ve formuláři **Možnosti uživatele** (**Společné > Nastavení > Možnosti uživatele**).</span><span class="sxs-lookup"><span data-stu-id="0f4da-111">When displaying data in a **Date and Time** field, Human Resources adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="0f4da-112">Informace o datu a čase, které zadáte do pole, nemusí být stejné jako informace zapsané do databáze.</span><span class="sxs-lookup"><span data-stu-id="0f4da-112">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="0f4da-113">[![Formulář Možnosti uživatele](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="0f4da-113">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="0f4da-114">Informace o polích Datum a čas ve formulářích</span><span class="sxs-lookup"><span data-stu-id="0f4da-114">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="0f4da-115">Při zadávání dat do pole **Datum a čas** se data zobrazená na obrazovce neshodují s daty uloženými v databázi, pokud časové pásmo uživatele není nastaveno na Koordinovaný světový čas (UTC).</span><span class="sxs-lookup"><span data-stu-id="0f4da-115">When entering data in a **Date and Time** field, the data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="0f4da-116">Data v polích **Datum a čas** jsou vždy uložena ve formátu UTC.</span><span class="sxs-lookup"><span data-stu-id="0f4da-116">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="0f4da-117">[![Formulář pracovníka](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="0f4da-117">[![Worker form](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="0f4da-118">Informace o polích Datum a čas v databázi</span><span class="sxs-lookup"><span data-stu-id="0f4da-118">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="0f4da-119">Když Human Resources zapíše hodnotu **Datum a čas** do databáze, uloží data v UTC.</span><span class="sxs-lookup"><span data-stu-id="0f4da-119">When Human Resources writes a **Date and time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="0f4da-120">To uživatelům umožňuje zobrazit **Datum a čas** ve vztahu k časovému pásmu definovanému ve svých uživatelských možnostech.</span><span class="sxs-lookup"><span data-stu-id="0f4da-120">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="0f4da-121">Ve výše uvedeném příkladu je počátečním časem okamžik, ne konkrétní datum.</span><span class="sxs-lookup"><span data-stu-id="0f4da-121">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="0f4da-122">Změnou časového pásma přihlášeného uživatele z GMT + 12:00 na čas GMT UTC se v tomtéž právě vytvořeném záznamu zobrazí 04/30/2019 12:00:00 místo 05/01/2019 12:00:00.</span><span class="sxs-lookup"><span data-stu-id="0f4da-122">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record just created shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="0f4da-123">V níže uvedeném příkladu bude zaměstnání zaměstnance 000724 aktivní ve stejnou dobu bez ohledu na časové pásmo.</span><span class="sxs-lookup"><span data-stu-id="0f4da-123">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="0f4da-124">Zaměstnanec bude aktivní dne 04/30/2019 v časovém pásmu GMT, který je stejný jako 05/01/2019 v časovém pásmu GMT + 12:00.</span><span class="sxs-lookup"><span data-stu-id="0f4da-124">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="0f4da-125">Oba odkazují na stejný bod v čase a ne na konkrétní datum.</span><span class="sxs-lookup"><span data-stu-id="0f4da-125">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="0f4da-126">[![Formulář pracovníka](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="0f4da-126">[![Worker form](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-common-data-service-and-power-bi"></a><span data-ttu-id="0f4da-127">Datum a čas v Data Management Framework, Excel, Common Data Service a Power BI</span><span class="sxs-lookup"><span data-stu-id="0f4da-127">Date and Time data in Data Management Framework, Excel, Common Data Service, and Power BI</span></span> 

<span data-ttu-id="0f4da-128">Data Management Framework, doplněk aplikace Excel, Common Data Service a sestavy Power BI jsou navrženy tak, aby spolupracovaly s daty přímo na úrovni databáze.</span><span class="sxs-lookup"><span data-stu-id="0f4da-128">The Data Management Framework, Excel Add-In, Common Data Service, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="0f4da-129">Vzhledem k tomu, že neexistuje žádný klient pro úpravu údajů **Datum a čas** na časové pásmo uživatele, všechny hodnoty **Datum a čas** jsou v UTC, což může při zadávání a zobrazování dat vést k nesprávným předpokladům.</span><span class="sxs-lookup"><span data-stu-id="0f4da-129">Since there is no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="0f4da-130">Údaje **Datum a čas** odeslané prostřednictvím DMF, Excel nebo Common Data Service jsou považována databází za standard UTC.</span><span class="sxs-lookup"><span data-stu-id="0f4da-130">**Date and Time** data that is submitted via DMF, Excel, or Common Data Service is assumed to be in UTC by the database.</span></span> <span data-ttu-id="0f4da-131">To může způsobit nějakou záměnu, pokud se odeslaná hodnota **Datum a čas** nezobrazuje očekávaným způsobem, protože uživatel, který zobrazuje data, nemá uživatelské časové pásmo nastavené na čas UTC.</span><span class="sxs-lookup"><span data-stu-id="0f4da-131">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="0f4da-132">Při exportu dat může dojít k obrácení stejné věci.</span><span class="sxs-lookup"><span data-stu-id="0f4da-132">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="0f4da-133">Údaje **Datum a čas** v exportované entitě DMF se mohou lišit podle toho, co se zobrazí v klientu Dynamics.</span><span class="sxs-lookup"><span data-stu-id="0f4da-133">The **Date and Time** data in the exported DMF entity can be different then what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="0f4da-134">Při použití externích zdrojů, například DMF pro zobrazení nebo data o autorovi, je důležité mít na paměti, že hodnoty **Datum a čas** jsou ve výchozím nastavení považovány za čas UTC, bez ohledu na časové pásmo počítače uživatele nebo na jeho aktuální uživatelské časové pásmo.</span><span class="sxs-lookup"><span data-stu-id="0f4da-134">When using external sources like DMF to view or author data, it is important to keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="0f4da-135">Příklady stejného záznamu, který je zobrazen v různých oblastech produktu</span><span class="sxs-lookup"><span data-stu-id="0f4da-135">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="0f4da-136">**Human Resources s uživatelským časovým pásmem nastaveným na UTC**</span><span class="sxs-lookup"><span data-stu-id="0f4da-136">**Human Resources with user time zone set to UTC**</span></span>

<span data-ttu-id="0f4da-137">[![Formulář pracovníka](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="0f4da-137">[![Worker form](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="0f4da-138">**Human Resources s uživatelským časovým pásmem nastaveným na GMT +12:00**</span><span class="sxs-lookup"><span data-stu-id="0f4da-138">**Human Resources with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="0f4da-139">[![Formulář pracovníka](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="0f4da-139">[![Worker form](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="0f4da-140">**Excel přes OData**</span><span class="sxs-lookup"><span data-stu-id="0f4da-140">**Excel Via OData**</span></span>

<span data-ttu-id="0f4da-141">[![Excel přes OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="0f4da-141">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="0f4da-142">**Fázování DMF**</span><span class="sxs-lookup"><span data-stu-id="0f4da-142">**DMF Staging**</span></span>

<span data-ttu-id="0f4da-143">[![Fázování DMF](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="0f4da-143">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="0f4da-144">**Export DMF**</span><span class="sxs-lookup"><span data-stu-id="0f4da-144">**DMF Export**</span></span>

<span data-ttu-id="0f4da-145">[![Fázování DMF](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="0f4da-145">[![DMF Staging](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="0f4da-146">**Excel přes Common Data Service**</span><span class="sxs-lookup"><span data-stu-id="0f4da-146">**Excel via Common Data Service**</span></span>

<span data-ttu-id="0f4da-147">[![Excel přes Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="0f4da-147">[![Excel via Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="0f4da-148">Viz také</span><span class="sxs-lookup"><span data-stu-id="0f4da-148">See also</span></span>

[<span data-ttu-id="0f4da-149">Údaje Datum a čas</span><span class="sxs-lookup"><span data-stu-id="0f4da-149">Date and time data</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="0f4da-150">Upřednostňované časové pásmo uživatele</span><span class="sxs-lookup"><span data-stu-id="0f4da-150">User preferred time zones</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 
