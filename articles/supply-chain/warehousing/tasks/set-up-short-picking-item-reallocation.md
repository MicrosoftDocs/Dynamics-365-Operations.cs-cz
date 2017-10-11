--- 
title: "Nastavení opakovaného přidělení zboží při krátkodobém vyskladnění"
description: "Tato procedura ukazuje, jak umožnit pracovníkům skladu rychle najít alternativní umístění, pokud nejsou k dispozici dostatečné zásoby v umístění, do něhož byl nasměrován."
author: YuyuScheller
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: fedd815cddfea4e00ed61ec6e176b633468c8fb2
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-short-picking-item-reallocation"></a>Nastavení opakovaného přidělení zboží při krátkodobém vyskladnění

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tato procedura ukazuje, jak umožnit pracovníkům skladu rychle najít alternativní umístění, pokud nejsou k dispozici dostatečné zásoby v umístění, do něhož byl nasměrován. Je možné použít automatický proces opětovného přidělení, který používá směrnice pro umístění k získání zboží, pokud je k dispozici na jiném místě. Také při použití ručního opětovné přidělení je seznam umístění s dostupným množstvím zobrazen na mobilním zařízení, což umožňuje pracovníkovi skladu zvolit umístění, ze kterého má použít zásoby. Tento postup můžete projít v ukázkových datech společnosti USMF. Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations verze 1611.


## <a name="set-up-work-exceptions"></a>Nastavit pracovní výjimky
1. Přejděte do nabídky Řízení skladu > Nastavení > Práce > Výjimky práce.
2. Klikněte na položku Nová.
    * Je možné definovat několik pracovních výjimek práce s jinými zásadami opakovaného přidělení zboží umožňujícími zaměstnanci skladu výběr na základě potřeb dodávky, kterou zpracovávají.  
3. Zadejte hodnotu do pole Kód výjimky práce.
    * Pracovní výjimku pojmenujte tak, aby indikovala, k čemu se používá. Například Návod ke krátkodobému vyskladnění.  
4. Zadejte nějakou hodnotu do pole Popis.
5. Na V poli Typ výjimky vyberte Krátkodobě vyskladnit.
6. Zaškrtněte políčko Upravit zásoby.
    * Tato možnost znamená, že zásoby budou automaticky upraveny na 0 v místě krátkodobého vyskladnění.  
7. V poli Výchozí kód typu úpravy zadejte nebo vyberte hodnotu.
    * Například v USMF můžete vybrat "Odebrat Res Adj Out".  
8. V poli Opakované přidělení zboží vyberte Ruční.
    * Pokud vyberete Ruční nebo Automatické a ruční, pracovník skladu musí mít povoleno použití ručního přerozdělení.  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>Nastavení pracovníka k použití ručního opakované přidělení zboží
1. Zavřete stránku.
2. Přejděte do nabídky Řízení skladu > Nastavení > Pracovník.
3. Klikněte na položku Upravit.
4. Vyberte ze seznamu Pracovník 24.
5. Rozbalte oddíl Práce.
6. Vyberte možnost Ano v poli Povolit ruční opakované přidělení zboží.

