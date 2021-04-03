---
title: Skupiny předmětů servisu
description: Použití skupin objektů je vhodné při řazení a filtrování dat o objektech pro účely sestav a statistik.
author: ShylaThompson
manager: tfehr
ms.date: 05/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectGroups
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9d19e29dbddb0bccf3221cc82e6dbb2c05f7e85
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5266072"
---
# <a name="service-object-groups"></a><span data-ttu-id="4a401-103">Skupiny předmětů servisu</span><span class="sxs-lookup"><span data-stu-id="4a401-103">Service object groups</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4a401-104">Použití skupin objektů je vhodné při řazení a filtrování dat o objektech pro účely sestav a statistik.</span><span class="sxs-lookup"><span data-stu-id="4a401-104">Object groups are useful for sorting and filtering the data about objects for reports and statistics.</span></span> <span data-ttu-id="4a401-105">Můžete například seskupit předměty podle geografického umístění nebo typu.</span><span class="sxs-lookup"><span data-stu-id="4a401-105">For example, you can group objects by geographical location or by type.</span></span>

## <a name="group-by-geographical-location"></a><span data-ttu-id="4a401-106">Seskupení podle geografického umístění</span><span class="sxs-lookup"><span data-stu-id="4a401-106">Group by geographical location</span></span>

<span data-ttu-id="4a401-107">Tato metoda seskupení slouží k zobrazení umístění různých objektů spravovaných vaší společností.</span><span class="sxs-lookup"><span data-stu-id="4a401-107">You can use this grouping method to show where the various different objects that your company services are located.</span></span> <span data-ttu-id="4a401-108">Seskupení předmětů podle geografického umístění může být vhodné například v případě, že potřebujete určit předměty, pro které již v konkrétní zemi nebo oblasti poskytuje vaše společnost servis.</span><span class="sxs-lookup"><span data-stu-id="4a401-108">Grouping objects by geographical location can also be useful if, for example, you must identify the objects that your company already provides services for in a particular country/region.</span></span>

## <a name="example"></a><span data-ttu-id="4a401-109">Příklad</span><span class="sxs-lookup"><span data-stu-id="4a401-109">Example</span></span>

<span data-ttu-id="4a401-110">Odběratel z Belgie volá vaše servisní středisko s požadavkem na vytvoření servisní smlouvy pro objekt ABC.</span><span class="sxs-lookup"><span data-stu-id="4a401-110">A customer from Belgium calls your service center and wants to create a service agreement for an object, ABC.</span></span> <span data-ttu-id="4a401-111">Do všech předmětů, které jsou v Belgii servisovány, jste připojili skupinu předmětů pro zeměpisné umístění Belgie.</span><span class="sxs-lookup"><span data-stu-id="4a401-111">You have attached an object group for geographical location, Belgium, to all objects that are serviced in Belgium.</span></span> <span data-ttu-id="4a401-112">Při použití této skupiny jako filtru můžete rychle vyhledat, zda již máte záznam pro ABC v programu, nebo zda je nutné nastavit nový předmět.</span><span class="sxs-lookup"><span data-stu-id="4a401-112">By using this group as a filter, you can quickly search to see whether you already have a record for ABC in the program, or whether you must set up a new object.</span></span> 

## <a name="group-by-type"></a><span data-ttu-id="4a401-113">Seskupení podle typu</span><span class="sxs-lookup"><span data-stu-id="4a401-113">Group by type</span></span>

<span data-ttu-id="4a401-114">Pomocí této metody seskupení můžete zobrazit typy předmětů, pro které vaše společnost provádí servis.</span><span class="sxs-lookup"><span data-stu-id="4a401-114">You can use this grouping method to show the types of objects that your company services.</span></span> <span data-ttu-id="4a401-115">Seskupení předmětů může být vhodné také v případě, že chcete vytvořit nový objekt na základě podobných předmětů již existujících v daném programu.</span><span class="sxs-lookup"><span data-stu-id="4a401-115">Grouping objects by type can also be useful if, for example, you want to create a new object based on similar objects that already exist in the program.</span></span>

## <a name="example"></a><span data-ttu-id="4a401-116">Příklad</span><span class="sxs-lookup"><span data-stu-id="4a401-116">Example</span></span>

