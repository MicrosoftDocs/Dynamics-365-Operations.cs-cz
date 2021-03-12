---
title: Přidání typů vztahu místa a strany
description: Toto téma vysvětluje postup při přidání nového skladového místa a typu vztahu strany.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 00810576d36339bf7ce0657b1577e1e322c36bf0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979082"
---
# <a name="add-location-and-party-relationship-types"></a><span data-ttu-id="d3fc7-103">Přidání typů vztahu místa a strany</span><span class="sxs-lookup"><span data-stu-id="d3fc7-103">Add location and party relationship types</span></span> 

[!include [banner](../includes/banner.md)]

## <a name="add-location-roles"></a><span data-ttu-id="d3fc7-104">Přidání rolí umístění</span><span class="sxs-lookup"><span data-stu-id="d3fc7-104">Add location roles</span></span>

<span data-ttu-id="d3fc7-105">Existují dva způsoby přidání nové role umístění adresy a kontaktních informací:</span><span class="sxs-lookup"><span data-stu-id="d3fc7-105">There are two ways to add a new location roles for address and contact information:</span></span>

-  <span data-ttu-id="d3fc7-106">Přidejte je prostřednictvím stránky **Účel adresy a kontaktních informací**.</span><span class="sxs-lookup"><span data-stu-id="d3fc7-106">Add it through the **Address and contact information purpose** page.</span></span> <span data-ttu-id="d3fc7-107">Nová role bude uložena do tabulky **LogisticsLocationRole** s typem = 0, což označuje, že role není systémem definovaná role ve výčtu **LogisticsLocationRoleType** a jeho rozšířeních.</span><span class="sxs-lookup"><span data-stu-id="d3fc7-107">The new role will be saved to the **LogisticsLocationRole** table with type = 0, which indicates that the role is not a system role defined in the **LogisticsLocationRoleType** enum and its extensions.</span></span> <span data-ttu-id="d3fc7-108">Uživatel bude moci používat tuto roli při vytváření adresy nebo kontaktních informací.</span><span class="sxs-lookup"><span data-stu-id="d3fc7-108">A user will be able to use this role when creating address or contact information.</span></span>

    ![Účel adresy a informací o obsahu](media/Address-Contact.PNG)

-  <span data-ttu-id="d3fc7-110">Přidejte jej do rozšíření výčtu **LogisticsLocationRoleType** a naplňte během procesu synchronizace databáze.</span><span class="sxs-lookup"><span data-stu-id="d3fc7-110">Add it to the **LogisticsLocationRoleType** enum extension, and let it populate through the database sync process.</span></span>

    1.  <span data-ttu-id="d3fc7-111">Vytvořte rozšíření výčtu **LogisticsLocationRoleType** a přidejte do něho novou roli.</span><span class="sxs-lookup"><span data-stu-id="d3fc7-111">Create an extension to the **LogisticsLocationRoleType** enum and add the new role in the extension.</span></span> 
  
        ![Rozšíření na výčet LogisticsLocationRoleType](media/Logistics.PNG)

    2. <span data-ttu-id="d3fc7-113">Vytvořte nový soubor prostředků pro novou roli a přiřaďte hodnotu pro jeho vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="d3fc7-113">Create a new resource file for the new role, and then assign a value for its properties.</span></span>
     
     ![Nový soubor prostředku](media/Resource.PNG)
        
    3.  <span data-ttu-id="d3fc7-115">Vytvořte datovou třídu souboru a zadejte metodu obslužné rutiny pro naplnění nové role.</span><span class="sxs-lookup"><span data-stu-id="d3fc7-115">Create a data population class and provide a handler method to populate the new role.</span></span> 

        ![Naplnění dat](media/Dirdata.PNG)

    4.  <span data-ttu-id="d3fc7-117">Pokud chcete otestovat naplnění nové role umístění, můžete vytvořit spustitelnou třídu a volat DirDataPopulation::insertLogisticsLocationRoles() in Main().</span><span class="sxs-lookup"><span data-stu-id="d3fc7-117">To test populating the new location role, you can create a runnable class, and call DirDataPopulation::insertLogisticsLocationRoles() in Main().</span></span> <span data-ttu-id="d3fc7-118">Po dokončení tohoto procesu by se měla zobrazit nová role naplněná v tabulce **LogisticsLocationRole** s typem \> 0.</span><span class="sxs-lookup"><span data-stu-id="d3fc7-118">After this process is complete, you should see the new role populated in the **LogisticsLocationRole** table with type \> 0.</span></span> <span data-ttu-id="d3fc7-119">Nová role se zobrazí na stránce **Účel adresy a kontaktních informací účel**.</span><span class="sxs-lookup"><span data-stu-id="d3fc7-119">The new role will display on the **Address and contact information purpose** page.</span></span>

        ![Vložení nového místa](media/InsertNewLocation.PNG)

