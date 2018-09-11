--- 
title: "Nastavit skupiny dlouhodobého majetku"
description: "Tento postup popisuje, jak vytvořit novou skupinu dlouhodobého majetku."
author: saraschi2
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetGroup, AssetGroupBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 50942d6bb8da8ec7b63f3c18ef0421d69fb76859
ms.contentlocale: cs-cz
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="2421e-103">Nastavit skupiny dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="2421e-103">Set up fixed asset groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2421e-104">Tento postup popisuje, jak vytvořit novou skupinu dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="2421e-104">This procedure shows how to create a new fixed asset group.</span></span> <span data-ttu-id="2421e-105">Využívá účetní role a ukázková data pro právnické osoby USMF.</span><span class="sxs-lookup"><span data-stu-id="2421e-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="2421e-106">Přejděte do části Dlouhodobý majetek > Nastavení > Skupiny dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="2421e-106">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="2421e-107">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="2421e-107">Click New.</span></span>
3. <span data-ttu-id="2421e-108">Zadejte hodnotu do pole Skupina dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="2421e-108">In the Fixed asset group field, type a value.</span></span>
4. <span data-ttu-id="2421e-109">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="2421e-109">In the Name field, type a value.</span></span>
    * <span data-ttu-id="2421e-110">Funkce Automaticky číslovat dlouhodobý majetek a Kód číselné řady ve skupině dlouhodobého majetku přepíše nastavení v parametrech dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="2421e-110">Autonumber fixed assets and Number sequence code on the Fixed asset group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="2421e-111">Nastavení zde můžete změnit v případě, že majetek v této skupině dlouhodobého majetku bude mít jiné číslování, než v jiných skupinách.</span><span class="sxs-lookup"><span data-stu-id="2421e-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="2421e-112">Klepněte na Knihy.</span><span class="sxs-lookup"><span data-stu-id="2421e-112">Click Books.</span></span>
6. <span data-ttu-id="2421e-113">V poli Kniha zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="2421e-113">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="2421e-114">Možnost Výpočet odpisu je nastavena na Ano a kniha majetku tak bude zahrnuta v návrzích odpisů.</span><span class="sxs-lookup"><span data-stu-id="2421e-114">The Calculate depreciation field is set to Yes, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="2421e-115">Je-li výpočet odpisu nastaven na hodnotu Ne, majetek nebude odepisován automaticky.</span><span class="sxs-lookup"><span data-stu-id="2421e-115">If Calculate depreciation is set to No, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="2421e-116">Nastavte dobu životnosti majetku v letech.</span><span class="sxs-lookup"><span data-stu-id="2421e-116">Set the Service life of the asset, in years.</span></span>
    * <span data-ttu-id="2421e-117">Všimněte si, že hodnota pole Období odpisu se vypočítá po nastavení doby životnosti.</span><span class="sxs-lookup"><span data-stu-id="2421e-117">Note that the Depreciation periods field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="2421e-118">Vyberte volbu v poli Způsob odpisu.</span><span class="sxs-lookup"><span data-stu-id="2421e-118">In the Depreciation convention field, select an option.</span></span>
9. <span data-ttu-id="2421e-119">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="2421e-119">Close the page.</span></span>


