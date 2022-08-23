---
title: Instalace motivu Adventure Works
description: Tento článek popisuje, jak nainstalovat motiv Adventure Works do Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 12/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: f5c195694633c96a473f0f824c1f182903082bff
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274279"
---
# <a name="install-the-adventure-works-theme"></a>Instalace motivu Adventure Works

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak nainstalovat motiv Adventure Works do Microsoft Dynamics 365 Commerce. 

> [!IMPORTANT]
> Motiv Adventure Works a moduly jsou k dispozici od Dynamics 365 Commerce verze 10.0.20. Jsou k dispozici v Microsoft AppSource.

## <a name="prerequisites"></a>Předpoklady

Před instalací motivu Adventure Works musíte mít prostředí Dynamics 365 Commerce (Commerce verze 10.0.20 nebo novější), které zahrnuje Retail Cloud Scale Unit (RCSU), Commerce online software development kit (SDK) a knihovnu modulů Commerce. Informace o tom, jak nainstalovat sadu Commerce SDK a knihovnu modulů, najdete v části [Nastavení vývojového prostředí](e-commerce-extensibility/setup-dev-environment.md). 

## <a name="installation-steps"></a>Instalační kroky

### <a name="install-the-adventure-works-theme-in-your-application"></a>Nainstalujte si do aplikace motiv Adventure Works

Balíček motivů Adventure Works je k dispozici v kanálu **dynamics365-commerce** jako **@msdyn365-commerce-theme/adventureworks-theme-kit**. Ačkoli je balíček motivů Adventure Works součástí tohoto kanálu, je pod jiným oborem názvů. Proto musíte podle těchto pokynů přidat položky registru pro obor názvů.

1. Aktualizujte soubor **.npmrc** tak, aby obsahoval následující položku registru (pokud položka již není zahrnuta):

    `@msdyn365-commerce-theme:registry=https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/`

1. Aktualizujte soubor **.yarnrc** tak, aby obsahoval následující položku registru (pokud položka již není zahrnuta):

    `"@msdyn365-commerce-theme:registry" "https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/"`  
    
Chcete-li nainstalovat balíček ve vašem místním prostředí, z příkazového řádku spusťte příkaz `yarn add THEME_PACKAGE@VERSION`, kde **THEME_PACKAGE** je balíček témat (@msdyn365-commerce-theme/adventureworks-theme-kit) a **VERSION** je číslo verze používané knihovny modulů. Je důležité, aby se verze balíčku témat a knihovny modulů shodovaly. Chcete-li najít správné číslo verze knihovny modulů, kterou chcete použít, otevřete soubor package.json a vyhledejte hodnotu **starter-pack** v sekci **dependencies**. V následujícím příkladu používá soubor package.json knihovnu modulů verze 9.32, která se mapuje na vydání Dynamics 365 Commerce verze 10.0.22.  

```json
"dependencies": {
    "@msdyn365-commerce-modules/starter-pack": "9.32",
}
```

Následující příklad ukazuje, jak spustit příkaz `yarn add` pro přidání verze 9.32 tématu Adventure Works. Příkaz automaticky aktualizuje soubor package.json tak, aby obsahoval závislost.

`yarn add @msdyn365-commerce-theme/adventureworks-theme-kit@9.32`

Další Informace o aktualizaci verze knihovny modulů najdete v části [Aktualizace SDK a knihoven modulů](e-commerce-extensibility/sdk-updates.md). 

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
