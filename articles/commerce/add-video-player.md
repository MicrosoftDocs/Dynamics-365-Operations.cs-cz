---
title: Modul přehrávače videa
description: Tohle téma se zabývá moduly přehrávače videa a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 12/02/2019
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
ms.openlocfilehash: 1c78583f39dbacdc7b38e89c33e67ae23731bf8a
ms.sourcegitcommit: 96bfc20eb748f4090a2b5e1ff9f54997d5a5d359
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/04/2019
ms.locfileid: "2885894"
---
# <a name="video-player-module"></a>Modul přehrávače videa

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tohle téma se zabývá moduly přehrávače videa a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Moduly přehrávače videa se používají k podpoře přehrávání videa. Ve startovací sadě obchodu jsou k dispozici dva moduly přehrávače videa: modul přehrávače ambientního videa a modul přehrávače videa. Oba přehrávače podporují typ média MP4.

## <a name="ambient-video-player-module"></a>Modul přehrávače ambientního videa

Modul přehrávače ambientního videa podporuje krátká informační videa. Měl by se používat pro videa, která jsou kratší než pět sekund. Tento přehrávač podporuje omezené možnosti přehrávání videa, jako přehrávání a pozastavení.

### <a name="examples-of-ambient-video-player-modules-in-e-commerce"></a>Příklady modulů přehrávače ambientního videa v elektronickém obchodu

- Krátká informační videa, která na domovské stránce zvýrazní nové produkty
- Krátká informační videa, která zdůrazňují charakteristiky produktu na stránce s podrobnostmi o produktu

### <a name="ambient-video-player-module-properties"></a>Vlastnosti modulu přehrávače ambientního videa

| Název vlastnosti     | Hodnota                 | Popis |
|-------------------|-----------------------|-------------|
| Přehrát automaticky          | **Pravda** nebo **Nepravda** | Je-li hodnota nastavena na **Pravda**, video se automaticky přehraje. |
| Ztlumit              | **Pravda** nebo **Nepravda** | Je-li hodnota nastavena na **Pravda**, zvuk je ztlumen. Pro tento přehrávač je výchozí hodnota **Pravda**. V prohlížeči Google Chrome je ve výchozím nastavení ztlumeno přehrávání videozáznamů a zvuk je přehráván pouze v případě, že uživatel video přehrává ručně. |
| Smyčka              | **Pravda** nebo **Nepravda** | Je-li hodnota nastavena na **Pravda**, video se opakuje ve smyčce. |
| Média             |  Cesta a název souboru videa | Soubor videa, který je přehráván přehrávačem videa. |
| Ovládací prvky pro přehrávání | **Pravda** nebo **Nepravda** | Je-li hodnota nastavena na **Pravda**, na videu se zobrazí tlačítko Přehrát/pozastavit. Je-li hodnota nastavena na **Nepravda**, tlačítko Přehrát/pozastavit není zobrazeno, ale uživatelé mohou video pozastavit a obnovit pomocí klávesnice. |

## <a name="video-player-module"></a>Modul přehrávače videa

Modul přehrávače videa lze použít k prezentaci videí na webu elektronického obchodu. Podporuje všechny schopnosti přehrávání, jako je například přehrávání, pozastavení, režim úplné velikosti a skryté titulky. Modul přehrávače videa podporuje také přizpůsobení skrytých titulků, které vyhovují standardům přístupnosti. Můžete například přizpůsobit velikost písma a barvu pozadí.

Modul přehrávače videa také podporuje sekundární zvukové stopy. Po nahrání videa lze také nahrát sekundární zvukovou stopu. Modul přehrávače videa pak může přehrávat sekundární zvukovou stopu, pokud ji uživatel vybere.

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
| Ovládací prvky pro přehrávání     | **Pravda** nebo **Nepravda**               | Je-li hodnota nastavena na **Pravda**, na videu se zobrazí tlačítko Přehrát/pozastavit. Je-li hodnota nastavena na **Nepravda**, tlačítko Přehrát/pozastavit není zobrazeno, ale uživatelé mohou video pozastavit a obnovit pomocí klávesnice. |
| Přehrání na celé obrazovce       | **Pravda** nebo **Nepravda**               | Je-li hodnota nastavena na **Pravda**, video se přehraje v režimu celé obrazovky. |
| Ovládací prvky              | **Pravda** nebo **Nepravda**               | Je-li tato hodnota nastavena nahodnotu **Pravda**, zobrazí se všechny ovládací prvky. Tyto ovládací prvky zahrnují tlačítka Přehrát a Pozastavit, ukazatel průběhu a skryté titulky. |
| Skrýt titulní snímek     | **Pravda** nebo **Nepravda**               | Video může mít titulní snímek. Je-li tato vlastnost nastavena na hodnotu **Pravda**, je titulní snímek skrytý. |
| Úroveň masky            | Číslo od **0** do **100** | Maska použitá na video pro úpravu stylů. |
| Styl ikony celé obrazovky | **Čtverec** nebo **šipka**             | Styl ikony celé obrazovky, která je zobrazena v přehrávači videa. |

## <a name="add-a-video-player-module-to-a-page"></a>Přidání modulu přehrávače videa na stránku

Chcete-li přidat modul přehrávače videa na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.

1. Vytvořte šablonu stránky s názvem **Šablona přehrávače videa**.
1. V pozici **Hlavní** na výchozí stránce přidejte modul kontejneru.
1. V modulu kontejneru přidejte moduly přehrávače videa a přehrávače ambientního videa.
1. Vraťte šablonu se změnami a publikujte ji.
1. Šablonu přehrávače videa, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Stránka přehrávače videa**.
1. V pozici **Hlavní** nové stránky přidejte modul přehrávače ambientního videa.
1. V nastavení modulu přehrávače ambientního videa přejděte na položku **Média** a odešlete soubor videa. Podle potřeby můžete změnit funkce **Automatické přehrávání**, **Smyčka** a další vlastnosti.
1. Uložte stránku a zobrazte náhled.
1. V pozici **Hlavní** nové stránky přidejte modul přehrávače videa.
1. V nastavení modulu přehrávače videa přejděte na položku **Média** a odešlete soubor videa.
1. Uložte stránku a zobrazte náhled. Na stránce by měly být zobrazeny oba moduly videa. Chcete-li přizpůsobit chování každého modulu, můžete změnit další nastavení.
1. Vraťte stránku se změnami a publikujte ji.

## <a name="additional-resources"></a>Další zdroje

[Přehled startovací sady](starter-kit-overview.md)

[Modul výstrahy](add-alert.md)

[Karuselový modul](add-carousel.md)

[Modul bloku s formátovaným obsahem](add-content-rich-block.md)

[Modul umístění obsahu](add-content-placement-modules.md)

[Propagační modul](add-feature-module.md)

[Modul hlavního banneru](add-hero-module.md)
