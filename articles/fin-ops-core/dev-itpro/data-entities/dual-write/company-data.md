---
title: Koncept společnosti v Dataverse
description: Toto téma popisuje integraci dat společností mezi aplikacemi Finance and Operations a Dataverse.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 2f0e3950f2b35dd8b8dbf50601b7d6b6d624863e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683668"
---
# <a name="company-concept-in-dataverse"></a><span data-ttu-id="edaeb-103">Koncept společnosti v Dataverse</span><span class="sxs-lookup"><span data-stu-id="edaeb-103">Company concept in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


<span data-ttu-id="edaeb-104">Koncept *společnosti* v Finance and Operations je právní i obchodní konstrukt.</span><span class="sxs-lookup"><span data-stu-id="edaeb-104">In Finance and Operations, the concept of a *company* is both a legal construct and a business construct.</span></span> <span data-ttu-id="edaeb-105">Je to také hranice pro zabezpečení a viditelnost dat.</span><span class="sxs-lookup"><span data-stu-id="edaeb-105">It's also a security and visibility boundary for data.</span></span> <span data-ttu-id="edaeb-106">Uživatelé pracují vždy v kontextu jedné společnosti a většina dat je rozdělena podle společnosti.</span><span class="sxs-lookup"><span data-stu-id="edaeb-106">Users always work in the context of a single company, and most of the data is striped by company.</span></span>

<span data-ttu-id="edaeb-107">Dataverse nemá ekvivalentní koncepci.</span><span class="sxs-lookup"><span data-stu-id="edaeb-107">Dataverse doesn't have an equivalent concept.</span></span> <span data-ttu-id="edaeb-108">Nejbližší koncept je *organizační jednotka*, která je primárně hranicí zabezpečení a viditelnosti pro uživatelská data.</span><span class="sxs-lookup"><span data-stu-id="edaeb-108">The closest concept is *business unit*, which is primarily a security and visibility boundary for user data.</span></span> <span data-ttu-id="edaeb-109">Tento koncept nemá stejné právní nebo obchodní důsledky jako koncepce společnosti.</span><span class="sxs-lookup"><span data-stu-id="edaeb-109">This concept doesn't have the same legal or business implications as the company concept.</span></span>

<span data-ttu-id="edaeb-110">Vzhledem k tomu, že organizační jednotka a společnost nejsou rovnocennými koncepty, není možné vynutit mapování mezi nimi (1:1) pro účely integrace Dataverse.</span><span class="sxs-lookup"><span data-stu-id="edaeb-110">Because business unit and company aren't equivalent concepts, it isn't possible to force a one-to-one (1:1) mapping between them for the purpose of Dataverse integration.</span></span> <span data-ttu-id="edaeb-111">Protože však uživatelé musí mít ve výchozím nastavení možnost zobrazit stejné řádky v aplikaci a Dataverse, společnost Microsoft zavedla novou entitu v aplikaci Dataverse s názvem cdm\_Company.</span><span class="sxs-lookup"><span data-stu-id="edaeb-111">However, because users must, by default, be able to see the same rows in the application and Dataverse, Microsoft has introduced a new entity in Dataverse that is named cdm\_Company.</span></span> <span data-ttu-id="edaeb-112">Tato entita je ekvivalentní s entitou společnosti v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="edaeb-112">This entity is equivalent to the Company entity in the application.</span></span> <span data-ttu-id="edaeb-113">Chcete-li zajistit, aby viditelnost řádků byla ekvivalentní mezi aplikací a Dataverse, doporučujeme následující nastavení dat v aplikaci Dataverse:</span><span class="sxs-lookup"><span data-stu-id="edaeb-113">To help guarantee that visibility of rows is equivalent between the application and Dataverse out of the box, we recommend the following setup for data in Dataverse:</span></span>