<span data-ttu-id="4a401-117">Odběratel volá s požadavkem na vytvoření servisní smlouvy pro klimatizační jednotku HIJ.</span><span class="sxs-lookup"><span data-stu-id="4a401-117">A customer calls and wants to set up a service agreement for an air conditioning machine, HIJ.</span></span> <span data-ttu-id="4a401-118">Pro tento stroj již nemáte záznam.</span><span class="sxs-lookup"><span data-stu-id="4a401-118">You do not already have a record for this machine.</span></span> <span data-ttu-id="4a401-119">Nastavili jste však skupinu předmětů s názvem Klimatizační jednotky a přiřadili tuto skupinu ke všem předmětům klimatizačních jednotek.</span><span class="sxs-lookup"><span data-stu-id="4a401-119">However, you have set up an object group titled Air Conditioners, and you have attached this group to all air conditioning objects.</span></span> <span data-ttu-id="4a401-120">Proto můžete rychle vyhledávat a identifikovat všechny ostatní klimatizační jednotky a používat informace o šablonách z těchto předmětů, abyste vytvořili řádky servisní smlouvy pro HIJ.</span><span class="sxs-lookup"><span data-stu-id="4a401-120">Therefore, you can quickly search for and identify all other air conditioning machines and use the template information from these objects to create service agreement lines for HIJ.</span></span> <span data-ttu-id="4a401-121">Použitím skupin předmětů tímto způsobem můžete rychle nastavit nové předměty a stanovit servisní úkoly služby, které je třeba na nich provést.</span><span class="sxs-lookup"><span data-stu-id="4a401-121">By using object groups in this manner, you can quickly set up new objects and determine the service tasks that must be performed on them.</span></span> 

## <a name="create-service-object-groups"></a><span data-ttu-id="4a401-122">Vytvoření skupin předmětů servisu</span><span class="sxs-lookup"><span data-stu-id="4a401-122">Create service object groups</span></span>

<span data-ttu-id="4a401-123">Vytvoření skupin, kterým lze přiřazovat předměty servisu.</span><span class="sxs-lookup"><span data-stu-id="4a401-123">Create groups that you can assign service objects to.</span></span> <span data-ttu-id="4a401-124">Servisní předměty jsou skladové položky a další produkty, u kterých se provádějí servis.</span><span class="sxs-lookup"><span data-stu-id="4a401-124">Service objects are inventory items and other products for which services are performed.</span></span> <span data-ttu-id="4a401-125">Vložením předmětů servisu do skupin můžete vytvářet sestavy pro podobné a související předměty servisu.</span><span class="sxs-lookup"><span data-stu-id="4a401-125">By grouping service objects, you can create reports for similar and related service objects.</span></span> <span data-ttu-id="4a401-126">Skupina předmětů servisu může například obsahovat dva předměty servisu: jeden předmět servisu je sada a druhý předmět servisu je služba umožňující nainstalovat sadu.</span><span class="sxs-lookup"><span data-stu-id="4a401-126">For example, a service object group might consist of two service objects: One service object is a kit, and the second service object is the service to install the kit.</span></span>

<span data-ttu-id="4a401-127">Pro vytvoření skupin předmětů servisu postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="4a401-127">To create service object groups, follow these steps:</span></span>

1. <span data-ttu-id="4a401-128">Klikněte na **Správa servisu > Nastavení > Předměty servisu > Skupiny předmětů servisu**.</span><span class="sxs-lookup"><span data-stu-id="4a401-128">Click **Service management > Setup > Service objects > Service object groups**.</span></span>

2. <span data-ttu-id="4a401-129">Kliknutím na možnost **Nový** vytvořte novou skupinu předmětů servisu.</span><span class="sxs-lookup"><span data-stu-id="4a401-129">Click **New** to create a new service object group.</span></span>

3. <span data-ttu-id="4a401-130">Zadejte pro skupinu předmětů servisu jedinečný název a volitelně také popis.</span><span class="sxs-lookup"><span data-stu-id="4a401-130">Enter a unique name for the service object group and, optionally, a description.</span></span>

<span data-ttu-id="4a401-131">Předměty servisu lze přiřadit ke skupině pomocí formuláře **Předměty servisu** .</span><span class="sxs-lookup"><span data-stu-id="4a401-131">You can assign service objects to the group by using the **Service objects** form.</span></span> 

## <a name="see-also"></a><span data-ttu-id="4a401-132">Viz také</span><span class="sxs-lookup"><span data-stu-id="4a401-132">See also</span></span>

[<span data-ttu-id="4a401-133">Tvorba předmětů servisu</span><span class="sxs-lookup"><span data-stu-id="4a401-133">Create service objects</span></span>](create-service-objects.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]