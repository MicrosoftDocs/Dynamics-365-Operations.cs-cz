---
title: Stavy životního cyklu majetku
description: Toto téma vysvětluje stavy životního cyklu majetku a modely životního cyklu v modulu Správa majetku.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetLifecycleModelStateNext, EntAssetObjectLifecycleState, EntAssetLifecycleStateUpdate, EntAssetObjectLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 55139c6458e569b15518f0f11f1c12c3a26cae2f26c6a2046a7ebdc1277cb144
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722456"
---
# <a name="asset-lifecycle-states"></a>Stavy životního cyklu majetku

[!include [banner](../../includes/banner.md)]

 

Toto téma vysvětluje stavy životního cyklu majetku a modely životního cyklu v modulu Správa majetku. Stavy životního cyklu majetku se používají k definování, zda je majetek aktivní nebo neaktivní. Můžete například nastavit stavy životního cyklu majetku jako **Vytvořené**, **Aktivní** a **Ukončené**.

> [!NOTE]
> - Stavy životního cyklu požadavku jsou propojeny se stavy životního cyklu majetku. Proto, pokud je požadavek změněn na nový stav životního cyklu požadavku, je majetek připojený k požadavku změněn na nový stav životního cyklu majetku. Pokud je například stav životního cyklu požadavku změněn na **Příchozí**, stav životního cyklu připojeného majetku se změní na stav životního cyklu, který je vybrán v poli **Stav aktivního cyklu příchozí** na pevné záložce **Stav životního cyklu majetku** na stránce **Modely životního cyklu majetku**. 


Stavy životního cyklu majetku lze nastavit v modelech životního cyklu majetku, kde můžete definovat požadované stavy životního cyklu pro různé typy majetku. Nejprve nastavíte stavy životního cyklu. Poté vytvořte model životního cyklu a vyberte pro něj stavy životního cyklu.

1. Vyberte **Správa majetku**\>**Nastavení**\> **Majetek** \>**Stavy životního cyklu**.
2. Zvolte **Nový** pro vytvoření stavu životního cyklu.
3. Do pole **Stav životního cyklu** zadejte ID stavu životního cyklu.
4. Do pole **Název** zadejte popis.

    Pole **Modely časového cyklu** zobrazuje počet modelů životního cyklu majetku, které používají stav životního cyklu majetku.

5. Nastavte možnost **Aktivní** na **Ano**, pokud by tento stav životního cyklu měl být aktivním stavem životního cyklu (jinými slovy, pokud lze vytvořit pracovní příkazy pro majetek, který je v tomto stavu životního cyklu).
6. Nastavte možnost **Odstranit řádky otevřeného kalendáře** na **Ano**, pokud si přejete odstranit řádky otevřeného kalendáře, které mají stav životního cyklu **Vytvořeno**, pokud jsou v tomto stavu životního cyklu. Toto nastavení je užitečné, pokud chcete vyčistit všechny otevřené plány údržby, které již nejsou pro daný majetek relevantní (například pokud majetek již není aktivní).

> [!NOTE]
> Stavy životního cyklu majetku, modely životního cyklu majetku a typy majetku jsou propojeny. Používají se stejným způsobem jako stavy životního cyklu pracovních příkazů, modely životního cyklu pracovních příkazů a typy pracovních příkazů. 


Po vytvoření požadovaných stavů životního cyklu majetku můžete nastavit stavy životního cyklu v modelech životního cyklu majetku.

1. Vyberte **Správa majetku**\>**Nastavení**\> **Majetek** \>**Modely životního cyklu**.
2. Zvolte **Nový** pro vytvoření modelu životního cyklu.
3. Do pole **Model životního cyklu** zadejte ID modelu životního cyklu.
4. Do pole **Název** zadejte popis.

    Pole **Stavy časového cyklu** zobrazuje počet stavů životního cyklu majetku, které jsou vybrány v modelu životního cyklu majetku. Pole **Typy majetku** zobrazuje počet typů životního cyklu majetku, které používají model životního cyklu majetku.

5. Na pevné záložce **Stavy časového cyklu** vyberte stavy životního cyklu majetku, které si přejete zahrnout v modelu životního cyklu majetku:

    - Chcete-li v modelu použít stav životního cyklu, vyberte jej v části **Zbývající stavy životního cyklu** a potom vyberte tlačítko šipky vpravo ![Šipka vpravo](media/15-setup-for-objects.png) a přesuňte jej do části Vybrané stavy životního cyklu. pro přesun do části **Vybrané stavy životního cyklu**.
    - Chcete-li pro model použít všechny dostupné stavy životního cyklu, vyberte tlačítko **Všechny dostupné stavy životního cyklu** ![Všechny dostupné stavy životního cyklu.](media/20-setup-for-objects.png). Všechny stavy životního cyklu jsou převedeny do části **Vybrané stavy životního cyklu**.
    - Chcete-li z modelu odstranit stav životního cyklu, vyberte jej v části **Vybrané stavy životního cyklu** a potom vyberte tlačítko šipky vlevo ![Šipka vlevo](media/16-setup-for-objects.png) a přesuňte jej do části Vybrané stavy životního cyklu. pro přesun do části **Zbývající stavy životního cyklu**.

6. Vyberte **Aktualizace stavu životního cyklu**, chcete-li definovat stavy životního cyklu majetku, které mohou následovat po vybraném stavu životního cyklu.
7. Pevná záložka **Stav majetku** se používá, pokud manipulujete s majetkem, který obdržíte k opravě. V sekci **Příchozí/odchozí** můžete vybrat stavy životního cyklu majetku a vyznačit tak pracovní postup majetku, který obdržíte k opravě. Pokud nabízíte zapůjčený majetek zákazníkům nebo oddělením, můžete v sekci **Výpůjčka** vybrat stavy životního cyklu pro zapůjčený majetek.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]