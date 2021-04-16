---
title: Vystavení elektronických faktur v aplikacích Finance a Supply Chain Management
description: Toto téma vysvětluje, jak vydávat elektronické faktury v Microsoft Dynamics 365 Finance a Dynamics 365 Supply Chain Management prostřednictvím Elektronické fakturace.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8d6ef59b64a96e13bdc2e5ddf299ef7ab98e105c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840069"
---
# <a name="issue-electronic-invoices-in-finance-and-supply-chain-management"></a>Vystavení elektronických faktur v aplikacích Finance a Supply Chain Management

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak vydávat elektronické faktury v Microsoft Dynamics 365 Finance a Dynamics 365 Supply Chain Management prostřednictvím Elektronické fakturace.


## <a name="feature-activation"></a>Aktivace funkce

Abyste mohli vystavovat elektronické faktury pomocí Elektronické fakturace, je nezbytné aktivovat odkaz na funkci v aplikacích Finance a Supply Chain Management.

Každá funkce odpovídá některé funkci elektronického fakturování, která odpovídá požadavkům na elektronické fakturování některé země/oblasti.

V následující tabulce jsou uvedeny funkce, které může podporovat Elektronická fakturace.

| Jméno                                              | Země nebo oblast |
|---------------------------------------------------|----------------|
|Elektronická faktura pro Rakousko                        |Rakousko         |
|Elektronická faktura pro Belgii                         |Belgie         |
|NF-e Federal - Brazilská elektronická faktura       |Brazílie          |
|NFS-e – elektronické faktura za služby (městské) pro Brazílii|Brazílie          |
|Elektronická faktura pro Dánsko                          |Dánsko         |
|Elektronická faktura pro Egypt                        |Egypt           |
|Elektronická faktura pro Estonsko                        |Estonsko         |
|Elektronická faktura pro Finsko                         |Finsko         |
|Elektronická faktura pro Francii                          |Francie          |
|Elektronická faktura pro Německo                          |Německo         |
|PEPPOL – globální elektronická faktura                 |Globální          |
|Elektronická faktura pro Itálii                         |Itálie           |
|CFDI – elektronická faktura pro Mexiko                  |Mexiko          |
|Elektronická faktura pro Nizozemí                           |Nizozemsko     |
|Elektronická faktura pro Norsko                       |Norsko          |
|Elektronická faktura pro Španělsko                         |Španělsko           |

V případech, kdy existuje starší funkce elektronické fakturace, která podporovala rozsah lokalizace dané země/oblast, aktivace těchto funkcí vypne starší funkci a zapne vydávání elektronických faktur prostřednictvím Elektronické fakturace a vypíná dřívější funkci.

> [!IMPORTANT]
> Poté, co je povolena funkce integrace Elektronické fakturace, je nové prostředí Elektronické fakturace ve výchozím nastavení vypnuto. Koncept funkce můžete použít k selektivnímu povolení nových zkušeností pro právnické osoby využívající funkce specifické pro zemi/oblast. Možnost **Globální** řídí nové prostředí pro zbývající okres/regiony, které nejsou konkrétně uvedeny v tabulce.

## <a name="submit-electronic-documents"></a>Odeslat elektronické dokumenty

Proces odesílání elektronických dokumentů představuje jediný bod komunikace mezi aplikacemi Finance a Supply Chain Management a Elektronickou fakturací. Během každé události odeslání probíhá komunikace v obou směrech:

- **Z aplikací Finance a Supply Chain Management do Elektronické fakturace** – Aplikace Finance a Supply Chain Management odešlou abstraktní faktury do Elektronické fakturace. Podle potřeby také odesílají obsah proměnných, které byly nakonfigurovány jako součást funkcí elektronické fakturace.
- **Z Elektronické fakturace do aplikací Finance a Supply Chain Management** – V závislosti na funkci elektronické fakturace obdrží aplikace Finance a Supply Chain Management aktualizace z Elektronické fakturace o výsledcích zpracování faktur, které byly dříve odeslány. Rovněž obdrží obsah proměnných, které byly nakonfigurovány jako součást funkcí elektronické fakturace.

