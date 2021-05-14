---
title: Pracovníci bez zaměstnání
description: Pracovníci bez budoucího, aktivního nebo historického zaměstnání ve vaší organizaci se objeví ve formuláři Pracovníci bez zaměstnání.
author: andreabichsel
ms.date: 04/06/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1a137de25924f4c4ec6f6b1fe70f9d21af591c0
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924564"
---
# <a name="workers-without-employment"></a><span data-ttu-id="6e768-103">Pracovníci bez zaměstnání</span><span class="sxs-lookup"><span data-stu-id="6e768-103">Workers without employment</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="6e768-104">Pracovníci bez budoucího, aktivního nebo historického zaměstnání ve vaší organizaci se objeví ve formuláři **Pracovníci bez zaměstnání**.</span><span class="sxs-lookup"><span data-stu-id="6e768-104">Workers with no future, active, or historical employment with your organization appear in the **Workers without employment** form.</span></span> <span data-ttu-id="6e768-105">Pracovníci s tímto stavem se mohou objevit, když importujete pracovníky bez záznamu o zaměstnání nebo když odstraníte zaměstnání pracovníka prostřednictvím **Pracovníci > Historie zaměstnání**.</span><span class="sxs-lookup"><span data-stu-id="6e768-105">Workers with this status can appear when you import workers without an employment record, or when you delete a worker's employment via **Workers > Employment history**.</span></span>

<span data-ttu-id="6e768-106">Ve výchozím nastavení je formulář **Pracovníci bez zaměstnání** k dispozici pro následující role:</span><span class="sxs-lookup"><span data-stu-id="6e768-106">By default, the **Workers without employment** form is available to the following roles:</span></span>

- <span data-ttu-id="6e768-107">Asistent lidských zdrojů</span><span class="sxs-lookup"><span data-stu-id="6e768-107">Human Resources Assistant</span></span>
- <span data-ttu-id="6e768-108">Manažer lidských zdrojů</span><span class="sxs-lookup"><span data-stu-id="6e768-108">Human Resources Manager</span></span>
- <span data-ttu-id="6e768-109">Náborový pracovník</span><span class="sxs-lookup"><span data-stu-id="6e768-109">Recruiter</span></span>
- <span data-ttu-id="6e768-110">Manažer kompenzací a zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="6e768-110">Comp and Benefits Manager</span></span>
- <span data-ttu-id="6e768-111">Správce mezd</span><span class="sxs-lookup"><span data-stu-id="6e768-111">Payroll Administrator</span></span>
- <span data-ttu-id="6e768-112">Manažer mezd</span><span class="sxs-lookup"><span data-stu-id="6e768-112">Payroll Manager</span></span>
- <span data-ttu-id="6e768-113">Manažer školení</span><span class="sxs-lookup"><span data-stu-id="6e768-113">Training Manager</span></span>

<span data-ttu-id="6e768-114">V seznamu **Pracovníci bez zaměstnání** můžete odstranit uvedené osoby.</span><span class="sxs-lookup"><span data-stu-id="6e768-114">In the **Workers without employment** list, you can delete the individuals listed.</span></span> <span data-ttu-id="6e768-115">Ve výchozím nastavení je toto oprávnění uděleno roli asistenta lidských zdrojů.</span><span class="sxs-lookup"><span data-stu-id="6e768-115">By default, this privilege is given to the Human Resources Assistant role.</span></span> <span data-ttu-id="6e768-116">Toto oprávnění můžete udělit dalším rolím pomocí následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="6e768-116">You can give this privilege to other roles with the following steps:</span></span>

1. <span data-ttu-id="6e768-117">Vyberte **Správa systému** a poté vyberte kartu **Konfigurace zabezpečení**.</span><span class="sxs-lookup"><span data-stu-id="6e768-117">Select **System administration**, and then select **Security configuration**.</span></span>

2. <span data-ttu-id="6e768-118">Na kartě **Oprávnění** vyfiltrujte seznam **Oprávnění**, aby bylo možné **spravovat pracovníky**.</span><span class="sxs-lookup"><span data-stu-id="6e768-118">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>

   <span data-ttu-id="6e768-119">[![Filtrovat seznam oprávnění](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span><span class="sxs-lookup"><span data-stu-id="6e768-119">[![Filter Privileges list](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span></span>

3. <span data-ttu-id="6e768-120">Ve sloupci **Reference** vyberte **zobrazit položky nabídky**.</span><span class="sxs-lookup"><span data-stu-id="6e768-120">In the **References** column, select **Display menu items**.</span></span>

4. <span data-ttu-id="6e768-121">V **Zobrazit položky nabídky** vyberte **HcmWorkersWithoutEmployment**.</span><span class="sxs-lookup"><span data-stu-id="6e768-121">In **Display menu items**, select **HcmWorkersWithoutEmployment**.</span></span>

   <span data-ttu-id="6e768-122">[![Zvolit formulář](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span><span class="sxs-lookup"><span data-stu-id="6e768-122">[![Select form](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span></span>

5. <span data-ttu-id="6e768-123">Nastavte oprávnění **Odstranit** na **Udělit**.</span><span class="sxs-lookup"><span data-stu-id="6e768-123">Set the **Delete** permission to **Grant**.</span></span>

6. <span data-ttu-id="6e768-124">Vyberte kartu **nepublikované objekty**.</span><span class="sxs-lookup"><span data-stu-id="6e768-124">Select the **Unpublished objects** tab.</span></span>

7. <span data-ttu-id="6e768-125">Zvolte **Publikovat vše**.</span><span class="sxs-lookup"><span data-stu-id="6e768-125">Select **Publish all**.</span></span>

   <span data-ttu-id="6e768-126">[![Publikovat změny](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span><span class="sxs-lookup"><span data-stu-id="6e768-126">[![Publish changes](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]