+ <span data-ttu-id="edaeb-114">Pro každý řádek společnosti Finance and Operations, který je povolen pro duální zápis, je vytvořen přidružený řádek cdm\_Company.</span><span class="sxs-lookup"><span data-stu-id="edaeb-114">For each Finance and Operations Company row that is enabled for dual-write, an associated cdm\_Company row is created.</span></span>
+ <span data-ttu-id="edaeb-115">Když je vytvořen řádek cdm\_Company a je povolen pro duální zápis, je vytvořena výchozí organizační jednotka se stejným názvem.</span><span class="sxs-lookup"><span data-stu-id="edaeb-115">When a cdm\_Company row is created and enabled for dual-write, a default business unit is created that has the same name.</span></span> <span data-ttu-id="edaeb-116">Přestože je pro tuto organizační jednotku automaticky vytvořen výchozí tým, není tato organizační jednotka použita.</span><span class="sxs-lookup"><span data-stu-id="edaeb-116">Although a default team is automatically created for that business unit, the business unit isn't used.</span></span>
+ <span data-ttu-id="edaeb-117">Je vytvořen samostatný tým vlastníků se stejným názvem.</span><span class="sxs-lookup"><span data-stu-id="edaeb-117">A separate owner team is created that has the same name.</span></span> <span data-ttu-id="edaeb-118">Je také spojen s organizační jednotkou.</span><span class="sxs-lookup"><span data-stu-id="edaeb-118">It's also associated with the business unit.</span></span>
+ <span data-ttu-id="edaeb-119">Ve výchozím nastavení je vlastník libovolného řádku vytvořeného a dvojitě zapsaného do Dataverse nastaven na tým "DW Owner", který je propojen s přidruženou organizační jednotkou.</span><span class="sxs-lookup"><span data-stu-id="edaeb-119">By default, the owner of any row that is created and dual-written to Dataverse is set to the "DW Owner" team that is linked to the associated business unit.</span></span>

<span data-ttu-id="edaeb-120">Následující obrázek znázorňuje příklad nastavení dat v Dataverse.</span><span class="sxs-lookup"><span data-stu-id="edaeb-120">The following illustration shows an example of this data setup in Dataverse.</span></span>

![Nastavení dat v Dataverse](media/dual-write-company-1.png)

<span data-ttu-id="edaeb-122">Z důvodu této konfigurace bude každý řádek, který se týká společnosti USMF, vlastněn týmem, který je propojen s organizační jednotkou USMF v aplikaci Dataverse.</span><span class="sxs-lookup"><span data-stu-id="edaeb-122">Because of this configuration, any row that is related to the USMF company will be owned by a team that is linked to the USMF business unit in Dataverse.</span></span> <span data-ttu-id="edaeb-123">Každý uživatel, který má přístup k této organizační jednotce prostřednictvím role zabezpečení nastavené na zobrazení na úrovni organizační jednotky, je tedy nyní schopen tyto řádky zobrazit.</span><span class="sxs-lookup"><span data-stu-id="edaeb-123">Therefore, any user who has access to that business unit through a security role that is set to business unit–level visibility can now see those rows.</span></span> <span data-ttu-id="edaeb-124">Následující příklad ukazuje, jak lze týmy použít k zajištění správného přístupu k těmto řádkům.</span><span class="sxs-lookup"><span data-stu-id="edaeb-124">The following example shows how teams can be used to provide the correct access to those rows.</span></span>

+ <span data-ttu-id="edaeb-125">Role Manažer prodeje je přidělena členům týmu USMF Sales.</span><span class="sxs-lookup"><span data-stu-id="edaeb-125">The "Sales Manager" role is assigned to members of the "USMF Sales" team.</span></span>
+ <span data-ttu-id="edaeb-126">Uživatelé, kteří mají roli manažer prodeje, mohou přistupovat ke všem řádkům obchodních vztahů, které jsou členy stejné organizační jednotky, v níž jsou členy.</span><span class="sxs-lookup"><span data-stu-id="edaeb-126">Users who have the "Sales Manager" role can access any account rows that are members of the same business unit that they are members of.</span></span>
+ <span data-ttu-id="edaeb-127">Tým USMF Sales je propojen s dříve uvedenou organizační jednotkou USMF.</span><span class="sxs-lookup"><span data-stu-id="edaeb-127">The "USMF Sales" team is linked to the USMF business unit that was mentioned earlier.</span></span>
+ <span data-ttu-id="edaeb-128">Proto mohou členové týmu USMF Sales zobrazit jakýkoli obchodní vztah, který je vlastněn uživatelem USMF DW, který by pocházel z entity společnosti USMF v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="edaeb-128">Therefore, members of the "USMF Sales" team can see any account that is owned by the "USMF DW" user, which would have come from the USMF Company entity in Finance and Operations.</span></span>

