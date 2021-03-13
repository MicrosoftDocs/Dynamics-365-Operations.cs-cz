---
title: Vystavení elektronických faktur v aplikacích Finance a Supply Chain Management
description: Toto téma poskytuje informace o vystavování elektronických faktur v Microsoft Dynamics 365 Finance a Dynamics 365 Supply Chain Management prostřednictvím doplňku elektronické fakturace.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 187f5a20d088b4fcd7af2a6576357a69c2efc2c6
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104354"
---
# <a name="issue-electronic-invoices-in-finance-and-supply-chain-management"></a>Vystavení elektronických faktur v aplikacích Finance a Supply Chain Management

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Toto téma poskytuje informace o vystavování elektronických faktur v Microsoft Dynamics 365 Finance a Dynamics 365 Supply Chain Management prostřednictvím doplňku elektronické fakturace.


## <a name="feature-activation"></a>Aktivace funkce

Abyste mohli vystavovat elektronické faktury pomocí doplňku elektronické fakturace, je nezbytné aktivovat odkaz na funkci v aplikacích Finance a Supply Chain Management.

Každý odkaz na funkci odpovídá některé funkci elektronického fakturování, která odpovídá požadavkům na elektronické fakturování některé země/oblasti.

V následující tabulce jsou uvedeny odkazy na formuláře, které podporuje doplněk elektronického fakturování.

| Odkaz na funkci | Jméno                                              | Země nebo oblast |
|-------------------|---------------------------------------------------|----------------|
| BR-00053          | Brazilská elektronická faktura NF-e Federal       | Brazílie         |
| BR-00095          | Brazilské elektronické faktury NFS-e               | Brazílie         |
| DK-00001          | Elektronická fakturace pro veřejný sektor (OIOUBL) – DK    | Dánsko        |
| EG-00008          | Elektronická fakturace pro Egypt                             | Egypt          |
| ES-00025          | Elektronická faktura pro veřejný sektor           | Španělsko          |
| EUR-00023         | Elektronická fakturace pro veřejný sektor Evropské unie       | Evropa         |
| ITA-00036         | IT – elektronická fakturace pro veřejný sektor (FatturaPA) | Itálie          |
| MX-00010          | Elektronické faktury CFDI                                  | Mexiko         |
| MX-00016          | Elektronická fakturace CFDI – proces zrušení           | Mexiko         |

V případech, kdy existuje starší funkce elektronické fakturace, která podporovala rozsah lokalizace dané země, aktivace odkazu na funkci povolí vydávání elektronických faktur prostřednictvím doplňku elektronické fakturace a vypíná dřívější funkci.

## <a name="submit-electronic-documents"></a>Odeslat elektronické dokumenty

Proces odesílání elektronických dokumentů představuje jediný bod komunikace mezi aplikacemi Finance a Supply Chain Management a doplňkem elektronické fakturace. Během každé události odeslání probíhá komunikace v obou směrech:

- **Z aplikací Finance a Supply Chain Management do doplňku elektronické fakturace** – Aplikace Finance a Supply Chain Management odešlou abstraktní faktury do doplňku elektronického fakturování. Podle potřeby také odesílají obsah proměnných, které byly nakonfigurovány jako součást funkcí elektronické fakturace.
- **Z doplňku elektronické fakturace do aplikací Finance a Supply Chain Management** – V závislosti na funkci elektronické fakturace obdrží aplikace Finance a Supply Chain Management aktualizace z doplňku elektronické fakturace o výsledcích zpracování faktur, které byly dříve odeslány. Rovněž obdrží obsah proměnných, které byly nakonfigurovány jako součást funkcí elektronické fakturace.

Chcete-li odeslat elektronické dokumenty do doplňku elektronické fakturace, v aplikacích Finance a Supply Chain Management přejděte na **Správa organizace &gt; Periodicky &gt; Elektronické dokumenty &gt; Odeslání elektronických dokumentů**.

