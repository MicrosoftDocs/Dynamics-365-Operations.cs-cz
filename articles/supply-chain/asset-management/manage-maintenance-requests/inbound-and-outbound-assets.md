---
title: Příchozí a odchozí majetek
description: Toto téma vysvětluje, jak registrovat příchozí a odchozí majetek v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetOutboundObjectsListPage, EntAssetOutboundObjectsDeliver, EntAssetInboundObjectsListPage, EntAssetInboundObjectsRecieve
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e6dfadf6824c6a3df7be9b3b6f3d9f5dd2749e34
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018064"
---
# <a name="inbound-and-outbound-assets"></a><span data-ttu-id="d6d24-103">Příchozí a odchozí majetek</span><span class="sxs-lookup"><span data-stu-id="d6d24-103">Inbound and outbound assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="d6d24-104">Pokud vaše společnost provádí úlohy oprav nebo údržby u majetku, který byl přijat z jiných míst nebo od jiných zákazníků, může správa majetku sledovat jak vstupní majetek, který je na cestě do vaší firmy, a příchozí majetek, který se vrací.</span><span class="sxs-lookup"><span data-stu-id="d6d24-104">If your company does repair jobs or maintenance jobs on assets that are received from other locations or customers, Asset Management can track both inbound assets that are on their way to your company and outbound assets that are being returned.</span></span>

> [!NOTE]
> <span data-ttu-id="d6d24-105">Pokud chcete použít příchozí a odchozí stavy životního cyklu pro správu majetku, který přichází nebo se vrací, musíte pro podporu těchto akcí nastavit stavy životního cyklu požadavků na údržbu a modely životního cyklu.</span><span class="sxs-lookup"><span data-stu-id="d6d24-105">If you want to use inbound and outbound lifecycle states to manage assets that are coming in and being returned, you must set up maintenance request lifecycle states and lifecycle models to support these actions.</span></span> <span data-ttu-id="d6d24-106">Další informace naleznete v tématu [Požadavky na údržbu](../setup-for-maintenance-requests/requests.md).</span><span class="sxs-lookup"><span data-stu-id="d6d24-106">For more information, see [Maintenance requests](../setup-for-maintenance-requests/requests.md).</span></span>

<span data-ttu-id="d6d24-107">Nastavení správy majetku určuje, zda můžete pracovat s příchozím nebo odchozím majetkem.</span><span class="sxs-lookup"><span data-stu-id="d6d24-107">The setup of Asset Management determines whether you can work with inbound and outbound assets.</span></span>

## <a name="register-assets-as-inbound"></a><span data-ttu-id="d6d24-108">Registrace majetku jako příchozího</span><span class="sxs-lookup"><span data-stu-id="d6d24-108">Register assets as inbound</span></span>

1. <span data-ttu-id="d6d24-109">Vyberte **Správa majetku** \> **Společné** \> **Požadavky na údržbu** \> **Aktivní požadavky na údržbu**.</span><span class="sxs-lookup"><span data-stu-id="d6d24-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="d6d24-110">Zvolte požadavek na údržbu.</span><span class="sxs-lookup"><span data-stu-id="d6d24-110">Select the maintenance request.</span></span>
3. <span data-ttu-id="d6d24-111">Zvolte **Aktualizovat stav požadavku na údržbu**.</span><span class="sxs-lookup"><span data-stu-id="d6d24-111">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="d6d24-112">Vyberte **Příchozí** (nebo jiný stav životního cyklu, který jste vytvořili pro příchozí majetek) a pak zvolte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6d24-112">Select **Inbound** (or another lifecycle state that you've created for inbound assets), and then select **OK**.</span></span>

