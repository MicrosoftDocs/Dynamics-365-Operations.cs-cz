---
title: Nastavení skupin dlouhodobého majetku
description: Toto téma vysvětluje, jak vytvořit novou skupinu dlouhodobého majetku.
author: saraschi2
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetGroup, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee3cec5c6abf08c88a61af2ec4bde6a863de2f95
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224638"
---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="b5eb1-103">Nastavení skupin dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="b5eb1-103">Set up fixed asset groups</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b5eb1-104">Toto téma vysvětluje, jak vytvořit novou skupinu dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="b5eb1-104">This topic explains how to create a new fixed asset group.</span></span> <span data-ttu-id="b5eb1-105">Využívá účetní role a ukázková data pro právnické osoby USMF.</span><span class="sxs-lookup"><span data-stu-id="b5eb1-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="b5eb1-106">V navigačním podokně přejděte na **Moduly > Dlouhodobý majetek > Nastavení > Skupiny dlouhodobého majetku**.</span><span class="sxs-lookup"><span data-stu-id="b5eb1-106">In the navigation pane, go to **Modules > Fixed assets > Setup > Fixed asset groups**.</span></span>
2. <span data-ttu-id="b5eb1-107">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="b5eb1-107">Select **New**.</span></span>
3. <span data-ttu-id="b5eb1-108">Zadejte hodnotu do pole **Skupina dlouhodobého majetku**.</span><span class="sxs-lookup"><span data-stu-id="b5eb1-108">In the **Fixed asset group** field, type a value.</span></span>
4. <span data-ttu-id="b5eb1-109">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="b5eb1-109">In the **Name** field, type a value.</span></span> <span data-ttu-id="b5eb1-110">Funkce Automaticky číslovat dlouhodobý majetek a Kód číselné řady ve skupině **Dlouhodobého majetku** přepíše nastavení v parametrech dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="b5eb1-110">Autonumber fixed assets and Number sequence code on the **Fixed asset** group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="b5eb1-111">Nastavení zde můžete změnit v případě, že majetek v této skupině dlouhodobého majetku bude mít jiné číslování, než v jiných skupinách.</span><span class="sxs-lookup"><span data-stu-id="b5eb1-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="b5eb1-112">Vyberte **Knihy**.</span><span class="sxs-lookup"><span data-stu-id="b5eb1-112">Select **Books**.</span></span>
6. <span data-ttu-id="b5eb1-113">V poli **Kniha** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b5eb1-113">In the **Book** field, enter or select a value.</span></span> <span data-ttu-id="b5eb1-114">Pole **Výpočet odpisu** je nastavena na **Ano** a kniha majetku tak bude zahrnuta v návrzích odpisů.</span><span class="sxs-lookup"><span data-stu-id="b5eb1-114">The **Calculate depreciation** field is set to **Yes**, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="b5eb1-115">Je-li **Výpočet odpisu** nastaven na hodnotu **Ne**, majetek nebude odepisován automaticky.</span><span class="sxs-lookup"><span data-stu-id="b5eb1-115">If **Calculate depreciation** is set to **No**, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="b5eb1-116">Nastavte dobu životnosti majetku v letech.</span><span class="sxs-lookup"><span data-stu-id="b5eb1-116">Set the Service life of the asset, in years.</span></span> <span data-ttu-id="b5eb1-117">Všimněte si, že hodnota pole **Období odpisu** se vypočítá po nastavení doby životnosti.</span><span class="sxs-lookup"><span data-stu-id="b5eb1-117">Note that the **Depreciation periods** field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="b5eb1-118">Vyberte volbu v poli **Způsob odpisu**.</span><span class="sxs-lookup"><span data-stu-id="b5eb1-118">In the **Depreciation convention** field, select an option.</span></span>
9. <span data-ttu-id="b5eb1-119">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b5eb1-119">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]