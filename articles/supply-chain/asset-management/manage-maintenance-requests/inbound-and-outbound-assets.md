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
ms.openlocfilehash: 9c77aa0dc10844fbe07afa0b8d2a6f3578a246ab
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253334"
---
# <a name="inbound-and-outbound-assets"></a><span data-ttu-id="fc156-103">Příchozí a odchozí majetek</span><span class="sxs-lookup"><span data-stu-id="fc156-103">Inbound and outbound assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="fc156-104">Pokud vaše společnost provádí úlohy oprav nebo údržby u majetku, který byl přijat z jiných míst nebo od jiných zákazníků, může správa majetku sledovat jak vstupní majetek, který je na cestě do vaší firmy, a příchozí majetek, který se vrací.</span><span class="sxs-lookup"><span data-stu-id="fc156-104">If your company does repair jobs or maintenance jobs on assets that are received from other locations or customers, Asset Management can track both inbound assets that are on their way to your company and outbound assets that are being returned.</span></span>

> [!NOTE]
> <span data-ttu-id="fc156-105">Pokud chcete použít příchozí a odchozí stavy životního cyklu pro správu majetku, který přichází nebo se vrací, musíte pro podporu těchto akcí nastavit stavy životního cyklu požadavků na údržbu a modely životního cyklu.</span><span class="sxs-lookup"><span data-stu-id="fc156-105">If you want to use inbound and outbound lifecycle states to manage assets that are coming in and being returned, you must set up maintenance request lifecycle states and lifecycle models to support these actions.</span></span> <span data-ttu-id="fc156-106">Další informace naleznete v tématu [Požadavky na údržbu](../setup-for-maintenance-requests/requests.md).</span><span class="sxs-lookup"><span data-stu-id="fc156-106">For more information, see [Maintenance requests](../setup-for-maintenance-requests/requests.md).</span></span>

<span data-ttu-id="fc156-107">Nastavení správy majetku určuje, zda můžete pracovat s příchozím nebo odchozím majetkem.</span><span class="sxs-lookup"><span data-stu-id="fc156-107">The setup of Asset Management determines whether you can work with inbound and outbound assets.</span></span>

## <a name="register-assets-as-inbound"></a><span data-ttu-id="fc156-108">Registrace majetku jako příchozího</span><span class="sxs-lookup"><span data-stu-id="fc156-108">Register assets as inbound</span></span>

1. <span data-ttu-id="fc156-109">Vyberte **Správa majetku** \> **Společné** \> **Požadavky na údržbu** \> **Aktivní požadavky na údržbu**.</span><span class="sxs-lookup"><span data-stu-id="fc156-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="fc156-110">Zvolte požadavek na údržbu.</span><span class="sxs-lookup"><span data-stu-id="fc156-110">Select the maintenance request.</span></span>
3. <span data-ttu-id="fc156-111">Zvolte **Aktualizovat stav požadavku na údržbu**.</span><span class="sxs-lookup"><span data-stu-id="fc156-111">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="fc156-112">Vyberte **Příchozí** (nebo jiný stav životního cyklu, který jste vytvořili pro příchozí majetek) a pak zvolte **OK**.</span><span class="sxs-lookup"><span data-stu-id="fc156-112">Select **Inbound** (or another lifecycle state that you've created for inbound assets), and then select **OK**.</span></span>

![Registrace majetku jako příchozího](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a><span data-ttu-id="fc156-114">Registrace příchozího majetku jako přijatého</span><span class="sxs-lookup"><span data-stu-id="fc156-114">Register inbound assets as received</span></span>

1. <span data-ttu-id="fc156-115">Vyberte **Správa majektu** \> **Společné** \> **Příchozí/odchozí** \> **Příchozí majetek**.</span><span class="sxs-lookup"><span data-stu-id="fc156-115">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Inbound assets**.</span></span>
2. <span data-ttu-id="fc156-116">Zvolte majetek nebo požadavek na údržbu.</span><span class="sxs-lookup"><span data-stu-id="fc156-116">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="fc156-117">Zvolte **Přijmout majetek**.</span><span class="sxs-lookup"><span data-stu-id="fc156-117">Select **Receive assets**.</span></span>
4. <span data-ttu-id="fc156-118">V poli **Přijato** zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="fc156-118">In the **Received** field, enter the date and time.</span></span> <span data-ttu-id="fc156-119">Pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="fc156-119">Then select **OK**.</span></span> <span data-ttu-id="fc156-120">Záznam bude odebrán ze stránky se seznamem **Příchozí majetek**.</span><span class="sxs-lookup"><span data-stu-id="fc156-120">The record is removed from the **Inbound assets** list page.</span></span>

![Registrace příchozího majetku jako přijatého](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a><span data-ttu-id="fc156-122">Registrace majetku jako odchozího</span><span class="sxs-lookup"><span data-stu-id="fc156-122">Register assets as outbound</span></span>

<span data-ttu-id="fc156-123">Po dokončení úlohy údržby nebo opravy můžete majetek zaregistrovat jako vrácený.</span><span class="sxs-lookup"><span data-stu-id="fc156-123">When you've completed the maintenance or repair job, you can register the asset as returned.</span></span>

1. <span data-ttu-id="fc156-124">Vyberte **Správa majetku** \> **Společné** \> **Požadavky na údržbu** \> **Aktivní požadavky na údržbu**.</span><span class="sxs-lookup"><span data-stu-id="fc156-124">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="fc156-125">Zvolte požadavek na údržbu.</span><span class="sxs-lookup"><span data-stu-id="fc156-125">Select the maintenance request.</span></span>
3. <span data-ttu-id="fc156-126">Zvolte **Aktualizovat stav požadavku na údržbu**.</span><span class="sxs-lookup"><span data-stu-id="fc156-126">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="fc156-127">Vyberte **Odchozí** (nebo jiný stav životního cyklu, který jste vytvořili pro odchozí majetek) a pak zvolte **OK**.</span><span class="sxs-lookup"><span data-stu-id="fc156-127">Select **Outbound** (or another lifecycle state that you've created for outbound assets), and then select **OK**.</span></span>

## <a name="register-outbound-assets-as-delivered"></a><span data-ttu-id="fc156-128">Registrace odchozího majetku jako doručeného</span><span class="sxs-lookup"><span data-stu-id="fc156-128">Register outbound assets as delivered</span></span>

1. <span data-ttu-id="fc156-129">Vyberte **Správa majektu** \> **Společné** \> **Příchozí/odchozí** \> **Odchozí majetek**.</span><span class="sxs-lookup"><span data-stu-id="fc156-129">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Outbound assets**.</span></span>
2. <span data-ttu-id="fc156-130">Zvolte majetek nebo požadavek na údržbu.</span><span class="sxs-lookup"><span data-stu-id="fc156-130">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="fc156-131">Vyberte **Doručit majetek**.</span><span class="sxs-lookup"><span data-stu-id="fc156-131">Select **Deliver assets**.</span></span>
4. <span data-ttu-id="fc156-132">V poli **Doručeno** zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="fc156-132">In the **Delivered** field, enter the date and time.</span></span> <span data-ttu-id="fc156-133">Pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="fc156-133">Then select **OK**.</span></span> <span data-ttu-id="fc156-134">Záznam bude odebrán ze stránky se seznamem **Odchozí majetek**.</span><span class="sxs-lookup"><span data-stu-id="fc156-134">The record is removed from the **Outbound assets** list page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]