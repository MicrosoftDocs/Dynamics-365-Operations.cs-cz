---
title: Zodpovědní pracovníci údržby
description: Toto téma vysvětluje, jak nastavit zodpovědné pracovníky údržby v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 432a235668bbd969f497003a98b7f66390e5308f
ms.sourcegitcommit: 2c73749779274e0b0abbcb4041bbc1df0fb6d6e4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/26/2019
ms.locfileid: "1790472"
---
# <a name="responsible-maintenance-workers"></a><span data-ttu-id="68272-103">Zodpovědní pracovníci údržby</span><span class="sxs-lookup"><span data-stu-id="68272-103">Responsible maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="68272-104">Zodpovědní pracovníci údržby mohou být spřízněni s typy majetku, majetkem, funkčními místy, kategoriemi typů údržby, typy prací údržby, variantami typů prací údržby a obchody.</span><span class="sxs-lookup"><span data-stu-id="68272-104">Responsible maintenance workers can be related to asset types, assets, functional locations, maintenance job type categories, maintenance job types, maintenance job type variants, and trades.</span></span> <span data-ttu-id="68272-105">Mohou být použity v pracovních příkazech a požadavcích na údržbu, aby označovali preference týkající se pracovníků údržby, kteří by měli být zodpovědní za pracovní příkaz.</span><span class="sxs-lookup"><span data-stu-id="68272-105">They can be used on work orders and maintenance requests to indicate a preference about the maintenance workers who should be responsible for a work order.</span></span> <span data-ttu-id="68272-106">(Tito pracovníci údržby však nemusí být nutně stejnými zaměstnanci, kteří mají v plánu provést pracovní příkaz.) Použití této funkce je nepovinné.</span><span class="sxs-lookup"><span data-stu-id="68272-106">(However, those maintenance workers aren't necessarily the same workers who are scheduled to carry out the work order.) Use of this functionality is optional.</span></span> <span data-ttu-id="68272-107">Lze jej například použít k výběru odpovědných pracovníků nebo skupin pracovníků pro určité typy práce nebo pracovní oblasti.</span><span class="sxs-lookup"><span data-stu-id="68272-107">For example, it can be used to select responsible workers or worker groups for specific work types or work areas.</span></span>

<span data-ttu-id="68272-108">Během životního cyklu pracovního příkazu nebo životního cyklu požadavků na údržbu je možné změnit nebo aktualizovat zodpovědné pracovníky údržby.</span><span class="sxs-lookup"><span data-stu-id="68272-108">During a work order lifecycle or a maintenance request lifecycle, responsible maintenance workers can be changed or updated.</span></span> <span data-ttu-id="68272-109">Tato změna nebo aktualizace může souviset například se změnou stavu životního cyklu požadavku na údržbu nebo stavem životního cyklu pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="68272-109">This change or update might be related to, for example, a change in the maintenance request lifecycle state or the work order lifecycle state.</span></span>

<span data-ttu-id="68272-110">Nastavení na stránce **Zodpovědní pracovníci údržby** se *nepoužívá* během plánování pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="68272-110">The setup on the **Responsible maintenance workers** page is *not* used during work order scheduling.</span></span>

> [!NOTE]
> <span data-ttu-id="68272-111">V modulu Správa majetku můžete také nastavit *upřednostňované* pracovníky údržby, kteří mohou být během plánování pracovních příkazů přidělovány do pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="68272-111">In Asset Management, you can also set up *preferred* maintenance workers who might be allocated to work orders during work order scheduling.</span></span>

<span data-ttu-id="68272-112">Před nastavením zodpovědných pracovníků údržby je nutné nastavit pracovníky a skupiny pracovníků údržby, kteří by měli být k dispozici pro výběr.</span><span class="sxs-lookup"><span data-stu-id="68272-112">Before you can set up responsible maintenance workers, you must set up the workers and maintenance worker groups that should be available for selection.</span></span> <span data-ttu-id="68272-113">Informace o tom, jak nastavit skupiny zaměstnanců a pracovníků údržby, naleznete v tématu [Pracovníci údržby a skupiny pracovníků](../setup-for-objects/workers-and-worker-groups.md).</span><span class="sxs-lookup"><span data-stu-id="68272-113">For information about how to set up workers and maintenance worker groups, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-responsible-maintenance-workers"></a><span data-ttu-id="68272-114">Nastavit odpovědné pracovníky údržby</span><span class="sxs-lookup"><span data-stu-id="68272-114">Set up responsible maintenance workers</span></span>

