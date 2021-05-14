---
title: Koncept společnosti v Dataverse
description: Toto téma popisuje integraci dat společností mezi aplikacemi Finance and Operations a Dataverse.
author: RamaKrishnamoorthy
ms.date: 08/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 6a858135d377b30d6e8885ae18b2dc50da11813b
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941022"
---
# <a name="company-concept-in-dataverse"></a><span data-ttu-id="e1bdf-103">Koncept společnosti v Dataverse</span><span class="sxs-lookup"><span data-stu-id="e1bdf-103">Company concept in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


<span data-ttu-id="e1bdf-104">Koncept *společnosti* v Finance and Operations je právní i obchodní konstrukt.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-104">In Finance and Operations, the concept of a *company* is both a legal construct and a business construct.</span></span> <span data-ttu-id="e1bdf-105">Je to také hranice pro zabezpečení a viditelnost dat.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-105">It's also a security and visibility boundary for data.</span></span> <span data-ttu-id="e1bdf-106">Uživatelé pracují vždy v kontextu jedné společnosti a většina dat je rozdělena podle společnosti.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-106">Users always work in the context of a single company, and most of the data is striped by company.</span></span>

<span data-ttu-id="e1bdf-107">Dataverse nemá ekvivalentní koncepci.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-107">Dataverse doesn't have an equivalent concept.</span></span> <span data-ttu-id="e1bdf-108">Nejbližší koncept je *organizační jednotka*, která je primárně hranicí zabezpečení a viditelnosti pro uživatelská data.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-108">The closest concept is *business unit*, which is primarily a security and visibility boundary for user data.</span></span> <span data-ttu-id="e1bdf-109">Tento koncept nemá stejné právní nebo obchodní důsledky jako koncepce společnosti.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-109">This concept doesn't have the same legal or business implications as the company concept.</span></span>

<span data-ttu-id="e1bdf-110">Vzhledem k tomu, že organizační jednotka a společnost nejsou rovnocennými koncepty, není možné vynutit mapování mezi nimi (1:1) pro účely integrace Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-110">Because business unit and company aren't equivalent concepts, it isn't possible to force a one-to-one (1:1) mapping between them for the purpose of Dataverse integration.</span></span> <span data-ttu-id="e1bdf-111">Protože však uživatelé musí mít ve výchozím nastavení možnost zobrazit stejné řádky v aplikaci a Dataverse, společnost Microsoft zavedla novou tabulku v aplikaci Dataverse s názvem cdm\_Company.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-111">However, because users must, by default, be able to see the same rows in the application and Dataverse, Microsoft has introduced a new table in Dataverse that is named cdm\_Company.</span></span> <span data-ttu-id="e1bdf-112">Tato tabulku je ekvivalentní s tabulkou společnosti v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-112">This table is equivalent to the Company table in the application.</span></span> <span data-ttu-id="e1bdf-113">Chcete-li zajistit, aby viditelnost řádků byla ekvivalentní mezi aplikací a Dataverse, doporučujeme následující nastavení dat v aplikaci Dataverse:</span><span class="sxs-lookup"><span data-stu-id="e1bdf-113">To help guarantee that visibility of rows is equivalent between the application and Dataverse out of the box, we recommend the following setup for data in Dataverse:</span></span>

+ <span data-ttu-id="e1bdf-114">Pro každý řádek společnosti Finance and Operations, který je povolen pro duální zápis, je vytvořen přidružený řádek cdm\_Company.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-114">For each Finance and Operations Company row that is enabled for dual-write, an associated cdm\_Company row is created.</span></span>
+ <span data-ttu-id="e1bdf-115">Když je vytvořen řádek cdm\_Company a je povolen pro duální zápis, je vytvořena výchozí organizační jednotka se stejným názvem.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-115">When a cdm\_Company row is created and enabled for dual-write, a default business unit is created that has the same name.</span></span> <span data-ttu-id="e1bdf-116">Přestože je pro tuto organizační jednotku automaticky vytvořen výchozí tým, není tato organizační jednotka použita.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-116">Although a default team is automatically created for that business unit, the business unit isn't used.</span></span>
+ <span data-ttu-id="e1bdf-117">Je vytvořen samostatný tým vlastníků se stejným názvem.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-117">A separate owner team is created that has the same name.</span></span> <span data-ttu-id="e1bdf-118">Je také spojen s organizační jednotkou.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-118">It's also associated with the business unit.</span></span>
+ <span data-ttu-id="e1bdf-119">Ve výchozím nastavení je vlastník libovolného řádku vytvořeného a dvojitě zapsaného do Dataverse nastaven na tým "DW Owner", který je propojen s přidruženou organizační jednotkou.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-119">By default, the owner of any row that is created and dual-written to Dataverse is set to the "DW Owner" team that is linked to the associated business unit.</span></span>

