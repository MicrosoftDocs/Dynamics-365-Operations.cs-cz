---
title: Export data z aplikací Attract a Onboard
description: Export data z aplikací Dynamics 365 Talent - Attract a Onboard.
author: andreabichsel
manager: AnnBe
ms.date: 01/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: eb97a16c15476c2f34ec581a32a677fa6fee8739
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460512"
---
# <a name="export-data-from-attract-and-onboard"></a><span data-ttu-id="647dd-103">Export data z aplikací Attract a Onboard</span><span class="sxs-lookup"><span data-stu-id="647dd-103">Export data from Attract and Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="647dd-104">Jak bylo ohlášeno v tématu [Vyřazení aplikací Dynamics 365 Talent: Attract a Dynamics 365 Talent: Onboard](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps), 1. února 2022 proběhne vyřazení aplikací Dynamics 365 Talent: Attract a Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="647dd-104">As announced in [Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps), we're retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard on February 1, 2022.</span></span> <span data-ttu-id="647dd-105">Chcete-li pomoci s migrací na jiný produkt, obě aplikace nyní poskytují možnosti exportu dat.</span><span class="sxs-lookup"><span data-stu-id="647dd-105">To help with your migration to another product, both apps now provide data export capabilities.</span></span>

## <a name="export-data-from-attract"></a><span data-ttu-id="647dd-106">Exportovat data z aplikace Attract</span><span class="sxs-lookup"><span data-stu-id="647dd-106">Export data from Attract</span></span>

<span data-ttu-id="647dd-107">Data můžete exportovat bez omezení přístupu k prostředí.</span><span class="sxs-lookup"><span data-stu-id="647dd-107">You can export your data without restricting access to your environment.</span></span> <span data-ttu-id="647dd-108">Tuto akci lze provést pro účely testování nebo pro pochopení struktury dat.</span><span class="sxs-lookup"><span data-stu-id="647dd-108">You might want to do this for testing purposes or to understand our data structure.</span></span> <span data-ttu-id="647dd-109">Až budete připraveni na migraci, omezte přístup k prostředí Attract podle pokynů v tomto postupu.</span><span class="sxs-lookup"><span data-stu-id="647dd-109">When you're ready to migrate, restrict access to your Attract environment using the instructions after this procedure.</span></span> <span data-ttu-id="647dd-110">Nezapomeňte data exportovat znovu.</span><span class="sxs-lookup"><span data-stu-id="647dd-110">Be sure to export your data again.</span></span> 

