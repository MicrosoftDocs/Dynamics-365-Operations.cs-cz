---
title: "Plány dodávek"
description: "Plány dodávek vám umožňují sledovat množství na řádku objednávky, když pracujete s více dodávkami na jedné prodejní objednávce, prodejní nabídce nebo nákupní objednávce."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: fbada697060c823b0afdb72d1c0cfd8703f4d527
ms.lasthandoff: 03/31/2017


---

# <a name="delivery-schedules"></a>Plány dodávek

[!include[banner](../includes/banner.md)]


Plány dodávek vám umožňují sledovat množství na řádku objednávky, když pracujete s více dodávkami na jedné prodejní objednávce, prodejní nabídce nebo nákupní objednávce.

Plán dodávek používejte pro celkové množství řádku objednávky nebo nabídky, musí být dodány ve více dodávkách. Jednotlivé dodávky jsou reprezentovány řádky dodávky. Dva nebo více řádků dodávek tvoří jeden plán dodávek. Řádky dodávky mohou mít jiná data dodání, množství, způsoby dodání a dimenze úložiště, jako například pracoviště a sklad.  

**Příklad plánu dodávek**

|                                   |                                          |
|-----------------------------------|------------------------------------------|
| Celková objednávka (původní řádek objednávky) | 600 židlí                               |
| Plán požadovaných dodávek       | 100 židlí měsíčně                     |
| Požadovaný časový rámec dodání | 6 měsíců, v první den každého měsíce |

V této situaci zákazník požaduje dodání 600 židlí v dávkách 100 židlí po dobu šesti měsíců. Ke sledování požadavků na dodání vytvoříte plán dodávek. Na stránce plánu dodávek vytvoříte šest samostatných řádků dodávky. Každý řádek dodávky obsahuje 100 židlí a označuje datum dodání těchto 100 židlí. V tomto případě se každý řádek posune u prvního dne měsíce po šest po sobě následujících měsíců.  

Při vytváření plánu dodávek se typ původního řádku objednávky automaticky změní na **Řádek objednávky s více dodávkami**. Řádek tohoto typu je označován jako obchodní řádek a je označen ikonou. Řádek dodávky je označen jinou ikonou. Pokud změníte množství na řádku dodávky, obchodní řádek aktualizován pro celkové množství plánu dodávek. Pokud obchodní smlouvě definoval Celková sleva objednávky, plán dodávek zajišťuje, že vaše objednávka má nárok na celkovou objednávku slevu i v případě, že objednávka je rozdělit na samostatné dodávky.  

Objednávky, které mají plán dodávek, se zpracují proti řádkům dodávky. Zpracování zahrnuje zaúčtování dodacích listů, příjemek produktů a fakturaci.  

Výtisky dokumentů objednávek a nabídek, které mají plán dodávek, zobrazují jen řádky dodávky. Neobsahují původní řádky (obchodní řádky). **Poznámka:** Navíc se zobrazí jen řádky dodávky při provedení těchto akcí:

-   Zaúčtovat
-   Kopírování stránek
-   Procházení stránek se seznamy a sestav

Při potvrzení prodejní nabídky se na výsledných prodejních objednávkách zobrazí celý plán dodávek, i když mají řádky objednávky více dodávek. Dále se celý plán dodávky zobrazí na všech hlavních stránkách, například na prodejních objednávkách, prodejních nabídkách a nákupních objednávkách.




