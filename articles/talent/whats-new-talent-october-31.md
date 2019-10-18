---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Talent – Core HR (31. října 2018)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/31/2018
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
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d2ad9be740d917a760815718a1473d7bcba97968
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025925"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-october-31-2018"></a><span data-ttu-id="b62ee-103">Co je nového nebo upraveného v aplikaci Dynamics 365 Talent: Core HR (31. října 2018)</span><span class="sxs-lookup"><span data-stu-id="b62ee-103">What's new or changed in Dynamics 365 Talent: Core HR (October 31, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b62ee-104">**Sestavení 8.1.2031**</span><span class="sxs-lookup"><span data-stu-id="b62ee-104">**Build 8.1.2031**</span></span>

<span data-ttu-id="b62ee-105">Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Core HR.</span><span class="sxs-lookup"><span data-stu-id="b62ee-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="create-links-from-talent-to-finance"></a><span data-ttu-id="b62ee-106">Vytvoření propojení z aplikace Talent do aplikace Finance</span><span class="sxs-lookup"><span data-stu-id="b62ee-106">Create links from Talent to Finance</span></span>
<span data-ttu-id="b62ee-107">Tato nová navigační funkce vám umožní propojit se z aplikace Talent do aplikace Finance, což vám umožní přímý přechod na stránky aplikace Finance.</span><span class="sxs-lookup"><span data-stu-id="b62ee-107">This new navigation functionality allows you to link from Talent to Finance, giving you direct navigation into Finance pages.</span></span> <span data-ttu-id="b62ee-108">Po nastavení propojení můžete zadat název a skupinu propojení, kde se má propojení objevit v aplikaci Talent a cílovou stránku, která se otevře v aplikaci Finance.</span><span class="sxs-lookup"><span data-stu-id="b62ee-108">When links are configured, you can specify the name and group of the link, where the link should surface in Talent, and the target page to be opened within Finance.</span></span>

#### <a name="coming-soon"></a><span data-ttu-id="b62ee-109">Již brzy</span><span class="sxs-lookup"><span data-stu-id="b62ee-109">Coming soon</span></span>
<span data-ttu-id="b62ee-110">Kontext pole bude přidán později, aby umožnil přímý přechod na odpovídající záznamy v aplikaci Finance.</span><span class="sxs-lookup"><span data-stu-id="b62ee-110">Field context will be added in the future to allow for direct navigation to corresponding records in Finance.</span></span> <span data-ttu-id="b62ee-111">Například můžete použít **Odkaz na pole** pro poskytnutí kontextu k přímému přechodu na konkrétního zaměstnance nebo pozici v aplikaci Finance.</span><span class="sxs-lookup"><span data-stu-id="b62ee-111">For example, you can use **Link to field** to provide the context to navigate directly to a specific employee or position in Finance.</span></span>

### <a name="configure-target-systems"></a><span data-ttu-id="b62ee-112">Konfigurace cílových systémů</span><span class="sxs-lookup"><span data-stu-id="b62ee-112">Configure target systems</span></span>

<span data-ttu-id="b62ee-113">V aplikaci Talent mohou definovat správci systému propojení, která se zobrazí, prostřednictvím pracovního prostoru Správa systému.</span><span class="sxs-lookup"><span data-stu-id="b62ee-113">In Talent, system administrators can define links that will be surfaced through the System Administration workspace.</span></span> <span data-ttu-id="b62ee-114">Součástí konfigurace je prostředí Finance, do kterého chcete přejít jako do cíle propojení.</span><span class="sxs-lookup"><span data-stu-id="b62ee-114">Part of the configuration is the Finance environments that you would like to navigate to as the "target" of the link.</span></span> <span data-ttu-id="b62ee-115">Toho dosáhnete přiřazením názvu cílovému systému a zadáním URL adresy prostředí Finance.</span><span class="sxs-lookup"><span data-stu-id="b62ee-115">You do this by giving the target system a name and providing the URL of the Finance environment.</span></span> <span data-ttu-id="b62ee-116">Zde je příklad URL adresy Finance, kterou můžete zadat: https://devax00124aos.cloud.test.dynamics.com/.</span><span class="sxs-lookup"><span data-stu-id="b62ee-116">Here is an example of a Finance URL that you would provide: https://devax00124aos.cloud.test.dynamics.com/.</span></span> <span data-ttu-id="b62ee-117">Po nakonfigurování cílových systémů můžete nadefinovat svá propojení.</span><span class="sxs-lookup"><span data-stu-id="b62ee-117">After you have configured your target systems,  you can define your links.</span></span>