Chcete-li odeslat elektronické dokumenty do Elektronické fakturace, v aplikacích Finance a Supply Chain Management přejděte na **Správa organizace &gt; Periodicky &gt; Elektronické dokumenty &gt; Odeslání elektronických dokumentů**.

Výchozím bodem je zaúčtovaná faktura. Tato faktura může pocházet z různých zdrojů, jako jsou prodejní objednávky, faktury projektů nebo volné faktury.

Proces odesílání lze spustit ručně nebo na pozadí.

- **Ruční spuštění** – Pro ruční spuštění musíte použít možnost **Filtr** pro definování rozsahu dokumentů, které mají být odeslány. Na stránce **Filtry** můžete konfigurací vlastního dotazu vybrat zaúčtované faktury, které je třeba odeslat. Po provedení výběru musíte ručně spustit zpracování a počkat na jeho dokončení. Po dokončení zpracování zobrazí zpráva v centru akcí zobrazující počet elektronických dokumentů, které byly úspěšně odeslány.
- **Spuštění na pozadí** – Spuštění na pozadí probíhá bez nutnosti přihlášení nebo ponechání otevřeného dialogového okna pro odeslání. Můžete naplánovat spuštění procesu a definovat frekvenci spouštění.

## <a name="view-the-submission-logs"></a>Zobrazení protokolů odeslání

V aplikacích Finance a Supply Chain Management můžete pomocí protokolů odeslání zobrazit výsledky zpracování odeslání do Elektronické fakturace. Přejděte na **Správa organizace &gt; Periodicky &gt; Elektronické dokumenty &gt; Elektronické odesílání dokumentů** a poté v poli **Typ dokumentu** vyberte hodnotu pro filtrování typu faktur, které protokoly zobrazují.

Existují tři možné stavy odeslání:

- **Plánováno** – Elektronická fakturace obdržela odeslané faktury z aplikací Finance a Supply Chain Management a probíhá zpracování funkce elektronické fakturace.
- **Dokončeno** – Elektronická fakturace úspěšně zpracovala funkci elektronické fakturace tak, jak byla konfigurována pro její spuštění.
- **Selhání** – Elektronická fakturace narazila na chybu nebo byla zastavena výjimkou během zpracování funkce elektronické fakturace.

> [!IMPORTANT]
> Stav odeslání představuje stav zpracování, který Elektronická fakturace vykazuje u funkce elektronické fakturace. Nepředstavuje konečný stav samotné elektronické faktury.
>
> Například, pokud musí být elektronická faktura odeslána ke schválení externí webové službě, může být stav odeslání **Dokončeno**, ale stav elektronické faktury může být **Zamítnuto**. V tomto případě byla Elektronická fakturace schopna úspěšně zpracovat funkci elektronické fakturace tak, jak byla konfigurována pro její zpracování. Elektronická faktura však byla zamítnuta, protože nesplňovala kritéria, která webová služba stanovila pro schválení faktury.

Protokoly odeslání obsahují následující dodatečné funkce:

- **Podrobnosti o odeslání** – Zobrazení podrobností o hlavním odeslání. Vizualizace zobrazuje kompletní protokol spuštěných akcí, které jsou konfigurovány ve funkci elektronické fakturace. Umožňuje také uživatelům stáhnout soubory, které jsou vytvořeny během zpracování. V přípdaech, kdy musí být faktura schválena externí webovou službou, umožňuje uživatelům zobrazit stav faktury.
- **Související odeslání** – Zobrazení podrobností o podřízených odesláních.
- **Zrušit odeslání** – Tato funkce umožňuje speciální zpracování odesílání v situacích, kdy musí být elektronická faktura schválena externí webovou službou. Dává pokyn Elektronické fakturaci, aby webové službě odeslal specifickou zprávu, která má zrušit stav schválené elektronické faktury v databázi webové služby.
- **Znovu odeslat dokument** – Opětovné odeslání elektronického dokumentu, který již byl odeslán do Elektronické fakturace. Na stránce **Podrobnosti o odeslání** se vytvoří nový protokol.
- **Provést související odeslání**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