1. <span data-ttu-id="647dd-111">Přejděte na [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span><span class="sxs-lookup"><span data-stu-id="647dd-111">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="647dd-112">V části **Export dat** vyberte **Požádat o export dat**.</span><span class="sxs-lookup"><span data-stu-id="647dd-112">Under **Data export**, select **Request a data export**.</span></span>

   ![[<span data-ttu-id="647dd-113">Žádost o export data z aplikace Attract</span><span class="sxs-lookup"><span data-stu-id="647dd-113">Request a data export from Attract</span></span>](./media/attract-onboard-export-data-attract-request.png)](./media/attract-onboard-export-data-attract-request.png)

3. <span data-ttu-id="647dd-114">Jakmile se objeví zpráva **Váš požadavek se zpravovává**, vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="647dd-114">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="647dd-115">Export dat může trvat až 20 minut, v závislosti na velikosti exportu.</span><span class="sxs-lookup"><span data-stu-id="647dd-115">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="647dd-116">Po dokončení exportu vyberte tlačítko vedle **Stáhnout**.</span><span class="sxs-lookup"><span data-stu-id="647dd-116">When your export completes, select the **Download** button next to it.</span></span> 

   >[!NOTE]
   ><span data-ttu-id="647dd-117">Všechny exporty dat jsou k dispozici po dobu sedmi dnů, kdy vyprší platnost odkazu pro **Stažení**.</span><span class="sxs-lookup"><span data-stu-id="647dd-117">All data exports are available for seven days, at which point the **Download** link expires.</span></span></br>
   
<span data-ttu-id="647dd-118">Stahování obsahuje soubor. zip s daty Attract včetně následujících složek:</span><span class="sxs-lookup"><span data-stu-id="647dd-118">The download contains a .zip file with your Attract data, including the following folders:</span></span>

| <span data-ttu-id="647dd-119">Název složky</span><span class="sxs-lookup"><span data-stu-id="647dd-119">Folder name</span></span> | <span data-ttu-id="647dd-120">Popis</span><span class="sxs-lookup"><span data-stu-id="647dd-120">Description</span></span> |
| --- | --- |
| <span data-ttu-id="647dd-121">Nastavení pro správu</span><span class="sxs-lookup"><span data-stu-id="647dd-121">Admin settings</span></span> | <span data-ttu-id="647dd-122">Konfigurace centra správy Attract.</span><span class="sxs-lookup"><span data-stu-id="647dd-122">Attract admin center configurations.</span></span> |
| <span data-ttu-id="647dd-123">Kandidáti</span><span class="sxs-lookup"><span data-stu-id="647dd-123">Candidates</span></span> | <span data-ttu-id="647dd-124">Všichni kandidáti, kteří byli přidáni do projektů nebo fondů talent.</span><span class="sxs-lookup"><span data-stu-id="647dd-124">All candidates that were added to jobs or talent pools.</span></span> |
| <span data-ttu-id="647dd-125">Šablony e-mailů</span><span class="sxs-lookup"><span data-stu-id="647dd-125">Email templates</span></span> | <span data-ttu-id="647dd-126">Všechny e-mailové šablony, které byly nakonfigurovány pro prostředí.</span><span class="sxs-lookup"><span data-stu-id="647dd-126">All email templates that were configured for the environment.</span></span> |
| <span data-ttu-id="647dd-127">Šablony balíčku nabídky práce</span><span class="sxs-lookup"><span data-stu-id="647dd-127">Job offer package templates</span></span> | <span data-ttu-id="647dd-128">Všechny vytvořené šablony balíků nabídek práce spolu s přidruženými konfiguracemi.</span><span class="sxs-lookup"><span data-stu-id="647dd-128">All job offer package templates that were created, plus their associated configurations.</span></span> |
| <span data-ttu-id="647dd-129">Sady pravidel nabídek práce</span><span class="sxs-lookup"><span data-stu-id="647dd-129">Job offer rule sets</span></span> |  <span data-ttu-id="647dd-130">Všechny soubory sady pravidel, které byly odeslány pro správu nabídek.</span><span class="sxs-lookup"><span data-stu-id="647dd-130">All rule set files that were uploaded for offer management.</span></span> |
| <span data-ttu-id="647dd-131">Šablony nabídky práce</span><span class="sxs-lookup"><span data-stu-id="647dd-131">Job offer templates</span></span> | <span data-ttu-id="647dd-132">Všechny šablony dokumentů nabídek práce jsou vytvořeny pro prostředí.</span><span class="sxs-lookup"><span data-stu-id="647dd-132">All job offer document templates created for the environment.</span></span> |
| <span data-ttu-id="647dd-133">Volná pracovní místa</span><span class="sxs-lookup"><span data-stu-id="647dd-133">Job openings</span></span> | <span data-ttu-id="647dd-134">Všechna vytvořená pracovní místa.</span><span class="sxs-lookup"><span data-stu-id="647dd-134">All created jobs.</span></span> <span data-ttu-id="647dd-135">Odstraněné práce nejsou exportovány.</span><span class="sxs-lookup"><span data-stu-id="647dd-135">Deleted jobs aren't exported.</span></span> <span data-ttu-id="647dd-136">Podsložky obsahují kandidátské žádosti, u nichž jsou dílčí složky pro přílohy kandidáta aplikace a balíčky nabídek, kde je to vhodné.</span><span class="sxs-lookup"><span data-stu-id="647dd-136">The sub-folders contain candidate applications, with sub-folders for candidate application attachments and offer packages, where applicable.</span></span> |
| <span data-ttu-id="647dd-137">Šablony volných pracovních míst</span><span class="sxs-lookup"><span data-stu-id="647dd-137">Job opening templates</span></span> | <span data-ttu-id="647dd-138">Šablony procesů nabídek práce, které byly nakonfigurovány v prostředí.</span><span class="sxs-lookup"><span data-stu-id="647dd-138">Job process templates that were configured in the environment.</span></span> |
| <span data-ttu-id="647dd-139">Skupiny talentů</span><span class="sxs-lookup"><span data-stu-id="647dd-139">Talent pools</span></span> | <span data-ttu-id="647dd-140">Všechny vytvořené skupiny talentů, jejich seznamy přispěvatelů a seznamy kandidátů pro skupiny talentů.</span><span class="sxs-lookup"><span data-stu-id="647dd-140">All created talent pools, their contributors lists, and the candidates lists for the talent pools.</span></span> |
| <span data-ttu-id="647dd-141">Pracovníci</span><span class="sxs-lookup"><span data-stu-id="647dd-141">Workers</span></span> | <span data-ttu-id="647dd-142">Seznam všech pracovníků přítomných v prostředí a jejich rolí.</span><span class="sxs-lookup"><span data-stu-id="647dd-142">List of all the workers who are present in the environment, plus their roles.</span></span> |
| <span data-ttu-id="647dd-143">(kořenová složka)</span><span class="sxs-lookup"><span data-stu-id="647dd-143">(root folder)</span></span> | <span data-ttu-id="647dd-144">Soubor schématu JSON, který popisuje pole struktury dat.</span><span class="sxs-lookup"><span data-stu-id="647dd-144">A JSON schema file that describes the data structure fields.</span></span> |

### <a name="restrict-access-to-attract"></a><span data-ttu-id="647dd-145">Omezit přístup k Attract</span><span class="sxs-lookup"><span data-stu-id="647dd-145">Restrict access to Attract</span></span>

<span data-ttu-id="647dd-146">Jakmile budete připraveni na migraci, omezte přístup uživatelů, kteří nepatří k prostředí Attract, a exportujte data.</span><span class="sxs-lookup"><span data-stu-id="647dd-146">When you're ready to migrate, restrict non-admins from accessing your Attract environment and export your data.</span></span>

>[!IMPORTANT]
><span data-ttu-id="647dd-147">Omezení přístupu k prostředí Attract je trvalé a nelze je vrátit zpět.</span><span class="sxs-lookup"><span data-stu-id="647dd-147">Restricting access to your Attract environment is permanent and can't be undone.</span></span> <span data-ttu-id="647dd-148">Chcete-li pokračovat v přístupu k prostředí, můžete tento krok přeskočit.</span><span class="sxs-lookup"><span data-stu-id="647dd-148">If you want non-admin users to continue accessing your environment, skip this step.</span></span>

1. <span data-ttu-id="647dd-149">Přejděte na [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span><span class="sxs-lookup"><span data-stu-id="647dd-149">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="647dd-150">Chcete-li omezit přístup nesprávců k vašemu prostředí Attract v rámci **Omezení přístupu k této aplikaci**, vyberte **Omezit přístup nyní**.</span><span class="sxs-lookup"><span data-stu-id="647dd-150">To restrict non-admins from accessing your Attract environment, under **Restrict access to this app**, select **Restrict access now**.</span></span> <span data-ttu-id="647dd-151">Omezením přístupu také zmizí všechny aktivní nabídky práce, které byly zveřejněny.</span><span class="sxs-lookup"><span data-stu-id="647dd-151">Restricting access also unposts any active jobs that have been posted.</span></span>

   ![[<span data-ttu-id="647dd-152">Omezit přístup nesprávců k Attract</span><span class="sxs-lookup"><span data-stu-id="647dd-152">Restrict non-admin access to Attract</span></span>](./media/attract-onboard-export-data-attract-restrict-access.png)](./media/attract-onboard-export-data-attract-restrict-access.png)

3. <span data-ttu-id="647dd-153">Pokud se zobrazí upozornění **Jedná o trvalou změnu změnu**, vyberte **Omezit přístup** k trvalému omezení přístupu uživatelů bez oprávnění správce do tohoto prostředí.</span><span class="sxs-lookup"><span data-stu-id="647dd-153">When you see the warning **This is a permanent change**, select **Restrict access** to permanently restrict non-admin users from this environment.</span></span> <span data-ttu-id="647dd-154">Nejste-li připraveni dokončit tento krok, vyberte možnost **Storno**.</span><span class="sxs-lookup"><span data-stu-id="647dd-154">If you're not ready to complete this step, select **Cancel**.</span></span>

   ![[<span data-ttu-id="647dd-155">Upozornění, že omezení přístupu je trvalá změna</span><span class="sxs-lookup"><span data-stu-id="647dd-155">Warning that restricting access is a permanent change</span></span>](./media/attract-onboard-export-data-attract-warning.png)](./media/attract-onboard-export-data-attract-warning.png)

   >[!NOTE]
   ><span data-ttu-id="647dd-156">Správci mohou po omezení přístupu k prostředí Attract i nadále přistupovat ke stránkám exportu dat a sestav osob.</span><span class="sxs-lookup"><span data-stu-id="647dd-156">Admins can continue to access the data export and person report pages after you restrict access to the Attract environment.</span></span>

## <a name="export-data-from-onboard"></a><span data-ttu-id="647dd-157">Exportovat data z aplikace Onboard</span><span class="sxs-lookup"><span data-stu-id="647dd-157">Export data from Onboard</span></span>

<span data-ttu-id="647dd-158">Až budete připraveni, můžete stáhnout šablony, příručky a data kandidátý z Onboard.</span><span class="sxs-lookup"><span data-stu-id="647dd-158">When you're ready, you can download templates, guides, and candidate data from Onboard.</span></span>

1. <span data-ttu-id="647dd-159">Přejděte na [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).</span><span class="sxs-lookup"><span data-stu-id="647dd-159">Go to [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).</span></span>

2. <span data-ttu-id="647dd-160">V části **Export dat** vyberte **Požádat o export dat**.</span><span class="sxs-lookup"><span data-stu-id="647dd-160">Under **Data export**, select **Request a data export**.</span></span> 

   ![[<span data-ttu-id="647dd-161">Žádost o export data z aplikace Onboard</span><span class="sxs-lookup"><span data-stu-id="647dd-161">Request a data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-request.png)](./media/attract-onboard-export-data-onboard-request.png)

3. <span data-ttu-id="647dd-162">Jakmile se objeví zpráva **Váš požadavek se zpravovává**, vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="647dd-162">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="647dd-163">Export dat může trvat až 20 minut, v závislosti na velikosti exportu.</span><span class="sxs-lookup"><span data-stu-id="647dd-163">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="647dd-164">Po dokončení exportu vyberte tlačítko vedle **Stáhnout**.</span><span class="sxs-lookup"><span data-stu-id="647dd-164">When your export completes, select the **Download** button next to it.</span></span> 

   ![[<span data-ttu-id="647dd-165">Stáhnout export dat z aplikace Onboard</span><span class="sxs-lookup"><span data-stu-id="647dd-165">Download data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-download.png)](./media/attract-onboard-export-data-onboard-download.png)

   >[!NOTE]
   ><span data-ttu-id="647dd-166">Export dat je k dispozici po sedm dní.</span><span class="sxs-lookup"><span data-stu-id="647dd-166">Your data export is available for seven days.</span></span> <span data-ttu-id="647dd-167">Po sedmi dnech vyprší platnost odkazu **Stažení** a je nutné požádat o nový export v případě, že je nutné data stáhnout znovu.</span><span class="sxs-lookup"><span data-stu-id="647dd-167">After seven days, the **Download** link expires, and you must request a new export if you need to download your data again.</span></span> <span data-ttu-id="647dd-168">Když spustíte nový export dat, platnost stávajících stahování skončí po úspěšném dokončení nového exportu.</span><span class="sxs-lookup"><span data-stu-id="647dd-168">When you start a new data export, any existing downloads will expire after the new export succeeds.</span></span>

<span data-ttu-id="647dd-169">Stahování je soubor zip, který obsahuje:</span><span class="sxs-lookup"><span data-stu-id="647dd-169">The download is a .zip file that contains:</span></span>

- <span data-ttu-id="647dd-170">Složku **Šablony**, která obsahuje šablony Onboard ve formátu dokumentu aplikace Word.</span><span class="sxs-lookup"><span data-stu-id="647dd-170">A **Templates** folder that contains your Onboard templates in Word document format.</span></span>

- <span data-ttu-id="647dd-171">Složku **Průvodci**, která obsahuje průvodce Onboard ve formátu dokumentu aplikace Word.</span><span class="sxs-lookup"><span data-stu-id="647dd-171">A **Guides** folder that contains your Onboard guides in Word document format.</span></span>

## <a name="see-also"></a><span data-ttu-id="647dd-172">Viz také</span><span class="sxs-lookup"><span data-stu-id="647dd-172">See also</span></span>

[<span data-ttu-id="647dd-173">Vyřazení aplikací Dynamics 365 Talent: Attract a Dynamics 365 Talent: Onboard</span><span class="sxs-lookup"><span data-stu-id="647dd-173">Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)