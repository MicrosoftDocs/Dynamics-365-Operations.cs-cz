---
title: Nastavení opakovaného přidělení zboží při krátkodobém vyskladnění
description: Toto téma ukazuje, jak umožnit pracovníkům skladu rychle najít alternativní umístění, pokud nejsou k dispozici dostatečné zásoby v umístění, do něhož byl nasměrován.
author: ShylaThompson
manager: tfehr
ms.date: 06/29/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker, WHSLocationWithWorkException
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab8baf846d65e6fefe9ca575b5af5a2dbceac666
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976881"
---
# <a name="set-up-short-picking-item-reallocation"></a>Nastavení opakovaného přidělení zboží při krátkodobém vyskladnění

[!include [banner](../../includes/banner.md)]

Tato procedura ukazuje, jak umožnit pracovníkům skladu rychle najít alternativní umístění, pokud nejsou k dispozici dostatečné zásoby v umístění, do něhož byl nasměrován. 

Proces opětovného přidělení řídí **Výjimka práce** a používá jej skladový **pracovník**.

Procesy opětovného přidělení mohou být automatické, ruční nebo obojí:

- Automatické opětovné přidělení – k určení, zda je zboží k dispozici na jiném místě, se používají směrnice skladového místa. Je-li to možné, práce se aktualizuje a uživatel skladu je přesměrován na alternativní umístění.
- Manuální opětovné přidělení – umožňuje uživateli skladu vybrat si z jednoho nebo více skladových míst s nerezervovaným množstvím zboží. 
- Automatický a ruční – pokud není systém schopen provést automatické opětovné přidělení a jsou k dispozici skladová místa s nerezervovaným množstvím, bude uživatel vyzván k výběru skladového místa.

## <a name="set-up-work-exceptions"></a>Nastavit pracovní výjimky
Je možné definovat několik pracovních výjimek práce s jinými zásadami opakovaného přidělení zboží umožňujícími zaměstnanci skladu výběr na základě potřeb dodávky, kterou zpracovávají.

K vytvoření této procedury jsou použita ukázková data společnosti USMF.

1. V **navigačním podokně** přejděte na **Řízení skladu > Nastavení > Práce > Výjimky práce**.
2. Klepněte na možnost **Nový** 
3. Zadejte hodnotu do pole **Kód výjimky práce**. Toto bude název této výjimky. Například Návod ke krátkodobému vyskladnění.
4. Zadejte hodnotu do pole **Popis**. Toto bude stručný popis použití této výjimky. Například Krátkodobé vyskladnění – položka není k dispozici.
5. V poli **Typ výjimky** vyberte hodnotu **Krátkodobě vyskladnit**.
6. Zaškrtněte políčko **Upravit zásoby**. Je-li vybrána tato možnost, budou zásoby v místě krátkodobého vyskladnění automaticky upraveny na 0.
7. V poli **Výchozí kód typu úpravy** zadejte nebo vyberte hodnotu. Například v USMF můžete vybrat **Odebrat Res Adj Out** . Každý kód typu úpravy obsahuje čtyři vlastnosti: název, popis, název skladového deníku a volbu **Odebrat rezervace**. Je-li volba **Odebrat rezervace** vybrána, budou rezervace v řádku objednávky krátkodobého výdeje odstraněny.  
8. V poli **Opakované přidělení zboží** zadejte hodnotu, například Ruční. Pokud vyberete Ruční nebo Automatické a ruční, pracovník skladu musí mít povoleno použití ručního přerozdělení.

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>Nastavení pracovníka k použití ručního opakované přidělení zboží

K vytvoření této procedury jsou použita ukázková data společnosti USMF.

1. Zavřete stránku.
2. V **Navigačním podokně** přejděte na **Řízení skladu > Nastavení > Pracovník**.
3. Klikněte na možnost **Upravit**.
4. Vyberte ze seznamu pracovníka. Příklad: Julia Funderburk.
5. Rozbalte pevnou záložku **Uživatelé**.
6. V seznamu vyberte **ID uživatele**. Například 24.
7. Rozbalte pevnou záložku **Práce**.
8. Vyberte možnost **Ano** v poli **Povolit ruční opakované přidělení zboží**.
