---
title: Přidání ikony oblíbené položky
description: Toto téma vysvětluje, jak přidat ikonu oblíbené položky na váš web.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 287663817232e7ce86e8fdb1fb5c2fcfeed33d20
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001524"
---
# <a name="add-a-favicon"></a>Přidání ikony oblíbené položky


[!include [banner](includes/banner.md)]

Toto téma vysvětluje, jak přidat ikonu oblíbené položky na váš web.

## <a name="overview"></a>Přehled

Ikona oblíbené položky je malý grafický soubor, který se mimo jiná umsítění zobrazuje na kartě webového prohlížeče, v adresním řádku, v historii procházení a v záložkách nebo oblíbených položkách. Doporučujeme přidat ikonu oblíbené položky na svůj web, protože reprezentuje a posiluje vaši značku a pomáhá rozlišit váš web od jiných webů, které vaši zákazníci navštěvují.

Ačkoli lze na web přidat více ikon oblíbené položky různých velikostí a typů souborů, tohle téma ukazuje, jak přidat jednu ikonu oblíbené položky. Stejný proces a umístění se však používají k přidání dalších ikon oblíbené položky.

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a>Odeslání ikony oblíbené položky do kolekce prostředků webu

Chcete-li odeslat ikonu oblíbené položky do kolekce prostředků vašeho webu, postupujte následovně.

1. Přejděte na **Prostředky \> Odeslat \> Odeslat prostředky**.
1. Vyhledejte a vyberte ikonu oblíbené položky v místním systému souborů.
1. Zadejte název a poté klikněte na tlačítko **OK**. 
1. V podokně vlastností vpravo zkopírujte veřejnou adresu URL ikony oblíbené položky.

> [!NOTE]
> Pokud nevyberete možnost **Publikovat prostředky po odeslání**, je nutné vrátit se na stránku **Prostředky** a ručně publikovat ikonu oblíbené položky později.

## <a name="create-the-html-for-the-favicon"></a>Vytvoření kódu HTML pro ikonu oblíbené položky

Chcete-li vytvořit kód HTML pro ikonu oblíbené položky, použijte následující fragment kódu HTML. Pro atribut **href** nahraďte **"Public\_URL\_for\_your\_favicon"** veřejnou adresou URL, kterou jste dříve zkopírovali.

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="add-the-html-for-the-favicon-to-the-head-element-of-your-pages"></a>Přidání kódu HTML ikony oblíbené položky do prvků \<head\> na stránkách

Chcete-li přidat ikonu oblíbené položky vašeho webu, použijte stejný postup, který se používá k přidání jakéhokoli typu kódu HTML nebo skriptu do prvku **\<head\>** na stránkách webu.

## <a name="additional-resources"></a>Další zdroje

[Přidání loga](add-logo.md)

[Volba motivu webu](select-site-theme.md)

[Práce se soubory přepisu šablon CSS](css-override-files.md)

[Přidání uvítací zprávy](add-welcome-message.md)

[Přidání oznámení o vlastnických právech](add-copyright-notice.md)

[Přidání jazyků na web](add-languages-to-site.md)

[Přidání kódu skriptu na webové stránky pro podporu telemetrie](add-telemetry.md)

