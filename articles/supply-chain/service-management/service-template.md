---
title: "Šablony servisu"
description: "Můžete definovat servisní smlouvu jako šablonu a později můžete zkopírovat řádky této šablony do jiné servisní smlouvy nebo do servisní zakázky."
author: ShylaThompson
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 6c4bde1869b2be6e4cbbf979dae1b84c2a4974a9
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---

# <a name="service-templates"></a><span data-ttu-id="3c8c6-103">Šablony servisu</span><span class="sxs-lookup"><span data-stu-id="3c8c6-103">Service templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c8c6-104">Můžete definovat servisní smlouvu jako šablonu a později můžete zkopírovat řádky této šablony do jiné servisní smlouvy nebo do servisní zakázky.</span><span class="sxs-lookup"><span data-stu-id="3c8c6-104">You can define a service agreement as a template and copy the lines of the template later into another service agreement or into a service order.</span></span>

## <a name="example"></a><span data-ttu-id="3c8c6-105">Příklad</span><span class="sxs-lookup"><span data-stu-id="3c8c6-105">Example</span></span>

<span data-ttu-id="3c8c6-106">Předpokládejme, že odběratel, pro kterého poskytujete služby, má stejné služební výtahy v pěti různých sídlech.</span><span class="sxs-lookup"><span data-stu-id="3c8c6-106">A customer for whom you provide service has identical service elevators at five different locations.</span></span>

<span data-ttu-id="3c8c6-107">Pro tohoto odběratele je třeba vytvořit pět servisních smluv, jednu pro každé sídlo.</span><span class="sxs-lookup"><span data-stu-id="3c8c6-107">You want to set up five service agreements for the customer, one for each site.</span></span>
<span data-ttu-id="3c8c6-108">Chcete-li omezit opakující se úkony konfigurace a přitom zajistit, že konfigurační údaje v servisních smlouvách budou shodné, vytvořte servisní smlouvu a specifikujte ji jako šablonu pro servisní práce na výtazích.</span><span class="sxs-lookup"><span data-stu-id="3c8c6-108">To limit repetitive setup work, and to make sure that the setup information in the service agreements is identical, you create a service agreement and specify it as a template for the service work on the elevators.</span></span>

<span data-ttu-id="3c8c6-109">Nyní můžete zkopírovat řádky šablony do pěti nových servisních smluv, takže každá servisní smlouva bude zaplněna řádky ze šablony.</span><span class="sxs-lookup"><span data-stu-id="3c8c6-109">You can now copy the template lines into the five new service agreements, so that each service agreement is populated with the lines from the template.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="3c8c6-110">Vytvořit šablonu</span><span class="sxs-lookup"><span data-stu-id="3c8c6-110">Create a template</span></span>

<span data-ttu-id="3c8c6-111">Při vytváření servisní šablony nejprve vytvořte servisní smlouvu, poté pro ni vytvořte povinné řádky a nakonec servisní smlouvu přiřaďte ke skupině servisních šablon.</span><span class="sxs-lookup"><span data-stu-id="3c8c6-111">When you create a service template, you create a service agreement, create the required lines on it, and attach the service agreement to a service-template group.</span></span>

> [!NOTE]
> <span data-ttu-id="3c8c6-112">Servisní smlouvu lze definovat jako šablonu pouze tehdy, pokud k ní nejsou připojeny žádné servisní zakázky.</span><span class="sxs-lookup"><span data-stu-id="3c8c6-112">A service agreement can be defined as a template only if it has no service orders attached to it.</span></span> <span data-ttu-id="3c8c6-113">Kromě toho nelze ze servisní smlouvy, která byla definována jako šablona, vygenerovat žádné servisní zakázky.</span><span class="sxs-lookup"><span data-stu-id="3c8c6-113">Also, no service orders can be generated from a service agreement that is defined as a template.</span></span>

## <a name="copy-template-lines"></a><span data-ttu-id="3c8c6-114">Kopírovat řádky šablony</span><span class="sxs-lookup"><span data-stu-id="3c8c6-114">Copy template lines</span></span>

<span data-ttu-id="3c8c6-115">Řádky šablony lze kopírovat ze servisní šablony do jiné servisní smlouvy nebo do servisní objednávky.</span><span class="sxs-lookup"><span data-stu-id="3c8c6-115">You can copy template lines from a service template into another service agreement or into a service order.</span></span>

<span data-ttu-id="3c8c6-116">Pokud kopírujete řádky šablony do servisních objednávek nebo servisních smluv, budou odpovídající skupiny šablon zobrazeny v zobrazení stromu, v němž lze jednotlivé skupiny rozbalit.</span><span class="sxs-lookup"><span data-stu-id="3c8c6-116">When you copy template lines into your service orders or service agreements, your template groups are displayed in a tree view in which each group can be expanded.</span></span> <span data-ttu-id="3c8c6-117">V tomto zobrazení lze zobrazit každou šablonu a řádek šablony.</span><span class="sxs-lookup"><span data-stu-id="3c8c6-117">This display lets you view each template and template line.</span></span>

<span data-ttu-id="3c8c6-118">Při seskupení šablon s použitím názvů odpovídajících použití těchto šablon lze snáze určit, které řádky servisní šablony mají být zkopírovány.</span><span class="sxs-lookup"><span data-stu-id="3c8c6-118">It is easier to determine the service-template lines that you want to copy if you have grouped the templates under names that reflect the use of the templates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c8c6-119">Související témata</span><span class="sxs-lookup"><span data-stu-id="3c8c6-119">Related topics</span></span>

[<span data-ttu-id="3c8c6-120">Kopírování řádků šablon servisu</span><span class="sxs-lookup"><span data-stu-id="3c8c6-120">Copy service templates lines</span></span>](copy-service-template-lines.md)

