---
title: Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních
description: Následující procedura vysvětluje, jak uživatel přiřazený k roli Správce systému nebo Návrhář elektronického výkaznictví může vytvořit poskytovatele konfigurace pro elektronické výkaznictví.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13a27c2fec2a2b226e9ae8d5b8f9a61e8b79ceb0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544902"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="6e28a-103">Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních</span><span class="sxs-lookup"><span data-stu-id="6e28a-103">Create configuration providers and mark them as active</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6e28a-104">Následující procedura vysvětluje, jak uživatel přiřazený k roli Správce systému nebo Návrhář elektronického výkaznictví může vytvořit poskytovatele konfigurace pro elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="6e28a-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="6e28a-105">Každá konfigurace ER bude odkazovat na zprostředkovatele jako na autora konfigurace.</span><span class="sxs-lookup"><span data-stu-id="6e28a-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="6e28a-106">V tomto příkladu vytvoříte konfiguraci poskytovatele pro vzorovou společnost Litware, Inc. Tyto kroky lze provést v kterékoli společnosti, protože konfigurace poskytovatele ER se sdílí mezi všemi společnostmi.</span><span class="sxs-lookup"><span data-stu-id="6e28a-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="6e28a-107">Vytvoření poskytovatele</span><span class="sxs-lookup"><span data-stu-id="6e28a-107">Create a provider</span></span>
1. <span data-ttu-id="6e28a-108">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="6e28a-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="6e28a-109">Klikněte na Poskytovatelé konfigurace.</span><span class="sxs-lookup"><span data-stu-id="6e28a-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="6e28a-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="6e28a-110">Click New.</span></span>
    * <span data-ttu-id="6e28a-111">Záznam poskytovatele má jedinečný název a adresu URL.</span><span class="sxs-lookup"><span data-stu-id="6e28a-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="6e28a-112">Pokud již záznam pro společnosti Litware, Inc. (http://www.litware.com) existuje, zkontrolujte obsah této stránky a přeskočte tuto proceduru.</span><span class="sxs-lookup"><span data-stu-id="6e28a-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (http://www.litware.com) already exists.</span></span>  
4. <span data-ttu-id="6e28a-113">Zadejte Litware, Inc. do pole Název.</span><span class="sxs-lookup"><span data-stu-id="6e28a-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="6e28a-114">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="6e28a-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="6e28a-115">Do pole Internetová adresa zadejte "http://www.litware.com'.</span><span class="sxs-lookup"><span data-stu-id="6e28a-115">In the Internet address field, type 'http://www.litware.com'.</span></span>
    * http://www.litware.com  
6. <span data-ttu-id="6e28a-116">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="6e28a-116">Click Save.</span></span>
7. <span data-ttu-id="6e28a-117">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="6e28a-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="6e28a-118">Výběr ve formě aktivního poskytovatele</span><span class="sxs-lookup"><span data-stu-id="6e28a-118">Select as an active provider</span></span>
1. <span data-ttu-id="6e28a-119">Vyberte poskytovatele Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="6e28a-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="6e28a-120">Klikněte na možnost Nastavit jako aktivní.</span><span class="sxs-lookup"><span data-stu-id="6e28a-120">Click Set active.</span></span>

