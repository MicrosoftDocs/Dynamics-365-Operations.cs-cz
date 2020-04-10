---
title: Nastavení dopravců
description: Toto téma popisuje, jak nastavit dopravce a definujte podrobnosti například pro službu, způsob dodávky, úhradu přepravy, omezení přepravy nebo sazbu expedice.
author: ShylaThompson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb39d58336e7f867e19d7ba6d9f801200de5a0aa
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148548"
---
# <a name="set-up-shipping-carriers"></a>Nastavení dopravců

[!include [banner](../../includes/banner.md)]

Toto téma popisuje, jak nastavit dopravce a definujte podrobnosti například pro službu, způsob dodávky, úhradu přepravy, omezení přepravy nebo sazbu expedice. Koordinátor přepravy potom může přiřadit dopravce k příchozímu nebo odchozímu vytížení.


## <a name="create-a-new-shipping-carrier"></a>Vytvoření nového dopravce
1. Přejděte na **Navigační > podokno Moduly > Správa přepravy > Nastavení > Dopravci > Dopravci.**
2. V podokně akcí vyberte **Nový**.
3. Zadejte hodnotu do pole **Dopravce dodávky**.
4. Zadejte hodnotu do pole **Název**.
5. V poli **Režim** vyberte z rozevírací nabídky požadovanou možnost.

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a>Zadání obecných informací pro dopravce
1. Přepněte rozšíření oddílu **Přehled**.
2. Zaškrtněte nebo zrušte zaškrtnutí políčka **Aktivovat dopravce**.
3. V poli **Účet dodavatele** vyberte z rozevírací nabídky požadovanou možnost. Vyberte účet dodavatele, ke kterému chcete přiřadit dopravce.  
4. V poli **Typ úhrady přepravy** vyberte požadovanou možnost. Vyberte **Ručně**, pokud chcete použít stránku Úhrada přepravy, nebo vyberte **EDI** a nechte aktualizovat úhrady pomocí služby Electronic Data Interchange (EDI).  
5. Zaškrtněte nebo zrušte zaškrtnutí políčka **Aktivovat hodnocení dopravce**.

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a>Vytvoření nezbytných služeb pro dopravce
1. Přepněte rozšíření oddílu **Služby**.
2. Zvolte **Nové**.
3. Zadejte hodnotu do pole **Služba dopravce**.
4. Zadejte hodnotu do pole **Název**.
5. V poli **Metoda přepravy** vyberte z rozevírací nabídky požadovanou možnost.

## <a name="set-up-the-address-for-the-carrier-optional"></a>Nastavení adresy pro dopravce (volitelné)
1. Přepněte rozšíření oddílu **Adresy**.
2. Zvolte **Nové**.
3. Zadejte hodnotu do pole **Název nebo popis**.
4. V poli **Země/oblast** vyberte z rozevírací nabídky požadovanou možnost.
5. V poli **PSČ** vyberte z rozevírací nabídky požadovanou možnost.
6. Zadejte hodnotu do pole **Ulice**.
7. Vyberte **OK**.

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a>Nastavení profilu hodnocení pro dopravce
1. Rozbalte oddíl **Profily sazeb**.
2. Zvolte **Nové**.
3. Zadejte hodnotu do pole **Profil sazeb**.
4. Zadejte hodnotu do pole **Název**.
5. V poli **Pracoviště** vyberte z rozevírací nabídky požadovanou možnost.
6. V poli **Sklad** vyberte z rozevírací nabídky požadovanou možnost.
7. V poli **Výpočet přepravních sazeb** vyberte z rozevírací nabídky požadovanou možnost. Vyberte modul sazeb, který je v souladu se smlouvou, které máte s dopravcem.  
8. V poli **Hlavní sazba** vyberte z rozevírací nabídky požadovanou možnost.
9. V poli **Modul mezioperačního času** vyberte z rozevírací nabídky požadovanou možnost.
10. Zvolte **Uložit**.

