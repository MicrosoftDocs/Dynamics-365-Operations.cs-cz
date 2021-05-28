---
title: Omezení úpravy osobních údajů
description: U zaměstnanců můžete omezit jejich upravování kontaktních údajů v aplikaci Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c5e3eeb66d4f32b1fea1a43fff9f5b09d87d1f53
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018702"
---
# <a name="restrict-editing-of-personal-information"></a><span data-ttu-id="0c037-103">Omezení úpravy osobních údajů</span><span class="sxs-lookup"><span data-stu-id="0c037-103">Restrict editing of personal information</span></span>

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

<span data-ttu-id="0c037-104">Toto téma popisuje, jak omezit zaměstnance v úpravách kontaktních údajů v aplikaci Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0c037-104">This topic describes how to restrict employees from editing contact details in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="0c037-105">Možná budete chtít zabránit zaměstnancům v úpravách určitých kontaktních údajů, například jejich sídla firmy nebo e-mailové adresy.</span><span class="sxs-lookup"><span data-stu-id="0c037-105">You might want to prevent employees from editing certain contact details, such as their business location or email address.</span></span>

> [!NOTE]
> <span data-ttu-id="0c037-106">Chcete-li použít tuto funkci, musíte nejprve povolit funkci **(Preview) Omezit zaměstnance v přidávání nebo úpravách adresy a kontaktních údajů pro vybrané účely** ve Správě funkcí.</span><span class="sxs-lookup"><span data-stu-id="0c037-106">To use this feature, you must first enable **(Preview) Restrict employees from adding or editing address and contact information for select purposes** in Feature management.</span></span> <span data-ttu-id="0c037-107">Další informace o povolení funkcí Preview naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="0c037-107">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span><br><br><span data-ttu-id="0c037-108">![Povolit funkci Preview](./media/hr-employee-self-service-restrict-enable.png)</span><span class="sxs-lookup"><span data-stu-id="0c037-108">![Enable preview feature](./media/hr-employee-self-service-restrict-enable.png)</span></span>

## <a name="choose-the-information-an-employee-can-add-or-edit"></a><span data-ttu-id="0c037-109">Vyberte informace, které zaměstnanec může přidat nebo upravit</span><span class="sxs-lookup"><span data-stu-id="0c037-109">Choose the information an employee can add or edit</span></span>

1. <span data-ttu-id="0c037-110">V Human Resources vyberte možnost **Správa zaměstnanců**, vyberte **Odkazy** a poté vyberte **Parametry lidských zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="0c037-110">In Human Resources, select **Personnel management**, select **Links**, and then select **Human resources parameters**.</span></span>

   ![Přechod na parametry lidských zdrojů](./media/hr-employee-self-service-human-resources-parameters.png)

2. <span data-ttu-id="0c037-112">Na stránce **Parametry lidských zdrojů** vyberte kartu **Samoobsluha pro zaměstnance**.</span><span class="sxs-lookup"><span data-stu-id="0c037-112">On the **Human resources parameters** page, select the **Employee self service** tab.</span></span>

   ![Výběr Samoobsluhy pro zaměstnance](./media/hr-employee-self-service-tab.png)

3. <span data-ttu-id="0c037-114">Na kartě **Samoobsluha pro zaměstnance** zrušte zaškrtnutí všech informací v části **Adresa a kontaktní informace**, kterou zaměstnanci nemají přidávat nebo upravovat.</span><span class="sxs-lookup"><span data-stu-id="0c037-114">On the **Employee self service** tab, uncheck all information in the **Address and contact information** section that you don't want employees to add or edit.</span></span> <span data-ttu-id="0c037-115">V tomto příkladu jsme zrušili zaškrtnutí **Obchodních** kontaktních informací.</span><span class="sxs-lookup"><span data-stu-id="0c037-115">In this example, we've unchecked **Business** contact information.</span></span>

   ![Omezení úprav obchodních kontaktních údajů](./media/hr-employee-self-service-restrict-business.png)

