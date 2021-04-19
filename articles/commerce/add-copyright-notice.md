---
title: Přidání oznámení o vlastnických právech
description: V tomto tématu je popsán postup při přidání oznámení o autorských právech na web elektronického obchodu.
author: psimolin
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 11195cc4e792820d88f820c7365a803ac75b5704
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797736"
---
# <a name="add-a-copyright-notice"></a>Přidání oznámení o vlastnických právech

[!include [banner](includes/banner.md)]

V tomto tématu je popsán postup při přidání oznámení o autorských právech na web elektronického obchodu.

## <a name="prerequisites"></a>Předpoklady

Před přidáním oznámení o autorských právech na web je nutné mít k dispozici následující položky:

- Šablonu obsahující sdílený fragment zápatí.
- Stránku používající tuto šablonu.

## <a name="add-a-copyright-notice"></a>Přidání oznámení o vlastnických právech

Chcete-li přidat oznámení o autorských právech do dolní části každé stránky, která používá určitou šablonu, postupujte takto.

1. Přejděte na **Fragmenty** a pak vyberte **Nový**.
1. V dialogovém okně **Nový fragment** vyberte modul **Zápatí** a pojmenujte fragment. Zadejte například **Zápatí–autorská práva**.
1. Vyberte **OK**.
1. V navigačním podokně vyberte tlačítko se třemi tečkami (**...**) vedle **Zápatí** a vyberte možnost **Přidat modul**.
1. V dialogovém okně vyberte **Kategorie zápati** a pak vyberte možnost **OK**.
1. V navigačním podokně vyberte tlačítko se třemi tečkami vedle **Kategorie zápatí** a vyberte možnost **Přidat modul**.
1. V dialogovém okně vyberte **Textový blok** a pak vyberte možnost **OK**.
1. V navigačním podokně vyberte položku **Textový blok**.
1. V podokně vlastností vpravo v poli **Odstavec** přidejte zprávu o autorských právech. Zadejte například **(C) Fabrikam 2019**.
1. Vyberte možnost **Uložit**, pak vyberte možnost **Dokončit úpravy** a pak vyberte možnost **Publikovat**.
1. Přejděte na **Šablony**, vyberte šablonu a poté vyberte možnost **Upravit**.
1. V části **Osnova stránky** rozbalte možnost **Text** a pak rozbalte možnost **Výchozí stránka**.
1. Vyberte tlačítko se třemi tečkami vedle **Pozice zápatí** a poté vyberte možnost **Přidat fragment**.
1. Vyberte fragment, který jste vytvořili dříve, a poté vyberte možnost **Vybrat**.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

Zápatí, které obsahuje poznámku o autorských právech, se automaticky zobrazí v dolní části všech stránek, které používají vybranou šablonu.

## <a name="additional-resources"></a>Další zdroje

[Přidání loga](add-logo.md)

[Volba motivu webu](select-site-theme.md)

[Práce se soubory přepisu šablon CSS](css-override-files.md)

[Přidání ikony oblíbené položky](add-favicon.md)

[Přidání uvítací zprávy](add-welcome-message.md)

[Přidání jazyků na web](add-languages-to-site.md)

[Přidání kódu skriptu na webové stránky pro podporu telemetrie](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]