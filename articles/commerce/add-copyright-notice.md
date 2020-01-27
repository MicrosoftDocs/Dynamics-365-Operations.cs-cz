---
title: Přidání oznámení o vlastnických právech
description: V tomto tématu je popsán postup při přidání oznámení o autorských právech na web elektronického obchodu.
author: psimolin
manager: AnnBe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 58c2949057ef777f706d12cee2dd3341d1a3b7e6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914557"
---
# <a name="add-a-copyright-notice"></a>Přidání oznámení o vlastnických právech

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

V tomto tématu je popsán postup při přidání oznámení o autorských právech na web elektronického obchodu.

## <a name="prerequisites"></a>Předpoklady

Před přidáním oznámení o autorských právech na web je nutné mít k dispozici následující položky:

- Šablonu obsahující sdílený fragment zápatí.
- Stránku používající tuto šablonu.

## <a name="add-a-copyright-notice"></a>Přidání oznámení o vlastnických právech

Chcete-li přidat oznámení o autorských právech do dolní části každé stránky, která používá určitou šablonu, postupujte takto.

1. Přejděte na **Fragmenty** a pak vyberte **Nový fragment stránky**.
1. V dialogovém okně vyberte modul **Zápatí** a tento fragment pojmenujte. Zadejte například **Zápatí–autorská práva**.
1. Vyberte **OK**.
1. V navigačním podokně vyberte tlačítko se třemi tečkami (**...**) vedle **Zápatí** a vyberte možnost **Přidat modul**.
1. V dialogovém okně vyberte **Kategorie zápati** a pak vyberte možnost **OK**.
1. V navigačním podokně vyberte tlačítko se třemi tečkami vedle **Kategorie zápatí** a vyberte možnost **Přidat modul**.
1. V dialogovém okně vyberte **Položka bloku s formátovaným obsahem** a pak vyberte možnost **OK**.
1. V navigačním podokně vyberte možnost **Položka bloku s formátovaným obsahem**
1. V podokně vlastností vpravo v poli **Odstavec** přidejte zprávu o autorských právech. Zadejte například **(C) Fabrikam 2019**.
1. Vyberte možnost **Uložit**, pak vyberte možnost **Vrátit se změnami** a pak vyberte možnost **Publikovat**.
1. Přejděte na **Šablony**, vyberte šablonu a poté vyberte možnost **Rezervovat**.
1. V části **Osnova stránky** rozbalte možnost **Text** a pak rozbalte možnost **Výchozí stránka**.
1. Vyberte tlačítko se třemi tečkami vedle **Pozice zápatí** a poté vyberte možnost **Přidat fragment**.
1. Vyberte fragment, který jste vytvořili dříve, a poté vyberte možnost **Vybrat**.
1. Vraťte šablonu se změnami a publikujte ji.

Zápatí, které obsahuje poznámku o autorských právech, se automaticky zobrazí v dolní části všech stránek, které používají vybranou šablonu.

## <a name="additional-resources"></a>Další zdroje

[Přidání loga](add-logo.md)

[Volba motivu webu](select-site-theme.md)

[Práce se soubory přepisu šablon CSS](css-override-files.md)

[Přidání ikony oblíbené položky](add-favicon.md)

[Přidání uvítací zprávy](add-welcome-message.md)

[Přidání jazyků na web](add-languages-to-site.md)

[Přidání kódu skriptu na webové stránky pro podporu telemetrie](add-telemetry.md)

