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
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: a4945f47c86d490f40a6b00cb823e6a6005e0ee4
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550502"
---
# <a name="add-location-and-party-relationship-types"></a>Přidání typů vztahu místa a strany 

[!include [banner](../includes/banner.md)]

## <a name="add-location-roles"></a>Přidání rolí umístění

Existují dva způsoby přidání nové role umístění adresy a kontaktních informací:

-  Přidejte je prostřednictvím stránky **Účel adresy a kontaktních informací**. Nová role bude uložena do tabulky **LogisticsLocationRole** s typem = 0, což označuje, že role není systémem definovaná role ve výčtu **LogisticsLocationRoleType** a jeho rozšířeních. Uživatel bude moci používat tuto roli při vytváření adresy nebo kontaktních informací.

    ![Účel adresy a informací o obsahu](media/Address-Contact.PNG)

-  Přidejte jej do rozšíření výčtu **LogisticsLocationRoleType** a naplňte během procesu synchronizace databáze.

    1.  Vytvořte rozšíření výčtu **LogisticsLocationRoleType** a přidejte do něho novou roli. 
  
        ![LogisticsLocationRoleType](media/Logistics.PNG)

    2. Vytvořte nový soubor prostředků pro novou roli a přiřaďte hodnotu pro jeho vlastnosti.
     
     ![Nový soubor prostředku](media/Resource.PNG)
        
    3.  Vytvořte datovou třídu souboru a zadejte metodu obslužné rutiny pro naplnění nové role. 

        ![Naplnění dat](media/Dirdata.PNG)

    4.  Pokud chcete otestovat naplnění nové role umístění, můžete vytvořit spustitelnou třídu a volat DirDataPopulation::insertLogisticsLocationRoles() in Main(). Po dokončení tohoto procesu by se měla zobrazit nová role naplněná v tabulce **LogisticsLocationRole** s typem \> 0. Nová role se zobrazí na stránce **Účel adresy a kontaktních informací účel**.

        ![Vložení nového místa](media/InsertNewLocation.PNG)

## <a name="add-party-relationship-types"></a>Přidání typů vztahu strany 

Nový typ vztahu lze přidat dvěma způsoby:

-   Prostřednictvím stránky **typy vztahů**. Nový vztah bude uložen tabulky **DirRelationshipTypeTable** s systemtype = 0.

    ![Typy vztahů](media/Relationship.PNG)

-  Přidejte jej do rozšíření výčtu **DirSystemRelationshipType** a naplňte během procesu synchronizace databáze.

    1.  Vytvořte rozšíření výčtu **DirSystemRelationshipType** a přidejte nový typ vztahu.

    2. Vytvořte inicializátor pro tento nový typ. Několik příkladů naleznete v základním kódu, jeden z nich je **DirRelationshipTypeChildInitialize**. Jedná se o třídu inicializátoru typu vztahu strany "Podřízené". Inicializátor můžete spustit zkopírováním a vložením tohoto kódu a následnou aktualizací zvýrazněných oblastí.
    
    ![DirRelationshipChild](media/DirRelationship.PNG)

    3.  Pokud chcete otestovat nový typ vztahu umístění, můžete vytvořit spustitelnou třídu a volat DirDataPopulation::insertDirRelationshipTypes() in Main(). Měli byste vidět nový typ vztahu v tabulce **DirRelationshipTypeTable** a nový typ vztahu, bude k dispozici na stránce **typy vztahů**.

        ![Spustitelná třída](media/Runnable.PNG)