<span data-ttu-id="e1bdf-120">Následující obrázek znázorňuje příklad nastavení dat v Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-120">The following illustration shows an example of this data setup in Dataverse.</span></span>

![Nastavení dat v Dataverse](media/dual-write-company-1.png)

<span data-ttu-id="e1bdf-122">Z důvodu této konfigurace bude každý řádek, který se týká společnosti USMF, vlastněn týmem, který je propojen s organizační jednotkou USMF v aplikaci Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-122">Because of this configuration, any row that is related to the USMF company will be owned by a team that is linked to the USMF business unit in Dataverse.</span></span> <span data-ttu-id="e1bdf-123">Každý uživatel, který má přístup k této organizační jednotce prostřednictvím role zabezpečení nastavené na zobrazení na úrovni organizační jednotky, je tedy nyní schopen tyto řádky zobrazit.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-123">Therefore, any user who has access to that business unit through a security role that is set to business unit–level visibility can now see those rows.</span></span> <span data-ttu-id="e1bdf-124">Následující příklad ukazuje, jak lze týmy použít k zajištění správného přístupu k těmto řádkům.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-124">The following example shows how teams can be used to provide the correct access to those rows.</span></span>

+ <span data-ttu-id="e1bdf-125">Role Manažer prodeje je přidělena členům týmu USMF Sales.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-125">The "Sales Manager" role is assigned to members of the "USMF Sales" team.</span></span>
+ <span data-ttu-id="e1bdf-126">Uživatelé, kteří mají roli manažer prodeje, mohou přistupovat ke všem řádkům obchodních vztahů, které jsou členy stejné organizační jednotky, v níž jsou členy.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-126">Users who have the "Sales Manager" role can access any account rows that are members of the same business unit that they are members of.</span></span>
+ <span data-ttu-id="e1bdf-127">Tým USMF Sales je propojen s dříve uvedenou organizační jednotkou USMF.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-127">The "USMF Sales" team is linked to the USMF business unit that was mentioned earlier.</span></span>
+ <span data-ttu-id="e1bdf-128">Proto mohou členové týmu USMF Sales zobrazit jakýkoli obchodní vztah, který je vlastněn uživatelem USMF DW, který by pocházel z tabulky společnosti USMF v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-128">Therefore, members of the "USMF Sales" team can see any account that is owned by the "USMF DW" user, which would have come from the USMF Company table in Finance and Operations.</span></span>

![Jak lze použít týmy](media/dual-write-company-2.png)

<span data-ttu-id="e1bdf-130">Jak ukazuje předchozí ilustrace, toto mapování 1:1 mezi organizační jednotkou, společností a týmem je pouze výchozím bodem.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-130">As the preceding illustration shows, this 1:1 mapping between business unit, company, and team is just a starting point.</span></span> <span data-ttu-id="e1bdf-131">V tomto příkladu je nová obchodní jednotka Europe vytvořena ručně v aplikaci Dataverse jako nadřazená pro DEMF i ESMF.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-131">In this example, a new "Europe" business unit is manually created in Dataverse as the parent for both DEMF and ESMF.</span></span> <span data-ttu-id="e1bdf-132">Tato nová kořenová organizační jednotka nesouvisí s dvojím zápisem.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-132">This new root business unit is unrelated to dual-write.</span></span> <span data-ttu-id="e1bdf-133">Lze ji však použít k tomu, aby členové týmu EUR Sales měli přístup k datům obchodních vztahů v DEMF i v ESMF nastavením viditelnosti dat na **Nadřazená/podřízená OJ** v přidružené roli zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-133">However, it can be used to give members of the "EUR Sales" team access to account data in both DEMF and ESMF by setting the data visibility to **Parent/Child BU** in the associated security role.</span></span>

