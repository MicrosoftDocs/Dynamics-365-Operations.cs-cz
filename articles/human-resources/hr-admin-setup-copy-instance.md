---
title: Kopírovat instanci
description: Pomocí služby Microsoft Dynamics Lifecycle Services (LCS) můžete kopírovat databázi Microsoft Dynamics 365 Human Resources do prostředí izolovaného prostoru (sandbox).
author: andreabichsel
manager: AnnBe
ms.date: 07/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6b52b696d323df6bafead2418ae322d1a9cdf64a
ms.sourcegitcommit: ec4df354602c20f48f8581bfe5be0c04c66d2927
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/19/2020
ms.locfileid: "3706221"
---
# <a name="copy-an-instance"></a><span data-ttu-id="fa4ff-103">Kopírovat instanci</span><span class="sxs-lookup"><span data-stu-id="fa4ff-103">Copy an instance</span></span>

<span data-ttu-id="fa4ff-104">Pomocí služby Microsoft Dynamics Lifecycle Services (LCS) můžete kopírovat databázi Microsoft Dynamics 365 Human Resources do prostředí izolovaného prostoru (sandbox).</span><span class="sxs-lookup"><span data-stu-id="fa4ff-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="fa4ff-105">Máte-li jiné prostředí izolovaného prostoru (sandbox), můžete také zkopírovat databázi z prostředí do cíleného prostředí sandbox.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-105">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="fa4ff-106">Při kopírování instance mějte na paměti následující tipy:</span><span class="sxs-lookup"><span data-stu-id="fa4ff-106">To copy an instance, keep the following tips in mind:</span></span>

- <span data-ttu-id="fa4ff-107">Instance aplikace Human Resources, kterou chcete přepsat, musí být prostředí izolovaného prostoru (sandbox).</span><span class="sxs-lookup"><span data-stu-id="fa4ff-107">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="fa4ff-108">Prostředí, ze kterých a do kterých kopírujete, musí být ve stejné oblasti.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-108">The environments you're copying from and to must be in the same region.</span></span> <span data-ttu-id="fa4ff-109">Nelze kopírovat mezi oblastmi.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-109">You can't copy across regions.</span></span>

