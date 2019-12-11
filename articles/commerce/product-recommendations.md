---
title: Přehled doporučení produktu
description: V tomto tématu jsou obecné informace o doporučování produktů. Doporučení produktů umožňují zákazníkům snadno a rychle vyhledat produkty, které chtějí, a také produkty, které původně nechtěly nakupovat.
author: Moonma
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: eb369e6d1356ba13a2310d523b671ac57b9642bf
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770039"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="98f9e-104">Přehled doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="98f9e-104">Product recommendations overview</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="98f9e-105">Microsoft Dynamics 365 Commerce lze použít k zobrazení doporučení produktů na webu e-Commerce a v zařízení pro prodej na místě (POS).</span><span class="sxs-lookup"><span data-stu-id="98f9e-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="98f9e-106">Doporučení produktu jsou položky, o které se může zákazník zajímat.</span><span class="sxs-lookup"><span data-stu-id="98f9e-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="98f9e-107">Doporučení jsou založena na trendech nákupu ostatních zákazníků v online i kamených obchodech.</span><span class="sxs-lookup"><span data-stu-id="98f9e-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="98f9e-108">Doporučení produktů umožňují zákazníkům snadno a rychle najít produkty, které chtějí, a u toho mají pozitivní zkušenosti.</span><span class="sxs-lookup"><span data-stu-id="98f9e-108">Product recommendations let customers easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="98f9e-109">Křížový prodej a návazný prodej může dokonce zákazníkům pomoci najít další produkty, než které původně nakupují.</span><span class="sxs-lookup"><span data-stu-id="98f9e-109">Cross-selling and upselling can even be used to help customers find additional products than they didn't originally intend to buy.</span></span> <span data-ttu-id="98f9e-110">Pokud se při zjišťování produktů používají doporučení, mohou vytvářet více možností převodu, pomoci zvýšit výnosy z prodeje a dokonce také zvýšit spokojenost a uchování zákazníků.</span><span class="sxs-lookup"><span data-stu-id="98f9e-110">When recommendations are used to help with product discovery, they can create more conversion opportunities, help increase sales revenue, and even help enhance customer satisfaction and retention.</span></span>

<span data-ttu-id="98f9e-111">V aplikaci Commerce doporučení produktů využívají technologie strojového učení Microsoft Recommendations ve velkém měřítku.</span><span class="sxs-lookup"><span data-stu-id="98f9e-111">In Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>


## <a name="scenarios"></a><span data-ttu-id="98f9e-112">Scénáře</span><span class="sxs-lookup"><span data-stu-id="98f9e-112">Scenarios</span></span>

<span data-ttu-id="98f9e-113">Doporučení produktu jsou dostupná pro následující scénáře:</span><span class="sxs-lookup"><span data-stu-id="98f9e-113">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="98f9e-114">**Na libovolné stránce obchodu pro procházení nebo cílovou stránku v e-Commerce:** Pokud zákazníci nebo pracovníci obchodu navštíví stránku obchodu, může modul doporučení navrhovat produkty v seznamech **Nový**, **Nejprodávanější**a **Trendující**.</span><span class="sxs-lookup"><span data-stu-id="98f9e-114">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="98f9e-115">**Na stránce Podrobnosti produktu:** Pokud zákaznící nebo pracovníci obchodu navštíví stránku **Podrobnosti produktu**, nabídne modul doporučení další položky, které se také mohou nakoupit.</span><span class="sxs-lookup"><span data-stu-id="98f9e-115">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="98f9e-116">Tyto položky se zobrazí v seznamu **Lidem se také líbí**.</span><span class="sxs-lookup"><span data-stu-id="98f9e-116">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="98f9e-117">**Na stránce transakce nebo na stránce s pokladnou:** modul doporučení navrhuje položky na základě celého seznamu položek v nákupním košíku.</span><span class="sxs-lookup"><span data-stu-id="98f9e-117">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="98f9e-118">Tyto položky se zobrazí v seznamu **Často zakoupené společně**.</span><span class="sxs-lookup"><span data-stu-id="98f9e-118">These items appear in the **Frequently bought together** list.</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="98f9e-119">Služba doporučení</span><span class="sxs-lookup"><span data-stu-id="98f9e-119">Recommendation service</span></span>

<span data-ttu-id="98f9e-120">Doporučení produktu používají technologie strojového učení Recommendations následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="98f9e-120">Product recommendations use the Recommendations machine learning technologies in the following way:</span></span>

- <span data-ttu-id="98f9e-121">Data ve formátu vyžadovaném službami Recommendation jsou extrahována z pracovní databáze Commerce a odeslána do úložiště entit.</span><span class="sxs-lookup"><span data-stu-id="98f9e-121">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to the Entity store.</span></span>
- <span data-ttu-id="98f9e-122">Služba doporučení používá data k trénování modelů doporučení pro seznamy **Lidem se také líbí**, **Často zakoupené společně**, **Nový**, **Nejprodávanější** a **Trendující**.</span><span class="sxs-lookup"><span data-stu-id="98f9e-122">The Recommendation service uses the data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="98f9e-123">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="98f9e-123">Additional resources</span></span>

[<span data-ttu-id="98f9e-124">Povolit doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="98f9e-124">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="98f9e-125">Vytvoření seznamů doporučení vybraných produktů</span><span class="sxs-lookup"><span data-stu-id="98f9e-125">Create curated product recommendation lists</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="98f9e-126">Správa výsledků doporučení produktů na základě umělé inteligence a strojového učení</span><span class="sxs-lookup"><span data-stu-id="98f9e-126">Manage AI-ML-based product recommendation results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="98f9e-127">Přidání seznamů doporučení produktu na stránky</span><span class="sxs-lookup"><span data-stu-id="98f9e-127">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
