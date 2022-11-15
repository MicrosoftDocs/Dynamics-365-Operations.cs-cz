---
title: Optimalizace uzávěrky na konci roku
description: Tento článek popisuje doplněk služby Optimalizace uzávěrky na konci roku, který je k dispozici pro proces uzavření hlavní knihy na konci roku.
author: moaamer
ms.date: 11/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2022-11-28
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 41d0c2975341cf3d612cc36be348326e24e94f1b
ms.sourcegitcommit: 707957bb7bcd98faf2600eff1c98067901a0fb73
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/08/2022
ms.locfileid: "9750004"
---
# <a name="optimize-year-end-close"></a>Optimalizace uzávěrky na konci roku

Doplněk služby Optimalizace uzávěrky na konci roku pro Microsoft Dynamics 365 Finance umožňuje, aby zpracování uzávěrky na konci roku probíhalo mimo instanci Application Object Server (AOS) pro prostředky Dynamics 365 Finance. Využívá technologii mikroslužeb. Výhody, které jsou přidruženy k funkcím Optimalizace uzávěrky na konci roku, zahrnují lepší výkon a minimální dopad na databázi SQL během zpracování uzávěrky na konci roku.

Chcete-li používat funkci Optimalizace uzávěrky na konci roku, musíte provést následující úkoly:

1. Nainstalujte si doplněk služby Optimalizace uzávěrky na konci roku ze svého projektu ve službě Lifecycle Microsoft Dynamics.
2. Povolte funkci **Optimalizace uzávěrky na konci roku** ve správě funkcí.

> [!NOTE]
> Stále můžete používat aktuální funkci uzávěrky na konci roku pro finanční zdroje, když deaktivujete funkci **Optimalizace uzávěrky na konci roku** ve správě funkcí.

## <a name="improved-performance"></a>Zlepšení výkonu

Funkce **Optimalizace uzávěrky na konci roku** je navržena tak, aby urychlila zpracování uzávěrky na konci roku, zejména pro zákazníky, kteří mají velké objemy dat. Když se u služby spustí uzávěrka na konci roku, náročné zpracování se odstraní z finančních zdrojů, aby se zkrátila doba zpracování a uvolnily se prostředky, které by mohly ovlivnit každodenní operace ostatních uživatelů.

Funkce **Optimalizace uzávěrky na konci roku** vám může pomoci dosáhnout následujících cílů:

- Zlepšete výkon uzávěrky na konci roku snížením doby běhu.
- Snížení dopadu na jiné procesy během spuštění uzávěrky na konci roku.
- Zlepšete vykazování a úpravy výsledků na konci roku, protože uzávěrka na konci roku trvá kratší dobu.

## <a name="new-options-and-visibility"></a>Nové možnosti a viditelnost

Když je povolena funkce **Optimalizace uzávěrky na konci roku**, dva nové sloupce, **Výsledek** a **Stav**, se přidají do následujících míst:

- Na stránku **Uzávěrka na konci roku**
- Do dialogového okna **Výsledky uzávěrky na konci roku**
- Do možnosti **Převod finančních dimenzí rozvahy** na stránce **Šablona uzávěrky na konci roku**

Následující obrázek ukazuje příklad polí **Výsledek** a **Stav** na stránce **Uzávěrka na konci roku**. Můžete vybrat odkaz **Zobrazit výsledky** ve sloupci **Výsledky** k otevření výsledků uzávěrky na konci roku. Sloupec **Stav** zobrazuje aktuální stav uzávěrky na konci roku. Nové sloupce proto poskytují přehled o průběhu procesu uzavírky na konci roku.

[![Sloupce Výsledky a Stav na stránce Uzávěrka na konci roku.](./media/Yearendclose.jpg)](./media/Yearendclose.jpg)

Kromě toho, když je povolena funkce **Optimalizace uzávěrky na konci roku**, zpřístupní se pevná záložka **Finanční dimenze rozvahy** na stránce **Šablona uzávěrky na konci roku**. Tuto pevnou záložku můžete použít k podrobnému zadání finančních dimenzí rozvahy při uzavření roku. Tato schopnost je paralelní se schopností, která je již k dispozici pro účty zisků a ztrát.

## <a name="architecture-and-data-flow"></a>Architektura a tok dat

Chcete-li použít funkci **Optimalizace uzávěrky na konci roku** a spustit uzávěrku na konci roku na mikroslužbě, musíte nainstalovat doplněk služby Optimalizace uzávěrky na konci roku ze služeb Lifecycle Services a poté povolit funkci **Optimalizace uzávěrky na konci roku** ve správě funkcí.

Jak ukazuje následující obrázek, zpracování uzávěrky na konci roku ověří, zda je doplněk nainstalován a funkce je povolena. Pokud jsou splněny oba předpoklady, uzávěrka na konci roku běží na mikroslužbě.

[![Diagram toku dat.](./media/Lifecycle-services.jpg)](./media/Lifecycle-services.jpg)

## <a name="high-level-flow-for-year-end-close-processing"></a>Tok na vysoké úrovni pro zpracování uzávěrky na konci roku

1. Proces uzávěrky na konci roku začíná ve Finance **Hlavní kniha \> Uzávěrka období \> Uzávěrka na konci roku**. Proces vytváří uzavírací dávkové úlohy a úkoly pro právnické osoby, které se uzavírají.
2. Uzávěrka na konci roku určuje, zda má být uzávěrka na konci roku spuštěna na mikroslužbě nebo na aktuální logice uzávěrky.

    - Pokud je nainstalován doplněk Optimalizace uzávěrky na konci roku ve službě Lifecycle Services a povolená funkce **Optimalizace uzávěrky na konci roku** ve správě funkcí, uzávěrka na konci roku bude spuštěna na mikroslužbě.

        1. Funkce Optimalizace uzávěrky na konci roku vytvoří úlohu služby uzávěrky na konci roku pro každou právnickou osobu, která se uzavírá, a poté spustí logiku uzavření na konci roku. Mikroslužba provádí uzávěrku roku.
        2. Finance naslouchají uzávěrce na konci roku na mikroslužbě, aby určily, kdy mikroslužba skončila. Výsledky uzávěrky na konci roku jsou pak aktualizovány na stránce **Uzávěrka na konci roku** ve Finance.

    - V opačném případě bude uzávěrka na konci roku probíhat podle aktuální logiky uzávěrky.
