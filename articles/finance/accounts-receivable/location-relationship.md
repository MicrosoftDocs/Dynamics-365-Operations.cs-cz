---
title: Přidání typů vztahu místa a strany
description: Toto téma vysvětluje postup při přidání nového skladového místa a typu vztahu strany.
author: ShivamPandey-msft
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 36c2c45c8f078abdc7e0bc40481a544491384245
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711485"
---
# <a name="add-location-and-party-relationship-types"></a>Přidání typů vztahu místa a strany 

[!include [banner](../includes/banner.md)]

## <a name="add-location-roles"></a>Přidání rolí umístění

Existují dva způsoby přidání nové role umístění adresy a kontaktních informací:

-  Přidejte je prostřednictvím stránky **Účel adresy a kontaktních informací**. Nová role bude uložena do tabulky **LogisticsLocationRole** s typem = 0, což označuje, že role není systémem definovaná role ve výčtu **LogisticsLocationRoleType** a jeho rozšířeních. Uživatel bude moci používat tuto roli při vytváření adresy nebo kontaktních informací.

    ![Účel adresy a informací o obsahu.](media/Address-Contact.PNG)

-  Přidejte jej do rozšíření výčtu **LogisticsLocationRoleType** a naplňte během procesu synchronizace databáze.

    1.  Vytvořte rozšíření výčtu **LogisticsLocationRoleType** a přidejte do něho novou roli. 
  
        ![Rozšíření na výčet LogisticsLocationRoleType.](media/Logistics.PNG)

    2. Vytvořte nový soubor prostředků pro novou roli a přiřaďte hodnotu pro jeho vlastnosti.
     
     ![Nový soubor prostředku.](media/Resource.PNG)
        
    3.  Vytvořte datovou třídu souboru a zadejte metodu obslužné rutiny pro naplnění nové role. 

        ![Naplnění dat.](media/Dirdata.PNG)

    4.  Pokud chcete otestovat naplnění nové role umístění, můžete vytvořit spustitelnou třídu a volat DirDataPopulation::insertLogisticsLocationRoles() in Main(). Po dokončení tohoto procesu by se měla zobrazit nová role naplněná v tabulce **LogisticsLocationRole** s typem \> 0. Nová role se zobrazí na stránce **Účel adresy a kontaktních informací účel**.

        ![Vložení nového místa.](media/InsertNewLocation.PNG)

## <a name="add-party-relationship-types"></a>Přidání typů vztahu strany 

Nový typ vztahu lze přidat dvěma způsoby:

-   Prostřednictvím stránky **typy vztahů**. Nový vztah bude uložen tabulky **DirRelationshipTypeTable** s systemtype = 0.

    ![Typy vztahů.](media/Relationship.PNG)

-  Přidejte jej do rozšíření výčtu **DirSystemRelationshipType** a naplňte během procesu synchronizace databáze.

    1.  Vytvořte rozšíření výčtu **DirSystemRelationshipType** a přidejte nový typ vztahu.

    2. Vytvořte inicializátor pro tento nový typ. Několik příkladů naleznete v základním kódu, jeden z nich je **DirRelationshipTypeChildInitialize**. Jedná se o třídu inicializátoru typu vztahu strany "Podřízené". Inicializátor můžete spustit zkopírováním a vložením tohoto kódu a následnou aktualizací zvýrazněných oblastí.
    
    ![Inicializátor DirRelationshipChild.](media/DirRelationship.PNG)

    3.  Pokud chcete otestovat nový typ vztahu umístění, můžete vytvořit spustitelnou třídu a volat DirDataPopulation::insertDirRelationshipTypes() in Main(). Měli byste vidět nový typ vztahu v tabulce **DirRelationshipTypeTable** a nový typ vztahu, bude k dispozici na stránce **typy vztahů**.

        ![Spustitelná třída.](media/Runnable.PNG)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