1. <span data-ttu-id="68272-115">Vyberte **Správa majetku** \> **Nastavení** \> **Pracovníci** \> **Zodpovědní pracovníci údržby**.</span><span class="sxs-lookup"><span data-stu-id="68272-115">Select **Asset management** \> **Setup** \> **Workers** \> **Responsible maintenance workers**.</span></span>
2. <span data-ttu-id="68272-116">Zvolte **Nový** pro vytvoření záznamu.</span><span class="sxs-lookup"><span data-stu-id="68272-116">Select **New** to create a record.</span></span>
3. <span data-ttu-id="68272-117">Nejprve vytvořte výchozího zodpovědného pracovníka údržby, který je odpovědný za údržbu, a v níž nastavíte pouze pole **Skupina zodpovědných pracovníků údržby** a/nebo pole **Zodpovědný pracovník**.</span><span class="sxs-lookup"><span data-stu-id="68272-117">First create a default responsible maintenance worker or responsible maintenance worker group setup, where you set only the **Responsible maintenance worker group** field and/or the **Responsible worker** field.</span></span> <span data-ttu-id="68272-118">Zbývající pole ponechejte prázdná.</span><span class="sxs-lookup"><span data-stu-id="68272-118">Leave the remaining fields blank.</span></span> <span data-ttu-id="68272-119">Toto výchozí nastavení bude použito během plánování pracovního příkazu, pokud žádná jiná specifická kombinace neodpovídá obsahu pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="68272-119">This default setup will be used during work order scheduling if no other, more specific combination matches the contents of the work order.</span></span>

    > [!NOTE]
    > <span data-ttu-id="68272-120">Při vytváření žádosti o údržbu, kdy je odpovědný pracovník údržby nebo odpovědná skupina pracovníků údržby zpřístupněna pro výběr na stránce **Všechny požadavky na údržbu**, bude správa majetku procházet všemi záznamy odpovědných pracovníků údržby, aby bylo možné vyhledat možnou shodu.</span><span class="sxs-lookup"><span data-stu-id="68272-120">During creation of a maintenance request, when a responsible maintenance worker or responsible maintenance worker group is made available for selection on the **All maintenance requests** page, Asset Management goes through all responsible maintenance worker records to check for a possible match.</span></span> <span data-ttu-id="68272-121">Vždy zkontroluje nejdříve nejkonkrétnější kombinaci.</span><span class="sxs-lookup"><span data-stu-id="68272-121">It always checks the most specific combination first.</span></span> <span data-ttu-id="68272-122">Jinými slovy, Správa majetku nejprve zkontroluje shodu v poli **Obchod**.</span><span class="sxs-lookup"><span data-stu-id="68272-122">In other words, Asset Management first checks for a match for the **Trade** field.</span></span> <span data-ttu-id="68272-123">Pokud není nalezena shoda, zkontroluje shodu v poli **Varianta typu práce údržby**.</span><span class="sxs-lookup"><span data-stu-id="68272-123">If no match is found, it checks for a match for the **Maintenance job type variant** field.</span></span> <span data-ttu-id="68272-124">Pokud není nalezena shoda, zkontroluje shodu v poli **Typ práce údržby** a tak dále.</span><span class="sxs-lookup"><span data-stu-id="68272-124">If no match is found, it checks for a match for the **Maintenance job type** field, and so on.</span></span> <span data-ttu-id="68272-125">Jak je vidět v rozvržení stránky, toto chování znamená, že pro nalezení nejspecifičtější kombinace kontroluje Správa majetku každý záznam zprava doleva pro shodu (nejprve **Obchod**, pak **Varianta typu práce údržby**, pak **Typ práce údržby**, pak **Kategorie typu práce údržby**, pak **Funkční místo**, potom **Majetek** a nakonec **Typ majetku**).</span><span class="sxs-lookup"><span data-stu-id="68272-125">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match (first **Trade**, then **Maintenance job type variant**, then **Maintenance job type**, then **Maintenance job type category**, then **Functional location**, then **Asset**, and finally **Asset type**).</span></span> <span data-ttu-id="68272-126">Není-li nalezena shoda, použije se výchozí záznam, který nemá žádné výběry v těchto sedmi polích.</span><span class="sxs-lookup"><span data-stu-id="68272-126">If no match is found, the default record that has no selections in those seven fields is used.</span></span>

<span data-ttu-id="68272-127">Následující ilustrace znázorňuje příklad stránky **Zodpovědní pracovníci údržby**.</span><span class="sxs-lookup"><span data-stu-id="68272-127">The following illustration shows an example of the **Responsible maintenance workers** page.</span></span>

![Obrázek č. 1](media/08-setup-for-requests.png)
