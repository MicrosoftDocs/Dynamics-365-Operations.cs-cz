---
title: "Nastavit fáze servisních zakázek"
description: "Nastavení fází servisních zakázek"
author: YuyuScheller
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 6e2556dd8f3f32da16e53bfe46faec7489d84efa
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="set-up-service-order-stages"></a><span data-ttu-id="0bd5c-103">Nastavit fáze servisních zakázek</span><span class="sxs-lookup"><span data-stu-id="0bd5c-103">Set up service order stages</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="0bd5c-104">Klepněte na tlačítko **řízení servisu** \> **nastavení** \> **servisní zakázky** \> **Fáze servisu**.</span><span class="sxs-lookup"><span data-stu-id="0bd5c-104">Click **Service management** \> **Setup** \> **Service orders** \> **Service stages**.</span></span>

2.  <span data-ttu-id="0bd5c-105">Stisknutím kombinace kláves CTRL+N vytvořte nový záznam.</span><span class="sxs-lookup"><span data-stu-id="0bd5c-105">Press CTRL+N to create a new record.</span></span>

3.  <span data-ttu-id="0bd5c-106">V polích **servisní fáze** a **popis** určete ID fáze servisu a popis.</span><span class="sxs-lookup"><span data-stu-id="0bd5c-106">In the **Service stage** and **Description** fields, specify a service stage ID and description.</span></span>

4.  <span data-ttu-id="0bd5c-107">Vyberte příslušné parametry pro fázi.</span><span class="sxs-lookup"><span data-stu-id="0bd5c-107">Select the appropriate parameters for the stage.</span></span>

5.  <span data-ttu-id="0bd5c-108">Vyberte nadřazenou fázi pro aktuální fázi nebo ponechejte pole **Nadřazené** prázdné, pokud je nastavena fáze v počáteční fázi.</span><span class="sxs-lookup"><span data-stu-id="0bd5c-108">Select the parent stage for the current stage or leave the **Parent** field blank if the stage is the initial stage in the stage setup.</span></span>


> [!NOTE]
> <P><span data-ttu-id="0bd5c-109">Pole <STRONG>Nadřazené</STRONG> nelze po uložení fáze změnit.</span><span class="sxs-lookup"><span data-stu-id="0bd5c-109">You cannot modify the <STRONG>Parent</STRONG> field after you save the stage.</span></span> <span data-ttu-id="0bd5c-110">Místo toho můžete odstranit záznam a vytvořit ho znovu pomocí jiného výběru v poli <STRONG>Nadřazené</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="0bd5c-110">Instead, you can delete the record and create the record again with a different selection in the <STRONG>Parent</STRONG> field.</span></span></P>
> <P><span data-ttu-id="0bd5c-111">Navíc můžete vytvořit pouze jednu fázi s prázdným polem <STRONG>Nadřazené</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="0bd5c-111">Also, you can only create one stage with a blank <STRONG>Parent</STRONG> field.</span></span> <span data-ttu-id="0bd5c-112">To znamená, že je povolena pouze jedna počáteční fáze.</span><span class="sxs-lookup"><span data-stu-id="0bd5c-112">That is, only one initial stage is permitted.</span></span></P>


  