4. <span data-ttu-id="0c037-117">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="0c037-117">Select **Save**.</span></span>

   ![Uložit změny](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a><span data-ttu-id="0c037-119">Zkušenosti zaměstnanců</span><span class="sxs-lookup"><span data-stu-id="0c037-119">Employee experience</span></span>

<span data-ttu-id="0c037-120">Poté, co jste omezili zaměstnance v přidávání nebo úpravách kontaktních údajů, mohou tyto informace zobrazit, ale nemohou je změnit.</span><span class="sxs-lookup"><span data-stu-id="0c037-120">After you've restricted employees from adding or editing contact details, they can see the information, but can't change it.</span></span>

<span data-ttu-id="0c037-121">V tomto příkladu, kde jsou zaměstnanci omezeni v úpravách **Obchodních** kontaktních údajů, mohou i nadále vidět informace v Samoobsluze pro zaměstnance:</span><span class="sxs-lookup"><span data-stu-id="0c037-121">In this example, where employees are restricted from editing **Business** contact details, they can still see the information in Employee self service:</span></span>

![Zobrazení obchodních kontaktních údajů](./media/hr-employee-self-service-restrict-view.png)

<span data-ttu-id="0c037-123">Když však vyberou obchodní kontaktní údaje, podokno **Upravit adresu** se zobrazí jen ke čtení a nemohou v něm změnit žádné z polí.</span><span class="sxs-lookup"><span data-stu-id="0c037-123">However, when they select the business contact details, the **Edit address** pane appears as read-only, and they can't change any of the fields.</span></span>

![Podrobnosti o obchodním kontaktu se zobrazují jen ke čtení](./media/hr-employee-self-service-restrict-read-only.png)

<span data-ttu-id="0c037-125">Kromě toho, pokud vyberou možnost **Přidat** za účelem přidání nové adresy, nemohou vybrat v rozevíracím poli **Účel** hodnotu **Obchodní**.</span><span class="sxs-lookup"><span data-stu-id="0c037-125">In addition, if they select **Add** to add a new address, they can't select **Business** from the **Purpose** dropdown box.</span></span>

![Zaměstnanec nemůže přidat obchodní adresu](./media/hr-employee-self-service-restrict-add.png)

<span data-ttu-id="0c037-127">To samé zaměstnanci zažijí při výběru části **Kontaktní údaje** na stránce **Osobní informace** a pokusu o přidání nové adresy.</span><span class="sxs-lookup"><span data-stu-id="0c037-127">Employees get the same experience when they select **Contact details** on the **Personal information** page and add a new address.</span></span> <span data-ttu-id="0c037-128">Rozevírací seznam **Účel** zobrazuje pouze ty typy informací, které mohou přidat.</span><span class="sxs-lookup"><span data-stu-id="0c037-128">The **Purpose** dropdown box only displays the types of information they can add.</span></span> 

![Zaměstnanec nemůže vybrat položku Obchodní v rozevírací nabídce Účel](./media/hr-employee-self-service-restrict-purpose.png)

<span data-ttu-id="0c037-130">**Kontaktní údaje** nyní ukazují v mřížce údaj **Účel**.</span><span class="sxs-lookup"><span data-stu-id="0c037-130">**Contact details** now shows **Purpose** in the grid.</span></span>

![Účel se zobrazí v mřížce podrobností kontaktu](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a><span data-ttu-id="0c037-132">Viz také</span><span class="sxs-lookup"><span data-stu-id="0c037-132">See also</span></span>

[<span data-ttu-id="0c037-133">Přehled samoobsluhy pro zaměstnance a manažera</span><span class="sxs-lookup"><span data-stu-id="0c037-133">Employee and Manager self service overview</span></span>](hr-employee-manager-self-service-overview.md)<br>
[<span data-ttu-id="0c037-134">Konfigurace parametrů Human Resources</span><span class="sxs-lookup"><span data-stu-id="0c037-134">Configure Human resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="0c037-135">Upravit osobní informace</span><span class="sxs-lookup"><span data-stu-id="0c037-135">Edit personal information</span></span>](hr-employee-manager-self-service-edit-personal-information.md)