![Jak lze použít týmy](media/dual-write-company-2.png)

<span data-ttu-id="edaeb-130">Jak ukazuje předchozí ilustrace, toto mapování 1:1 mezi organizační jednotkou, společností a týmem je pouze výchozím bodem.</span><span class="sxs-lookup"><span data-stu-id="edaeb-130">As the preceding illustration shows, this 1:1 mapping between business unit, company, and team is just a starting point.</span></span> <span data-ttu-id="edaeb-131">V tomto příkladu je nová obchodní jednotka Europe vytvořena ručně v aplikaci Dataverse jako nadřazená pro DEMF i ESMF.</span><span class="sxs-lookup"><span data-stu-id="edaeb-131">In this example, a new "Europe" business unit is manually created in Dataverse as the parent for both DEMF and ESMF.</span></span> <span data-ttu-id="edaeb-132">Tato nová kořenová organizační jednotka nesouvisí s dvojím zápisem.</span><span class="sxs-lookup"><span data-stu-id="edaeb-132">This new root business unit is unrelated to dual-write.</span></span> <span data-ttu-id="edaeb-133">Lze ji však použít k tomu, aby členové týmu EUR Sales měli přístup k datům obchodních vztahů v DEMF i v ESMF nastavením viditelnosti dat na **Nadřazená/podřízená OJ** v přidružené roli zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="edaeb-133">However, it can be used to give members of the "EUR Sales" team access to account data in both DEMF and ESMF by setting the data visibility to **Parent/Child BU** in the associated security role.</span></span>