<span data-ttu-id="e1bdf-134">Závěrečným tématem, které je třeba projednat, je jak dvojí zápis určuje, kterému týmu vlastníků se mají přiřadit řádky.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-134">A final topic to discuss is how dual-write determines which owner team it should assign rows to.</span></span> <span data-ttu-id="e1bdf-135">Toto chování je řízeno sloupcem **Výchozí vlastnící tým** na řádku cdm\_Company.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-135">This behavior is controlled by the **Default owning team** column on the cdm\_Company row.</span></span> <span data-ttu-id="e1bdf-136">Je-li pro řádek cdm\_Company povolen duální zápis, modul plug-in automaticky vytvoří přidruženou organizační jednotku a tým vlastníků (pokud již neexistuje) a nastaví sloupec **Výchozí vlastnící tým**.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-136">When a cdm\_Company row is enabled for dual-write, a plug-in automatically creates the associated business unit and owner team (if it doesn't already exist), and sets the **Default owning team** column.</span></span> <span data-ttu-id="e1bdf-137">Správce může tento sloupec změnit na jinou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-137">The admin can change this column to a different value.</span></span> <span data-ttu-id="e1bdf-138">Správce však nemůže vymazat sloupec, pokud je tabulka povolena pro duální zápis.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-138">However, the admin can't clear the column as long as the table is enabled for dual-write.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="e1bdf-139">![Sloupec výchozího vlastnícího týmu](media/dual-write-default-owning-team.jpg)</span><span class="sxs-lookup"><span data-stu-id="e1bdf-139">![Default owning team column](media/dual-write-default-owning-team.jpg)</span></span>

## <a name="company-striping-and-bootstrapping"></a><span data-ttu-id="e1bdf-140">Prokládání a zavádění společnosti</span><span class="sxs-lookup"><span data-stu-id="e1bdf-140">Company striping and bootstrapping</span></span>

<span data-ttu-id="e1bdf-141">Integrace Dataverse přináší paritu společnosti použitím identifikátoru společnosti k prokládání dat.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-141">Dataverse integration brings company parity by using a company identifier to stripe data.</span></span> <span data-ttu-id="e1bdf-142">Jak ukazuje následující ilustrace, všechny tabulky specifické pro společnost jsou rozšířeny tak, aby měly vztah N:1 s tabulkou cdm\_Company.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-142">As the following illustration shows, all company-specific tables are extended so that they have a many-to-one (N:1) relationship with the cdm\_Company table.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="e1bdf-143">![Vztah N:1 mezi tabulkou specifickou pro společnost a entitou cdm_Company](media/dual-write-bootstrapping.png)</span><span class="sxs-lookup"><span data-stu-id="e1bdf-143">![N:1 relationship between a company-specific table and the cdm_Company table](media/dual-write-bootstrapping.png)</span></span>

+ <span data-ttu-id="e1bdf-144">U řádků se po přidání a uložení společnosti hodnota změní na jen pro čtení.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-144">For rows, after a company is added and saved, the value becomes read-only.</span></span> <span data-ttu-id="e1bdf-145">Uživatelé by proto měli zajistit, aby vybrali správnou firmu.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-145">Therefore, users should make sure that they select the correct company.</span></span>
+ <span data-ttu-id="e1bdf-146">Pouze řádky s daty společnosti jsou způsobilé pro duální zápis mezi aplikací a Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-146">Only rows that have company data are eligible for dual-write between the application and Dataverse.</span></span>
+ <span data-ttu-id="e1bdf-147">Pro existující data Dataverse bude brzy k dispozici zaváděcí praxe vedená správcem.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-147">For existing Dataverse data, an admin-led bootstrapping experience will soon be available.</span></span>


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a><span data-ttu-id="e1bdf-148">Automatické vyplnění názvu společnosti v aplikacích pro zapojení zákazníků</span><span class="sxs-lookup"><span data-stu-id="e1bdf-148">Autopopulate company name in customer engagement apps</span></span>

<span data-ttu-id="e1bdf-149">Existuje několik způsobů, jak automaticky vyplnit název společnosti v aplikacích pro zapojení zákazníků.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-149">There are several ways to auto-populate the company name in customer engagement apps.</span></span>