### <a name="configure-links"></a><span data-ttu-id="b62ee-118">Konfigurovat odkaz</span><span class="sxs-lookup"><span data-stu-id="b62ee-118">Configure links</span></span>

<span data-ttu-id="b62ee-119">Každé propojení, které je vytvořeno, má definovány následující informace.</span><span class="sxs-lookup"><span data-stu-id="b62ee-119">Each link that is created will have the following information defined.</span></span>

- <span data-ttu-id="b62ee-120">Propojení – Název propojení, používaný pouze k identifikaci.</span><span class="sxs-lookup"><span data-stu-id="b62ee-120">Link - Name of the link, used for identification only.</span></span>

- <span data-ttu-id="b62ee-121">Povolit toto propojení - Nastavte tuto možnost na **Ano**, pokud chcete zobrazit toto propojení pro uživatele aplikace Talent.</span><span class="sxs-lookup"><span data-stu-id="b62ee-121">Enable this Link - Set to **Yes** if you want to display the link to users of Talent.</span></span>

- <span data-ttu-id="b62ee-122">Zobrazovaný název – Definujte název, který se zobrazí jako propojení do aplikace Finance.</span><span class="sxs-lookup"><span data-stu-id="b62ee-122">Display name - Define the name that will appear as a link to Finance.</span></span> <span data-ttu-id="b62ee-123">Tato data nejsou momentálně přeložena.</span><span class="sxs-lookup"><span data-stu-id="b62ee-123">This data is currently is not translated.</span></span>

- <span data-ttu-id="b62ee-124">Odkaz na místo zobrazení ve formuláři - Vyberte, na které stránce se má zobrazit propojení.</span><span class="sxs-lookup"><span data-stu-id="b62ee-124">Surface link on form - Choose which page you would like to display the link on.</span></span>

- <span data-ttu-id="b62ee-125">Skupina - Skupiny nejsou vyžadovány, ale pokud chcete uspořádat svá propojení pomocí skupin, vyberte existující skupinu, nebo vytvořte novou pomocí pole **Skupina**.</span><span class="sxs-lookup"><span data-stu-id="b62ee-125">Group - Groups are not required, but if you want to organize your links using groups, select an existing group or create a new one using the **Group** field.</span></span>

- <span data-ttu-id="b62ee-126">Cílový systém - Vyberte cílový systém, který byl vytvořen pomocí možnosti **Konfigurace cílového systému**.</span><span class="sxs-lookup"><span data-stu-id="b62ee-126">Target system - Select the target system that was created using the **Configure target system** option.</span></span> <span data-ttu-id="b62ee-127">Bude se jednat o prostředí Finance, které bude použito při navigaci pomocí propojení.</span><span class="sxs-lookup"><span data-stu-id="b62ee-127">This will be the Finance environment that will be used when navigating by using the link.</span></span>

- <span data-ttu-id="b62ee-128">Použít aktuální společnosti uživatele – Vyberte **Ano**, budete-li chtít používat kontext aktuální společnosti uživatele při navigaci do Finance.</span><span class="sxs-lookup"><span data-stu-id="b62ee-128">Use user's current Company - Select **Yes** if you would like to use the User's current company context when navigating to Finance.</span></span> <span data-ttu-id="b62ee-129">Pokud zvolíte **Ne**, můžete vybrat společnost, která má být použita.</span><span class="sxs-lookup"><span data-stu-id="b62ee-129">If **No** is selected, then you can select the company that should be used.</span></span>

- <span data-ttu-id="b62ee-130">Cílová položka nabídky- Zadejte položku nabídky z Finance, kterou má používat propojení při navigaci.</span><span class="sxs-lookup"><span data-stu-id="b62ee-130">Target menu item - Enter the menu item from Finance that the link should use when navigating.</span></span> <span data-ttu-id="b62ee-131">K dispozici jsou položky nabídky, ke kterým můžete přímo navigovat.</span><span class="sxs-lookup"><span data-stu-id="b62ee-131">Menu items that you can directly navigate to are available.</span></span> <span data-ttu-id="b62ee-132">Chcete-li vyhledat požadovanou položku nabídky, otevřete Finance a otevřete stránku, která je cílem navigace.</span><span class="sxs-lookup"><span data-stu-id="b62ee-132">To find the menu item required, open Finance and open the page that is the target of the navigation.</span></span> <span data-ttu-id="b62ee-133">Zkopírujte položku nabídky z adresy URL.</span><span class="sxs-lookup"><span data-stu-id="b62ee-133">Copy the menu item from the URL.</span></span> <span data-ttu-id="b62ee-134">Například pokud chcete, aby vás odkaz navedl na seznam zaměstnanců v aplikaci Finance and Operations, zadejte hodnotu, které se objeví v URL adrese za „&mi“.</span><span class="sxs-lookup"><span data-stu-id="b62ee-134">For example, if you want the link to take you to the employee list in Finance and Operations, enter the value that appears after the "&mi" in the URL.</span></span> <span data-ttu-id="b62ee-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees.</span><span class="sxs-lookup"><span data-stu-id="b62ee-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees.</span></span> <span data-ttu-id="b62ee-136">Položka nabídky pro navigaci na stránku se seznamem zaměstnanců v tomto příkladu je: HcmWorkerListPage_Employees.</span><span class="sxs-lookup"><span data-stu-id="b62ee-136">The menu item to navigate to the employee list page in this example is: HcmWorkerListPage_Employees.</span></span>

