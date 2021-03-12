---
title: Nastavení intervalů servisu
description: Servisní interval určuje, jak často jsou pro řádky servisní smlouvy vytvářeny řádky servisní zakázky při automatickém vytváření servisních zakázek.
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementinterval
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 815da6b24de401ad11febb0b0564738ce6967a9c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991658"
---
# <a name="set-up-service-intervals"></a><span data-ttu-id="cba18-103">Nastavení intervalů servisu</span><span class="sxs-lookup"><span data-stu-id="cba18-103">Set up service intervals</span></span>  

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cba18-104">Servisní interval určuje, jak často jsou pro řádky servisní smlouvy vytvářeny řádky servisní zakázky při automatickém vytváření servisních zakázek.</span><span class="sxs-lookup"><span data-stu-id="cba18-104">Service interval indicates the frequency with which service order lines are created for service agreement lines when you create service orders.</span></span>

1. <span data-ttu-id="cba18-105">Klikněte na **Správa servisu** \> **Nastavení** \> **Servisní smlouvy** \> **Intervaly servisu**.</span><span class="sxs-lookup"><span data-stu-id="cba18-105">Click **Service management** \> **Setup** \> **Service agreements** \> **Service intervals**.</span></span>
2. <span data-ttu-id="cba18-106">Vytvořte nový interval servisu.</span><span class="sxs-lookup"><span data-stu-id="cba18-106">Create a new service interval.</span></span>
3. <span data-ttu-id="cba18-107">Zadejte ID a popis intervalu servisu.</span><span class="sxs-lookup"><span data-stu-id="cba18-107">Enter the ID and description of the service interval.</span></span>
4. <span data-ttu-id="cba18-108">Rozsah vyberte v poli **Rozsah**.</span><span class="sxs-lookup"><span data-stu-id="cba18-108">In the **Range** field, select the range.</span></span>
5. <span data-ttu-id="cba18-109">Do pole **Frekvence** zadejte frekvenci.</span><span class="sxs-lookup"><span data-stu-id="cba18-109">In the **Frequency** field, type the frequency.</span></span> <span data-ttu-id="cba18-110">Četnost je koeficient, kterým je nutné vynásobit rozsah, abyste získali interval servisní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="cba18-110">The frequency is the factor by which you must multiply the range to obtain the interval for a service agreement.</span></span>
6. <span data-ttu-id="cba18-111">Stiskem kláves **Alt+S** interval servisu uložte.</span><span class="sxs-lookup"><span data-stu-id="cba18-111">Press **Alt+S** to save the service interval.</span></span>

## <a name="example"></a><span data-ttu-id="cba18-112">Příklad</span><span class="sxs-lookup"><span data-stu-id="cba18-112">Example</span></span>

<span data-ttu-id="cba18-113">Chcete například vytvořit interval servisu o délce 10 dní.</span><span class="sxs-lookup"><span data-stu-id="cba18-113">You want to create a service interval of 10 days.</span></span>

<span data-ttu-id="cba18-114">**Vytvoření intervalu servisu o délce 10 dní**</span><span class="sxs-lookup"><span data-stu-id="cba18-114">**Create a 10-day service interval**</span></span>

1. <span data-ttu-id="cba18-115">Klikněte na **Správa servisu** \> **Nastavení** \> **Servisní smlouvy** \> **Intervaly servisu**.</span><span class="sxs-lookup"><span data-stu-id="cba18-115">Click **Service management** \> **Setup** \> **Service agreements** \> **Service intervals**.</span></span>
2. <span data-ttu-id="cba18-116">Vytvořte nový interval servisu.</span><span class="sxs-lookup"><span data-stu-id="cba18-116">Create a new service interval.</span></span>
3. <span data-ttu-id="cba18-117">Zadejte ID a popis intervalu servisu.</span><span class="sxs-lookup"><span data-stu-id="cba18-117">Enter the ID and description of the service interval.</span></span>
4. <span data-ttu-id="cba18-118">V poli **Rozsah** vyberte **Denně**.</span><span class="sxs-lookup"><span data-stu-id="cba18-118">In the **Range** field, select **Daily**.</span></span>
5. <span data-ttu-id="cba18-119">Do pole **Četnost** zadejte hodnotu 10.</span><span class="sxs-lookup"><span data-stu-id="cba18-119">In the **Frequency** field, type 10.</span></span>
6. <span data-ttu-id="cba18-120">Stiskem kláves **Alt+S** interval servisu uložte.</span><span class="sxs-lookup"><span data-stu-id="cba18-120">Press **Alt+S** to save the service interval.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cba18-121">Související témata</span><span class="sxs-lookup"><span data-stu-id="cba18-121">Related topics</span></span>

[<span data-ttu-id="cba18-122">Intervaly servisu</span><span class="sxs-lookup"><span data-stu-id="cba18-122">Service intervals</span></span>](service-intervals.md)  
