---
title: Šablony dat s více listy
description: Toto téma popisuje, jak importovat data pomocí šablon datové entity Excelu do Finance and Operations.
author: peakerbl
ms.date: 01/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: cf3c423bdf06685a3c4025551927123773ae818a
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070054"
---
# <a name="data-templates-with-multiple-worksheets"></a>Šablony dat s více listy

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Správa dat v aplikaci podporuje šablony založené na aplikaci Microsoft Excel pro datové entity. Tyto šablony mohou obsahovat jeden nebo více listů. Šablony s více listy se často používají tehdy, když je vhodné spravovat data v jednom souboru a importovat je do vícero datových entit. Příkladem by byla pracoviště a sklady.

## <a name="upload-a-file-once-and-map-it-to-all-entities"></a>Nahrajte soubor jednou a namapujte ho na všechny entity
Podíváme se na příklad, kde existuje jeden soubor aplikace Excel s listy nazvanými **Pracoviště** a **Sklady**. Chcete-li nastavit projekt importu dat, přidali byste první datovou entitu **Pracoviště** a poté odeslali soubor. Budete moci vybrat **Pracoviště** jako list, který bude použit pro tuto entitu.

Pokud přidáte druhou entitu **Sklady**, aniž byste opustili formulář **Přidat soubor**, vyhledávání listu vám umožní vybrat list **Sklady** bez nutnosti znovu odeslat soubor. Jediný důvod k odeslání nového souboru by byl ten, kdyby data **Sklady** byla v jiném souboru.

![Více listů.](./media/AddFileMultipleWorkSheets.png)

## <a name="fix-worksheet-to-entity-mapping"></a>Opravení listu pro mapování entit

Mapování listu na datovou entitu v úloze importu lze opravit z mřížky. Sloupec **List** v mřížce zobrazí listy ze souboru, který byl mapován. Jiný list můžete vybrat z rozevírací nabídky. Pokud je zvolený list již namapován na entitu v datovém projektu, systém zobrazí výzvu k potvrzení změny. Doporučujeme, abyste v mřížce opravili všechna mapování.

![Aktualizace mapování listu.](./media/UpdateMappings.png)

## <a name="re-map-to-a-new-file"></a>Opětovné namapování na nový soubor

V případech, kdy musí být odeslána nová verze stejného nebo zcela nového souboru pro existující entity v datovém projektu, je třeba použít možnost **Přidat soubor** a znovu přidat entity, jako kdyby byly přidány poprvé. Systém potvrdí, že chcete přepsat existující entity v projektu dat, než budete pokračovat. Entity, které nejsou znovu přidány (nebo přepsány) budou nadále udržovat mapování z přechozího souboru.

## <a name="upload-a-file-using-run-project"></a>Odeslání souboru pomocí spuštění projektu

Můžete načíst soubor aplikace Excel při používání možnosti **Spustit projekt** pro provedení projektu importu. Musíte si dávat pozor, abyste odeslali pouze soubory, které mají stejné listy jako existující mapování na datových entitách v datovém projektu. Pokud není list nalezen v nově odeslaném souboru, systém zobrazí chybovou zprávu a zastaví import. Pokud u entity musí být změněno mapování na list, musí být nejprve aktualizováno mapování v datovém projektu z datového projektu předtím, než použijete soubor v možnosti **Spustit projekt**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