![Registrace majetku jako příchozího](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a><span data-ttu-id="d6d24-114">Registrace příchozího majetku jako přijatého</span><span class="sxs-lookup"><span data-stu-id="d6d24-114">Register inbound assets as received</span></span>

1. <span data-ttu-id="d6d24-115">Vyberte **Správa majektu** \> **Společné** \> **Příchozí/odchozí** \> **Příchozí majetek**.</span><span class="sxs-lookup"><span data-stu-id="d6d24-115">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Inbound assets**.</span></span>
2. <span data-ttu-id="d6d24-116">Zvolte majetek nebo požadavek na údržbu.</span><span class="sxs-lookup"><span data-stu-id="d6d24-116">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="d6d24-117">Zvolte **Přijmout majetek**.</span><span class="sxs-lookup"><span data-stu-id="d6d24-117">Select **Receive assets**.</span></span>
4. <span data-ttu-id="d6d24-118">V poli **Přijato** zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="d6d24-118">In the **Received** field, enter the date and time.</span></span> <span data-ttu-id="d6d24-119">Pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6d24-119">Then select **OK**.</span></span> <span data-ttu-id="d6d24-120">Záznam bude odebrán ze stránky se seznamem **Příchozí majetek**.</span><span class="sxs-lookup"><span data-stu-id="d6d24-120">The record is removed from the **Inbound assets** list page.</span></span>

![Registrace příchozího majetku jako přijatého](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a><span data-ttu-id="d6d24-122">Registrace majetku jako odchozího</span><span class="sxs-lookup"><span data-stu-id="d6d24-122">Register assets as outbound</span></span>

<span data-ttu-id="d6d24-123">Po dokončení úlohy údržby nebo opravy můžete majetek zaregistrovat jako vrácený.</span><span class="sxs-lookup"><span data-stu-id="d6d24-123">When you've completed the maintenance or repair job, you can register the asset as returned.</span></span>

1. <span data-ttu-id="d6d24-124">Vyberte **Správa majetku** \> **Společné** \> **Požadavky na údržbu** \> **Aktivní požadavky na údržbu**.</span><span class="sxs-lookup"><span data-stu-id="d6d24-124">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="d6d24-125">Zvolte požadavek na údržbu.</span><span class="sxs-lookup"><span data-stu-id="d6d24-125">Select the maintenance request.</span></span>
3. <span data-ttu-id="d6d24-126">Zvolte **Aktualizovat stav požadavku na údržbu**.</span><span class="sxs-lookup"><span data-stu-id="d6d24-126">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="d6d24-127">Vyberte **Odchozí** (nebo jiný stav životního cyklu, který jste vytvořili pro odchozí majetek) a pak zvolte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6d24-127">Select **Outbound** (or another lifecycle state that you've created for outbound assets), and then select **OK**.</span></span>

## <a name="register-outbound-assets-as-delivered"></a><span data-ttu-id="d6d24-128">Registrace odchozího majetku jako doručeného</span><span class="sxs-lookup"><span data-stu-id="d6d24-128">Register outbound assets as delivered</span></span>

1. <span data-ttu-id="d6d24-129">Vyberte **Správa majektu** \> **Společné** \> **Příchozí/odchozí** \> **Odchozí majetek**.</span><span class="sxs-lookup"><span data-stu-id="d6d24-129">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Outbound assets**.</span></span>
2. <span data-ttu-id="d6d24-130">Zvolte majetek nebo požadavek na údržbu.</span><span class="sxs-lookup"><span data-stu-id="d6d24-130">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="d6d24-131">Vyberte **Doručit majetek**.</span><span class="sxs-lookup"><span data-stu-id="d6d24-131">Select **Deliver assets**.</span></span>
4. <span data-ttu-id="d6d24-132">V poli **Doručeno** zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="d6d24-132">In the **Delivered** field, enter the date and time.</span></span> <span data-ttu-id="d6d24-133">Pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6d24-133">Then select **OK**.</span></span> <span data-ttu-id="d6d24-134">Záznam bude odebrán ze stránky se seznamem **Odchozí majetek**.</span><span class="sxs-lookup"><span data-stu-id="d6d24-134">The record is removed from the **Outbound assets** list page.</span></span>
