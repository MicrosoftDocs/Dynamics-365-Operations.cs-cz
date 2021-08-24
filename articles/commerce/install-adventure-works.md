---
title: Instalace motivu Adventure Works
description: Toto téma popisuje, jak nainstalovat motiv Adventure Works do Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ad704c6c3b95abcfd52e449a0ffbb4b82b236498ae8d2775c4e65811de3ef503
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763829"
---
# <a name="install-the-adventure-works-theme"></a>Instalace motivu Adventure Works

[!include [banner](includes/banner.md)]

Toto téma popisuje, jak nainstalovat motiv Adventure Works do Microsoft Dynamics 365 Commerce. 

> [!IMPORTANT]
> Motiv Adventure Works a moduly jsou k dispozici od Dynamics 365 Commerce verze 10.0.20. Jsou k dispozici v Microsoft AppSource.

## <a name="prerequisites"></a>Předpoklady

Před instalací motivu Adventure Works musíte mít prostředí Dynamics 365 Commerce (Commerce verze 10.0.20 nebo novější), které zahrnuje Retail Cloud Scale Unit (RCSU), Commerce online software development kit (SDK) a knihovnu modulů Commerce. Informace o tom, jak nainstalovat sadu Commerce SDK a knihovnu modulů, najdete v části [Aktualizace SDK a knihoven modulů](e-commerce-extensibility/sdk-updates.md). 

## <a name="installation-steps"></a>Instalační kroky

### <a name="install-the-adventure-works-theme-in-your-application"></a>Nainstalujte si do aplikace motiv Adventure Works

Balíček motivů Adventure Works je k dispozici v kanálu **dynamics365-commerce** jako **@msdyn365-commerce-theme/adventureworks-theme-kit**. Ačkoli je balíček motivů Adventure Works součástí tohoto kanálu, je pod jiným oborem názvů. Proto musíte podle těchto pokynů přidat položky registru pro obor názvů.

1. Aktualizujte soubor **.npmrc** tak, aby obsahoval následující položku registru (pokud položka již není zahrnuta):

    `@msdyn365-commerce-theme:registry=https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/`

1. Aktualizujte soubor **.yarnrc** tak, aby obsahoval následující položku registru (pokud položka již není zahrnuta):

    `"@msdyn365-commerce-theme:registry" "https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/"`  
    
Chcete-li nainstalovat balíček do místního prostředí, spusťte z příkazového řádku následující příkaz. Tento příkaz automaticky aktualizuje soubor package.json tak, aby obsahoval závislost.

`yarn add @msdyn365-commerce-theme/adventureworks-theme-kit`

V souboru **package.json** byste měli aktualizovat verzi motivu na konkrétní verzi.

> [!IMPORTANT]
> - Verze motivu by měla odpovídat verzi knihovny modulů, aby bylo zajištěno, že všechny funkce fungují podle očekávání. 
> - Minimální verze pro knihovnu modulů Commerce a SDK by měla být 10.0.20 (9.31). 

### <a name="add-the-font-files-for-the-adventure-works-theme"></a>Přidejte soubory písem pro motiv Adventure Works

Po instalaci motivu Adventure Works do aplikace musíte přidat soubory písem, které jsou pro něj vyžadovány. Chcete-li tento krok dokončit, zkopírujte všechny soubory písem z **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks\public\webfonts** do cesty veřejného adresáře aplikace partnera **\public\webfonts**.

### <a name="set-up-the-resources-for-the-adventure-works-theme"></a>Nastavte zdroje pro motiv Adventure Works

Dalším krokem je aktualizace požadovaného výchozího zdroje pro motiv. Chcete-li tento krok dokončit, zkopírujte obsah ze souboru global.json pod **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks\rzdroje\moduly** do souboru partnerské aplikace global.json pod **\src\rzdroje\moduly**. Pokud cílový adresář **\ src\resources** neexistuje, lze jej celý zkopírovat ze zdrojového adresáře **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks** do cílového adresáře **\src**.

### <a name="pull-updates-and-validate-the-theme"></a>Vyžádejte aktualizace a ověřte motiv

Informace o tom, jak stáhnout nejnovější sadu SDK, knihovnu modulů a další aktualizace závislostí, najdete v části "Vyžádat aktualizace" v [Aktualizaci SDK a knihoven modulů](e-commerce-extensibility/sdk-updates.md#pull-updates).

Po stažení nejnovějších závislostí můžete spustit příkaz **yarn start** pro spuštění serveru Node ve vývojovém prostředí a testování nového motivu Adventure Works. Procházejte aplikaci místně pomocí parametru řetězce dotazu `?theme=adventureworks` (například `https://localhost:4000/?theme=adventureworks`).

## <a name="additional-resources"></a>Další prostředky

[Motiv Adventure Works](adventure-works-theme.md)

[Přehled knihovny modulů](starter-kit-overview.md)

[SDK a aktualizace knihovny modulů](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
