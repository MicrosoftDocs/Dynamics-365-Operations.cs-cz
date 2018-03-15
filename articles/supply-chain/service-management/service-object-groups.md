---
title: "Skupiny předmětů servisu"
description: "Použití skupin objektů je vhodné při řazení a filtrování dat o objektech pro účely sestav a statistik."
author: YuyuScheller
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectGroups
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
ms.sourcegitcommit: 221b9dae7e83e7f4a535ac60f2a2011533d7861c
ms.openlocfilehash: fa503ac82286099a0eafc7034d169e165b538e2c
ms.contentlocale: cs-cz
ms.lasthandoff: 02/21/2018

---

# <a name="service-object-groups"></a><span data-ttu-id="8c3f2-103">Skupiny předmětů servisu</span><span class="sxs-lookup"><span data-stu-id="8c3f2-103">Service object groups</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8c3f2-104">Použití skupin objektů je vhodné při řazení a filtrování dat o objektech pro účely sestav a statistik.</span><span class="sxs-lookup"><span data-stu-id="8c3f2-104">Object groups are useful for sorting and filtering the data about objects for reports and statistics.</span></span> <span data-ttu-id="8c3f2-105">Můžete například seskupit předměty podle geografického umístění nebo typu.</span><span class="sxs-lookup"><span data-stu-id="8c3f2-105">For example, you can group objects by geographical location or by type.</span></span>

## <a name="group-by-geographical-location"></a><span data-ttu-id="8c3f2-106">Seskupení podle geografického umístění</span><span class="sxs-lookup"><span data-stu-id="8c3f2-106">Group by geographical location</span></span>

<span data-ttu-id="8c3f2-107">Tato metoda seskupení slouží k zobrazení umístění různých objektů spravovaných vaší společností.</span><span class="sxs-lookup"><span data-stu-id="8c3f2-107">You can use this grouping method to show where the various different objects that your company services are located.</span></span> <span data-ttu-id="8c3f2-108">Seskupení předmětů podle geografického umístění může být vhodné například v případě, že potřebujete určit předměty, pro které již v konkrétní zemi nebo oblasti poskytuje vaše společnost servis.</span><span class="sxs-lookup"><span data-stu-id="8c3f2-108">Grouping objects by geographical location can also be useful if, for example, you must identify the objects that your company already provides services for in a particular country/region.</span></span>

## <a name="example"></a><span data-ttu-id="8c3f2-109">Příklad</span><span class="sxs-lookup"><span data-stu-id="8c3f2-109">Example</span></span>

<span data-ttu-id="8c3f2-110">Odběratel z Belgie volá vaše servisní středisko s požadavkem na vytvoření servisní smlouvy pro objekt ABC.</span><span class="sxs-lookup"><span data-stu-id="8c3f2-110">A customer from Belgium calls your service center and wants to create a service agreement for an object, ABC.</span></span> <span data-ttu-id="8c3f2-111">Do všech předmětů, které jsou v Belgii servisovány, jste připojili skupinu předmětů pro zeměpisné umístění Belgie.</span><span class="sxs-lookup"><span data-stu-id="8c3f2-111">You have attached an object group for geographical location, Belgium, to all objects that are serviced in Belgium.</span></span> <span data-ttu-id="8c3f2-112">Při použití této skupiny jako filtru můžete rychle vyhledat, zda již máte záznam pro ABC v programu, nebo zda je nutné nastavit nový předmět.</span><span class="sxs-lookup"><span data-stu-id="8c3f2-112">By using this group as a filter, you can quickly search to see whether you already have a record for ABC in the program, or whether you must set up a new object.</span></span> 

## <a name="group-by-type"></a><span data-ttu-id="8c3f2-113">Seskupení podle typu</span><span class="sxs-lookup"><span data-stu-id="8c3f2-113">Group by type</span></span>

<span data-ttu-id="8c3f2-114">Pomocí této metody seskupení můžete zobrazit typy předmětů, pro které vaše společnost provádí servis.</span><span class="sxs-lookup"><span data-stu-id="8c3f2-114">You can use this grouping method to show the types of objects that your company services.</span></span> <span data-ttu-id="8c3f2-115">Seskupení předmětů může být vhodné také v případě, že chcete vytvořit nový objekt na základě podobných předmětů již existujících v daném programu.</span><span class="sxs-lookup"><span data-stu-id="8c3f2-115">Grouping objects by type can also be useful if, for example, you want to create a new object based on similar objects that already exist in the program.</span></span>

## <a name="example"></a><span data-ttu-id="8c3f2-116">Příklad</span><span class="sxs-lookup"><span data-stu-id="8c3f2-116">Example</span></span>

<span data-ttu-id="8c3f2-117">Odběratel volá s požadavkem na vytvoření servisní smlouvy pro klimatizační jednotku HIJ.</span><span class="sxs-lookup"><span data-stu-id="8c3f2-117">A customer calls and wants to set up a service agreement for an air conditioning machine, HIJ.</span></span> <span data-ttu-id="8c3f2-118">Pro tento stroj již nemáte záznam.</span><span class="sxs-lookup"><span data-stu-id="8c3f2-118">You do not already have a record for this machine.</span></span> <span data-ttu-id="8c3f2-119">Nastavili jste však skupinu předmětů s názvem Klimatizační jednotky a přiřadili tuto skupinu ke všem předmětům klimatizačních jednotek.</span><span class="sxs-lookup"><span data-stu-id="8c3f2-119">However, you have set up an object group titled Air Conditioners, and you have attached this group to all air conditioning objects.</span></span> <span data-ttu-id="8c3f2-120">Proto můžete rychle vyhledávat a identifikovat všechny ostatní klimatizační jednotky a používat informace o šablonách z těchto předmětů, abyste vytvořili řádky servisní smlouvy pro HIJ.</span><span class="sxs-lookup"><span data-stu-id="8c3f2-120">Therefore, you can quickly search for and identify all other air conditioning machines and use the template information from these objects to create service agreement lines for HIJ.</span></span> <span data-ttu-id="8c3f2-121">Použitím skupin předmětů tímto způsobem můžete rychle nastavit nové předměty a stanovit servisní úkoly služby, které je třeba na nich provést.</span><span class="sxs-lookup"><span data-stu-id="8c3f2-121">By using object groups in this manner, you can quickly set up new objects and determine the service tasks that must be performed on them.</span></span> 




