---
title: "Šablony záznamu"
description: "Tento článek představuje koncept šablon záznamů a vysvětluje, jak je lze použít k vytváření záznamů pro sdílení informací."
author: pvillads
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ef5e95d9d6beed10cd6c80aa131c5cbef85c07a8
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="record-templates"></a><span data-ttu-id="d45ed-103">Šablony záznamu</span><span class="sxs-lookup"><span data-stu-id="d45ed-103">Record templates</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d45ed-104">Tento článek představuje koncept šablon záznamů a vysvětluje, jak je lze použít k vytváření záznamů pro sdílení informací.</span><span class="sxs-lookup"><span data-stu-id="d45ed-104">This article introduces the concept of record templates and explains how they can be used to create records that share information.</span></span>

<span data-ttu-id="d45ed-105">Šablony záznamu vám mohou pomoci vytvořit záznamy rychleji v aplikaci Microsoft 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d45ed-105">Record templates can help you to create records more quickly in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="d45ed-106">Šablony záznamu můžete vytvořit pouze pro některé typy záznamů v aplikaci Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d45ed-106">You can create record templates for only some of the record types in Microsoft Dynamics 365 for Finance and Operations.</span></span> 

<span data-ttu-id="d45ed-107">Například si představte že zadáváte informace o půjčovně automobilů, která se nachází v Brně.</span><span class="sxs-lookup"><span data-stu-id="d45ed-107">For example, imagine you are entering rental information for a car rental business that is located in San Francisco.</span></span> <span data-ttu-id="d45ed-108">Vzhledem k tomu, že většina zákazníků bude pravděpodobně z okolí Brna, bylo by výhodné automaticky vyplnit hodnoty pro pole **Stát**, **Země** a **Město** ve formuláři pronájmu.</span><span class="sxs-lookup"><span data-stu-id="d45ed-108">Since most of the customers are likely to be from the San Francisco area, it would be nice if you could automatically fill in the values for the **State**, **Country**, and **City** fields on the rental form.</span></span> 

> [!Note]
> <span data-ttu-id="d45ed-109">Šablony lze použít pouze na ty oblasti aplikace Finance and Operations, k nimž máte přístup.</span><span class="sxs-lookup"><span data-stu-id="d45ed-109">You can apply templates only for the areas of Finance and Operations that you have access to.</span></span> <span data-ttu-id="d45ed-110">Všechny názvy šablon však vidíte také při vytvoření nového záznamu a ostatní uživatelé je vidí, když vytváříte šablony dostupné pro všechny uživatele.</span><span class="sxs-lookup"><span data-stu-id="d45ed-110">However all template titles are visible to you when you create a new record, and to other users as well, if you are creating templates that will be available for all users.</span></span> <span data-ttu-id="d45ed-111">Při pojmenování šablon je třeba mít tento fakt na paměti.</span><span class="sxs-lookup"><span data-stu-id="d45ed-111">Be sure to consider this when naming templates.</span></span> <span data-ttu-id="d45ed-112">Nepoužívejte například názvy, které zahrnují slovo „provize“, pokud je důvěrnou informací to, že někteří zaměstnanci ve společnosti mají plat založený na provizích.</span><span class="sxs-lookup"><span data-stu-id="d45ed-112">For example, avoid using names that include words, such as "commission," if is confidential that some employees in the company have commission-based salaries.</span></span> 

<span data-ttu-id="d45ed-113">Pokud v určitém formuláři existuje jedna nebo více šablon, ke kterým máte přístup, a pokusíte se o vytvoření nového záznamu ve formuláři, zobrazí se stránka **Vyberte šablonu pro...**.</span><span class="sxs-lookup"><span data-stu-id="d45ed-113">When one or more templates that you have access to exist for a specific form and you attempt to create a new record in the form, the **Select a template for** page is displayed.</span></span> <span data-ttu-id="d45ed-114">Pokud vyberete ze seznamu některou šablonu, bude vytvořen nový záznam obsahující výchozí údaje založené na této vybrané šabloně.</span><span class="sxs-lookup"><span data-stu-id="d45ed-114">When you select a template from the list, the new record is created and contains default information that is based on the template that you selected.</span></span> <span data-ttu-id="d45ed-115">Pokud nechcete použít šablony při vytváření nových záznamů, zaškrtněte políčko **Tento dotaz příště nezobrazovat** na stránce **Vybrat šablonu pro**.</span><span class="sxs-lookup"><span data-stu-id="d45ed-115">If you do not want to use templates when you create new records, select the **Do not ask again** check box in the **Select a template for** page.</span></span> <span data-ttu-id="d45ed-116">Pokud chcete zobrazit dialogové okno pro výběr šablony znovu, klikněte pravým tlačítkem na jakýkoli záznam, klikněte na **Informace o záznamu** a pak klikněte na **Zobrazit výběr šablony**.</span><span class="sxs-lookup"><span data-stu-id="d45ed-116">To display the template selection dialog box again, right-click any record, click **Record info**, and then click **Show template selection**.</span></span>




