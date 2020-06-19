---
title: Kopírovat instanci
description: Pomocí služby Microsoft Dynamics Lifecycle Services (LCS) můžete kopírovat databázi Microsoft Dynamics 365 Human Resources do prostředí izolovaného prostoru (sandbox).
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: e8385b7dfcd1d7294542c7f54f609b26b7988ac4
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431238"
---
# <a name="copy-an-instance"></a><span data-ttu-id="09b50-103">Kopírovat instanci</span><span class="sxs-lookup"><span data-stu-id="09b50-103">Copy an instance</span></span>

<span data-ttu-id="09b50-104">Pomocí služby Microsoft Dynamics Lifecycle Services (LCS) můžete kopírovat databázi Microsoft Dynamics 365 Human Resources do prostředí izolovaného prostoru (sandbox).</span><span class="sxs-lookup"><span data-stu-id="09b50-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="09b50-105">Máte-li jiné prostředí izolovaného prostoru (sandbox), můžete také zkopírovat databázi z prostředí do cíleného prostředí sandbox.</span><span class="sxs-lookup"><span data-stu-id="09b50-105">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="09b50-106">Chcete-li zkopírovat instanci, je nutné zajistit následující:</span><span class="sxs-lookup"><span data-stu-id="09b50-106">To copy an instance, you need to ensure the following:</span></span>

- <span data-ttu-id="09b50-107">Instance aplikace Human Resources, kterou chcete přepsat, musí být prostředí izolovaného prostoru (sandbox).</span><span class="sxs-lookup"><span data-stu-id="09b50-107">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="09b50-108">Prostředí, ze kterých kopírujete, musí být ve stejné oblasti.</span><span class="sxs-lookup"><span data-stu-id="09b50-108">The environments you are copying from and to must be in the same region.</span></span> <span data-ttu-id="09b50-109">Nelze kopírovat mezi oblastmi.</span><span class="sxs-lookup"><span data-stu-id="09b50-109">You can't copy across regions.</span></span>

