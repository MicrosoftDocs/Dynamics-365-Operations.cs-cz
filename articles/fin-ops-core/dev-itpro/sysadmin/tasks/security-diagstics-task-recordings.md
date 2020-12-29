---
title: Diagnostika zabezpečení pro záznamy úkolů
description: Toto téma poskytuje informace o tom, jak analyzovat a spravovat požadavky na zabezpečení na základě záznamu úlohy.
author: Peakerbl
manager: AnnBe
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.openlocfilehash: 88eb90b35f1a9754cc4daa01d8f40cdf712db4f8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679783"
---
# <a name="security-diagnostics-for-task-recordings"></a><span data-ttu-id="7e9bc-103">Diagnostika zabezpečení pro záznamy úkolů</span><span class="sxs-lookup"><span data-stu-id="7e9bc-103">Security diagnostics for task recordings</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a><span data-ttu-id="7e9bc-104">Než začnete</span><span class="sxs-lookup"><span data-stu-id="7e9bc-104">Before you begin</span></span>

<span data-ttu-id="7e9bc-105">Toto téma poskytuje informace o tom, jak analyzovat a spravovat požadavky na zabezpečení na základě záznamu úlohy.</span><span class="sxs-lookup"><span data-stu-id="7e9bc-105">This topic provides information about how to analyze and manage security permission requirements based on a task recording.</span></span> <span data-ttu-id="7e9bc-106">Než dokončíte kroky v tomto tématu, musíte mít záznam úkolu obchodního procesu, který chcete analyzovat.</span><span class="sxs-lookup"><span data-stu-id="7e9bc-106">Before you complete the steps in this topic, you must have a task recording of the business process that you want to analyze.</span></span> <span data-ttu-id="7e9bc-107">Chcete-li zaznamenat obchodní proces, získáte informace v tématu [Zdroje záznamu úloh](../../user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="7e9bc-107">To record a business process, see [Task recorder resources](../../user-interface/task-recorder.md).</span></span> 

## <a name="manage-security-for-a-task-recording"></a><span data-ttu-id="7e9bc-108">Správa zabezpečení záznamu úlohy</span><span class="sxs-lookup"><span data-stu-id="7e9bc-108">Manage security for a task recording</span></span>

1. <span data-ttu-id="7e9bc-109">Přejděte na **Správa systému** > **Zabezpečení** > **Diagnostika zabezpečení pro záznam úlohy**.</span><span class="sxs-lookup"><span data-stu-id="7e9bc-109">Go to **System administration** > **Security** > **Security diagnostic for task recording**.</span></span>
2. <span data-ttu-id="7e9bc-110">Otevřete záznam úlohy z jeho umístění.</span><span class="sxs-lookup"><span data-stu-id="7e9bc-110">Open the task recording from its location.</span></span> <span data-ttu-id="7e9bc-111">Vyberte **Otevřít z tohoto počítače** nebo **Otevřít ze služby Lifecycle Services** a pak vyberte **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="7e9bc-111">Select **Open from this PC** or **Open from Lifecycle Services**, and then select **Close**.</span></span>
3. <span data-ttu-id="7e9bc-112">Tím se otevře stránka **Podrobnosti položky nabídky zabezpečení**, která obsahuje seznam objektů zabezpečení požadovaných pro proces.</span><span class="sxs-lookup"><span data-stu-id="7e9bc-112">This will open the **Security menu item details** page that lists the security objects required for the process.</span></span>

 > [!NOTE]
 > <span data-ttu-id="7e9bc-113">V seznamu nejsou uvedeny položky nabídky **Akce** a **Výstup**.</span><span class="sxs-lookup"><span data-stu-id="7e9bc-113">The **Action** and **Output** menu items are not included in the list.</span></span>

4. <span data-ttu-id="7e9bc-114">V poli **ID uživatele** vyberte uživatele.</span><span class="sxs-lookup"><span data-stu-id="7e9bc-114">In the **User ID** field, select a user.</span></span> <span data-ttu-id="7e9bc-115">Pokud uživatel nemá oprávnění pro některé položky nabídky, pole **Chybějící oprávnění** se aktualizuje na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="7e9bc-115">If the user does not have permissions for some menu items, the **Missing permissions** field will update to **Yes**.</span></span>
  
  ![Stránka podrobností položky nabídky zabezpečení](../media/Security-Menu-Item-Details.png)

5. <span data-ttu-id="7e9bc-117">Vyberte **Přidat odkaz** pro zobrazení seznamu bezpečnostních objektů, včetně rolí, povinností a oprávnění, která udělují chybějící oprávnění.</span><span class="sxs-lookup"><span data-stu-id="7e9bc-117">Select **Add Reference** to see a list of the security objects, including roles, duties, and privileges that grant the missing permission.</span></span>
6. <span data-ttu-id="7e9bc-118">Vyberte objekt zabezpečení ze seznamu.</span><span class="sxs-lookup"><span data-stu-id="7e9bc-118">Select a security object from the list:</span></span>

    - <span data-ttu-id="7e9bc-119">Pokud je vybraná **Role**, vyberte **Přidat roli uživateli**.</span><span class="sxs-lookup"><span data-stu-id="7e9bc-119">If **Role** is selected, select **Add role to user**.</span></span> <span data-ttu-id="7e9bc-120">Otevře se stránka **Přiřadit uživatele rolím**.</span><span class="sxs-lookup"><span data-stu-id="7e9bc-120">This will open the **Assign users to roles** page.</span></span> <span data-ttu-id="7e9bc-121">Další informace viz [Přiřazení uživatelů rolím zabezpečení](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7e9bc-121">For more information, see [Assign users to security roles](assign-users-security-roles.md) page.</span></span>
    - <span data-ttu-id="7e9bc-122">Pokud je vybraná **Povinnost**, vyberte **Přiřadit povinnost roli**, vyberte role, k nimž má být povinnost přidána, a vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="7e9bc-122">If **Duty** is selected, select **Add duty to role**, select the roles that the duty should be added to, and then select **OK**.</span></span>
    - <span data-ttu-id="7e9bc-123">Pokud je vybráno **Oprávnění**, vyberte **Přiřadit oprávnění povinnostem**, vyberte role, k nimž má být povinnost přidána, a vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="7e9bc-123">If **Privilege** is selected, select **Add privilege to duties**, select the roles that the duty should be added to, and then select **OK**.</span></span>
