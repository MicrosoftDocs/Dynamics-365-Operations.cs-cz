---
title: Práce s datem a časem v Microsoft Dynamics 365 Talent
description: Zjistěte, co je třeba očekávat při používání polí data a času v aplikaci Microsoft Dynamics 365 Talent. Získejte srozumitelnost, co by bylo možné očekávat při interakci s daty data a času ve formuláři v aplikaci Talent, v externím zdroji nebo v Common Data Service.
author: Darinkramer
manager: AnnBe
ms.date: 06/24/2019
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
ms.search.validFrom: 2019-06-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: abd215243cbda68ba3f57b5fa41054a10745d11f
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551019"
---
# <a name="work-with-date-and-time-in-microsoft-dynamics-365-talent"></a><span data-ttu-id="401b9-104">Práce s datem a časem v Microsoft Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="401b9-104">Work with date and time in Microsoft Dynamics 365 Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="401b9-105">Pole **Datum a čas** jsou základním konceptem v aplikaci Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="401b9-105">**Date and Time** fields are a fundamental concept in Dynamics 365 Talent.</span></span> <span data-ttu-id="401b9-106">Je důležité pochopit, jak pracovat s údaji **Datum a čas** ve formuláři Dynamics 365, Common Data Service a v externích zdrojích.</span><span class="sxs-lookup"><span data-stu-id="401b9-106">It's important to understand how to work with **Date and Time** data in a Dynamics 365 form, Common Data Service, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="401b9-107">Vysvětlení rozdílu mezi datovými typy v polích Datum a Čas</span><span class="sxs-lookup"><span data-stu-id="401b9-107">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="401b9-108">Pole **Datum a čas** obsahují informace o časovém pásmu, zatímco pole **Datum** ne.</span><span class="sxs-lookup"><span data-stu-id="401b9-108">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="401b9-109">Pole **Datum** zobrazují stejné informace v libovolném umístění.</span><span class="sxs-lookup"><span data-stu-id="401b9-109">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="401b9-110">Když zadáte datum do pole **Datum**, Talent zapíše stejné datum do databáze.</span><span class="sxs-lookup"><span data-stu-id="401b9-110">When you enter a date into a **Date** field, Talent writes that same date to the database.</span></span>

