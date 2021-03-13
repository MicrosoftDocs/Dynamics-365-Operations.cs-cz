---
title: Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních
description: Toto téma vysvětluje, jak uživatel přiřazený k roli Správce systému nebo Návrhář elektronického výkaznictví může vytvořit poskytovatele.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 835e35ef233ba5734e5a4d47f624629e95ae5b89
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092053"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="c5696-103">Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních</span><span class="sxs-lookup"><span data-stu-id="c5696-103">Create configuration providers and mark them as active</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c5696-104">Toto téma vysvětluje, jak uživatel přiřazený k roli Správce systému nebo Návrhář elektronického výkaznictví může vytvořit poskytovatele konfigurace pro elektronické výkaznictví (ER).</span><span class="sxs-lookup"><span data-stu-id="c5696-104">This topic explains how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="c5696-105">Každá konfigurace ER bude odkazovat na zprostředkovatele jako na autora konfigurace.</span><span class="sxs-lookup"><span data-stu-id="c5696-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="c5696-106">V tomto příkladu vytvoříte konfiguraci poskytovatele pro vzorovou společnost Litware, Inc. Tyto kroky lze provést v kterékoli společnosti, protože konfigurace poskytovatele ER se sdílí mezi všemi společnostmi.</span><span class="sxs-lookup"><span data-stu-id="c5696-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>

## <a name="create-a-provider"></a><span data-ttu-id="c5696-107">Vytvoření poskytovatele</span><span class="sxs-lookup"><span data-stu-id="c5696-107">Create a provider</span></span>
1. <span data-ttu-id="c5696-108">Přejděte do **navigačního podokna** v levém horním rohu a vyberte možnost **Správa organizace**.</span><span class="sxs-lookup"><span data-stu-id="c5696-108">Go to the **navigation pane** in the upper left corner and select **Organization administration**.</span></span>
2. <span data-ttu-id="c5696-109">Přejděte na **Pracovní prostory > Elektronické sestavy**.</span><span class="sxs-lookup"><span data-stu-id="c5696-109">Go to **Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="c5696-110">Přejděte na **Související odkazy > Poskytovatelé konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="c5696-110">Go to **Related links > Configuration providers**.</span></span>
4. <span data-ttu-id="c5696-111">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="c5696-111">Select **New**.</span></span>
    - <span data-ttu-id="c5696-112">Záznam poskytovatele má jedinečný název a adresu URL.</span><span class="sxs-lookup"><span data-stu-id="c5696-112">A provider record has a unique name and URL.</span></span> <span data-ttu-id="c5696-113">Pokud již záznam pro společnosti Litware, Inc. (https://www.litware.com) existuje, zkontrolujte obsah této stránky a přeskočte tuto proceduru.</span><span class="sxs-lookup"><span data-stu-id="c5696-113">Review the content of this page and skip this procedure if a record for Litware, Inc. (https://www.litware.com) already exists.</span></span>  
5. <span data-ttu-id="c5696-114">Do pole Název zadejte `Litware, Inc.`.</span><span class="sxs-lookup"><span data-stu-id="c5696-114">In the Name field, type `Litware, Inc.`.</span></span>
6. <span data-ttu-id="c5696-115">Do pole Internetová adresa zadejte `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="c5696-115">In the Internet address field, type `https://www.litware.com`.</span></span>
7. <span data-ttu-id="c5696-116">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="c5696-116">Select **Save**.</span></span>
8. <span data-ttu-id="c5696-117">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c5696-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="c5696-118">Výběr ve formě aktivního poskytovatele</span><span class="sxs-lookup"><span data-stu-id="c5696-118">Select as an active provider</span></span>
1. <span data-ttu-id="c5696-119">Vyberte poskytovatele Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="c5696-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="c5696-120">Vyberte **Nastavit jako aktivní**.</span><span class="sxs-lookup"><span data-stu-id="c5696-120">Select **Set active**.</span></span>

![Stránka pracovního prostoru elektronického vykazování](../media/GER-Task-ActiveProvider-1.png)