Výchozím bodem je zaúčtovaná faktura. Tato faktura může pocházet z různých zdrojů, jako jsou prodejní objednávky, faktury projektů nebo volné faktury.

Proces odesílání lze spustit ručně nebo na pozadí.

- **Ruční spuštění** – Pro ruční spuštění musíte použít možnost **Filtr** pro definování rozsahu dokumentů, které mají být odeslány. Na stránce **Filtry** můžete konfigurací vlastního dotazu vybrat zaúčtované faktury, které je třeba odeslat. Po provedení výběru musíte ručně spustit zpracování a počkat na jeho dokončení. Po dokončení zpracování zobrazí zpráva v centru akcí zobrazující počet elektronických dokumentů, které byly úspěšně odeslány.
- **Spuštění na pozadí** – Spuštění na pozadí probíhá bez nutnosti přihlášení nebo ponechání otevřeného dialogového okna pro odeslání. Můžete naplánovat spuštění procesu a definovat frekvenci spouštění.

## <a name="view-the-submission-logs"></a>Zobrazení protokolů odeslání

V aplikacích Finance a Supply Chain Management můžete pomocí protokolů odeslání zobrazit výsledky zpracování odeslání do doplňku elektronické fakturace. Přejděte na **Správa organizace &gt; Periodicky &gt; Elektronické dokumenty &gt; Elektronické odesílání dokumentů** a poté v poli **Typ dokumentu** vyberte hodnotu pro filtrování typu faktur, které protokoly zobrazují.

Existují tři možné stavy odeslání:

- **Plánováno** – Doplněk elektronické fakturace obdržel odeslané faktury z aplikací Finance a Supply Chain Management a probíhá zpracování funkce elektronické fakturace.
- **Dokončeno** – Doplněk elektronické fakturace úspěšně zpracoval funkci elektronické fakturace tak, jak byl nakonfigurován pro její spuštění.
- **Selhání** – Doplněk elektronické fakturace narazil na chybu nebo byl zastaven výjimkou během zpracování funkce elektronické fakturace.

> [!IMPORTANT]
> Stav odeslání představuje stav zpracování, který doplněk elektronické fakturace vykazuje u funkce elektronické fakturace. Nepředstavuje konečný stav samotné elektronické faktury.
>
> Například, pokud musí být elektronická faktura odeslána ke schválení externí webové službě, může být stav odeslání **Dokončeno**, ale stav elektronické faktury může být **Zamítnuto**. V tomto případě byl doplněk elektronické fakturace schopen úspěšně zpracovat funkci elektronické fakturace tak, jak byl nakonfigurován pro její zpracování. Elektronická faktura však byla zamítnuta, protože nesplňovala kritéria, která webová služba stanovila pro schválení faktury.

Protokoly odeslání obsahují následující dodatečné funkce:

- **Podrobnosti o odeslání** – Zobrazení podrobností o hlavním odeslání. Vizualizace zobrazuje kompletní protokol spuštěných akcí, které jsou konfigurovány ve funkci elektronické fakturace. Umožňuje také uživatelům stáhnout soubory, které jsou vytvořeny během zpracování. V přípdaech, kdy musí být faktura schválena externí webovou službou, umožňuje uživatelům zobrazit stav faktury.
- **Související odeslání** – Zobrazení podrobností o podřízených odesláních.
- **Zrušit odeslání** – Tato funkce umožňuje speciální zpracování odesílání v situacích, kdy musí být elektronická faktura schválena externí webovou službou. Dává pokyn doplňku elektronické fakturace, aby webové službě odeslal specifickou zprávu, která má zrušit stav schválené elektronické faktury v databázi webové služby.
- **Znovu odeslat dokument** – Opětovné odeslání elektronického dokumentu, který již byl odeslán do doplňku elektronické fakturace. Na stránce **Podrobnosti o odeslání** se vytvoří celý nový protokol.
- **Provést související odeslání**