## <a name="add-party-relationship-types"></a><span data-ttu-id="d3fc7-121">Přidání typů vztahu strany</span><span class="sxs-lookup"><span data-stu-id="d3fc7-121">Add party relationship types</span></span> 

<span data-ttu-id="d3fc7-122">Nový typ vztahu lze přidat dvěma způsoby:</span><span class="sxs-lookup"><span data-stu-id="d3fc7-122">There are two ways to add a new relationship type:</span></span>

-   <span data-ttu-id="d3fc7-123">Prostřednictvím stránky **typy vztahů**.</span><span class="sxs-lookup"><span data-stu-id="d3fc7-123">Add it through the **Relationship types** page.</span></span> <span data-ttu-id="d3fc7-124">Nový vztah bude uložen tabulky **DirRelationshipTypeTable** s systemtype = 0.</span><span class="sxs-lookup"><span data-stu-id="d3fc7-124">The new relationship will be saved to **DirRelationshipTypeTable** with systemtype = 0.</span></span>

    ![Typy vztahů](media/Relationship.PNG)

-  <span data-ttu-id="d3fc7-126">Přidejte jej do rozšíření výčtu **DirSystemRelationshipType** a naplňte během procesu synchronizace databáze.</span><span class="sxs-lookup"><span data-stu-id="d3fc7-126">Add it to the extension of the **DirSystemRelationshipType** enum, and let it populate through database sync process.</span></span>

    1.  <span data-ttu-id="d3fc7-127">Vytvořte rozšíření výčtu **DirSystemRelationshipType** a přidejte nový typ vztahu.</span><span class="sxs-lookup"><span data-stu-id="d3fc7-127">Create an extension to the **DirSystemRelationshipType** enum and add the new relationship type.</span></span>

    2. <span data-ttu-id="d3fc7-128">Vytvořte inicializátor pro tento nový typ.</span><span class="sxs-lookup"><span data-stu-id="d3fc7-128">Create an initializer for this new type.</span></span> <span data-ttu-id="d3fc7-129">Několik příkladů naleznete v základním kódu, jeden z nich je **DirRelationshipTypeChildInitialize**.</span><span class="sxs-lookup"><span data-stu-id="d3fc7-129">You can find several examples in the core code, one of them is  **DirRelationshipTypeChildInitialize**.</span></span> <span data-ttu-id="d3fc7-130">Jedná se o třídu inicializátoru typu vztahu strany "Podřízené".</span><span class="sxs-lookup"><span data-stu-id="d3fc7-130">This is an initializer class for party relationship type “Child”.</span></span> <span data-ttu-id="d3fc7-131">Inicializátor můžete spustit zkopírováním a vložením tohoto kódu a následnou aktualizací zvýrazněných oblastí.</span><span class="sxs-lookup"><span data-stu-id="d3fc7-131">You can start with your initializer by copying and pasting this code and then update the highlighted areas.</span></span>
    
    ![Inicializátor DirRelationshipChild](media/DirRelationship.PNG)

    3.  <span data-ttu-id="d3fc7-133">Pokud chcete otestovat nový typ vztahu umístění, můžete vytvořit spustitelnou třídu a volat DirDataPopulation::insertDirRelationshipTypes() in Main().</span><span class="sxs-lookup"><span data-stu-id="d3fc7-133">To test populating the new relationship type, you can create a runnable class, and call DirDataPopulation::insertDirRelationshipTypes() in Main().</span></span> <span data-ttu-id="d3fc7-134">Měli byste vidět nový typ vztahu v tabulce **DirRelationshipTypeTable** a nový typ vztahu, bude k dispozici na stránce **typy vztahů**.</span><span class="sxs-lookup"><span data-stu-id="d3fc7-134">You should see the new relationship type in the **DirRelationshipTypeTable**, and the new relationship type will be available on the **Relationship types** page.</span></span>

        ![Spustitelná třída](media/Runnable.PNG)
