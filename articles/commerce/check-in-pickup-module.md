---
title: Přihlášení k modulu vyzvednutí
description: Tento článek popisuje přihlášení pro modul vyzvednutí a popisuje, jak ho konfigurovat v řešení Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 7002db893da1802063148a9b800ffa92f3e5f065
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885468"
---
# <a name="check-in-for-pickup-module"></a>Přihlášení k modulu vyzvednutí

[!include [banner](includes/banner.md)]

Tento článek popisuje přihlášení pro modul vyzvednutí a popisuje, jak ho konfigurovat v řešení Microsoft Dynamics 365 Commerce.

Modul přihlášení pro vyzvednutí poskytuje stránku s potvrzením pro zákazníky, kteří používají možnosti přihlášení zákazníka Dynamics 365 Commerce, aby obchod informoval o jejich příjezdu. Modul přihlášení pro vyzvednutí také umožňuje nakonfigurovat formulář, který shromažďuje další informace od zákazníků, aby se usnadnilo doručení objednávky. Tyto informace zahrnují číslo parkovacího místa zákazníka a značku a model jeho vozidla. 

## <a name="module-properties"></a>Vlastnosti modulu

| Název vlastnosti | Hodnoty | popis |
|---------------|--------|-------------|
| Text potvrzení | Textový řetězec | Obsah nadpisu, který se zobrazí na stránce s potvrzením ohlášení. |
| Zobrazit QR kód | **Pravda** nebo **nepravda** | Když je tato vlastnost nastavena na **True**, stránka pro potvrzení přihlášení zobrazuje QR kód, který představuje ID potvrzení objednávky. |
| Nadpis s dalšími informacemi | Textový řetězec | Obsah nadpisu, který se zobrazí, když byla nakonfigurována další informační pole. |
| Další informační klíče | Dvojice ID zdroje / hodnota prostředku | Každý klíč vytváří pole formuláře a přidružený štítek, které se používají ke shromažďování dalších informací od zákazníků. |
| Další informační klíče \> ID zdroje | Textový řetězec | Každý klíč informací vytváří pole formuláře a přidružený štítek, které se používají ke shromažďování dalších informací od zákazníků. Tato vlastnost identifikuje klíč dalších informací. V úloze, která je vytvořena v místě prodeje (POS), se hodnota této vlastnosti zobrazí jako popisek v poli s pokyny. |
| Další informační klíče \> Hodnota prostředku | Textový řetězec | Popisek pro textové pole v úkolu v POS. |
| Další informační klíče \> Povinné | **Pravda** nebo **nepravda** | Tato vlastnost určuje, zda musí zákazníci před pokračováním vyplnit pole formuláře. Když je tato vlastnost nastavena na **True**, vedle popisku formuláře se vykreslí hvězdička a provede se nulová kontrola, aby se zabránilo pokračování zákazníků, pokud není zadána žádná hodnota. |

## <a name="add-the-check-in-for-pickup-module-to-a-page"></a>Přidání modulu přihlášení pro vyzvednutí na stránku

Modul přihlášení pro vyzvednutí by měl být přidán na novou stránku, kterou vytvoříte pro potvrzení přihlášení. Tato stránka bude sloužit jako prostředí s potvrzením přihlášení pro zákazníky, kteří vyberou odkaz **Jsem tady** nebo tlačítko v e-mailu. 

## <a name="configure-the-additional-information-form"></a>Konfigurace formuláře s dalšími informacemi

Ve výchozím nastavení, pokud nejsou nakonfigurovány žádné další informační klíče, modul zobrazí zákazníkům stránku s potvrzením přihlášení. Jakmile se zobrazí potvrzení o přihlášení, vytvoří se v POS úkol pro obchod, kde se vyzvedává objednávka.

Když je nakonfigurován jeden nebo více dalších informačních klíčů, zákazníci jsou nejprve vyzváni k zadání informací. Když si vyberou **Odeslat**, zobrazí se jim potvrzení odbavení a v POS se vytvoří úkol. 

## <a name="additional-resources"></a>Další prostředky

[Povolit oznámení o přihlášení zákazníka v místě prodeje (POS)](enable-customer-check-in.md)
