---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Talent (7. ledna 2020)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 615ed3e4260192ba36826e128f1afa1588e94845
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/21/2020
ms.locfileid: "2974423"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a><span data-ttu-id="f6886-103">Co je nového nebo změněného v aplikaci Dynamics 365 Talent (7. ledna 2020)</span><span class="sxs-lookup"><span data-stu-id="f6886-103">What's new or changed in Dynamics 365 Talent (January 7, 2020)</span></span>

<span data-ttu-id="f6886-104">Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="f6886-104">This article describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="f6886-105">Změny v aplikaci Attract</span><span class="sxs-lookup"><span data-stu-id="f6886-105">Changes in Attract</span></span>

<span data-ttu-id="f6886-106">Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="f6886-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="f6886-107">Změny v aplikaci Onboard</span><span class="sxs-lookup"><span data-stu-id="f6886-107">Changes in Onboard</span></span>

<span data-ttu-id="f6886-108">Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="f6886-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="f6886-109">Změny v Core HR</span><span class="sxs-lookup"><span data-stu-id="f6886-109">Changes in Core HR</span></span>

<span data-ttu-id="f6886-110">Změny popsané v této části se vztahují na číslo sestavení 8.1.2697.</span><span class="sxs-lookup"><span data-stu-id="f6886-110">Changes described in this section apply to build number 8.1.2697.</span></span> <span data-ttu-id="f6886-111">Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="f6886-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a><span data-ttu-id="f6886-112">Nelze odstranit pracovníky, kteří nemají záznamy o zaměstnání – (386157)</span><span class="sxs-lookup"><span data-stu-id="f6886-112">Can't delete workers that don't have employment records - (386157)</span></span>

<span data-ttu-id="f6886-113">Tato změna přidá možnost odstranění do formuláře **Pracovníci bez zaměstnání**.</span><span class="sxs-lookup"><span data-stu-id="f6886-113">This change adds a delete option in the **Workers without employment** form.</span></span> <span data-ttu-id="f6886-114">Pracovníci se v tomto formuláři zobrazují v případě, že pro daného pracovníka neexistuje budoucí, aktivní nebo historická zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="f6886-114">Workers appear in this form when no future, active, or historical employments exist for the worker.</span></span> <span data-ttu-id="f6886-115">V této verzi je možnost odstranění povolena pouze správcům systému.</span><span class="sxs-lookup"><span data-stu-id="f6886-115">In this release, delete is only enabled for System Administrators.</span></span> <span data-ttu-id="f6886-116">Avšak ve vydání příští týden bude zabezpečení aktualizováno tak, aby všichni uživatelé s rolí asistenta lidských zdrojů mohli odebírat zaměstnance bez zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="f6886-116">However, in next week's release, security will be updated to allow all users with the HR assistant role to remove employees without employments.</span></span> <span data-ttu-id="f6886-117">Tyto změny můžete provést také ručně pomocí následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="f6886-117">You can also make these changes manually by following the following steps.</span></span>

1. <span data-ttu-id="f6886-118">Přejděte na **Konfigurace zabezpečení**.</span><span class="sxs-lookup"><span data-stu-id="f6886-118">Go to **Security configuration**.</span></span>
2. <span data-ttu-id="f6886-119">Na kartě **Oprávnění** vyfiltrujte seznam **Oprávnění**, aby bylo možné **spravovat pracovníky**.</span><span class="sxs-lookup"><span data-stu-id="f6886-119">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>
3. <span data-ttu-id="f6886-120">Ve sloupci **Reference** vyberte **zobrazit položky nabídky**.</span><span class="sxs-lookup"><span data-stu-id="f6886-120">In the **References** column, select **Display menu items**.</span></span>
4. <span data-ttu-id="f6886-121">V **Zobrazit položky nabídky** vyberte **HcmWOrkersWithoutEmployment**.</span><span class="sxs-lookup"><span data-stu-id="f6886-121">In **Display menu items**, select **HcmWOrkersWithoutEmployment**.</span></span>
5. <span data-ttu-id="f6886-122">Nastavte oprávnění **Odstranit**, které má být uděleno.</span><span class="sxs-lookup"><span data-stu-id="f6886-122">Set the **Delete** permission to Grant.</span></span>
6. <span data-ttu-id="f6886-123">Vyberte kartu **nepublikované objekty**.</span><span class="sxs-lookup"><span data-stu-id="f6886-123">Select the **Unpublished objects** tab.</span></span>
7. <span data-ttu-id="f6886-124">Zvolte **Publikovat vše**.</span><span class="sxs-lookup"><span data-stu-id="f6886-124">Select **Publish all**.</span></span>
