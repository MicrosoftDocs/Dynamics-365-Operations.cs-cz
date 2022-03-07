---
title: Instalace doplňku IoT Intelligence v LCS
description: Toto téma vysvětluje, jak nainstalovat doplněk IoT Intelligence ve službě Microsoft Dynamics Lifecycle Services (LCS).
author: tonyafehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: tfehr
ms.custom: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ebf11b55f1034b9a84dda9ada77c2f1b7f587a58
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781581"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a>Instalace doplňku IoT Intelligence v LCS

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje, jak nainstalovat doplněk IoT Intelligence ve službě Microsoft Dynamics Lifecycle Services (LCS). Upozorňujeme, že doplňky nelze nainstalovat v demo / zkušebním prostředí. Před instalací doplňku musíte [vytvořit zdroje Azure](iot-azure-setup.md).

## <a name="set-up-the-lcs-environment"></a>Nastavení prostředí LCS

1. Otevřete LCS a přejděte do prostředí Microsoft Dynamics 365 Supply Chain Management.
2. Přejděte do části **Doplňky prostředí**.
3. Vyberte **Nainstalovat nový doplněk** a zobrazte seznam doplňků, které byly pro dané prostředí povoleny.
4. V dialogovém okně **Vybrat doplněk pro instalaci** vyberte **IoT Intelligence**.
5. V dialogovém okně **Nastavení doplňku** zadejte podrobnosti vašeho centra IoT a Redis Cache. Požadované hodnoty najdete v úložišti klíčů, které jste vytvořili v části [Vytvoření zdrojů Azure](iot-azure-setup.md).

    + **ID klienta** - Na portálu Azure přejděte do úložiště klíčů a poté v levém navigačním podokně vyberte možnost **Přehled** a zkopírujte hodnotu **ID adresáře**. Vložte tuto hodnotu do dialogového okna **Nastavení doplňku**.
    + **URI Key Vault koncového bodu kompatibilní s centrem událostí IoT** - Přejděte do úložiště klíčů a poté v levém navigačním podokně vyberte možnost **Přehled** a zkopírujte hodnotu **Název DNS**. Vložte tuto hodnotu do dialogového okna **Nastavení doplňku**.
    + **Název tajného klíče koncového bodu kompatibilní s centrem událostí IoT** - Přejděte do úložiště klíčů a poté v levém navigačním podokně vyberte možnost **Tajné klíče** a zkopírujte název tajného klíče tam, kde je uložen řetězec připojení k centru událostí pro centrum IoT. Vložte tuto hodnotu do dialogového okna **Nastavení doplňku**.
    + **URI úložiště klíčů Redis Cache** - Přejděte do úložiště klíčů a poté v levém navigačním podokně vyberte možnost **Přehled** a zkopírujte hodnotu **Název DNS**. Vložte tuto hodnotu do dialogového okna **Nastavení doplňku**.
    + **Název tajného klíče koncového bodu Redis Cache** - Přejděte do úložiště klíčů a poté v levém navigačním podokně vyberte možnost **Tajné klíče** a zkopírujte název tajného klíče tam, kde je uložen řetězec připojení pro Redis Cache. Vložte tuto hodnotu do dialogového okna **Nastavení doplňku**.

6. Zaškrtnutím políčka přijměte smluvní podmínky.
7. Vyberte **Instalovat**.
8. Zobrazí se okno se zprávou, že „Doplněk byl úspěšně spuštěn pro instalaci.“ Vyberte **OK**.

Nastavení LCS je nyní dokončeno. Dalším krokem je [nastavení scénáře](iot-scenario-setup.md).

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a>Odinstalace doplňku

1. V aplikaci Supply Chain Management [zakažte scénáře](iot-scenario-setup.md#disable-a-scenario).
2. V LCS přejděte k podrobnostem prostředí Supply Chain Management .
3. Přejděte do části **Doplňky prostředí**.
4. Vyberte **Odinstalovat** pro doplněk IoT Intelligence.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]