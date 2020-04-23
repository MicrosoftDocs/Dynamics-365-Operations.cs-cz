---
title: Nastavení opakovaného přidělení zboží při krátkodobém vyskladnění
description: Tato procedura ukazuje, jak umožnit pracovníkům skladu rychle najít alternativní umístění, pokud nejsou k dispozici dostatečné zásoby v umístění, do něhož byl nasměrován.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e860a54c2306f8140947b77cdcb538160a84e06f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216797"
---
# <a name="set-up-short-picking-item-reallocation"></a>Nastavení opakovaného přidělení zboží při krátkodobém vyskladnění

[!include [banner](../../includes/banner.md)]

Tato procedura ukazuje, jak umožnit pracovníkům skladu rychle najít alternativní umístění, pokud nejsou k dispozici dostatečné zásoby v umístění, do něhož byl nasměrován. Je možné použít automatický proces opětovného přidělení, který používá směrnice pro umístění k získání zboží, pokud je k dispozici na jiném místě. Také při použití ručního opětovné přidělení je seznam umístění s dostupným množstvím zobrazen na mobilním zařízení, což umožňuje pracovníkovi skladu zvolit umístění, ze kterého má použít zásoby. Tento postup můžete projít v ukázkových datech společnosti USMF. Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.


## <a name="set-up-work-exceptions"></a>Nastavit pracovní výjimky
1. V **navigačním podokně** přejděte na **Řízení skladu > Nastavení > Práce > Výjimky práce**.
2. Klepněte na možnost **Nový**. Je možné definovat několik pracovních výjimek práce s jinými zásadami opakovaného přidělení zboží umožňujícími zaměstnanci skladu výběr na základě potřeb dodávky, kterou zpracovávají.  
3. Zadejte hodnotu do pole **Kód výjimky práce**. Pracovní výjimku pojmenujte tak, aby indikovala, k čemu se používá. Například Návod ke krátkodobému vyskladnění.  
4. Zadejte hodnotu do pole **Popis**.
5. V poli **Typ výjimky** vyberte Krátkodobě vyskladnit.
6. Zaškrtněte políčko **Upravit zásoby**. Tato možnost znamená, že zásoby budou automaticky upraveny na 0 v místě krátkodobého vyskladnění.  
7. V poli **Výchozí kód typu úpravy** zadejte nebo vyberte hodnotu. Například v USMF můžete vybrat "Odebrat Res Adj Out".  
8. V poli **Opakované přidělení zboží** vyberte Ruční. Pokud vyberete Ruční nebo Automatické a ruční, pracovník skladu musí mít povoleno použití ručního přerozdělení.  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>Nastavení pracovníka k použití ručního opakované přidělení zboží
1. Zavřete stránku.
2. V **Navigačním podokně** přejděte na **Řízení skladu > Nastavení > Pracovník**.
3. Klikněte na možnost **Upravit**.
4. Vyberte ze seznamu Pracovník 24.
5. Rozbalte pevnou záložku **Práce**.
6. Vyberte možnost Ano v poli **Povolit ruční opakované přidělení zboží**.

