---
title: "Katalogy kontaktního střediska"
description: "Tento článek popisuje funkce kontaktního střediska pro katalogy v aplikaci Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e5a97ab749259fcc97b269b0134792820ebf13af
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="call-center-catalogs"></a><span data-ttu-id="05c91-103">Katalogy kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="05c91-103">Call center catalogs</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="05c91-104">Tento článek popisuje funkce kontaktního střediska pro katalogy v aplikaci Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="05c91-104">This article describes the call center–specific functionality for catalogs in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="05c91-105">V kontaktním středisku můžete pomocí katalogů produktů identifikovat produkty, které chcete nabízet odběratelům.</span><span class="sxs-lookup"><span data-stu-id="05c91-105">In a call center, you can use product catalogs to identify the products that you want to offer to customers.</span></span> <span data-ttu-id="05c91-106">Kontaktní střediska obvykle používají tištěné katalogy.</span><span class="sxs-lookup"><span data-stu-id="05c91-106">Call centers typically use printed catalogs.</span></span> <span data-ttu-id="05c91-107">Návrhy a výroba tištěného katalogu jsou zpracovány mimo aplikaci Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="05c91-107">The design and production of a printed catalog is handled outside Dynamics 365 for Retail.</span></span> <span data-ttu-id="05c91-108">Můžete však vytvořit a uložit digitální kopii katalogu s použitím stejných stránek, které slouží k nastavení online maloobchodních katalogů.</span><span class="sxs-lookup"><span data-stu-id="05c91-108">However, you can create and store a digital form of a catalog by using the same pages that you use to set up online retail catalogs.</span></span> <span data-ttu-id="05c91-109">Před vytvořením katalogu musíte nastavit sortiment produktů a přiřadit sortiment kontaktnímu středisku.</span><span class="sxs-lookup"><span data-stu-id="05c91-109">Before you can create a catalog, you must set up product assortments and assign the assortments to a call center.</span></span> <span data-ttu-id="05c91-110">Poté přidáte produkty do katalogu výběrem produktů z těchto sortimentů.</span><span class="sxs-lookup"><span data-stu-id="05c91-110">You then add products to the catalog by selecting products from these assortments.</span></span> <span data-ttu-id="05c91-111">Poté, co byly produkty přidány do katalogu a katalog je dokončeno, je třeba ověřit katalog pro ověření dat.</span><span class="sxs-lookup"><span data-stu-id="05c91-111">After products have been added to the catalog, and the catalog is complete, you must validate the catalog to verify the data.</span></span> <span data-ttu-id="05c91-112">Poté musíte odeslat katalog ke kontrole a schválení.</span><span class="sxs-lookup"><span data-stu-id="05c91-112">You must then submit the catalog for review and approval.</span></span> <span data-ttu-id="05c91-113">Po schválení katalogu jej můžete publikovat.</span><span class="sxs-lookup"><span data-stu-id="05c91-113">After the catalog is approved, it can be published.</span></span> <span data-ttu-id="05c91-114">Při vytvoření katalogu kontaktního střediska můžete pořídit snímek dat katalogu v době publikování katalogu.</span><span class="sxs-lookup"><span data-stu-id="05c91-114">When a call center catalog is created, you can take a snapshot of the catalog data at the time that the catalog is published.</span></span> <span data-ttu-id="05c91-115">Tato funkce snímku vám umožňuje přístup k určité verzi katalogu i v případě, že je katalog později změněn a aktualizován.</span><span class="sxs-lookup"><span data-stu-id="05c91-115">This snapshot functionality lets you access a particular version of the catalog even if the catalog is later changed and updated.</span></span> <span data-ttu-id="05c91-116">Katalogy kontaktního střediska lze rovněž nastavit tak, aby obsahovaly následující volitelné funkce:</span><span class="sxs-lookup"><span data-stu-id="05c91-116">Call center catalogs can also be set up to include the following optional features:</span></span>

-   <span data-ttu-id="05c91-117">**Zdrojové kódy** – kódy, které se používají ke sledování reakcí odběratele na konkrétní poštu katalogu.</span><span class="sxs-lookup"><span data-stu-id="05c91-117">**Source codes** – Source codes are used to track the customer response to specific catalog mailings.</span></span>
-   <span data-ttu-id="05c91-118">**Produkty zdarma** – produkty, které mohou být zahrnuty do objednávky zákazníka bez dalších příplatků.</span><span class="sxs-lookup"><span data-stu-id="05c91-118">**Free products** – Products can be included in a customer's order at no additional charge.</span></span> <span data-ttu-id="05c91-119">Tyto produkty jsou přidány do objednávky automaticky při zadání zdrojového kódu katalogu do objednávky.</span><span class="sxs-lookup"><span data-stu-id="05c91-119">These products are automatically added to an order when the source code for the catalog is entered into the order.</span></span>
-   <span data-ttu-id="05c91-120">**Skripty** – texty, které přečte pracovník kontaktního střediska odběrateli při vytváření prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="05c91-120">**Scripts** – Scripts are texts that a call center worker reads to a customer when a sales order is being created.</span></span> <span data-ttu-id="05c91-121">Skripty mohou zahrnovat pozdravy nebo nákupní návrhy.</span><span class="sxs-lookup"><span data-stu-id="05c91-121">Scripts can include greetings or purchase suggestions.</span></span>
-   <span data-ttu-id="05c91-122">**Rozvržení stránky** – určuje rozmístění produktů na stránce ve vytištěném katalogu.</span><span class="sxs-lookup"><span data-stu-id="05c91-122">**Page layout** – A page layout captures the page position of products in the printed catalog.</span></span> <span data-ttu-id="05c91-123">Tyto informace se používají pro sestavu analýzy oblasti katalogu.</span><span class="sxs-lookup"><span data-stu-id="05c91-123">This information is used for the catalog area analysis report.</span></span>