- <span data-ttu-id="fa4ff-110">Musíte být správcem cílového prostředí, abyste se k němu mohli po zkopírování instance přihlásit.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-110">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="fa4ff-111">Při kopírování databáze aplikace Human Resources nejsou zkopírovány prvky (aplikace nebo data), které jsou obsaženy v prostředí Microsoft Power Apps.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-111">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft Power Apps environment.</span></span> <span data-ttu-id="fa4ff-112">Informace o tom, jak kopírovat prvky do prostředí Power Apps, naleznete v tématu [kopírování prostředí](https://docs.microsoft.com/power-platform/admin/copy-environment).</span><span class="sxs-lookup"><span data-stu-id="fa4ff-112">For information about how to copy elements in a Power Apps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="fa4ff-113">Prostředí Power Apps, které chcete přepsat, musí být prostředí izolovaného prostoru (sandbox).</span><span class="sxs-lookup"><span data-stu-id="fa4ff-113">The Power Apps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="fa4ff-114">Chcete-li změnit produkční prostředí Power Apps na prostředí s izolovaným prostorem, musíte být globálním správcem klienta.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-114">You must be a global tenant admin to change a Power Apps production environment to a sandbox environment.</span></span> <span data-ttu-id="fa4ff-115">Další informace o změně prostředí Power Apps naleznete v tématu [přepnutí instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span><span class="sxs-lookup"><span data-stu-id="fa4ff-115">For more information about changing a Power Apps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

- <span data-ttu-id="fa4ff-116">Pokud zkopírujete instanci do prostředí sandbox a chcete integrovat prostředí sandbox s Common Data Service, musíte znovu použít vlastní pole na entity Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-116">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Common Data Service, you must reapply custom fields to Common Data Service entities.</span></span> <span data-ttu-id="fa4ff-117">Viz [Použití vlastních polí na Common Data Service](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).</span><span class="sxs-lookup"><span data-stu-id="fa4ff-117">See [Apply custom fields to Common Data Service](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="fa4ff-118">Vliv kopírování databáze aplikace Human Resources</span><span class="sxs-lookup"><span data-stu-id="fa4ff-118">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="fa4ff-119">Při kopírování databáze aplikace Human Resources dojde k následujícím událostem:</span><span class="sxs-lookup"><span data-stu-id="fa4ff-119">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="fa4ff-120">Při kopírování bude existující databáze vymazána v cílovém prostředí.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-120">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="fa4ff-121">Po dokončení kopírování nelze stávající databázi obnovit.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-121">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="fa4ff-122">Cílové prostředí nebude k dispozici, dokud nebude proces kopírování dokončen.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-122">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="fa4ff-123">Dokumenty v úložišti objektů BLOB Microsoft Azure nejsou kopírovány z jednoho prostředí do jiného.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-123">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="fa4ff-124">Ve výsledku nebudou žádné připojené dokumenty a šablony, které jsou připojeny, zkopírovány a zůstanou ve zdrojovém prostředí.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-124">As a result, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="fa4ff-125">Všichni uživatelé, kromě správce a ostatních interních uživatelských účtů služby budou nedostupní.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-125">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="fa4ff-126">Správce může odstranit nebo zamlžit data před tím, než se budou moci ostatní uživatelé vrátit do systému.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-126">The Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="fa4ff-127">Uživatel s oprávněními správce musí provést požadované změny konfigurace, například opětovné připojení koncových bodů integrace pro určité služby nebo adresy URL.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-127">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="fa4ff-128">Kopírování databáze aplikace Human Resources</span><span class="sxs-lookup"><span data-stu-id="fa4ff-128">Copy the Human Resources database</span></span>

<span data-ttu-id="fa4ff-129">Chcete-li dokončit tento úkol, nejprve zkopírujte instanci a poté se přihlaste do centra pro správu Microsoft Power Platform a zkopírujte vaše prostředí Power Apps.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-129">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your Power Apps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="fa4ff-130">Při kopírování instance je databáze vymazána v cílové instanci.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-130">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="fa4ff-131">Cílová instance není během tohoto procesu k dispozici.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-131">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="fa4ff-132">Přihlaste se k LCS a vyberte projekt LCS obsahující instanci, kterou chcete zkopírovat.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-132">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="fa4ff-133">Ve svém LCS projektu vyberte dlaždici **Správa aplikace Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-133">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="fa4ff-134">Vyberte instanci, kterou chcete zkopírovat, a pak vyberte **Kopírovat**.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-134">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="fa4ff-135">V podokně úloh **Kopírovat instanci** vyberte instanci, kterou chcete přepsat, a poté vyberte možnost **kopírovat**.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-135">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="fa4ff-136">Počkejte, až bude hodnota pole **Kopírovat stav** aktualizována na hodnotu **dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-136">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="fa4ff-137">Výběr instance, která má být přepsána</span><span class="sxs-lookup"><span data-stu-id="fa4ff-137">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="fa4ff-138">Vyberte **Power Platform** a přihlaste se do centra pro správu Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-138">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="fa4ff-139">Vyberte Power Platform</span><span class="sxs-lookup"><span data-stu-id="fa4ff-139">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="fa4ff-140">Vyberte prostředí Power Apps, ke zkopírování a pak vyberte **Kopírovat**.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-140">Select the Power Apps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="fa4ff-141">Po dokončení procesu kopírování se přihlaste k cílové instanci a povolte integraci Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-141">When the copy process is completed, sign in to the target instance, and enable Common Data Service integration.</span></span> <span data-ttu-id="fa4ff-142">Další informace a pokyny naleznete v části [Konfigurace integrace Common Data Service](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span><span class="sxs-lookup"><span data-stu-id="fa4ff-142">For more information and instructions, see [Configure Common Data Service integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="fa4ff-143">Datové prvky a stavy</span><span class="sxs-lookup"><span data-stu-id="fa4ff-143">Data elements and statuses</span></span>

<span data-ttu-id="fa4ff-144">Při kopírování instance Human Resources nejsou zkopírovány následující datové prvky:</span><span class="sxs-lookup"><span data-stu-id="fa4ff-144">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="fa4ff-145">E-mailové adres z tabulky **LogisticsElectronicAddress**</span><span class="sxs-lookup"><span data-stu-id="fa4ff-145">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="fa4ff-146">Historie dávkové úlohy v tabulkách **BatchJobHistory**, **BatchHistory** a **BatchConstraintHistory**</span><span class="sxs-lookup"><span data-stu-id="fa4ff-146">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="fa4ff-147">Heslo protokolu SMTP (Simple Mail Transfer Protocol) v tabulce **SysEmailSMTPPassword**</span><span class="sxs-lookup"><span data-stu-id="fa4ff-147">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="fa4ff-148">Server pro předávání SMTP v tabulce **SysEmailParameters**</span><span class="sxs-lookup"><span data-stu-id="fa4ff-148">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="fa4ff-149">Nastavení správy tisku v tabulkách **PrintMgmtSettings** a **PrintMgmtDocInstance**</span><span class="sxs-lookup"><span data-stu-id="fa4ff-149">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="fa4ff-150">Záznamy specifické pro prostředí v tabulkách **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** a **BatchServerGroup**</span><span class="sxs-lookup"><span data-stu-id="fa4ff-150">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="fa4ff-151">Přílohy dokumentu v tabulce DocuValue.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-151">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="fa4ff-152">Tyto přílohy zahrnují všechny šablony Microsoft Office, které byly přepsány ve zdrojovém prostředí.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-152">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="fa4ff-153">Připojovací řetězec v tabulce **PersonnelIntegrationConfiguration**</span><span class="sxs-lookup"><span data-stu-id="fa4ff-153">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="fa4ff-154">Některé z těchto prvků nebyly zkopírovány, protože jsou specifické pro prostředí.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-154">Some of these elements aren't copied because they're environment-specific.</span></span> <span data-ttu-id="fa4ff-155">Příklady zahrnují záznamy **BatchServerConfig** a **SysCorpNetPrinters**.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-155">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="fa4ff-156">Ostatní prvky nebudou zkopírovány z důvodu objemu lístků podpory.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-156">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="fa4ff-157">Například:</span><span class="sxs-lookup"><span data-stu-id="fa4ff-157">For example:</span></span>

- <span data-ttu-id="fa4ff-158">Mohou být odesílány duplicitní e-maily, protože v prostředí sandbox pro testování přijetí uživatele je stále povolen protokol SMTP.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-158">Duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment.</span></span>

- <span data-ttu-id="fa4ff-159">Mohou být odesílány neplatné integrační zprávy, protože dávkové úlohy jsou stále povoleny.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-159">Invalid integration messages might be sent because batch jobs are still enabled.</span></span>

- <span data-ttu-id="fa4ff-160">Uživatelé mohou být povoleni, než mohou správci provádět akce čištění po aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-160">Users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="fa4ff-161">Při kopírování instance se dále mění následující stavy:</span><span class="sxs-lookup"><span data-stu-id="fa4ff-161">Also, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="fa4ff-162">Všichni uživatelé s výjimkou správce jsou nastaveni na **Zakázáno**.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-162">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="fa4ff-163">Všechny dávkové úlohy, s výjimkou některých systémových úloh, jsou nastaveny na **srážka**.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-163">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="fa4ff-164">Správce prostředí</span><span class="sxs-lookup"><span data-stu-id="fa4ff-164">Environment admin</span></span>

<span data-ttu-id="fa4ff-165">Všichni uživatelé v cílovém prostředí izolovaného prostoru (sandbox) včetně správců budou nahrazeni uživateli zdrojového prostředí.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-165">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="fa4ff-166">Před kopírováním instance se ujistěte, zda jste správcem zdrojového prostředí.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-166">Before you copy an instance, be sure that you're an Administrator in the source environment.</span></span> <span data-ttu-id="fa4ff-167">Pokud ne, nebudete se moci po dokončení kopírování přihlásit k cílovému prostředí sandbox.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-167">If you aren't, you can't sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="fa4ff-168">Všichni uživatelé, kteří nejsou správci v cílovém prostředí izolovaného prostoru (sandbox), jsou zakázáni, aby zabránili nechtěným přihlášením v prostředí karantény.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-168">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="fa4ff-169">Správci mohou v případě potřeby znovu povolit uživatele.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-169">Administrators can reenable users if needed.</span></span>

## <a name="apply-custom-fields-to-common-data-service"></a><span data-ttu-id="fa4ff-170">Použití vlastních polí na Common Data Service</span><span class="sxs-lookup"><span data-stu-id="fa4ff-170">Apply custom fields to Common Data Service</span></span>

<span data-ttu-id="fa4ff-171">Pokud zkopírujete instanci do prostředí sandbox a chcete integrovat prostředí sandbox s Common Data Service, musíte znovu použít vlastní pole na entity Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-171">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Common Data Service, you must reapply custom fields to Common Data Service entities.</span></span>

<span data-ttu-id="fa4ff-172">Pro každé vlastní pole, které je vystaveno v entitách Common Data Service, proveďte následující kroky:</span><span class="sxs-lookup"><span data-stu-id="fa4ff-172">For each custom field that's exposed on Common Data Service entities, do the following steps:</span></span>

1. <span data-ttu-id="fa4ff-173">Přejděte do vlastního pole a vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-173">Go to the custom field and select **Edit**.</span></span>

2. <span data-ttu-id="fa4ff-174">Zrušte výběr pole **Povoleno** pro každou entitu cdm_\*, pro kterou je povoleno vlastní pole.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-174">Unselect the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

3. <span data-ttu-id="fa4ff-175">Vyberte **Použít změny**.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-175">Select **Apply Changes**.</span></span>

4. <span data-ttu-id="fa4ff-176">Znovu vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-176">Select **Edit** again.</span></span>

5. <span data-ttu-id="fa4ff-177">Vyberte pole **Povoleno** pro každou entitu cdm_\*, pro kterou je povoleno vlastní pole.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-177">Select the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

6. <span data-ttu-id="fa4ff-178">Znovu vyberte **Použít změny**.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-178">Select **Apply Changes** again.</span></span>

<span data-ttu-id="fa4ff-179">Proces zrušení výběru, použití změn, opětovného výběru a opětovného použití změn vyzve schéma k aktualizaci v Common Data Service pro zahrnutí vlastních polí.</span><span class="sxs-lookup"><span data-stu-id="fa4ff-179">The process of unselecting, applying changes, reselecting, and reapplying changes prompts the schema to update in Common Data Service to include the custom fields.</span></span>

<span data-ttu-id="fa4ff-180">Další informace o vlastních polích naleznete v tématu [Vytvoření vlastních polí a práce s nimi](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields).</span><span class="sxs-lookup"><span data-stu-id="fa4ff-180">For more information about custom fields, see [Create and work with custom fields](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields).</span></span>

## <a name="see-also"></a><span data-ttu-id="fa4ff-181">Viz také</span><span class="sxs-lookup"><span data-stu-id="fa4ff-181">See also</span></span>

[<span data-ttu-id="fa4ff-182">Zřízení Human Resources</span><span class="sxs-lookup"><span data-stu-id="fa4ff-182">Provision Human Resources</span></span>](hr-admin-setup-provision.md)</br>
[<span data-ttu-id="fa4ff-183">Odebrání instance</span><span class="sxs-lookup"><span data-stu-id="fa4ff-183">Remove an instance</span></span>](hr-admin-setup-remove-instance.md)</br>
[<span data-ttu-id="fa4ff-184">Aktualizace procesu</span><span class="sxs-lookup"><span data-stu-id="fa4ff-184">Update process</span></span>](hr-admin-setup-update-process.md)

