---
title: Zaměstnanci odpovědní za schvalování neshod
description: Toto téma popisuje, jak konfigurovat pracovníky odpovědné za schvalování neshod.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5979cb33146a00c3ea49ada9577140b24c07928f
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956582"
---
# <a name="workers-responsible-for-approving-nonconformances"></a><span data-ttu-id="b6654-103">Zaměstnanci odpovědní za schvalování neshod</span><span class="sxs-lookup"><span data-stu-id="b6654-103">Workers responsible for approving nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6654-104">Toto téma popisuje, jak konfigurovat pracovníky odpovědné za schvalování neshod.</span><span class="sxs-lookup"><span data-stu-id="b6654-104">This topic describes how to configure workers that are responsible for approving nonconformances.</span></span>

<span data-ttu-id="b6654-105">Neshody musí být schváleny, než uživatelé mohou začít zadávat podrobnosti, jako jsou opravy nebo operace.</span><span class="sxs-lookup"><span data-stu-id="b6654-105">Nonconformances must be approved before users can start to enter details such as corrections or operations.</span></span> <span data-ttu-id="b6654-106">Než uživatelé mohou schválit nebo odmítnout neshody, musí být jejich ID uživatele (záznam uživatele) propojeno se záznamem pracovníka.</span><span class="sxs-lookup"><span data-stu-id="b6654-106">Before users can approve or reject nonconformances, their user ID (user record) must be linked to a worker record.</span></span> <span data-ttu-id="b6654-107">Můžete volitelně nakonfigurovat pracovníky, kteří jsou zodpovědní za kvalitu, a poté jednomu pracovníkovi povolit schválení práce jménem jiného pracovníka.</span><span class="sxs-lookup"><span data-stu-id="b6654-107">You can optionally configure workers that are responsible for quality and then allow one worker to approve work on behalf of another worker.</span></span>

## <a name="enable-a-user-for-nonconformance-processing"></a><span data-ttu-id="b6654-108">Povolení zpracování neshody uživateli</span><span class="sxs-lookup"><span data-stu-id="b6654-108">Enable a user for nonconformance processing</span></span>

<span data-ttu-id="b6654-109">Než uživatel může schválit nebo odmítnout neshody, musíte jeho záznam uživatele propojit se záznamem pracovníka.</span><span class="sxs-lookup"><span data-stu-id="b6654-109">Before a user can approve or reject nonconformances, you must link their user record to a worker record.</span></span> <span data-ttu-id="b6654-110">Pole schválení lze poté nastavit automaticky a aktuálního uživatele lze automaticky vyplnit pro časový rozvrh.</span><span class="sxs-lookup"><span data-stu-id="b6654-110">The approval fields can then be automatically set, and the current user can be automatically filled in for the timesheet.</span></span> <span data-ttu-id="b6654-111">Než může uživatel použít poznámky k dokumentům, musíte v jeho v možnostech uživatele aktivovat manipulaci s dokumenty.</span><span class="sxs-lookup"><span data-stu-id="b6654-111">Before the user can use the document notes, you must activate document handling in their user options.</span></span>

1. <span data-ttu-id="b6654-112">Přejděte do nabídky **Správa systému \> Uživatelé \> Uživatelé**.</span><span class="sxs-lookup"><span data-stu-id="b6654-112">Go to **System administration \> Users \> Users**.</span></span>
1. <span data-ttu-id="b6654-113">Najděte a otevřete uživatele, který by měl být schopen schválit nebo odmítnout neshody.</span><span class="sxs-lookup"><span data-stu-id="b6654-113">Find and open the user who should be able to approve or reject nonconformances.</span></span>
1. <span data-ttu-id="b6654-114">Nastavte pole **Osoba** na jméno pracovníka, který souvisí s aktuálním záznamem uživatele.</span><span class="sxs-lookup"><span data-stu-id="b6654-114">Set the **Person** field to the name of the worker that is related to the current user record.</span></span>
1. <span data-ttu-id="b6654-115">V podokně akcí vyberte volbu **Možnosti uživatele**.</span><span class="sxs-lookup"><span data-stu-id="b6654-115">On the Action Pane, select **User options**.</span></span>
1. <span data-ttu-id="b6654-116">Na stránce **Možnosti** pro aktuální záznam uživatele nastavte na kartě **Předvolby** možnost **Povolit manipulaci s dokumenty** na hodnotu *Ano*.</span><span class="sxs-lookup"><span data-stu-id="b6654-116">On the **Options** page for the current user record, on the **Preferences** tab, set the **Enable document handling** option to *Yes*.</span></span>
1. <span data-ttu-id="b6654-117">Zavřete stránky.</span><span class="sxs-lookup"><span data-stu-id="b6654-117">Close the pages.</span></span>

## <a name="define-workers-that-are-responsible-for-quality"></a><span data-ttu-id="b6654-118">Definování pracovníků odpovědných za kvalitu</span><span class="sxs-lookup"><span data-stu-id="b6654-118">Define workers that are responsible for quality</span></span>

1. <span data-ttu-id="b6654-119">Přejděte k nabídce **Řízení zásob \> Nastavení \> Řízení kvality \> Pracovníci odpovědní za kvalitu**.</span><span class="sxs-lookup"><span data-stu-id="b6654-119">Go to **Inventory management \> Setup \> Quality control \> Workers responsible for quality**.</span></span>
2. <span data-ttu-id="b6654-120">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="b6654-120">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="b6654-121">V poli **Pracovník** vyberte pracovníka, který zadává data o kvalitě.</span><span class="sxs-lookup"><span data-stu-id="b6654-121">In the **Worker** field, select the worker that enters quality data.</span></span>
4. <span data-ttu-id="b6654-122">V poli **Odpovědný pracovník** vyberte pracovníka, pro kterého vybraný pracovník zadává práci jeho jménem.</span><span class="sxs-lookup"><span data-stu-id="b6654-122">In the **Worker responsible** field, select the worker that the selected worker enters work on behalf of.</span></span> <span data-ttu-id="b6654-123">Když se vytvoří a aktualizují neshody, bude tento pracovník ve výchozím nastavení zadán v polích **Pracovník**.</span><span class="sxs-lookup"><span data-stu-id="b6654-123">When nonconformances are created and updated, this worker will be entered by default in **Worker** fields.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b6654-124">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="b6654-124">Additional resources</span></span>

- [<span data-ttu-id="b6654-125">Přehled správy kvality</span><span class="sxs-lookup"><span data-stu-id="b6654-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="b6654-126">Povolit správu kvality a neshod</span><span class="sxs-lookup"><span data-stu-id="b6654-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="b6654-127">Náklady kvality</span><span class="sxs-lookup"><span data-stu-id="b6654-127">Quality charges</span></span>](quality-charges.md)
- [<span data-ttu-id="b6654-128">Karanténní zóny pro neshody</span><span class="sxs-lookup"><span data-stu-id="b6654-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="b6654-129">Diagnostické typy pro neshody</span><span class="sxs-lookup"><span data-stu-id="b6654-129">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="b6654-130">Kódy kvality pro náklady.</span><span class="sxs-lookup"><span data-stu-id="b6654-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="b6654-131">Operace pro neshody</span><span class="sxs-lookup"><span data-stu-id="b6654-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="b6654-132">Správa kvality pro procesy skladu</span><span class="sxs-lookup"><span data-stu-id="b6654-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
