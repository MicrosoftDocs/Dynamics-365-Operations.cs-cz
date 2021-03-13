---
title: Integrace s LinkedIn Talent Hub
description: Toto téma vysvětluje, jak nastavit integraci mezi Microsoft Dynamics 365 Human Resources a LinkedIn Talent Hub.
author: jaredha
manager: tfehr
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4fda9d85b459d233e6239f3fcffbb48e596d4085
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111847"
---
# <a name="integrate-with-linkedin-talent-hub"></a><span data-ttu-id="1ba29-103">Integrace s LinkedIn Talent Hub</span><span class="sxs-lookup"><span data-stu-id="1ba29-103">Integrate with LinkedIn Talent Hub</span></span>

[!include [banner](includes/preview-feature.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="1ba29-104">[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) je platforma pro systém sledování žadatelů (ATS).</span><span class="sxs-lookup"><span data-stu-id="1ba29-104">[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) is an applicant tracking system (ATS) platform.</span></span> <span data-ttu-id="1ba29-105">Umožňuje vám získávat, spravovat a najímat zaměstnance z jednoho místa.</span><span class="sxs-lookup"><span data-stu-id="1ba29-105">It lets you source, manage, and hire employees all in one place.</span></span> <span data-ttu-id="1ba29-106">Integrací Microsoft Dynamics 365 Human Resources s LinkedIn Talent Hub můžete snadno vytvářet záznamy o zaměstnancích v Human Resources pro uchazeče, kteří byli najati na pozici.</span><span class="sxs-lookup"><span data-stu-id="1ba29-106">By integrating Microsoft Dynamics 365 Human Resources with LinkedIn Talent Hub, you can easily create employee records in Human Resources for applicants who have been hired for a position.</span></span>

## <a name="setup"></a><span data-ttu-id="1ba29-107">Nastavení</span><span class="sxs-lookup"><span data-stu-id="1ba29-107">Setup</span></span>

<span data-ttu-id="1ba29-108">Nastavení integrace s LinkedIn Talent Hub musí provést správce systému.</span><span class="sxs-lookup"><span data-stu-id="1ba29-108">A system administrator must complete setup tasks to enable integration with LinkedIn Talent Hub.</span></span> <span data-ttu-id="1ba29-109">Nejprve v prostředí Power Apps musíte nastavit uživatele a roli zabezpečení, abyste LinkedIn Talent Hub udělili příslušná oprávnění k zápisu dat do Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1ba29-109">First, in the Power Apps environment, you must set up a user and security role to grant LinkedIn Talent Hub the appropriate permissions to write data into Human Resources.</span></span>

### <a name="link-your-environment-to-linkedin-talent-hub"></a><span data-ttu-id="1ba29-110">Propojte své prostředí s LinkedIn Talent Hub</span><span class="sxs-lookup"><span data-stu-id="1ba29-110">Link your environment to LinkedIn Talent Hub</span></span>

1. <span data-ttu-id="1ba29-111">Otevřete [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).</span><span class="sxs-lookup"><span data-stu-id="1ba29-111">Open [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).</span></span>

2. <span data-ttu-id="1ba29-112">V rozevírací nabídce uživatele vyberte možnost **Nastavení produktu**.</span><span class="sxs-lookup"><span data-stu-id="1ba29-112">On the user drop-down menu, select **Product Settings**.</span></span>

3. <span data-ttu-id="1ba29-113">V levém navigačním podokně v sekci **Rozšířené** vyberte **Integrace**.</span><span class="sxs-lookup"><span data-stu-id="1ba29-113">In the left navigation pane, in the **Advanced** section, select **Integrations**.</span></span>

4. <span data-ttu-id="1ba29-114">Vyberte **Autorizovat** pro integraci Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1ba29-114">Select **Authorize** for the Microsoft Dynamics 365 Human Resources integration.</span></span>

5. <span data-ttu-id="1ba29-115">Na stránce **Dynamics 365 Human Resources** vyberte prostředí, ke kterému chcete propojit LinkedIn Talent Hub, a poté vyberte **Propojit**.</span><span class="sxs-lookup"><span data-stu-id="1ba29-115">On the **Dynamics 365 Human Resources** page, select the environment to link LinkedIn Talent Hub to, and then select **Link**.</span></span>

    ![Zprovoznění LinkedIn Talent Hub](./media/hr-admin-integration-talent-hub-onboarding.jpg)

    > [!NOTE]
    > <span data-ttu-id="1ba29-117">Můžete se připojit pouze k prostředím, kde má váš uživatelský účet přístup správce do prostředí Human Resources i do přidruženého prostředí Power Apps.</span><span class="sxs-lookup"><span data-stu-id="1ba29-117">You can link only to environments where your user account has administrator access to both the Human Resources environment and the associated Power Apps environment.</span></span> <span data-ttu-id="1ba29-118">Pokud na stránce propojení s Human Resources nejsou uvedena žádná prostředí, ujistěte se, že máte v klientovi licencovaná prostředí Human Resources a že uživatel, pod kterým jste se přihlásili ke stránce s propojením, má oprávnění správce jak do prostředí Human Resources, tak do prostředí Power Apps.</span><span class="sxs-lookup"><span data-stu-id="1ba29-118">If no environments are listed on the Human Resources link page, make sure that you have licensed Human Resources environments on the tenant, and that the user that you signed in to the link page as has administrator permissions to both the Human Resources environment and the Power Apps environment.</span></span>

### <a name="create-a-power-apps-security-role"></a><span data-ttu-id="1ba29-119">Vytvoření role zabezpečení Power Apps</span><span class="sxs-lookup"><span data-stu-id="1ba29-119">Create a Power Apps security role</span></span>

1. <span data-ttu-id="1ba29-120">Otevřete [centrum pro správu Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="1ba29-120">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="1ba29-121">V seznamu **Prostředí** vyberte prostředí přidružené k prostředí Human Resources, se kterým chcete propojit instanci LinkedIn Talent Hub.</span><span class="sxs-lookup"><span data-stu-id="1ba29-121">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="1ba29-122">Vyberte **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="1ba29-122">Select **Settings**.</span></span>

4. <span data-ttu-id="1ba29-123">Rozbalte uzel **Uživatelé + oprávnění** a vyberte **Role zabezpečení**.</span><span class="sxs-lookup"><span data-stu-id="1ba29-123">Expand the **Users + Permissions** node, and select **Security Roles**.</span></span>

5. <span data-ttu-id="1ba29-124">Na stránce **Role zabezpečení** vyberte **Nová role**.</span><span class="sxs-lookup"><span data-stu-id="1ba29-124">On the **Security Roles** page, on the toolbar, select **New role**.</span></span>

6. <span data-ttu-id="1ba29-125">Na kartě **Podrobnosti** zadejte název role, například **Integrace LinkedIn Talent Hub HRIS**.</span><span class="sxs-lookup"><span data-stu-id="1ba29-125">On the **Details** tab, enter a name for the role, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>

7. <span data-ttu-id="1ba29-126">Na kartě **Vlastní nastavení** vyberte na úrovni organizace oprávnění **Čtení** pro následující entity:</span><span class="sxs-lookup"><span data-stu-id="1ba29-126">On the **Customization** tab, select organization-level **Read** permission for the following entities:</span></span>

    - <span data-ttu-id="1ba29-127">Entita</span><span class="sxs-lookup"><span data-stu-id="1ba29-127">Entity</span></span>
    - <span data-ttu-id="1ba29-128">Pole</span><span class="sxs-lookup"><span data-stu-id="1ba29-128">Field</span></span>
    - <span data-ttu-id="1ba29-129">Vztah</span><span class="sxs-lookup"><span data-stu-id="1ba29-129">Relationship</span></span>

8. <span data-ttu-id="1ba29-130">Uložte a zavřete roli zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="1ba29-130">Save and close the security role.</span></span>

### <a name="create-a-power-apps-application-user"></a><span data-ttu-id="1ba29-131">Vytvoření uživatele aplikace Power Apps</span><span class="sxs-lookup"><span data-stu-id="1ba29-131">Create a Power Apps application user</span></span>

<span data-ttu-id="1ba29-132">Pro adaptér LinkedIn Talent Hub musí být vytvořen uživatel aplikace, aby byla adaptéru udělena oprávnění k zápisu záznamů kandidátů do prostředí Power Apps.</span><span class="sxs-lookup"><span data-stu-id="1ba29-132">An application user must be created for the LinkedIn Talent Hub adapter to grant permissions to the adapter to write candidate records into the Power Apps environment.</span></span>

1. <span data-ttu-id="1ba29-133">Otevřete [centrum pro správu Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="1ba29-133">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="1ba29-134">V seznamu **Prostředí** vyberte prostředí přidružené k prostředí Human Resources, se kterým chcete propojit instanci LinkedIn Talent Hub.</span><span class="sxs-lookup"><span data-stu-id="1ba29-134">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="1ba29-135">Vyberte **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="1ba29-135">Select **Settings**.</span></span>

4. <span data-ttu-id="1ba29-136">Rozbalte uzel **Uživatelé + oprávnění** a vyberte možnost **Uživatelé**.</span><span class="sxs-lookup"><span data-stu-id="1ba29-136">Expand the **Users + Permissions** node, and select **Users**.</span></span>

5. <span data-ttu-id="1ba29-137">Vyberte **Spravovat uživatele v Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="1ba29-137">Select **Manage users in Dynamics 365**.</span></span>

6. <span data-ttu-id="1ba29-138">V rozevírací nabídce nad seznamem můžete změnit zobrazení z výchozího **Povolení uživatelé** na **Uživatelé aplikace**.</span><span class="sxs-lookup"><span data-stu-id="1ba29-138">Use the drop-down menu above the list to change the view from the default **Enabled Users** view to **Application Users**.</span></span>

    ![Zobrazení Uživatelé aplikace](./media/hr-admin-integration-power-apps-application-users.jpg)

7. <span data-ttu-id="1ba29-140">Na panelu nástrojů vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="1ba29-140">On the toolbar, select **New**.</span></span>

8. <span data-ttu-id="1ba29-141">Na stránce **Nový uživatel** proveďte následující kroky:</span><span class="sxs-lookup"><span data-stu-id="1ba29-141">On the **New user** page, follow these steps:</span></span>

    1. <span data-ttu-id="1ba29-142">Změňte hodnotu pole **Typ uživatele** na **Uživatel aplikace**.</span><span class="sxs-lookup"><span data-stu-id="1ba29-142">Change the value of the **User type** field to **Application User**.</span></span>
    2. <span data-ttu-id="1ba29-143">Nastavte pole **Uživatelské jméno** na **Integrace Dynamics365 HR LinkedIn HRIS**.</span><span class="sxs-lookup"><span data-stu-id="1ba29-143">Set the **User Name** field to **Dynamics365 HR LinkedIn HRIS Integration**.</span></span>
    3. <span data-ttu-id="1ba29-144">Nastavte pole **ID aplikace** na **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span><span class="sxs-lookup"><span data-stu-id="1ba29-144">Set the **Application ID** field to **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    4. <span data-ttu-id="1ba29-145">Zadejte libovolnou hodnotu do polí **Křestní jméno**, **Příjmení** a **Primární e-mail**.</span><span class="sxs-lookup"><span data-stu-id="1ba29-145">Enter any value in the **First Name**, **Last Name**, and **Primary Email** fields.</span></span>
    5. <span data-ttu-id="1ba29-146">Na panelu nástrojů vyberte **Uložit a zavřít**.</span><span class="sxs-lookup"><span data-stu-id="1ba29-146">On the toolbar, select **Save \& Close**.</span></span>

### <a name="assign-a-security-role-to-the-new-user"></a><span data-ttu-id="1ba29-147">Přiřazení role zabezpečení novému uživateli</span><span class="sxs-lookup"><span data-stu-id="1ba29-147">Assign a security role to the new user</span></span>

<span data-ttu-id="1ba29-148">Po uložení a zavření nového uživatele aplikace v předchozí části jste se vrátili na stránku **Seznam uživatelů**.</span><span class="sxs-lookup"><span data-stu-id="1ba29-148">After you save and close the new application user in the previous section, you're returned to the **Users list** page.</span></span>

1. <span data-ttu-id="1ba29-149">Na stránce **Seznam uživatelů** změňte zobrazení na **Uživatelé aplikace**.</span><span class="sxs-lookup"><span data-stu-id="1ba29-149">On the **Users list** page, change the view to **Application Users**.</span></span>

2. <span data-ttu-id="1ba29-150">Vyberte uživatele aplikace, kterého jste vytvořili v předchozí části.</span><span class="sxs-lookup"><span data-stu-id="1ba29-150">Select the application user that you created in the previous section.</span></span>

3. <span data-ttu-id="1ba29-151">Na panelu nástrojů vyberte **Správa rolí**.</span><span class="sxs-lookup"><span data-stu-id="1ba29-151">On the toolbar, select **Manage Roles**.</span></span>

4. <span data-ttu-id="1ba29-152">Vyberte roli zabezpečení, kterou jste vytvořili dříve pro integraci.</span><span class="sxs-lookup"><span data-stu-id="1ba29-152">Select the security role that you created earlier for the integration.</span></span>

5. <span data-ttu-id="1ba29-153">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="1ba29-153">Select **OK**.</span></span>

### <a name="add-an-azure-active-directory-app-in-human-resources"></a><span data-ttu-id="1ba29-154">Přidání aplikace Azure Active Directory v Human Resources</span><span class="sxs-lookup"><span data-stu-id="1ba29-154">Add an Azure Active Directory app in Human Resources</span></span>

1. <span data-ttu-id="1ba29-155">V Dynamics 365 Human Resources otevřete stránku **Aplikace Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="1ba29-155">In Dynamics 365 Human Resources, open the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="1ba29-156">Přidejte nový záznam do seznamu a nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="1ba29-156">Add a new record to the list, and set the following fields:</span></span>

    - <span data-ttu-id="1ba29-157">**ID klienta**: Zadejte **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span><span class="sxs-lookup"><span data-stu-id="1ba29-157">**Client ID**: Enter **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    - <span data-ttu-id="1ba29-158">**Název**: Zadejte název role zabezpečení Power Apps, kterou jste vytvořili dříve, například **Integrace LinkedIn Talent Hub HRIS**.</span><span class="sxs-lookup"><span data-stu-id="1ba29-158">**Name**: Enter the name of the Power Apps security role that you created earlier, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>
    - <span data-ttu-id="1ba29-159">**ID uživatele**: Vyberte uživatele, který má oprávnění k zápisu dat do pracovního prostoru Správa zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="1ba29-159">**User ID**: Select a user who has permissions to write data in Personnel Management.</span></span>

### <a name="create-the-table-in-dataverse"></a><span data-ttu-id="1ba29-160">Vytvoření tabulky v Dataverse</span><span class="sxs-lookup"><span data-stu-id="1ba29-160">Create the table in Dataverse</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1ba29-161">Integrace s LinkedIn Talent Hub závisí na virtuálních tabulkách v Dataverse pro Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1ba29-161">The integration with LinkedIn Talent Hub depends on virtual tables in Dataverse for Human Resources.</span></span> <span data-ttu-id="1ba29-162">Jako předpoklad pro tento krok musíte v nastavení nakonfigurovat virtuální tabulky.</span><span class="sxs-lookup"><span data-stu-id="1ba29-162">As a prerequisite for this step in the setup, you must configure virtual tables.</span></span> <span data-ttu-id="1ba29-163">Informace o konfiguraci virtuálních tabulke najdete v tématu [Konfigurace virtuálních tabulek Dataverse](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span><span class="sxs-lookup"><span data-stu-id="1ba29-163">For information about how to configure virtual tables, see [Configure Dataverse virtual tables](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span></span>

1. <span data-ttu-id="1ba29-164">V Human Resources otevřete stránku **Integrace Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="1ba29-164">In Human Resources, open the **Dataverse integration** page.</span></span>

2. <span data-ttu-id="1ba29-165">Vyberte kartu **Virtuální tabulky**.</span><span class="sxs-lookup"><span data-stu-id="1ba29-165">Select the **Virtual tables** tab.</span></span>

3. <span data-ttu-id="1ba29-166">Filtrujte seznam entit podle popisku entity a vyhledejte **Exportovaný kandidát LinkedIn**.</span><span class="sxs-lookup"><span data-stu-id="1ba29-166">Filter the entity list by entity label to find **LinkedIn exported candidate**.</span></span>

4. <span data-ttu-id="1ba29-167">Vyberte entitu a poté vyberte možnost **Generovat/aktualizovat**.</span><span class="sxs-lookup"><span data-stu-id="1ba29-167">Select the entity, and then select **Generate/refresh**.</span></span>

## <a name="exporting-candidate-records"></a><span data-ttu-id="1ba29-168">Export záznamů kandidátů</span><span class="sxs-lookup"><span data-stu-id="1ba29-168">Exporting candidate records</span></span>

<span data-ttu-id="1ba29-169">Po dokončení nastavení mohou pracovníci náboru a odborníci na personalistiku (HR) používat funkci **Export to HRIS** (Exportovat do HRIS) v LinkedIn Talent Hub pro export záznamů přijatých kandidátů z LinkedIn Talent Hub do Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1ba29-169">After the setup is completed, recruiters and human resources (HR) professionals can use the **Export to HRIS** function in LinkedIn Talent Hub to export hired candidate records from LinkedIn Talent Hub to Human Resources.</span></span>

### <a name="export-records-from-linkedin-talent-hub"></a><span data-ttu-id="1ba29-170">Export záznamů z LinkedIn Talent Hub</span><span class="sxs-lookup"><span data-stu-id="1ba29-170">Export records from LinkedIn Talent Hub</span></span>

<span data-ttu-id="1ba29-171">Poté, co kandidát prošel náborovým procesem a byl přijat, můžete exportovat záznam kandidáta z LinkedIn Talent Hub do Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1ba29-171">After a candidate has moved through the recruiting process and has been hired, you can export the candidate record from LinkedIn Talent Hub to Human Resources.</span></span>

1. <span data-ttu-id="1ba29-172">V LinkedIn Talent Hub otevřete projekt, pro který jste nového zaměstnance najali.</span><span class="sxs-lookup"><span data-stu-id="1ba29-172">In LinkedIn Talent Hub, open the project that you hired the new employee for.</span></span>

2. <span data-ttu-id="1ba29-173">Vyberte záznam kandidáta.</span><span class="sxs-lookup"><span data-stu-id="1ba29-173">Select a candidate record.</span></span>

3. <span data-ttu-id="1ba29-174">Vyberte **Change state** (Změnit stav) a poté vyberte **Hired** (Zařazen).</span><span class="sxs-lookup"><span data-stu-id="1ba29-174">Select **Change stage**, and then select **Hired**.</span></span>

4. <span data-ttu-id="1ba29-175">V nabídce se třemi tečkami (**...**) pro kandidáta vyberte **Export to HRIS** (Exportovat do HRIS).</span><span class="sxs-lookup"><span data-stu-id="1ba29-175">On the ellipsis menu (**...**) for the candidate, select **Export to HRIS**.</span></span>

5. <span data-ttu-id="1ba29-176">V podokně **Export do HRIS** zadejte informace, které je třeba exportovat:</span><span class="sxs-lookup"><span data-stu-id="1ba29-176">In the **Export to HRIS** pane, enter the information that must be exported:</span></span>

    - <span data-ttu-id="1ba29-177">V poli **HRIS provider** (Poskytovatel HRIS) vyberte **Microsoft Dynamics 365 Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="1ba29-177">In the **HRIS provider** field, select **Microsoft Dynamics 365 Human Resources**.</span></span>
    - <span data-ttu-id="1ba29-178">V poli **Start date** (Počáteční datum) vyberte hodnotu pro nového zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="1ba29-178">In the **Start date** field, select a value for the new employee.</span></span>
    - <span data-ttu-id="1ba29-179">V poli **Job title** (Pracovní pozice) zadejte název pozice nového zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="1ba29-179">In the **Job title** field, enter a job title for the new employee's job.</span></span>
    - <span data-ttu-id="1ba29-180">V poli **Location** (Umístění) zadejte umístění, kde bude zaměstnanec sídlit.</span><span class="sxs-lookup"><span data-stu-id="1ba29-180">In the **Location** field, enter the location where the employee will be based.</span></span>
    - <span data-ttu-id="1ba29-181">Zadejte nebo ověřte e-mailovou adresu zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="1ba29-181">Enter or verify the employee's email address.</span></span>

![Export do podokna HRIS v LinkedIn Talent Hub](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

## <a name="complete-onboarding-in-human-resources"></a><span data-ttu-id="1ba29-183">Dokončení zprovoznění v Human Resources</span><span class="sxs-lookup"><span data-stu-id="1ba29-183">Complete onboarding in Human Resources</span></span>

<span data-ttu-id="1ba29-184">Záznamy kandidátů, které jsou exportovány z LinkedIn Talent Hub do Human resources, se objeví v sekci **Uchazeči o pracovní místo** na stránce **Správa zaměstnanců**.</span><span class="sxs-lookup"><span data-stu-id="1ba29-184">Candidate records that are exported from LinkedIn Talent Hub to Human Resources appear in the **Candidates to hire** section of the **Personnel management** page.</span></span>

1. <span data-ttu-id="1ba29-185">V Human Resources otevřete stránku **Správa zaměstnanců**.</span><span class="sxs-lookup"><span data-stu-id="1ba29-185">In Human Resources, open the **Personnel management** page.</span></span>

2. <span data-ttu-id="1ba29-186">V sekci **Uchazeči o pracovní místo** vyberte **Zařadit** pro vybraného kandidáta.</span><span class="sxs-lookup"><span data-stu-id="1ba29-186">In the **Candidates to hire** section, select **Hire** for the selected candidate.</span></span>

3. <span data-ttu-id="1ba29-187">V dialogovém okně **Přijmout nového pracovníka** zkontrolujte záznam a přidejte všechny požadované informace.</span><span class="sxs-lookup"><span data-stu-id="1ba29-187">In the **Hire new worker** dialog box, review the record, and add any required information.</span></span> <span data-ttu-id="1ba29-188">Můžete také vybrat číslo pozice, na kterou byl kandidát přijat.</span><span class="sxs-lookup"><span data-stu-id="1ba29-188">You can also select the position number that the candidate has been hired for.</span></span>

<span data-ttu-id="1ba29-189">Po zadání požadovaných informací můžete pokračovat ve standardních procesech pro vytváření záznamů zaměstnanců a nabírání zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="1ba29-189">After the required information has been entered, you can continue with your standard processes for creating employee records and onboarding employees.</span></span>

<span data-ttu-id="1ba29-190">Následující údaje se importují a zahrnou do nového záznamu zaměstnance:</span><span class="sxs-lookup"><span data-stu-id="1ba29-190">The following details are imported and included on the new employee record:</span></span>

- <span data-ttu-id="1ba29-191">Křestní jméno</span><span class="sxs-lookup"><span data-stu-id="1ba29-191">First name</span></span>
- <span data-ttu-id="1ba29-192">Příjmení</span><span class="sxs-lookup"><span data-stu-id="1ba29-192">Last name</span></span>
- <span data-ttu-id="1ba29-193">Počáteční datum zaměstnání</span><span class="sxs-lookup"><span data-stu-id="1ba29-193">Employment start date</span></span>
- <span data-ttu-id="1ba29-194">E-mailová adresa</span><span class="sxs-lookup"><span data-stu-id="1ba29-194">Email address</span></span>
- <span data-ttu-id="1ba29-195">Telefonní číslo</span><span class="sxs-lookup"><span data-stu-id="1ba29-195">Phone number</span></span>

## <a name="see-also"></a><span data-ttu-id="1ba29-196">Viz také</span><span class="sxs-lookup"><span data-stu-id="1ba29-196">See also</span></span>

[<span data-ttu-id="1ba29-197">Konfigurace virtuálních tabulek Dataverse</span><span class="sxs-lookup"><span data-stu-id="1ba29-197">Configure Dataverse virtual tables</span></span>](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="1ba29-198">Co je Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="1ba29-198">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)
