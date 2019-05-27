---
title: Přijetí smíšené registrační značky
description: Toto téma popisuje, jak používat kombinovaný příjem do registračních pokladen a vytvářet práci pro více položek pomocí mobilního zařízení.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a44165bc59d65a9dfdf8e591152f427b97930b34
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569375"
---
# <a name="mixed-license-plate-receiving"></a><span data-ttu-id="82b9a-103">Přijetí smíšené registrační značky</span><span class="sxs-lookup"><span data-stu-id="82b9a-103">Mixed license plate receiving</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82b9a-104">Přijetí smíšené registrační značky umožňuje vytvořit registrační značku sestávající z více položek předtím, než zaregistrujete a vytvoříte odloženou práci.</span><span class="sxs-lookup"><span data-stu-id="82b9a-104">Mixed license plate receiving allows you to build a license plate consisting of multiple items before you register and create put-away work.</span></span> 

<span data-ttu-id="82b9a-105">Registrační značka, která se skládá z několika položek, nemusí být rozdělená v přijímacím překladišti, kde můžete registrovat jednotlivé položky.</span><span class="sxs-lookup"><span data-stu-id="82b9a-105">A license plate that consists of multiple items does not have to be split at the receiving dock for you to register each item.</span></span> 

<span data-ttu-id="82b9a-106">Používáte-li tok související s položkou k identifikaci řádek zdrojového dokumentu, můžete naskenovat čárové kódy na ovládacím prvku položky.</span><span class="sxs-lookup"><span data-stu-id="82b9a-106">When using an item-related flow to identify the source document lines, you can scan bar codes on the item control.</span></span> <span data-ttu-id="82b9a-107">Pokud má čárový kód nakonfigurované množství a měrnou jednotku, položka a množství budou automaticky přidány do smíšené registrační značky a vy se vrátíte na obrazovku k naskenování jiné položky.</span><span class="sxs-lookup"><span data-stu-id="82b9a-107">If the bar code has a quantity and a unit of measure (UOM) configured on it, the item and quantity will automatically be added to the mixed license plate, and you will be returned to the screen to scan another item.</span></span> <span data-ttu-id="82b9a-108">Tímto způsobem lze rychle skenovat položky bez nutnosti provádět potvrzení při každém kroku prohledávání všech položek.</span><span class="sxs-lookup"><span data-stu-id="82b9a-108">This allows you to quickly scan all the items without having to make a confirmation at each step.</span></span> 

<span data-ttu-id="82b9a-109">V průběhu přijetí smíšené registrační značky můžete zobrazit seznam položek, které jsou již zkontrolovány pro registrační značku a odsud můžete upravit nebo opravit množství položky.</span><span class="sxs-lookup"><span data-stu-id="82b9a-109">In the flow for mixed license plate receiving, you can display the list of items that are already scanned to the license plate and from here you can modify or correct the quantity of an item.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="82b9a-110">Kdy se to používá</span><span class="sxs-lookup"><span data-stu-id="82b9a-110">Where it applies</span></span>

<span data-ttu-id="82b9a-111">Kombinovaný příjem registrační značky je tok příjmu na mobilní zařízení k registraci a vytvoření práce pro více řádek / položek současně.</span><span class="sxs-lookup"><span data-stu-id="82b9a-111">Mixed license plate receiving is a mobile device receiving flow to register and create work for multiple lines/items at the same time.</span></span> <span data-ttu-id="82b9a-112">To je užitečné, pokud přijímáte příchozí registrační značky s více položkami.</span><span class="sxs-lookup"><span data-stu-id="82b9a-112">This is useful if you receive inbound license plates with multiple items.</span></span> 

## <a name="how-to-set-up-mixed-license-plate-receiving"></a><span data-ttu-id="82b9a-113">Jak nastavit příjem smíšené registrační značky</span><span class="sxs-lookup"><span data-stu-id="82b9a-113">How to set up mixed license plate receiving</span></span>
<span data-ttu-id="82b9a-114">Příjem smíšené registrační značky je nastaven jako položka nabídky mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="82b9a-114">Mixed license plate receiving is set up as a mobile device menu item.</span></span>

<span data-ttu-id="82b9a-115">Je nutné vytvořit novou položku nabídky s prací v režimu, která nepoužívá stávající práci a používá některou z následujících metod:</span><span class="sxs-lookup"><span data-stu-id="82b9a-115">You need to create a new menu item with mode work that does not use existing work and use one of the following methods:</span></span>

- <span data-ttu-id="82b9a-116">Přijetí smíšené registrační značky</span><span class="sxs-lookup"><span data-stu-id="82b9a-116">Mixed license plate receiving</span></span>
- <span data-ttu-id="82b9a-117">Přijetí a odložení smíšené registrační značky</span><span class="sxs-lookup"><span data-stu-id="82b9a-117">Mixed license plate receiving and put away</span></span>

<span data-ttu-id="82b9a-118">Možnosti pro identifikaci řádky zdrojového dokumentu jsou položka nákupní objednávky, řádek nákupní objednávky, vratka, položka převodu objednávky a řádek převodního příkazu.</span><span class="sxs-lookup"><span data-stu-id="82b9a-118">The options to identify the source document lines are purchase order item, purchase order line, return order, transfer order item, and transfer order line.</span></span> <span data-ttu-id="82b9a-119">Tyto volby mohou změnit pořadí příjmu u jedné registrační značky.</span><span class="sxs-lookup"><span data-stu-id="82b9a-119">These options can change the receiving order on a single license plate.</span></span> <span data-ttu-id="82b9a-120">Poslední možností je podle položky nákladu.</span><span class="sxs-lookup"><span data-stu-id="82b9a-120">The last option is by load item.</span></span> <span data-ttu-id="82b9a-121">Můžete přidat více položek do registrační značky vozidla, ale nelze přepínat mezi více náklady.</span><span class="sxs-lookup"><span data-stu-id="82b9a-121">You can add multiple items to a license plate, but you cannot switch between multiple loads.</span></span>
