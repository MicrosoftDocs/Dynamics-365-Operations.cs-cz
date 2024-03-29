---
title: Konfigurace správy úkolů
description: Tento článek popisuje, jak konfigurovat funkce správy úkolů v aplikaci Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.search.industry: ''
ms.openlocfilehash: cc2d75f52b183559de344982c8e4208000af786e
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746055"
---
# <a name="configure-task-management"></a>Konfigurace správy úkolů

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak konfigurovat funkce správy úkolů v aplikaci Microsoft Dynamics 365 Commerce.

Než budou moci manažeři a zaměstnanci používat funkce správy úkolů v Dynamics 365 Commerce, nejprve musí být nakonfigurována správa úkolů. Konfigurace zahrnuje udělení oprávnění manažerům a zaměstnancům, distribuci oprávnění klientům v pokladním místě (POS), nastavení oznámení POS a konfiguraci dlaždice **Úkoly** na domovské stránce aplikace POS.

## <a name="configure-permissions-for-store-managers"></a>Konfigurace oprávnění pro manažery obchodů

Každý pracovník v daném obchodě může zobrazit všechny úkoly, které jsou k tomuto obchodu přiřazeny. Může také aktualizovat stav úkolů, které jsou mu přiřazeny. Nicméně osoby jako manažeři obchodu musí mít oprávnění ke správě úkolů, aby mohli spravovat úkoly, které jsou přiřazeny k obchodu, a vytvářet jednoúčelové úkoly.

Chcete-li nakonfigurovat oprávnění pro správu úkolů pro manažery obchodů, postupujte takto.

1. Přejděte na **Retail a Commerce \> Zaměstnanci \> Skupiny oprávnění**.
1. Vyberte určitou skupinu oprávnění ( například **Manažer**) a poté vyberte možnost **Upravit**.
1. Na pevné záložce **Oprávnění** nastavte možnost **Povolit správu úkolů** na hodnotu **Ano**.
1. Na pevné záložce **Oznámění** přidejte operaci **Správa úloh** a zadejte hodnotu do pole **Pořadí zobrazení**. Například zadejte **2**, pokud operace **Plnění objednávek** již má hodnotu **1** pro **Pořadí zobrazení**.
    
> [!NOTE]
> Pokud uživatel, který není manažerem, musí mít v POS oprávnění ke správě úkolů, můžete dané osobě udělit oprávnění. Alternativně můžete vytvořit novou skupinu oprávnění pro nemanažery a nastavit možnost **Povolit správu úkolů** na hodnotu **Ano**.

Následující obrázek znázorňuje, jak nakonfigurovat oprávnění pro správu úkolů pro manažery obchodů.

![Konfigurace oprávnění pro správu úkolů pro manažery obchodů.](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a>Konfigurace oprávnění pro zaměstnance

Zaměstnanci musí mít oprávnění k vytváření seznamů úkolů, ke správě kritérií přiřazení a ke konfiguraci opakování všech seznamů úkolů. Chcete-li tato oprávnění konfigurovat, přiřaďte zaměstnance k roli **Manažer maloobchodních úkolů**.

Chcete-li konfigurovat oprávnění pro zaměstnance, postupujte takto.

1. Přejděte na **Retail a Commerce \> Zaměstnanci \> Uživatelé**.
1. Vyberte zaměstnance.
1. Na pevné záložce **Role uživatele** vyberte možnost **Přiřadit role**.
1. V dialogovém okně **Přiřadit uživateli role** vyberte roli **Manažer maloobchodních úkolů** a pak tlačítko **OK**.

## <a name="distribute-permissions-to-pos-clients"></a>Distribuce oprávnění klientům POS

Aby mohli zaměstnanci používat klienty POS, musí být oprávnění distribuována a synchronizována s těmito klienty.

Chcete-li oprávnění distribuovat klientům POS, postupujte podle následujících kroků.

1. Přejděte na **Retail and Commerce \> IT pro Retail and Commerce \> Plán distribuce**.
1. Vyberte plán distribuce **1060** (**Personál**) a poté vyberte možnost **Spustit**.
1. Vyberte plán distribuce **1070** (**Konfigurace kanálu**) a poté vyberte možnost **Spustit**.

## <a name="configure-pos-notifications-for-tasks"></a>Konfigurace oznámení POS pro úkoly

Správa úkolů musí být nakonfigurována tak, aby v aplikaci POS byla k dispozici oznámení.

Chcete-li konfigurovat oznámení POS pro úkoly, postupujte takto.

1. Přejděte do nabídky **Retail a Commerce \> Instalace kanálu \> Nastavení POS \> POS \> Operace POS**.
1. Vyhledejte operaci **1400** (**Správa úkolů**) a zaškrtněte u ní políčko **Povolit oznámení**.

Následující obrázek znázorňuje operaci **Správa úkolů** na stránce **Operace POS**.

![Operace správy úkolů na stránce Operace POS.](media/HQ-POS-Tasks-Notifications.png)

Další informace o konfiguraci oznámení POS naleznete v článku [Zobrazení oznámení objednávek v pokladním místě (POS)](notifications-pos.md).

> [!NOTE]
> Když uložíte změny, zobrazí se následující varování: **Parametr operace nebude povolen návrháři mřížky tlačítek pro ID operace rovnající se nebo menší než 4000. Pokud vytváříte vlastní operaci a chcete předat parametr z návrháře mřížky tlačítek, použijte ID operace větší než 4000.** Vyberte **Zavřít** a zavřete dialog.


## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a>Konfigurace dlaždice Úkoly na domovské stránce aplikace POS

Před konfigurací dlaždice **Úkoly** na domovské stránce aplikace POS si přečtěte téma [Rozložení obrazovky pokladního místa (POS)](pos-screen-layouts.md), které obsahuje informace o konfiguraci a přidání nových tlačítek do rozložení obrazovky POS.

Chcete-li konfigurovat dlaždici **Úkoly** na domovské stránce aplikace POS, postupujte takto.

1. Přejděte do nabídky **Retail a Commerce \> Instalace kanálu \> Nastavení POS \> POS \> Rozložení obrazovky**.
1. Vyberte rozložení obrazovky, vyberte velikost rozvržení a vyberte mřížku tlačítek.
1. Na pevné záložce **Mřížky tlačítek** vyberte možnost **Návrhář**, chcete-li upravit vybranou mřížku tlačítek.
1. Přidejte dlaždici **Úkoly** do příslušné části domovské stránky.

Následující obrázek znázorňuje příklad dlaždice **Úkoly** na domovské stránce POS.

![Dlaždice Úkoly na domovské stránce POS.](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a>Další prostředky

[Přehled správy úkolů](task-mgmt-overview.md)

[Vytvoření seznamů úkolů a přidání úkolů](task-mgmt-create-lists.md)

[Přiřazení seznamů úkolů k obchodům nebo zaměstnancům](task-mgmt-assign-lists.md)

[Správa úkolů v POS](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