<span data-ttu-id="edaeb-134">Závěrečným tématem, které je třeba projednat, je jak dvojí zápis určuje, kterému týmu vlastníků se mají přiřadit řádky.</span><span class="sxs-lookup"><span data-stu-id="edaeb-134">A final topic to discuss is how dual-write determines which owner team it should assign rows to.</span></span> <span data-ttu-id="edaeb-135">Toto chování je řízeno polem **Výchozí vlastnící tým** v řádku cdm\_Company.</span><span class="sxs-lookup"><span data-stu-id="edaeb-135">This behavior is controlled by the **Default owning team** field on the cdm\_Company row.</span></span> <span data-ttu-id="edaeb-136">Je-li pro řádek cdm\_Company povolen duální zápis, modul plug-in automaticky vytvoří přidruženou organizační jednotku a tým vlastníků (pokud již neexistuje) a nastaví pole **Výchozí vlastnící tým**.</span><span class="sxs-lookup"><span data-stu-id="edaeb-136">When a cdm\_Company row is enabled for dual-write, a plug-in automatically creates the associated business unit and owner team (if it doesn't already exist), and sets the **Default owning team** field.</span></span> <span data-ttu-id="edaeb-137">Správce může toto pole změnit na jinou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="edaeb-137">The admin can change this field to a different value.</span></span> <span data-ttu-id="edaeb-138">Správce však nemůže vymazat pole, pokud je entita povolena pro duální zápis.</span><span class="sxs-lookup"><span data-stu-id="edaeb-138">However, the admin can't clear the field as long as the entity is enabled for dual-write.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="edaeb-139">![Pole výchozího vlastnícího týmu](media/dual-write-default-owning-team.jpg)</span><span class="sxs-lookup"><span data-stu-id="edaeb-139">![Default owning team field](media/dual-write-default-owning-team.jpg)</span></span>

## <a name="company-striping-and-bootstrapping"></a><span data-ttu-id="edaeb-140">Prokládání a zavádění společnosti</span><span class="sxs-lookup"><span data-stu-id="edaeb-140">Company striping and bootstrapping</span></span>

<span data-ttu-id="edaeb-141">Integrace Dataverse přináší paritu společnosti použitím identifikátoru společnosti k prokládání dat.</span><span class="sxs-lookup"><span data-stu-id="edaeb-141">Dataverse integration brings company parity by using a company identifier to stripe data.</span></span> <span data-ttu-id="edaeb-142">Jak ukazuje následující ilustrace, všechny tabulky specifické pro společnost jsou rozšířeny tak, aby měly vztah N:1 s entitou cdm\_Company.</span><span class="sxs-lookup"><span data-stu-id="edaeb-142">As the following illustration shows, all company-specific tables are extended so that they have a many-to-one (N:1) relationship with the cdm\_Company entity.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="edaeb-143">![Vztah N:1 mezi entitou specifickou pro společnost a entitou cdm_Company](media/dual-write-bootstrapping.png)</span><span class="sxs-lookup"><span data-stu-id="edaeb-143">![N:1 relationship between a company-specific entity and the cdm_Company entity](media/dual-write-bootstrapping.png)</span></span>

+ <span data-ttu-id="edaeb-144">U řádků se po přidání a uložení společnosti hodnota změní na jen pro čtení.</span><span class="sxs-lookup"><span data-stu-id="edaeb-144">For rows, after a company is added and saved, the value becomes read-only.</span></span> <span data-ttu-id="edaeb-145">Uživatelé by proto měli zajistit, aby vybrali správnou firmu.</span><span class="sxs-lookup"><span data-stu-id="edaeb-145">Therefore, users should make sure that they select the correct company.</span></span>
+ <span data-ttu-id="edaeb-146">Pouze řádky s daty společnosti jsou způsobilé pro duální zápis mezi aplikací a Dataverse.</span><span class="sxs-lookup"><span data-stu-id="edaeb-146">Only rows that have company data are eligible for dual-write between the application and Dataverse.</span></span>
+ <span data-ttu-id="edaeb-147">Pro existující data Dataverse bude brzy k dispozici zaváděcí praxe vedená správcem.</span><span class="sxs-lookup"><span data-stu-id="edaeb-147">For existing Dataverse data, an admin-led bootstrapping experience will soon be available.</span></span>


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a><span data-ttu-id="edaeb-148">Automatické vyplnění názvu společnosti v aplikacích pro zapojení zákazníků</span><span class="sxs-lookup"><span data-stu-id="edaeb-148">Autopopulate company name in customer engagement apps</span></span>

<span data-ttu-id="edaeb-149">Existuje několik způsobů, jak automaticky vyplnit název společnosti v aplikacích pro zapojení zákazníků.</span><span class="sxs-lookup"><span data-stu-id="edaeb-149">There are several ways to auto-populate the company name in customer engagement apps.</span></span>

+ <span data-ttu-id="edaeb-150">Pokud jste správcem systému, můžete výchozí společnost nastavit přechodem na **Pokročilé nastavení > Systém > Zabezpečení > Uživatelé**.</span><span class="sxs-lookup"><span data-stu-id="edaeb-150">If you are a system administrator, you can set the default company by navigating to **Advanced Settings > System > Security > Users**.</span></span> <span data-ttu-id="edaeb-151">Otevřete formulář **Uživatel** a v sekci **Informace o organizaci** nastavte hodnotu **Výchozí společnost ve Forms**.</span><span class="sxs-lookup"><span data-stu-id="edaeb-151">Open the **User** form, and in the **Organization Information** section, set the **Company to default on Forms** value.</span></span>

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="Nastavení výchozí společnosti v sekci Informace o organizaci.":::

+ <span data-ttu-id="edaeb-153">Pokud máte oprávnění pro **zápis** v entitě **Systémový uživatel** pro úroveň **Obchodní jednotka**, můžete výchozí společnost změnit v libovolném formuláři výběrem společnosti z rozevírací nabídky **Společnost**.</span><span class="sxs-lookup"><span data-stu-id="edaeb-153">If you have **Write** access to the **SystemUser** entity for the **Business Unit** level, then you can change the default company on any form by selecting a company from the **Company** drop-down menu.</span></span>

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="Změna názvu společnosti pro nový účet.":::

+ <span data-ttu-id="edaeb-155">Pokud máte oprávnění pro **zápis** v datech více než jedné společnosti, můžete výchozí společnost změnit výběrem řádku, který patří jiné společnosti.</span><span class="sxs-lookup"><span data-stu-id="edaeb-155">If you have **Write** access to data in more than one company, then you can change the default company by choosing a row that belongs to different company.</span></span>

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="Výběr řádku změní výchozí společnost.":::

+ <span data-ttu-id="edaeb-157">Pokud jste konfigurátor nebo správce systému a chcete automaticky vyplnit data společnosti do vlastního formuláře, můžete použít [události formuláře](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids).</span><span class="sxs-lookup"><span data-stu-id="edaeb-157">If you are a system configurator or administrator, and you want to auto-populate company data on a custom form, then you can use [form events](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids).</span></span> <span data-ttu-id="edaeb-158">Přidejte odkaz na JavaScript do **msdyn_ / DefaultCompany.js** a použijte následující události.</span><span class="sxs-lookup"><span data-stu-id="edaeb-158">Add a JavaScript reference to **msdyn_/DefaultCompany.js** and use the following events.</span></span> <span data-ttu-id="edaeb-159">Můžete použít jakýkoli předpřipravný formulář, například formulář **Účet**.</span><span class="sxs-lookup"><span data-stu-id="edaeb-159">You can use any out-of-the-box form, for example, the **Account** form.</span></span>

    + <span data-ttu-id="edaeb-160">Událost **OnLoad** pro formulář: Nastavte pole **defaultCompany**.</span><span class="sxs-lookup"><span data-stu-id="edaeb-160">**OnLoad** event for the form: Set the **defaultCompany** field.</span></span>
    + <span data-ttu-id="edaeb-161">Událost **OnChange** pro pole **Společnost**: Nastavte pole **updateDefaultCompany**.</span><span class="sxs-lookup"><span data-stu-id="edaeb-161">**OnChange** event for the **Company** field: Set the **updateDefaultCompany** field.</span></span>

## <a name="apply-filtering-based-on-the-company-context"></a><span data-ttu-id="edaeb-162">Použití filtrování na základě kontextu společnosti</span><span class="sxs-lookup"><span data-stu-id="edaeb-162">Apply filtering based on the company context</span></span>

<span data-ttu-id="edaeb-163">Chcete-li použít filtrování na základě kontextu společnosti ve vlastních formulářích nebo ve vlastních vyhledávacích polích přidaných do standardních formulářů, otevřete formulář a použijte sekci **Filtrování souvisejících záznamů** pro použití filtru společnosti.</span><span class="sxs-lookup"><span data-stu-id="edaeb-163">To apply filtering based on the company context on your custom forms or on custom lookup fields added to the standard forms, open the form and use the **Related Records Filtering** section to apply the company filter.</span></span> <span data-ttu-id="edaeb-164">Tohle musíte pro každé vyhledávací pole, které vyžaduje filtrování na základě nejnižší společnosti v daném řádku.</span><span class="sxs-lookup"><span data-stu-id="edaeb-164">You must set this for each lookup field that requires filtering based on the underlying company on a given row.</span></span> <span data-ttu-id="edaeb-165">Nastavení je zobrazeno pro **Účet** na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="edaeb-165">The setting is shown for **Account** in the following illustration.</span></span>

:::image type="content" source="media/apply-company-context.png" alt-text="Použití kontextu společnosti":::

