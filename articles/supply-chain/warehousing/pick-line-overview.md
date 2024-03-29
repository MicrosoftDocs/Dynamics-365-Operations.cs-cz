---
title: Nastavte položku nabídky mobilního zařízení a poskytněte přehled řádků výdeje
description: Tento článek vysvětluje, jak definovat, kdy se seznam všech řádků práce zobrazí pracovníkům skladu, kteří zpracovávají skladovou práci na mobilním zařízení. Tato funkce může být užitečná pro pracovníky skladu, kteří často vyžadují přehled řádků výdeje v pracovním příkazu, aby mohli optimalizovat sekvenci výdeje.
author: Mirzaab
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: aeadca6f3c31d5d8c1ef9d334b0e531896ac99b1
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336298"
---
# <a name="set-up-a-mobile-device-menu-item-to-provide-a-pick-line-overview"></a>Nastavte položku nabídky mobilního zařízení a poskytněte přehled řádků výdeje

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje, jak konfigurovat možnosti, které souvisejí s přehledem řádku výdeje pro položky nabídky mobilního zařízení, které se používají ke zpracování práce výdeje. Přehled řádků výdeje umožňuje pracovníkům skladu zobrazit a vybrat ze seznamu všech řádků práce, které souvisejí s jejich aktuálním úkolem. Tato schopnost může pracovníkům pomoci optimalizovat jejich sekvenci vychystávání. Tato funkce poskytuje možnosti, které nahrazují standardní tlačítko **Přeskočit**, které umožňuje pracovníkům procházet řádky jeden po druhém v pevném pořadí. (Možnost použít toto tlačítko je však stále k dispozici.)

Správci mohou nakonfigurovat každou položku nabídky samostatně, aby určili, jak, kdy a kde mobilní aplikace Řízení skladu zobrazuje přehled řádků výdeje.

## <a name="turn-on-the-work-pick-line-overview-feature"></a>Zapnutí funkce přehledu řádků práce výdeje

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, je-li to potřeba. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** _Řízení skladu_
- **Název funkce:** _Přehled řádků práce výdeje_

## <a name="configure-menu-items-to-show-a-list-of-all-work-lines"></a>Nakonfigurujte položky nabídky tak, aby zobrazovaly seznam všech pracovních řádků

Chcete-li nastavit položku nabídky mobilního zařízení a poskytnout tak přehled řádků výdeje, postupujte následujícím způsobem.

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.
1. Vyberte nebo vytvořte položku nabídky, která souvisí s výběrem práce, a nastavte následující hodnoty:

    - **Režim:** *Práce*
    - **Použít existující práci:** - *Ano*
    - **Řídí:** *Uživatel* nebo *Systém*

    Další informace o tom, jak vytvořit položky nabídky a použít různá nastavení, která jsou k dispozici na stránce **Položky nabídky mobilního zařízení**, přečtěte si [Nastavte mobilní zařízení pro práci ve skladu](configure-mobile-devices-warehouse.md).

1. Na pevné záložce **Obecné** nakonfigurujte funkci nastavením pole **Zobrazit seznam řádků práce** na jednu z následujících hodnot:

    - **Zobrazit pouze na vyžádání** - Pracovníci se mohou rozhodnout zobrazit seznam výběrových řádků výběrem tlačítka **Přeskočit na** v mobilní aplikaci Řízení skladu.
    - **Zobrazit na začátku každého výdeje** - Pracovníci vidí seznam pokaždé, když zahájí nebo dokončí výdej. Seznam mohou také znovu zobrazit výběrem tlačítka **Přeskočit na** v mobilní aplikaci Řízení skladu.
    - **Zobrazit pouze na začátku prvního výdeje** - Pracovníci uvidí seznam pokaždé, když zahájí novou práci výdeje, ale ne po každém řádku. Seznam mohou také znovu zobrazit výběrem tlačítka **Přeskočit na** v mobilní aplikaci Řízení skladu.
    - **Nikdy neukazovat** - Standardní tlačítko **Přeskočit** se zobrazí v mobilní aplikaci Řízení skladu a zobrazení seznamu pracovních řádků je vypnuto. Tlačítko **Přeskočit** umožňuje pracovníkům procházet řádky jeden po druhém, v pevném pořadí. Mohou také procházet seznamem tolikrát, kolikrát vyžadují, dokud nebudou zpracovány všechny řádky.

1. V podokně akcí vyberte **Uložit**.

    Pokud nastavíte pole **Zobrazit seznam řádků práce** na libovolnou hodnotu kromě *Nikdy neukazovat*, tlačítko **Seznam polí** v podokně akcí bude k dispozici.

1. V podokně akcí vyberte možnost **Seznam polí**.
1. Na stránce **Seznam polí** nakonfigurujte informace, které mobilní aplikace Řízení skladu zobrazuje pro každý řádek v seznamu.

    - Pole **Primární ovládací prvek** je vždy nastaveno na *LineNum*. Každý řádek v seznamu proto začíná číslem řádku.
    - Použijte zbývající pole **Zobrazit pole** pro přidání až sedmi dalších polí zobrazení, jak požadujete. V každém poli **Zobrazit pole** vyberte název pole řádku práce. Každý řádek poté zobrazí hodnotu pro toto pole. Hodnoty se zobrazí v pořadí, které zde vyberete. Můžete nachat některá z polí **Zobrazit pole** prázdná, pokud nevyžadujete všech sedm hodnot.

1. V podokně akcí vyberte **Uložit** a pak vyberte stránku **Seznam polí**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]