---
title: Modul přehrávače videa
description: Tohle téma se zabývá moduly přehrávače videa a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e94658eed12b12d6666e63d2c06b86646c81a120
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025636"
---
# <a name="video-player-module"></a>Modul přehrávače videa


[!include [banner](includes/banner.md)]

Tohle téma se zabývá moduly přehrávače videa a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Modul přehrávače videa se používá k podpoře přehrávání videa. Lze jej přidat na libovolnou stránku za předpokladu, že se obsah videa nahrává do systému správy obsahu (CMS) a je k dispozici. Modul přehrávače videa podporuje typ média MP4.

## <a name="video-player-module"></a>Modul videopřehrávače

Modul přehrávače videa lze použít k prezentaci videí na webu elektronického obchodu. Podporuje všechny schopnosti přehrávání, jako je například přehrávání, pozastavení, režim úplné velikosti, audio popis a skryté titulky. Modul přehrávače videa podporuje také přizpůsobení skrytých titulků, které vyhovují standardům přístupnosti. Můžete například přizpůsobit velikost písma a barvu pozadí.

Modul přehrávače videa také podporuje sekundární zvukové stopy. Po nahrání videa do CMS lze také nahrát sekundární zvukovou stopu. Modul přehrávače videa pak může přehrávat sekundární zvukovou stopu, pokud ji uživatel vybere.

### <a name="examples-of-video-player-modules-in-e-commerce"></a>Příklady modulů přehrávače videa v elektronickém obchodu

- Instruktážní videa na stránkách s podrobnostmi o produktech nebo na marketingových stránkách
- Reklamní videa a videa o zásadách na marketingové stránce
- Marketingová videa se zvýrazněním charakteristik produktů na stránkách s podrobnostmi o produktech nebo na marketingových stránkách

### <a name="video-player-module-properties"></a>Vlastnosti modulu přehrávače videa

| Název vlastnosti         | Hodnota                               | Popis |
|-----------------------|-------------------------------------|-------------|
| Automatické přehrání             | **Pravda** nebo **Nepravda**               | Je-li hodnota nastavena na **Pravda**, video se automaticky přehraje. |
| Ztlumit                  | **Pravda** nebo **Nepravda**               | Je-li hodnota nastavena na **Pravda**, zvuk je ztlumen. Pro tento přehrávač je výchozí hodnota **Nepravda**. V prohlížeči Chrome je ve výchozím nastavení ztlumeno přehrávání videozáznamů a zvuk je přehráván pouze v případě, že uživatel video přehrává ručně. |
| Smyčka                  | **Pravda** nebo **Nepravda**               | Je-li hodnota nastavena na **Pravda**, video se opakuje ve smyčce. |
| Média                 | Cesta a název souboru videa | Soubor videa, který je přehráván přehrávačem videa. |
| Přehrání na celé obrazovce       | **Pravda** nebo **nepravda**               | Je-li hodnota nastavena na **Pravda**, video se přehraje v režimu celé obrazovky. |
| Spuštění přehrání a pozastavení    | **Pravda** nebo **nepravda**               | Je-li hodnota nastavena na **Pravda**, na videu se zobrazí tlačítko Přehrát/pozastavit. |
| Ovládací prvky přehrávače videa | **Pravda** nebo **nepravda**               | Je-li tato hodnota nastavena nahodnotu **Pravda**, zobrazí se všechny ovládací prvky přehrávače videa. Tyto ovládací prvky zahrnují tlačítka Přehrát a Pozastavit, ukazatel průběhu a možnosti skrytých titulků. |
| Skrýt obrázek plakátu     | **Pravda** nebo **nepravda**               | Video může mít titulní snímek. Je-li tato vlastnost nastavena na hodnotu **Pravda**, je titulní snímek skrytý. |
| Úroveň masky            | Číslo od **0** do **100** | Maska použitá na video pro úpravu stylů. |

## <a name="add-a-video-player-module-to-a-page"></a>Přidání modulu přehrávače videa na stránku

> [!NOTE] 
> Před vytvořením modulu přehrávače videa je nejprve nutné odeslat video do knihovny médií.

Chcete-li přidat modul přehrávače videa na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.

1. Vytvořte šablonu stránky s názvem **Šablona přehrávače videa**.
1. V pozici **Hlavní** na výchozí stránce přidejte modul kontejneru.
1. V modulu kontejneru přidejte moduly přehrávače videa a přehrávače ambientního videa.
1. Dokončete úpravy šablony a publikujte ji.
1. Šablonu přehrávače videa, kterou jste vytvořili, použijte pro vytvoření stránky s názvem **Stránka přehrávače videa**.
1. V pozici **Hlavní** nové stránky přidejte modul přehrávače videa.
1. V podokně vlastností modulu přehrávač videa vyberte možnost **Přidat video**.
1. V dialogovém okně **Výběr média** vyberte video a poté vyberte možnost **Odeslat novou mediální položku**.
1. Uložte stránku a zobrazte náhled. Na stránce by měl být zobrazen modul videa. Chcete-li přizpůsobit chování modulu, můžete změnit další nastavení.
1. Dokončete úpravy stránky a publikujte ji.

## <a name="additional-resources"></a>Další zdroje

[Přehled startovací sady](starter-kit-overview.md)

[Modul propagačního banneru](add-alert.md)

[Karuselový modul](add-carousel.md)

[Modul textového bloku](add-content-rich-block.md)

[Modul bloku obsahu](add-hero-module.md)
