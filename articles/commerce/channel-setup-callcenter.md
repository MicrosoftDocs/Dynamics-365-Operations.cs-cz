---
title: Nastavení kanálu kontaktního střediska
description: Toto téma popisuje, jak vytvořit kanálu kontaktního střediska v řešení Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6ec42ab920868f541eeac54556f4f24cb1efaa3a
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002443"
---
# <a name="set-up-a-call-center-channel"></a>Nastavení kanálu kontaktního střediska


[!include [banner](includes/banner.md)]

Toto téma popisuje, jak vytvořit kanálu kontaktního střediska v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

V aplikaci Dynamics 365 Commerce je kontaktní středisko typu maloobchodní sítě, které lze definovat v aplikaci. Definování kanálu pro entity kontaktního střediska umožňuje systému zařadit specifická data a zpracovat výchozí hodnoty do prodejních objednávek. Společnost může definovat ve více kanálů kontaktního střediska v aplikaci Commerce. 

Před vytvořením nového kanálu kontaktního centra se ujistěte, že jste splnili [Požadavky pro zřízení kanálů](channels-prerequisites.md).

## <a name="create-and-configure-a-new-call-center-channel"></a>Vytvořit a konfigurovat nový kanál kontaktního střediska

Chcete-li vytvořit a konfigurovat nový kanál kontaktního střediska, postupujte dle těchto kroků.

1. V navigačním podokně přejděte na **Moduly \> Kanály \> Kontaktní střediska \> Všechna kontaktní střediska**.
1. V podokně akcí zvolte **Nový**.
1. Do pole **Název** zadejte název nového kanálu.
1. Vyberte patřičnou **Právnickou osobu** z rozevírací nabídky.
1. Vyberte odpovídající umístění **Skladu** z rozevírací nabídky.
1. Do pole **Výchozí odběratel** zadejte platného výchozího odběratele.
1. V poli **Profil oznámení e-mailem** zadejte platný profil e-mailového oznámení.
1. Zadejte informační kód **Přepisu ceny**. Poznámka: je možné, že pro vás bude nutné vytvořit informační kód.
1. Zadejte informační kód **Kód blokování**. Poznámka: je možné, že pro vás bude nutné vytvořit informační kód.
1. Zadejte informační kód **Kredit**. Poznámka: je možné, že pro vás bude nutné vytvořit informační kód.
1. Zvolte **Uložit**.

V následujícím obrázku je znázorněno vytvoření nového kanálu kontaktního střediska.

![Nový kanál kontaktního střediska](media/channel-setup-callcenter-1.png)

Následující obrázek znázorňuje příklad kanálu kontaktního centra.

![Příklad kanálu kontaktního střediska](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a>Nastavení dodatečného kanálu

Další úkoly požadované pro nastavení kanálu kontaktního střediska zahrnují nastavení způsobů plateb a způsobů dodání.

Následující obrázek znázorňuje možnosti nastavení **Režimy dodávek** a **Způsobů platby** na kartě **Nastavení**.

![Další akce nastavení kanálu kontaktního střediska](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a>Nastavení metod platby

Chcete-li nastavit metody platby pro každý typ platby podporovaný v tomto kanálu, postupujte takto.

1. V podokně akcí vyberte kartu **Nastavení** a poté vyberte možnost **Metody platby**.
1. V podokně akcí zvolte **Nový**.
1. V navigačním podokně vyberte požadovaný způsob platby.
1. V části **Obecné** zadejte **Název operace** a nakonfigurujte další požadovaná nastavení.
1. Konfigurujte libovolná další nastavení, která jsou požadována pro typ platby.
1. V podokně akcí vyberte **Uložit**.

Na následujícím obrázku je znázorněn příklad hotovostní způsob platby.

![Příklad způsobů platby](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a>Nastavit způsoby dodání

Nastavené způsoby dodání lze zobrazit výběrem **Způsobů dodání** z karty **Nastavení** v **Podokně akcí**.  

Chcete-li změnit nebo přidat způsob dodání, postupujte podle následujících kroků.

1. V navigačním podokně přejděte na **Moduly \> Řízení zásob \> Způsoby dodání**.
1. V podokně akcí vyberte možnost **Nový** a vytvořte nový způsob dodání nebo vyberte existující režim.
1. V oddílu **Maloobchodní kanály** vyberte možnost **Přidat řádek**, chcete-li přidat kanál. Přidání kanálů pomocí organizačních uzlů namísto přidání jednotlivých kanálů může zjednodušit přidávání kanálů.

Na následujícím obrázku je znázorněn příklad způsobu dodání.

![Nastavit způsoby dodání](media/channel-setup-retail-7.png)

## <a name="additional-resources"></a>Další zdroje

[Předpoklady nastavení kanálu](channels-prerequisites.md)

[Funkce prodeje kontaktního střediska](call-center-functionality.md)

[Nastavení možností zpracování objednávky kontaktního střediska](set-up-order-processing-options.md)

[Katalogy kontaktního střediska](call-center-catalogs.md)

[Nastavení a práce s výstrahami u podvodů](set-up-fraud-alerts.md)

[Nastavení programů kontinuity pro kontaktní střediska](set-up-continuity-program.md)