<span data-ttu-id="401b9-111">Při zobrazení dat v poli **Datum a čas** Talent upraví datum a čas na základě časového pásma uživatele nastaveného ve formuláři **Možnosti uživatele** (**Společné > Nastavení > Možnosti uživatele**).</span><span class="sxs-lookup"><span data-stu-id="401b9-111">When displaying data in a **Date and Time** field, Talent adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="401b9-112">Informace o datu a čase, které zadáte do pole, nemusí být stejné jako informace zapsané do databáze.</span><span class="sxs-lookup"><span data-stu-id="401b9-112">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="401b9-113">[![Formulář Možnosti uživatele](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="401b9-113">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="401b9-114">Informace o polích Datum a čas ve formulářích</span><span class="sxs-lookup"><span data-stu-id="401b9-114">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="401b9-115">Při zadávání dat do pole **Datum a čas** se data zobrazená na obrazovce neshodují s daty uloženými v databázi, pokud časové pásmo uživatele není nastaveno na Koordinovaný světový čas (UTC).</span><span class="sxs-lookup"><span data-stu-id="401b9-115">When entering data in a **Date and Time** field, the data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="401b9-116">Data v polích **Datum a čas** jsou vždy uložena ve formátu UTC.</span><span class="sxs-lookup"><span data-stu-id="401b9-116">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="401b9-117">[![Formulář pracovníka](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="401b9-117">[![Worker form](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="401b9-118">Informace o polích Datum a čas v databázi</span><span class="sxs-lookup"><span data-stu-id="401b9-118">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="401b9-119">Když Talent zapíše hodnotu **Datum a čas** do databáze, uloží data v UTC.</span><span class="sxs-lookup"><span data-stu-id="401b9-119">When Talent writes a **Date and time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="401b9-120">To uživatelům umožňuje zobrazit **Datum a čas** ve vztahu k časovému pásmu definovanému ve svých uživatelských možnostech.</span><span class="sxs-lookup"><span data-stu-id="401b9-120">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="401b9-121">Ve výše uvedeném příkladu je počátečním časem okamžik, ne konkrétní datum.</span><span class="sxs-lookup"><span data-stu-id="401b9-121">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="401b9-122">Změnou časového pásma přihlášeného uživatele z GMT + 12:00 na čas GMT UTC se v tomtéž právě vytvořeném záznamu zobrazí 04/30/2019 12:00:00 místo 05/01/2019 12:00:00.</span><span class="sxs-lookup"><span data-stu-id="401b9-122">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record just created shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="401b9-123">V níže uvedeném příkladu bude zaměstnání zaměstnance 000724 aktivní ve stejnou dobu bez ohledu na časové pásmo.</span><span class="sxs-lookup"><span data-stu-id="401b9-123">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="401b9-124">Zaměstnanec bude aktivní dne 04/30/2019 v časovém pásmu GMT, který je stejný jako 05/01/2019 v časovém pásmu GMT + 12:00.</span><span class="sxs-lookup"><span data-stu-id="401b9-124">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="401b9-125">Oba odkazují na stejný bod v čase a ne na konkrétní datum.</span><span class="sxs-lookup"><span data-stu-id="401b9-125">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="401b9-126">[![Formulář pracovníka](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="401b9-126">[![Worker form](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-common-data-service-and-power-bi"></a><span data-ttu-id="401b9-127">Datum a čas v Data Management Framework, Excel, Common Data Service a Power BI</span><span class="sxs-lookup"><span data-stu-id="401b9-127">Date and Time data in Data Management Framework, Excel, Common Data Service, and Power BI</span></span> 

<span data-ttu-id="401b9-128">Data Management Framework, doplněk aplikace Excel, Common Data Service a sestavy Power BI jsou navrženy tak, aby spolupracovaly s daty přímo na úrovni databáze.</span><span class="sxs-lookup"><span data-stu-id="401b9-128">The Data Management Framework, Excel Add-In, Common Data Service, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="401b9-129">Vzhledem k tomu, že neexistuje žádný klient pro úpravu údajů **Datum a čas** na časové pásmo uživatele, všechny hodnoty **Datum a čas** jsou v UTC, což může při zadávání a zobrazování dat vést k nesprávným předpokladům.</span><span class="sxs-lookup"><span data-stu-id="401b9-129">Since there is no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="401b9-130">Údaje **Datum a čas** odeslané prostřednictvím DMF, Excel nebo Common Data Service jsou považována databází za standard UTC.</span><span class="sxs-lookup"><span data-stu-id="401b9-130">**Date and Time** data that is submitted via DMF, Excel, or Common Data Service is assumed to be in UTC by the database.</span></span> <span data-ttu-id="401b9-131">To může způsobit nějakou záměnu, pokud se odeslaná hodnota **Datum a čas** nezobrazuje očekávaným způsobem, protože uživatel, který zobrazuje data, nemá uživatelské časové pásmo nastavené na čas UTC.</span><span class="sxs-lookup"><span data-stu-id="401b9-131">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="401b9-132">Při exportu dat může dojít k obrácení stejné věci.</span><span class="sxs-lookup"><span data-stu-id="401b9-132">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="401b9-133">Údaje **Datum a čas** v exportované entitě DMF se mohou lišit podle toho, co se zobrazí v klientu Dynamics.</span><span class="sxs-lookup"><span data-stu-id="401b9-133">The **Date and Time** data in the exported DMF entity can be different then what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="401b9-134">Při použití externích zdrojů, například DMF pro zobrazení nebo data o autorovi, je důležité mít na paměti, že hodnoty **Datum a čas** jsou ve výchozím nastavení považovány za čas UTC, bez ohledu na časové pásmo počítače uživatele nebo na jeho aktuální uživatelské časové pásmo.</span><span class="sxs-lookup"><span data-stu-id="401b9-134">When using external sources like DMF to view or author data, it is important to keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="401b9-135">Příklady stejného záznamu, který je zobrazen v různých oblastech produktu</span><span class="sxs-lookup"><span data-stu-id="401b9-135">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="401b9-136">**Talent s uživatelským časovým pásmem nastaveným na UTC**</span><span class="sxs-lookup"><span data-stu-id="401b9-136">**Talent with user time zone set to UTC**</span></span>

<span data-ttu-id="401b9-137">[![Formulář pracovníka](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="401b9-137">[![Worker form](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="401b9-138">**Talent s uživatelským časovým pásmem nastaveným na GMT +12:00**</span><span class="sxs-lookup"><span data-stu-id="401b9-138">**Talent with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="401b9-139">[![Formulář pracovníka](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="401b9-139">[![Worker form](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="401b9-140">**Excel přes OData**</span><span class="sxs-lookup"><span data-stu-id="401b9-140">**Excel Via OData**</span></span>

<span data-ttu-id="401b9-141">[![Excel přes OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="401b9-141">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="401b9-142">**Fázování DMF**</span><span class="sxs-lookup"><span data-stu-id="401b9-142">**DMF Staging**</span></span>

<span data-ttu-id="401b9-143">[![Fázování DMF](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="401b9-143">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="401b9-144">**Export DMF**</span><span class="sxs-lookup"><span data-stu-id="401b9-144">**DMF Export**</span></span>

<span data-ttu-id="401b9-145">[![Fázování DMF](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="401b9-145">[![DMF Staging](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="401b9-146">**Excel přes Common Data Service**</span><span class="sxs-lookup"><span data-stu-id="401b9-146">**Excel via Common Data Service**</span></span>

<span data-ttu-id="401b9-147">[![Excel přes Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="401b9-147">[![Excel via Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

### <a name="see-also"></a><span data-ttu-id="401b9-148">Viz také</span><span class="sxs-lookup"><span data-stu-id="401b9-148">See also</span></span>

[<span data-ttu-id="401b9-149">Údaje Datum a čas</span><span class="sxs-lookup"><span data-stu-id="401b9-149">Date and time data</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="401b9-150">Upřednostňované časové pásmo uživatele</span><span class="sxs-lookup"><span data-stu-id="401b9-150">User preferred time zones</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 
