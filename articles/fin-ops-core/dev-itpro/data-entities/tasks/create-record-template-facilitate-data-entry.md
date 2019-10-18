---
title: Vytvoření šablony záznamu pro usnadnění zadávání dat
description: Toto téma ukazuje, jak vytvořit šablonu záznamu tak, že hodnoty pole, které jsou často používány, nemusí být zadány explicitně pro každý nový záznam.
author: margoc
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 08ee7d0f0ce7e92eaa85137dcd2761bfd702eb8c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181926"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="23540-103">Vytvoření šablony záznamu pro usnadnění zadávání dat</span><span class="sxs-lookup"><span data-stu-id="23540-103">Create a record template to facilitate data entry</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="23540-104">Toto téma ukazuje, jak vytvořit šablonu záznamu tak, že hodnoty pole, které jsou často používány, nemusí být zadány explicitně pro každý nový záznam.</span><span class="sxs-lookup"><span data-stu-id="23540-104">This topic demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="23540-105">V tomto postupu vytvoříte nový záznam pro nové laptopy, které mají být přidány do dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="23540-105">In this procedure, you’ll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="23540-106">Tento postup používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="23540-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="23540-107">V navigačním podokně přejděte na **Moduly > Dlouhodobý majetek > Dlouhodobý majetek > Dlouhodobý majetek**.</span><span class="sxs-lookup"><span data-stu-id="23540-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="23540-108">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="23540-108">Select **New**.</span></span>
3. <span data-ttu-id="23540-109">Zadejte nebo vyberte hodnotu v poli **Skupina dlouhodobého majetku**.</span><span class="sxs-lookup"><span data-stu-id="23540-109">In the **Fixed asset group** field, enter or select a value.</span></span>
4. <span data-ttu-id="23540-110">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="23540-110">In the **Name** field, type a value.</span></span> <span data-ttu-id="23540-111">Zadejte například **laptop potenciálního zákazníka společnosti**.</span><span class="sxs-lookup"><span data-stu-id="23540-111">For example, enter **Corporate lead laptop**.</span></span>  
5. <span data-ttu-id="23540-112">Do pole **Vyhledávání jména** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="23540-112">In the **Search name** field, type a value.</span></span> <span data-ttu-id="23540-113">Například zadejte **laptop**.</span><span class="sxs-lookup"><span data-stu-id="23540-113">For example, enter **laptop**.</span></span>  
6. <span data-ttu-id="23540-114">Rozbalte oddíl **Technické informace**.</span><span class="sxs-lookup"><span data-stu-id="23540-114">Expand the **Technical information** section.</span></span>
7. <span data-ttu-id="23540-115">V polích **Značka**, **Model** a **Rok modelu** zadejte hodnoty.</span><span class="sxs-lookup"><span data-stu-id="23540-115">In the **Make**, **Model**, and **Model year** fields, type values.</span></span>
8. <span data-ttu-id="23540-116">V podokně akcí vyberte **Možnosti**.</span><span class="sxs-lookup"><span data-stu-id="23540-116">On the Action Pane, select **Options**.</span></span>
9. <span data-ttu-id="23540-117">Vyberte **Informace o záznamu**.</span><span class="sxs-lookup"><span data-stu-id="23540-117">Select **Record info**.</span></span>
10. <span data-ttu-id="23540-118">Vyberte **Šablona uživatele**.</span><span class="sxs-lookup"><span data-stu-id="23540-118">Select **User template**.</span></span>
11. <span data-ttu-id="23540-119">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="23540-119">In the **Name** field, type a value.</span></span>
12. <span data-ttu-id="23540-120">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="23540-120">In the **Description** field, type a value.</span></span>
13. <span data-ttu-id="23540-121">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="23540-121">Select **OK**.</span></span>
14. <span data-ttu-id="23540-122">Vyberte **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="23540-122">Select **Close**.</span></span>

