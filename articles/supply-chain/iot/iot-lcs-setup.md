---
title: Instalace doplňku IoT Intelligence v LCS
description: Toto téma vysvětluje, jak nainstalovat doplněk IoT Intelligence ve službě Microsoft Dynamics Lifecycle Services (LCS).
author: robinarh
manager: tfehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ad8b33633646f27bc368dc4bbedc1eb64c150a9f
ms.sourcegitcommit: 092ef6a45f515b38be2a4481abdbe7518a636f85
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424125"
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