- <span data-ttu-id="09b50-110">Musíte být správcem cílového prostředí, abyste se k němu mohli po zkopírování instance přihlásit.</span><span class="sxs-lookup"><span data-stu-id="09b50-110">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="09b50-111">Při kopírování databáze aplikace Human Resources nejsou zkopírovány prvky (aplikace nebo data), které jsou obsaženy v prostředí Microsoft PowerApps.</span><span class="sxs-lookup"><span data-stu-id="09b50-111">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft PowerApps environment.</span></span> <span data-ttu-id="09b50-112">Informace o tom, jak kopírovat prvky do prostředí PowerApps, naleznete v tématu [kopírování prostředí](https://docs.microsoft.com/power-platform/admin/copy-environment).</span><span class="sxs-lookup"><span data-stu-id="09b50-112">For information about how to copy elements in a PowerApps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="09b50-113">Prostředí PowerApps, které chcete přepsat, musí být prostředí izolovaného prostoru (sandbox).</span><span class="sxs-lookup"><span data-stu-id="09b50-113">The PowerApps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="09b50-114">Chcete-li změnit produkční prostředí PowerApps na prostředí s izolovaným prostorem, musíte být globálním správcem klienta.</span><span class="sxs-lookup"><span data-stu-id="09b50-114">You must be a global tenant admin to change a PowerApps production environment to a sandbox environment.</span></span> <span data-ttu-id="09b50-115">Další informace o změně prostředí PowerApps naleznete v tématu [přepnutí instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span><span class="sxs-lookup"><span data-stu-id="09b50-115">For more information about changing a PowerApps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="09b50-116">Vliv kopírování databáze aplikace Human Resources</span><span class="sxs-lookup"><span data-stu-id="09b50-116">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="09b50-117">Při kopírování databáze aplikace Human Resources dojde k následujícím událostem:</span><span class="sxs-lookup"><span data-stu-id="09b50-117">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="09b50-118">Při kopírování bude existující databáze vymazána v cílovém prostředí.</span><span class="sxs-lookup"><span data-stu-id="09b50-118">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="09b50-119">Po dokončení kopírování nelze stávající databázi obnovit.</span><span class="sxs-lookup"><span data-stu-id="09b50-119">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="09b50-120">Cílové prostředí nebude k dispozici, dokud nebude proces kopírování dokončen.</span><span class="sxs-lookup"><span data-stu-id="09b50-120">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="09b50-121">Dokumenty v úložišti objektů BLOB Microsoft Azure nejsou kopírovány z jednoho prostředí do jiného.</span><span class="sxs-lookup"><span data-stu-id="09b50-121">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="09b50-122">Proto nebudou žádné připojené dokumenty a šablony, které jsou připojeny, zkopírovány a zůstanou ve zdrojovém prostředí.</span><span class="sxs-lookup"><span data-stu-id="09b50-122">Therefore, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="09b50-123">Všichni uživatelé, kromě správce a ostatních interních uživatelských účtů služby budou nedostupní.</span><span class="sxs-lookup"><span data-stu-id="09b50-123">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="09b50-124">Správce tedy může odstranit nebo zamlžit data před tím, než se budou moci ostatní uživatelé vrátit do systému.</span><span class="sxs-lookup"><span data-stu-id="09b50-124">Therefore, the Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="09b50-125">Uživatel s oprávněními správce musí provést požadované změny konfigurace, například opětovné připojení koncových bodů integrace pro určité služby nebo adresy URL.</span><span class="sxs-lookup"><span data-stu-id="09b50-125">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="09b50-126">Kopírování databáze aplikace Human Resources</span><span class="sxs-lookup"><span data-stu-id="09b50-126">Copy the Human Resources database</span></span>

<span data-ttu-id="09b50-127">Chcete-li dokončit tento úkol, nejprve zkopírujte instanci a poté se přihlaste do centra pro správu Microsoft Power Platform a zkopírujte vaše prostředí PowerApps.</span><span class="sxs-lookup"><span data-stu-id="09b50-127">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your PowerApps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="09b50-128">Při kopírování instance je databáze vymazána v cílové instanci.</span><span class="sxs-lookup"><span data-stu-id="09b50-128">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="09b50-129">Cílová instance není během tohoto procesu k dispozici.</span><span class="sxs-lookup"><span data-stu-id="09b50-129">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="09b50-130">Přihlaste se k LCS a vyberte projekt LCS obsahující instanci, kterou chcete zkopírovat.</span><span class="sxs-lookup"><span data-stu-id="09b50-130">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="09b50-131">Ve svém LCS projektu vyberte dlaždici **Správa aplikace Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="09b50-131">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="09b50-132">Vyberte instanci, kterou chcete zkopírovat, a pak vyberte **Kopírovat**.</span><span class="sxs-lookup"><span data-stu-id="09b50-132">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="09b50-133">V podokně úloh **Kopírovat instanci** vyberte instanci, kterou chcete přepsat, a poté vyberte možnost **kopírovat**.</span><span class="sxs-lookup"><span data-stu-id="09b50-133">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="09b50-134">Počkejte, až bude hodnota pole **Kopírovat stav** aktualizována na hodnotu **dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="09b50-134">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="09b50-135">Výběr instance, kterou chcete přepsat</span><span class="sxs-lookup"><span data-stu-id="09b50-135">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="09b50-136">Vyberte **Power Platform** a přihlaste se do centra pro správu Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="09b50-136">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="09b50-137">Výběr Power Platform</span><span class="sxs-lookup"><span data-stu-id="09b50-137">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="09b50-138">Vyberte prostředí PowerApps, ke zkopírování a pak vyberte **Kopírovat**.</span><span class="sxs-lookup"><span data-stu-id="09b50-138">Select the PowerApps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="09b50-139">Po dokončení procesu kopírování se přihlaste k cílové instanci a povolte integraci Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="09b50-139">When the copy process is completed, sign in to the target instance, and enable Common Data Service integration.</span></span> <span data-ttu-id="09b50-140">Další informace a pokyny naleznete v části [Konfigurace integrace Common Data Service](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span><span class="sxs-lookup"><span data-stu-id="09b50-140">For more information and instructions, see [Configure Common Data Service integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="09b50-141">Datové prvky a stavy</span><span class="sxs-lookup"><span data-stu-id="09b50-141">Data elements and statuses</span></span>

<span data-ttu-id="09b50-142">Při kopírování instance Human Resources nejsou zkopírovány následující datové prvky:</span><span class="sxs-lookup"><span data-stu-id="09b50-142">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="09b50-143">E-mailové adres z tabulky **LogisticsElectronicAddress**</span><span class="sxs-lookup"><span data-stu-id="09b50-143">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="09b50-144">Historie dávkové úlohy v tabulkách **BatchJobHistory**, **BatchHistory** a **BatchConstraintHistory**</span><span class="sxs-lookup"><span data-stu-id="09b50-144">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="09b50-145">Heslo protokolu SMTP (Simple Mail Transfer Protocol) v tabulce **SysEmailSMTPPassword**</span><span class="sxs-lookup"><span data-stu-id="09b50-145">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="09b50-146">Server pro předávání SMTP v tabulce **SysEmailParameters**</span><span class="sxs-lookup"><span data-stu-id="09b50-146">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="09b50-147">Nastavení správy tisku v tabulkách **PrintMgmtSettings** a **PrintMgmtDocInstance**</span><span class="sxs-lookup"><span data-stu-id="09b50-147">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="09b50-148">Záznamy specifické pro prostředí v tabulkách **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** a **BatchServerGroup**</span><span class="sxs-lookup"><span data-stu-id="09b50-148">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="09b50-149">Přílohy dokumentu v tabulce DocuValue.</span><span class="sxs-lookup"><span data-stu-id="09b50-149">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="09b50-150">Tyto přílohy zahrnují všechny šablony Microsoft Office, které byly přepsány ve zdrojovém prostředí.</span><span class="sxs-lookup"><span data-stu-id="09b50-150">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="09b50-151">Připojovací řetězec v tabulce **PersonnelIntegrationConfiguration**</span><span class="sxs-lookup"><span data-stu-id="09b50-151">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="09b50-152">Některé z těchto prvků nebyly zkopírovány, protože jsou specifické pro prostředí.</span><span class="sxs-lookup"><span data-stu-id="09b50-152">Some of these elements aren't copied because they are environment-specific.</span></span> <span data-ttu-id="09b50-153">Příklady zahrnují záznamy **BatchServerConfig** a **SysCorpNetPrinters**.</span><span class="sxs-lookup"><span data-stu-id="09b50-153">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="09b50-154">Ostatní prvky nebudou zkopírovány z důvodu objemu lístků podpory.</span><span class="sxs-lookup"><span data-stu-id="09b50-154">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="09b50-155">Je například možné, že duplicitní e-maily budou odeslány, protože v prostředí pro testování přijetí uživatele (sandbox) je stále povolen protokol SMTP, mohou být odeslány neplatné integrační zprávy, protože jsou stále povoleny dávkové úlohy a uživatelé mohou být povoleni předtím, než mohou správci provést akce čištění po aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="09b50-155">For example, duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment, invalid integration messages might be sent because batch jobs are still enabled, and users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="09b50-156">Při kopírování instance se dále mění následující stavy:</span><span class="sxs-lookup"><span data-stu-id="09b50-156">In addition, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="09b50-157">Všichni uživatelé s výjimkou správce jsou nastaveni na **Zakázáno**.</span><span class="sxs-lookup"><span data-stu-id="09b50-157">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="09b50-158">Všechny dávkové úlohy, s výjimkou některých systémových úloh, jsou nastaveny na **srážka**.</span><span class="sxs-lookup"><span data-stu-id="09b50-158">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="09b50-159">Správce prostředí</span><span class="sxs-lookup"><span data-stu-id="09b50-159">Environment admin</span></span>

<span data-ttu-id="09b50-160">Všichni uživatelé v cílovém prostředí izolovaného prostoru (sandbox) včetně správců budou nahrazeni uživateli zdrojového prostředí.</span><span class="sxs-lookup"><span data-stu-id="09b50-160">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="09b50-161">Před kopírováním instance se ujistěte, zda jste správcem cílového prostředí.</span><span class="sxs-lookup"><span data-stu-id="09b50-161">Before you copy an instance, be sure that you're an Administrator in the target environment.</span></span> <span data-ttu-id="09b50-162">Pokud ne, nebudete se moci po dokončení kopírování přihlásit k cílovému prostředí izolovaného prostoru (sandbox).</span><span class="sxs-lookup"><span data-stu-id="09b50-162">If you aren't, you won't be able to sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="09b50-163">Všichni uživatelé, kteří nejsou správci v cílovém prostředí izolovaného prostoru (sandbox), jsou zakázáni, aby zabránili nechtěným přihlášením v prostředí karantény.</span><span class="sxs-lookup"><span data-stu-id="09b50-163">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="09b50-164">Správci mohou v případě potřeby znovu povolit uživatele.</span><span class="sxs-lookup"><span data-stu-id="09b50-164">Administrators can reenable users if needed.</span></span>
