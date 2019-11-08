---
title: Vytvoření pracovních příkazů z požadavků na údržbu
description: Toto téma vysvětluje, jak vytvořit pracovní příkaz z požadavku na údržbu v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c42f259a57675c3dbac829d6d671e91982ef9011
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571684"
---
# <a name="create-work-orders-from-maintenance-requests"></a><span data-ttu-id="eeefc-103">Vytvoření pracovních příkazů z požadavků na údržbu</span><span class="sxs-lookup"><span data-stu-id="eeefc-103">Create work orders from maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="eeefc-104">Po vytvoření požadavků na údržbu je lze snadno převést na pracovní příkazy.</span><span class="sxs-lookup"><span data-stu-id="eeefc-104">After you've created maintenance requests, you can easily convert them to work orders.</span></span> <span data-ttu-id="eeefc-105">Toto téma popisuje nejrychlejší způsob, jak pracovat s požadavky na údržbu, aktualizovat několik požadavků na údržbu současně a pak vytvořit pracovní příkaz pro několik požadavků na údržbu současně.</span><span class="sxs-lookup"><span data-stu-id="eeefc-105">This topic describes the quickest way to work with maintenance requests, update several maintenance requests at the same time, and then create a work order for several maintenance requests at the same time.</span></span> <span data-ttu-id="eeefc-106">Na stránce **aktivní požadavky na údržbu** nebo **Moje požadavky na správu mého funkčního místa** je možné také současně pracovat s jedním požadavkem na údržbu a převést jeden požadavek na údržbu na pracovní příkaz.</span><span class="sxs-lookup"><span data-stu-id="eeefc-106">On the **Active maintenance requests** or **My functional location maintenance requests** page, you can also work with one maintenance request at a time and convert one maintenance request to a work order.</span></span>

> [!NOTE]
> <span data-ttu-id="eeefc-107">Každý požadavek na údržbu může souviset pouze s jedním pracovním příkazem.</span><span class="sxs-lookup"><span data-stu-id="eeefc-107">Every maintenance request can be related to only one work order.</span></span> <span data-ttu-id="eeefc-108">Do jednoho pracovního příkazu je však možné zahrnout více požadavků na údržbu, a to i v případě, že požadavky na údržbu mají různý majetek.</span><span class="sxs-lookup"><span data-stu-id="eeefc-108">However, multiple maintenance requests can be included in one work order, even if the maintenance requests have different assets.</span></span>

1. <span data-ttu-id="eeefc-109">Vyberte **Správa majetku** \> **Společné** \> **Požadavky na údržbu** \> **Všechny požadavky na údržbu**.</span><span class="sxs-lookup"><span data-stu-id="eeefc-109">Select **Asset management** \> **Common** \> **maintenance requests** \> **All maintenance requests**.</span></span>
2. <span data-ttu-id="eeefc-110">Před vytvořením pracovní objednávky z požadavků na údržbu je nutné vybrat přinejmenším typ úlohy údržby pro požadavky na údržbu a také variantu typu úlohy údržby a obchod, pokud jsou tyto informace relevantní.</span><span class="sxs-lookup"><span data-stu-id="eeefc-110">Before you can create a work order from maintenance requests, you must select, at a minimum, a maintenance job type for the maintenance requests, and also a maintenance job type variant and trade, if this information is relevant.</span></span> <span data-ttu-id="eeefc-111">V zobrazení mřížky můžete snadno aktualizovat informace o požadavku na údržbu.</span><span class="sxs-lookup"><span data-stu-id="eeefc-111">In the grid view, you can easily update information for a maintenance request.</span></span>
3. <span data-ttu-id="eeefc-112">Jakmile budete připraveni vytvořit pracovní příkaz, vyberte požadavky na údržbu, které mají být do ní zahrnuty.</span><span class="sxs-lookup"><span data-stu-id="eeefc-112">When you're ready to create a work order, select the maintenance requests to include in it.</span></span>

    - <span data-ttu-id="eeefc-113">Pokud vyberete několik požadavků na údržbu pro převod do pracovního příkazu, musí být před vytvořením pracovního příkazu nastavena hodnota v poli **Majetek** a **Typ práce údržby**.</span><span class="sxs-lookup"><span data-stu-id="eeefc-113">If you select several maintenance requests to convert to a work order, both the **Asset** field and the **Maintenance job type** field must be set before you create the work order.</span></span>
    - <span data-ttu-id="eeefc-114">Pokud vyberete jeden požadavek na údržbu pro převod na pracovní příkaz, je nutné před vytvořením pracovního příkazu nastavit pouze pole **Majetek**.</span><span class="sxs-lookup"><span data-stu-id="eeefc-114">If you select one maintenance request to convert to a work order, only the **Asset** field must be set before you create the work order.</span></span> <span data-ttu-id="eeefc-115">Pokud však vytváříte pracovní příkaz, můžete vybrat typ práce údržby (a související variantu a obchod typu práce údržby, pokud jsou tyto informace relevantní) v dialogovém okně **Vytvořit pracovní příkaz**.</span><span class="sxs-lookup"><span data-stu-id="eeefc-115">However, when you create the work order, you can select a maintenance job type (and a related maintenance job type variant and trade, if this information is relevant) in the **Create work order** dialog box.</span></span>

4. <span data-ttu-id="eeefc-116">Vyberte **Pracovní příkaz**.</span><span class="sxs-lookup"><span data-stu-id="eeefc-116">Select **Work order**.</span></span>
5. <span data-ttu-id="eeefc-117">V dialogovém okně **Vytvořit pracovní příkaz** nastavte pole a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="eeefc-117">In the **Create work order** dialog box, set the fields, and then select **OK**.</span></span>

    <span data-ttu-id="eeefc-118">Na panelu zpráv může být zobrazeno upozornění, že byl vytvořen nový pracovní příkaz.</span><span class="sxs-lookup"><span data-stu-id="eeefc-118">A message bar might notify you that a new work order has been created.</span></span>

    <span data-ttu-id="eeefc-119">Pokud navíc vytvoříte pracovní příkaz, který je založený na požadavku na údržbu, bude v případě, že je majetek související s požadavkem na údržbu zahrnut do záruční smlouvy, zobrazí se na panelu zpráv upozornění na záruční smlouvu.</span><span class="sxs-lookup"><span data-stu-id="eeefc-119">Additionally, when you create a work order that is based on a maintenance request, if the asset that is related to the maintenance request is included in a warranty agreement, a message bar notifies you about the warranty agreement.</span></span>

6. <span data-ttu-id="eeefc-120">Vyberte **Správa majetku** \> **Společné** \> **Pracovní příkazy** \> **Všechny pracovní příkazy** a otevřete nový pracovní příkaz.</span><span class="sxs-lookup"><span data-stu-id="eeefc-120">Select **Asset management** \> **Common** \> **Work orders** \> **All work orders**, and open the new work order.</span></span>

    ![Otevření nového pracovního příkazu](media/05-manage-maintenance-requests.png)