- <span data-ttu-id="b62ee-137">Odkaz na zdroj dat – Vyberte zdroj dat, na která se odkaz odkazuje.</span><span class="sxs-lookup"><span data-stu-id="b62ee-137">Link to data source - Select the source of data that the link is referencing.</span></span> <span data-ttu-id="b62ee-138">Nejběžnější zdroje, jako je například **Pracovník** a **Pozice**, jsou k dispozici.</span><span class="sxs-lookup"><span data-stu-id="b62ee-138">The most common sources like **Worker** and **Position** are available.</span></span>

- <span data-ttu-id="b62ee-139">Odkaz na pole - (připravuje se) Tento výběr pole umožní přímou navigaci z jednoho záznamu v aplikaci Talent do jednoho záznamu v aplikaci Finance.</span><span class="sxs-lookup"><span data-stu-id="b62ee-139">Link to field - (Coming soon) This field selection will allow for direct navigation from a single record in Talent to a single record in Finance.</span></span>

### <a name="access-to-links"></a><span data-ttu-id="b62ee-140">Přístup k odkazům</span><span class="sxs-lookup"><span data-stu-id="b62ee-140">Access to links</span></span>

<span data-ttu-id="b62ee-141">Správci systému uvidí nově vytvořené odkazy na definovaných stránkách, i když je možnost **Povolit tento odkaz** nastavena na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="b62ee-141">System administrators will see the newly created links on the defined pages even if the **Enable this link** option is set to **No**.</span></span> <span data-ttu-id="b62ee-142">To lze použít k testování odkazů předtím, než budou vystaveny k použití pro jiné zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="b62ee-142">This can be used for testing links prior to surfacing them to other employees.</span></span> <span data-ttu-id="b62ee-143">Všechny ostatní role uvidí jen konfigurované odkazy poté, co bude možnost **Povolit teto odkaz** nastavena na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="b62ee-143">All other roles will only see the configured links after the **Enable this link** option is set to **Yes**.</span></span> <span data-ttu-id="b62ee-144">Zaměstnanci, kteří mají přístup ke stránkám, na kterých jsou odkazy k dispozici, budou mít přístup k odkazům.</span><span class="sxs-lookup"><span data-stu-id="b62ee-144">Employees who have access to the pages in which the links are surfaced will have access to the links.</span></span>

<span data-ttu-id="b62ee-145">Uživatelé také mají bezpečnostní oprávnění v rámci aplikace Finance definované pro přístup ke stránkám v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b62ee-145">Users can also have security rights within Finance defined to access the pages in Finance and Operations.</span></span> <span data-ttu-id="b62ee-146">Pokud ne, zobrazí se při použití odkazu dialogové okno zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="b62ee-146">If they don't, a security dialog box will be displayed when using the link.</span></span>


## <a name="other-changesfixes"></a><span data-ttu-id="b62ee-147">Další změny/opravy</span><span class="sxs-lookup"><span data-stu-id="b62ee-147">Other changes/fixes</span></span>

### <a name="positions-with-a-future-start-date-cannot-be-assigned-to-a-new-employee"></a><span data-ttu-id="b62ee-148">Pozice s budoucím počátečním datem nelze přiřadit k novému zaměstnanci</span><span class="sxs-lookup"><span data-stu-id="b62ee-148">Positions with a future start date cannot be assigned to a new employee</span></span>

<span data-ttu-id="b62ee-149">Byly provedeny změny, které umožní přiřazení zaměstnanců k pozicím s budoucím datem.</span><span class="sxs-lookup"><span data-stu-id="b62ee-149">Changes have been made to allow employee assignments to future-dated positions.</span></span> <span data-ttu-id="b62ee-150">Pozice, které mají počáteční datum v budoucnosti, lze vybrat, a přiřazení zaměstnance bude provedeno při uložení nebo dokončení workflow (pokud je workflow povoleno).</span><span class="sxs-lookup"><span data-stu-id="b62ee-150">Positions that have start dates in the future can be selected and the employee assignment will be made upon save or completion of the workflow (if the workflow is enabled).</span></span>