+ <span data-ttu-id="e1bdf-150">Pokud jste správcem systému, můžete výchozí společnost nastavit přechodem na **Pokročilé nastavení > Systém > Zabezpečení > Uživatelé**.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-150">If you are a system administrator, you can set the default company by navigating to **Advanced Settings > System > Security > Users**.</span></span> <span data-ttu-id="e1bdf-151">Otevřete formulář **Uživatel** a v sekci **Informace o organizaci** nastavte hodnotu **Výchozí společnost ve Forms**.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-151">Open the **User** form, and in the **Organization Information** section, set the **Company to default on Forms** value.</span></span>

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="Nastavení výchozí společnosti v sekci Informace o organizaci.":::

+ <span data-ttu-id="e1bdf-153">Pokud máte oprávnění pro **zápis** v tabulce **Systémový uživatel** pro úroveň **Obchodní jednotka**, můžete výchozí společnost změnit v libovolném formuláři výběrem společnosti z rozevírací nabídky **Společnost**.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-153">If you have **Write** access to the **SystemUser** table for the **Business Unit** level, then you can change the default company on any form by selecting a company from the **Company** drop-down menu.</span></span>

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="Změna názvu společnosti pro nový účet.":::

+ <span data-ttu-id="e1bdf-155">Pokud máte oprávnění pro **zápis** v datech více než jedné společnosti, můžete výchozí společnost změnit výběrem řádku, který patří jiné společnosti.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-155">If you have **Write** access to data in more than one company, then you can change the default company by choosing a row that belongs to different company.</span></span>

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="Výběr řádku změní výchozí společnost.":::

+ <span data-ttu-id="e1bdf-157">Pokud jste konfigurátor nebo správce systému a chcete automaticky vyplnit data společnosti do vlastního formuláře, můžete použít [události formuláře](/powerapps/developer/model-driven-apps/clientapi/events-forms-grids).</span><span class="sxs-lookup"><span data-stu-id="e1bdf-157">If you are a system configurator or administrator, and you want to auto-populate company data on a custom form, then you can use [form events](/powerapps/developer/model-driven-apps/clientapi/events-forms-grids).</span></span> <span data-ttu-id="e1bdf-158">Přidejte odkaz na JavaScript do **msdyn_ / DefaultCompany.js** a použijte následující události.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-158">Add a JavaScript reference to **msdyn_/DefaultCompany.js** and use the following events.</span></span> <span data-ttu-id="e1bdf-159">Můžete použít jakýkoli předpřipravný formulář, například formulář **Účet**.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-159">You can use any out-of-the-box form, for example, the **Account** form.</span></span>

    + <span data-ttu-id="e1bdf-160">Událost **OnLoad** pro formulář: Nastavte sloupec **defaultCompany**.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-160">**OnLoad** event for the form: Set the **defaultCompany** column.</span></span>
    + <span data-ttu-id="e1bdf-161">Událost **OnChange** pro sloupec **Společnost**: Nastavte sloupec **updateDefaultCompany**.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-161">**OnChange** event for the **Company** column: Set the **updateDefaultCompany** column.</span></span>

## <a name="apply-filtering-based-on-the-company-context"></a><span data-ttu-id="e1bdf-162">Použití filtrování na základě kontextu společnosti</span><span class="sxs-lookup"><span data-stu-id="e1bdf-162">Apply filtering based on the company context</span></span>

<span data-ttu-id="e1bdf-163">Chcete-li použít filtrování na základě kontextu společnosti ve vlastních formulářích nebo ve vlastních vyhledávacích sloupcích přidaných do standardních formulářů, otevřete formulář a použijte sekci **Filtrování souvisejících záznamů** pro použití filtru společnosti.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-163">To apply filtering based on the company context on your custom forms or on custom lookup columns added to the standard forms, open the form and use the **Related Records Filtering** section to apply the company filter.</span></span> <span data-ttu-id="e1bdf-164">Tohle musíte pro každé vyhledávací sloupec, který vyžaduje filtrování na základě nejnižší společnosti v daném řádku.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-164">You must set this for each lookup column that requires filtering based on the underlying company on a given row.</span></span> <span data-ttu-id="e1bdf-165">Nastavení je zobrazeno pro **Účet** na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="e1bdf-165">The setting is shown for **Account** in the following illustration.</span></span>

:::image type="content" source="media/apply-company-context.png" alt-text="Použití kontextu společnosti":::



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]