### <a name="new-employee-cannot-be-assigned-existing-position"></a><span data-ttu-id="b62ee-151">Nový zaměstnanec nemůže být přiřazen k existující pozici</span><span class="sxs-lookup"><span data-stu-id="b62ee-151">New employee cannot be assigned existing position</span></span>

<span data-ttu-id="b62ee-152">Byly provedeny změny, aby mohl být nový zaměstnanec přiřazen k existujícím pozicím.</span><span class="sxs-lookup"><span data-stu-id="b62ee-152">Changes have been made so new employee assignment can now be assigned to existing positions.</span></span>

### <a name="seniority-dateoffice-location-disappears-when-the-employment-start-date-is-in-the-past-and-the-record-is-saved"></a><span data-ttu-id="b62ee-153">Datum služebního věku/Umístění pracoviště zmizí, když je počáteční datum zaměstnání v minulosti a záznam je ukládán.</span><span class="sxs-lookup"><span data-stu-id="b62ee-153">Seniority date/Office location disappears when the employment start date is in the past and the record is saved</span></span>

<span data-ttu-id="b62ee-154">Byly provedeny změny, aby byla opravena viditelnost položek **Datum služebního věku** a **Umístění pracoviště** při ukládání bývalých zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="b62ee-154">Changes have been made to correct the visibilty of the **Senority date** and **Office location** when saving changes for past employees.</span></span>

### <a name="cant-enter-data-for-future-dated-employments-on-the-worker-page"></a><span data-ttu-id="b62ee-155">Nelze zadat data pro budoucí zaměstnání na stránce pracovníka</span><span class="sxs-lookup"><span data-stu-id="b62ee-155">Can't enter data for future-dated employments on the worker page</span></span>

<span data-ttu-id="b62ee-156">Na hlavní stránce pracovníka byla zakázána data zaměstnání pro budoucí zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="b62ee-156">Employment data for future-dated employments has been disabled on the main worker page.</span></span> <span data-ttu-id="b62ee-157">Data zaměstnání lze zadat pomocí stránek **Správce dat**.</span><span class="sxs-lookup"><span data-stu-id="b62ee-157">Employment data can be entered through the **Date Manager** pages.</span></span> <span data-ttu-id="b62ee-158">Další změny budou provedeny v příštích verzích, aby bylo možné zadávat údaje o zaměstnancích během procesu workflowu.</span><span class="sxs-lookup"><span data-stu-id="b62ee-158">Additional changes will be made in future releases to enable entering employment data directly during the workflow process.</span></span>

### <a name="add-validfrom-and-validto-to-hcmpersonalcontactpersonentity"></a><span data-ttu-id="b62ee-159">Přidání ValidFrom a ValidTo do HcmPersonalContactPersonEntity</span><span class="sxs-lookup"><span data-stu-id="b62ee-159">Add ValidFrom and ValidTo to HcmPersonalContactPersonEntity</span></span>

<span data-ttu-id="b62ee-160">Enitita Data Management Framework (DMF) s názvem HcmPersonalContactPersonEntity byla aktualizována tak, aby zahrnovala data „platné od“ a „platné do“ pro povolení určitých scénářů integrace výhod.</span><span class="sxs-lookup"><span data-stu-id="b62ee-160">The Data Management Framework (DMF) entity HcmPersonalContactPersonEntity has been updated to include "valid from" and "valid to" dates to enable certain benefit integration scenarios.</span></span> 

## <a name="known-issue"></a><span data-ttu-id="b62ee-161">Známý problém</span><span class="sxs-lookup"><span data-stu-id="b62ee-161">Known issue</span></span>
- <span data-ttu-id="b62ee-162">**Problém**: Při přidání nové přílohy k pracovníkovi jsou tlačítka **Nová** a **Upravit** zobrazena šedě.</span><span class="sxs-lookup"><span data-stu-id="b62ee-162">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="b62ee-163">**Řešení:** Než otevřete stránku přílohy, ujistěte se, že jsou zavřena okna s fakty na stránce **Pracovník**.</span><span class="sxs-lookup"><span data-stu-id="b62ee-163">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="b62ee-164">Jsou-li okna s fakty uzavřena při načítání stránky **Pracovník**, budou tlačítka přílohy k dispozici.</span><span class="sxs-lookup"><span data-stu-id="b62ee-164">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="b62ee-165">(Tento problém bude opraven v další aktualizaci Platform Update.)</span><span class="sxs-lookup"><span data-stu-id="b62ee-165">(This issue will be fixed in the next platform update.)</span></span>
